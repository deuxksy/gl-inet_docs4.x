# GL.iNet Documentation

<div align="center">

**Language / 언어 / Sprache / Idioma / 言語:**

[English](#english) | [한국어](README_KO.md) | [Deutsch](#deutsch) | [Español](#español) | [日本語](#日本語)

</div>

---

## English

This repository contains the source files for GL.iNet router firmware 4.x documentation.

It is now a multilingual documentation repository. The current language sites in this repo are:

- English: `docs/en/`
- German: `docs/de/`
- Spanish: `docs/es/`
- Japanese: `docs/jp/`
- Korean: `docs/ko/`

Each language has its own `mkdocs.yml`, `docs/`, and `overrides/` directory.

## Environment

The documentation is built with [MkDocs](https://www.mkdocs.org/) 1.5.3 and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme 9.4.6.

## Installation

Create a Python virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment, then install dependencies:

```bash
pip install -r requirements.txt
```

You can also install Material for MkDocs directly:

```bash
pip install mkdocs-material
```

Reference: [https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip](https://squidfunk.github.io/mkdocs-material/getting-started/#with-pip)

## Repository Structure

The root `docs/` folder contains one MkDocs project per language:

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

In most cases, localized pages should mirror the corresponding English page path under `docs/en/docs/`.

## Local Preview

Run MkDocs against the language you want to preview.

Examples:

```bash
mkdocs serve -f docs/en/mkdocs.yml
mkdocs serve -f docs/de/mkdocs.yml
mkdocs serve -f docs/es/mkdocs.yml
mkdocs serve -f docs/jp/mkdocs.yml
mkdocs serve -f docs/ko/mkdocs.yml
```

If you are reviewing or translating localized content, open the English source page and the matching localized page side by side in VS Code.

## Online View

Published documentation:

- English: [https://docs.gl-inet.com/router/en/4/](https://docs.gl-inet.com/router/en/4/)
- German: [https://docs.gl-inet.com/router/de/4/](https://docs.gl-inet.com/router/de/4/)
- Spanish: [https://docs.gl-inet.com/router/es/4/](https://docs.gl-inet.com/router/es/4/)
- Japanese: [https://docs.gl-inet.com/router/jp/4/](https://docs.gl-inet.com/router/jp/4/)
- Korean: [https://docs.gl-inet.com/router/ko/4/](https://docs.gl-inet.com/router/ko/4/)

## Writing Guide

### Markdown Syntax

All pages are written in Markdown. For basic syntax, see [Markdown Guide](https://www.markdownguide.org/basic-syntax/).

### Open a Link in a New Tab

To open a link in a new tab, add `{target="_blank"}` at the end of the link.

### Image File Type

Prefer PNG unless there is a clear reason to use another format.

### Image Lightbox

If an image is large, use PhotoSwipe. See [About PhotoSwipe](#about-photoswipe).

### Image Size

Use `gl-50-desktop`, `gl-60-desktop`, `gl-70-desktop`, `gl-80-desktop`, or `gl-90-desktop` to control image width on desktop.

Example:

`![gl.inet enable vpn cascading](https://static.gl-inet.com/docs/router/en/4/tutorials/vpn_cascading/enable_vpn_cascading.png){class="gl-50-desktop"}`

### Image Shadow Effect

Use `{class="glboxshadow"}` to add a shadow to an image.

Example:

`![tap block](https://static.gl-inet.com/docs/router/en/4/tutorials/how-to-block-client-devices/tap-block.jpeg){class="glboxshadow"}`

### Image Captions

```html
<figure>
  <img src="https://dummyimage.com/600x400/eee/aaa" width="300" />
  <figcaption>Image caption</figcaption>
</figure>
```

### Internal Links

Use relative paths for internal links.

```md
[easytethering](../../../tutorials/tether)
```

## About PhotoSwipe

This project currently uses PhotoSwipe v4. Version 5 looks better, but it requires loading JavaScript modules and is not integrated here.

Use PhotoSwipe when the image width is larger than 1021 px.

```html
<div class="gl-lightbox" itemscope itemtype="http://schema.org/ImageGallery">
  <figure
    itemprop="associatedMedia"
    itemscope
    itemtype="http://schema.org/ImageObject"
  >
    <a
      href="https://static.gl-inet.com/docs/router/en/3/setup/gl-b2200/hardware/hardware_1.jpg"
      itemprop="contentUrl"
      data-size="3167x2480"
    >
      <img
        src="https://static.gl-inet.com/docs/router/en/3/setup/gl-b2200/hardware/hardware_1.jpg"
        itemprop="thumbnail"
        alt="gl-b2200 pcb pinout"
      />
    </a>
  </figure>
</div>
```

Reference:

- [https://photoswipe.com/documentation/getting-started.html](https://photoswipe.com/documentation/getting-started.html)
- [https://codepen.io/dimsemenov/pen/ZYbPJM](https://codepen.io/dimsemenov/pen/ZYbPJM)

## About Versioning

The `mike` plugin is designed for versioned MkDocs deployments, usually with GitHub Pages. This repository does not deploy with GitHub Pages, but it follows a similar output structure.

Reference:

- [Setting up versioning](https://squidfunk.github.io/mkdocs-material/setup/setting-up-versioning/)
- [mkdocs-material-example-versioning](https://github.com/squidfunk/mkdocs-material-example-versioning)

---

## 한국어

이 저장소는 GL.iNet 라우터 펌웨어 4.x 문서의 소스 파일을 포함하고 있습니다.

현재 다국어 문서 저장소로 운영되고 있으며 지원하는 언어는 다음과 같습니다:

- **영어**: `docs/en/`
- **독일어**: `docs/de/`
- **스페인어**: `docs/es/`
- **일본어**: `docs/jp/`
- **한국어**: `docs/ko/`

각 언어는 자체적인 `mkdocs.yml`, `docs/`, `overrides/` 디렉토리를 가지고 있습니다.

### 환경

문서는 [MkDocs](https://www.mkdocs.org/) 1.5.3과 [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 테마 9.4.6로 빌드됩니다.

### 설치

Python 가상 환경 생성:

```bash
python -m venv .venv
```

가상 환경을 활성화한 후 의존성 설치:

```bash
pip install -r requirements.txt
```

### 로컬 미리보기

미리보기할 언어에 대해 MkDocs를 실행합니다:

```bash
mkdocs serve -f docs/ko/mkdocs.yml
```

### 온라인 보기

- **한국어**: [https://docs.gl-inet.com/router/ko/4/](https://docs.gl-inet.com/router/ko/4/)

---

## Deutsch

Dieses Repository enthält die Quelldateien für die GL.iNet Router-Firmware 4.x Dokumentation.

Es handelt sich um ein mehrsprachiges Dokumentations-Repository. Die aktuellen Sprachseiten in diesem Repo sind:

- **Englisch**: `docs/en/`
- **Deutsch**: `docs/de/`
- **Spanisch**: `docs/es/`
- **Japanisch**: `docs/jp/`
- **Koreanisch**: `docs/ko/`

Jede Sprache hat ihr eigenes `mkdocs.yml`-, `docs/`- und `overrides/`-Verzeichnis.

### Umgebung

Die Dokumentation wird mit [MkDocs](https://www.mkdocs.org/) 1.5.3 und dem [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) Theme 9.4.6 erstellt.

### Installation

Erstellen Sie eine Python-virtuelle Umgebung:

```bash
python -m venv .venv
```

Aktivieren Sie die virtuelle Umgebung und installieren Sie die Abhängigkeiten:

```bash
pip install -r requirements.txt
```

### Lokale Vorschau

Führen Sie MkDocs für die Sprache aus, die Sie Vorschauen möchten:

```bash
mkdocs serve -f docs/de/mkdocs.yml
```

### Online-Ansicht

- **Deutsch**: [https://docs.gl-inet.com/router/de/4/](https://docs.gl-inet.com/router/de/4/)

---

## Español

Este repositorio contiene los archivos fuente para la documentación del firmware 4.x de los routers GL.iNet.

Ahora es un repositorio de documentación multilingüe. Los sitios de idioma actuales en este repositorio son:

- **Inglés**: `docs/en/`
- **Alemán**: `docs/de/`
- **Español**: `docs/es/`
- **Japonés**: `docs/jp/`
- **Coreano**: `docs/ko/`

Cada idioma tiene su propio directorio `mkdocs.yml`, `docs/` y `overrides/`.

### Entorno

La documentación se construye con [MkDocs](https://www.mkdocs.org/) 1.5.3 y el tema [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 9.4.6.

### Instalación

Cree un entorno virtual de Python:

```bash
python -m venv .venv
```

Active el entorno virtual y luego instale las dependencias:

```bash
pip install -r requirements.txt
```

### Vista previa local

Ejecute MkDocs contra el idioma que desea previsualizar:

```bash
mkdocs serve -f docs/es/mkdocs.yml
```

### Vista en línea

- **Español**: [https://docs.gl-inet.com/router/es/4/](https://docs.gl-inet.com/router/es/4/)

---

## 日本語

このリポジトリには、GL.iNetルーターファームウェア4.xドキュメントのソースファイルが含まれています。

現在、多言語ドキュメントリポジトリとして運営されています。このリポジトリの現在の言語サイトは以下の通りです：

- **英語**: `docs/en/`
- **ドイツ語**: `docs/de/`
- **スペイン語**: `docs/es/`
- **日本語**: `docs/jp/`
- **韓国語**: `docs/ko/`

各言語には独自の `mkdocs.yml`、`docs/`、および `overrides/` ディレクトリがあります。

### 環境

ドキュメントは [MkDocs](https://www.mkdocs.org/) 1.5.3 および [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) テーマ 9.4.6 でビルドされています。

### インストール

Python仮想環境を作成します：

```bash
python -m venv .venv
```

仮想環境をアクティブにしてから、依存関係をインストールします：

```bash
pip install -r requirements.txt
```

### ローカルプレビュー

プレビューする言語でMkDocsを実行します：

```bash
mkdocs serve -f docs/jp/mkdocs.yml
```

### オンラインビュー

- **日本語**: [https://docs.gl-inet.com/router/jp/4/](https://docs.gl-inet.com/router/jp/4/)

---
