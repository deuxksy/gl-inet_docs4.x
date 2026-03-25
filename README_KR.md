# GL.iNet 문서

이 저장소는 GL.iNet 라우터 펌웨어 4.x 문서의 소스 파일을 포함하고 있습니다.

현재 다국어 문서 저장소로 운영되고 있으며 지원하는 언어는 다음과 같습니다:

- **영어**: `docs/en/`
- **독일어**: `docs/de/`
- **스페인어**: `docs/es/`
- **일본어**: `docs/jp/`
- **한국어**: `docs/ko/`

각 언어는 자체적인 `mkdocs.yml`, `docs/`, `overrides/` 디렉토리를 가지고 있습니다.

## 환경

문서는 [MkDocs](https://www.mkdocs.org/) 1.5.3과 [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 테마 9.4.6로 빌드됩니다.

## 설치

Python 가상 환경 생성:

```bash
python -m venv .venv
```

가상 환경을 활성화한 후 의존성 설치:

```bash
pip install -r requirements.txt
```

또는 Material for MkDocs를 직접 설치할 수도 있습니다:

```bash
pip install mkdocs-material
```

참조: [https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip](https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip)

## 저장소 구조

루트 `docs/` 폴더는 언어별 MkDocs 프로젝트를 포함합니다:

```text
docs/
  en/
    mkdocs.yml
    docs/
    overrides/
  de/
    mkdocs.yml
    docs/
    overrides/
  es/
    mkdocs.yml
    docs/
    overrides/
  jp/
    mkdocs.yml
    docs/
    overrides/
  ko/
    mkdocs.yml
    docs/
    overrides/
```

대부분의 경우 현지화된 페이지는 `docs/en/docs/` 아래의 해당 영어 페이지 경로를 미러링해야 합니다.

## 로컬 미리보기

미리보기할 언어에 대해 MkDocs를 실행합니다.

예시:

```bash
mkdocs serve -f docs/en/mkdocs.yml
mkdocs serve -f docs/de/mkdocs.yml
mkdocs serve -f docs/es/mkdocs.yml
mkdocs serve -f docs/jp/mkdocs.yml
mkdocs serve -f docs/ko/mkdocs.yml
```

현지화된 콘텐츠를 검토하거나 번역하는 경우 VS Code에서 영어 소스 페이지와 일치하는 현지화된 페이지를 나란히 엽니다.

## 온라인 보기

게시된 문서:

- **영어**: [https://docs.gl-inet.com/router/en/4/](https://docs.gl-inet.com/router/en/4/)
- **독일어**: [https://docs.gl-inet.com/router/de/4/](https://docs.gl-inet.com/router/de/4/)
- **스페인어**: [https://docs.gl-inet.com/router/es/4/](https://docs.gl-inet.com/router/es/4/)
- **일본어**: [https://docs.gl-inet.com/router/jp/4/](https://docs.gl-inet.com/router/jp/4/)
- **한국어**: [https://docs.gl-inet.com/router/ko/4/](https://docs.gl-inet.com/router/ko/4/)

## 작성 가이드

### Markdown 문법

모든 페이지는 Markdown으로 작성됩니다. 기본 문법은 [Markdown Guide](https://www.markdownguide.org/basic-syntax/)를 참조하세요.

### 새 탭에서 링크 열기

새 탭에서 링크를 열려면 링크 끝에 `{target="_blank"}`를 추가합니다.

### 이미지 파일 형식

명확한 이유가 없는 한 PNG를 선호합니다.

### 이미지 라이트박스

이미지가 큰 경우 PhotoSwipe를 사용합니다. [PhotoSwipe 정보](#about-photoswipe)를 참조하세요.

### 이미지 크기

`gl-50-desktop`, `gl-60-desktop`, `gl-70-desktop`, `gl-80-desktop`, 또는 `gl-90-desktop`를 사용하여 데스크톱에서 이미지 너비를 제어합니다.

예시:

`![gl.inet enable vpn cascading](https://static.gl-inet.com/docs/router/en/4/tutorials/vpn_cascading/enable_vpn_cascading.png){class="gl-50-desktop"}`

### 이미지 그림자 효과

`{class="glboxshadow"}`를 사용하여 이미지에 그림자를 추가합니다.

예시:

`![tap block](https://static.gl.inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/tap-block.jpeg){class="glboxshadow"}`

### 이미지 캡션

```html
<figure>
  <img src="https://dummyimage.com/600x400/eee/aaa" width="300" />
  <figcaption>이미지 캡션</figcaption>
</figure>
```

### 내부 링크

내부 링크에는 상대 경로를 사용합니다.

```md
[easytethering](../../../tutorials/tether)
```

## PhotoSwipe 정보

이 프로젝트는 현재 PhotoSwipe v4를 사용합니다. v5가 더 좋아 보이지만 JavaScript 모듈 로딩이 필요하고 여기에 통합되지 않았습니다.

이미지 너비가 1021px보다 큰 경우 PhotoSwipe를 사용합니다.

```html
<div class="gl-lightbox" itemscope itemtype="http://schema.org/ImageGallery">
  <figure
    itemprop="associatedMedia"
    itemscope
    itemtype="http://schema.org/ImageObject"
  >
    <a
      href="https://static.gl.inet.com/docs/router/en/3/setup/gl-b2200/hardware/hardware_1.jpg"
      itemprop="contentUrl"
      data-size="3167x2480"
    >
      <img
        src="https://static.gl.inet.com/docs/router/en/3/setup/gl-b2200/hardware/hardware_1.jpg"
        itemprop="thumbnail"
        alt="gl-b2200 pcb pinout"
      />
    </a>
  </figure>
</div>
```

참조:

- [https://photoswipe.com/documentation/getting-started.html](https://photoswipe.com/documentation/getting-started.html)
- [https://codepen.io/dimsemenov/pen/ZYbPQM](https://codepen.io/dimsemenov/pen/ZYbPQM)

## 버전 관리 정보

`mike` 플러그인은 버전이 지정된 MkDocs 배포를 위해 설계되었으며 일반적으로 GitHub Pages와 함께 사용됩니다. 이 저장소는 GitHub Pages로 배포하지 않지만 유사한 출력 구조를 따릅니다.

참조:

- [버전 관리 설정](https://squidfunk.github.io/mkdocs-material/setup/setting-up-versioning/)
- [mkdocs-material-example-versioning](https://github.com/squidfunk/mkdocs-material-example-versioning)
