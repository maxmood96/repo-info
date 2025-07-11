<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250710`](#odoo160-20250710)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250710`](#odoo170-20250710)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250710`](#odoo180-20250710)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:3164b5dc56b190806fc5795bcc8d0047cd5528155535e18ba05dbdb29518b7bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:cf9336a7f946d6a5f92151fd5d8446dc75745c4902c9b0947193d3a43ad7c210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.1 MB (585140148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e935082be1b2d273c82b36f310fc9b739be0310a86f28639f01644be07e3bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=C.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=16.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49064d53a2fab77e9bb6937622c490c40122e9754b82e884d3b42e99eba4d8c7`  
		Last Modified: Thu, 10 Jul 2025 22:12:53 GMT  
		Size: 219.6 MB (219627137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2a6d9421b08426be3da064f45a41e008f9e7c1e5c3883ef480fdc64c5a92f1`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 2.6 MB (2627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b4570317fbbc64a556932bcf87e7b601b7fdbbb3167a7f3378d55ab2ff730c`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 479.1 KB (479054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8f637e575f8813d0c94d4bcde1bdbea824780cbe37d648b188b94d5cf68a4`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 332.1 MB (332148369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3339c9a829f78c58991d85925d25c01dc7908b2b5fae5182254b2d11515d01b1`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 701.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5026f862d773d6f14b549e130c488fdf18fe5cfe5f3ee9184f204e0d2e3c4a2c`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e6995e4b9e98d6ce37146a8a760dd7c751326f235a6b75c74d86cef7f3fa8`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ae20cf8498cb9148ad67e7623f7e98eb291063ae6fe1ff1effc2d6ef32931`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:00e4f0b5c91fe8d271b62325ab6765b3e156a75247e5354edb882af6f90ab41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39557319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4b325a03b484e39df870f29baf7c2303d8c1b49603d6c1f4f9341130fdabb5`

```dockerfile
```

-	Layers:
	-	`sha256:15a6a8f2e81412fde2f19a1891afa2ae42e27dd5384362adb54710ccb421854c`  
		Last Modified: Thu, 10 Jul 2025 22:12:25 GMT  
		Size: 39.5 MB (39530601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb215474ad0185c511cdcbe25322f7b4c0e8cc277bf7e78b2fdd6695285f962e`  
		Last Modified: Thu, 10 Jul 2025 22:12:26 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8261c7c667051c2548ebe60901b2a18d19eeacc33a349cad7aaba1a7a881bfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.6 MB (580590873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2b6b132fc3d7768653de7e11e8936eaacf5ca5eb4e0b498c93815300866c75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=C.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=16.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f139329725c25fb45908efd4d1b3f14835959b80ee921e82449f1b9c1c7e33`  
		Last Modified: Thu, 10 Jul 2025 22:15:54 GMT  
		Size: 216.9 MB (216918856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23980098e07377e4ec86a9b4771ba6b2bb8b503aab11c5bad6125b37692ef219`  
		Last Modified: Thu, 10 Jul 2025 19:19:12 GMT  
		Size: 2.6 MB (2635403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aa109192a5870c08a039d2b6126a8c339267745d089af8c0ea6f97226f365a`  
		Last Modified: Thu, 10 Jul 2025 19:19:12 GMT  
		Size: 479.0 KB (479042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef75f050913c558602a5ce34a4b61e82c29785f96522899eee0f65efb82fd05`  
		Last Modified: Thu, 10 Jul 2025 22:15:49 GMT  
		Size: 331.8 MB (331811007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf811f41225924fd084ca9305cccbd0a124bb1e0bc16369dba394711158927`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37efdcd3def2bc24566219168efb48c2d357c215f13ac0834f8d5710bb31d23`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1671d60bd9835024a9337c8525d2dde04ace7d6b127a1a198fdbc541227bf98`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54b50c045e31b92e133ccea4b31637e74f2258471fd82d9bc301f1a4360d472`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e63b1631277f4c5cb3c1922b1be771108ae7633b02e3da907798b0f5e8391fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39563937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86baea812e3aa70df5ddd4d341ee2426733278d2df0a7d217772a94bcabeb32`

```dockerfile
```

-	Layers:
	-	`sha256:9a18fdf752cb0114d024e3434a14ae3c23004fdd954e3f35130d34e67c3377a1`  
		Last Modified: Thu, 10 Jul 2025 22:13:02 GMT  
		Size: 39.5 MB (39537067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ee48fe1a9d8942d5bfe4a42f5441563700622f7e253bc3eefa00c31a262764`  
		Last Modified: Thu, 10 Jul 2025 22:13:03 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:3164b5dc56b190806fc5795bcc8d0047cd5528155535e18ba05dbdb29518b7bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:cf9336a7f946d6a5f92151fd5d8446dc75745c4902c9b0947193d3a43ad7c210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.1 MB (585140148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e935082be1b2d273c82b36f310fc9b739be0310a86f28639f01644be07e3bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=C.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=16.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49064d53a2fab77e9bb6937622c490c40122e9754b82e884d3b42e99eba4d8c7`  
		Last Modified: Thu, 10 Jul 2025 22:12:53 GMT  
		Size: 219.6 MB (219627137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2a6d9421b08426be3da064f45a41e008f9e7c1e5c3883ef480fdc64c5a92f1`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 2.6 MB (2627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b4570317fbbc64a556932bcf87e7b601b7fdbbb3167a7f3378d55ab2ff730c`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 479.1 KB (479054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8f637e575f8813d0c94d4bcde1bdbea824780cbe37d648b188b94d5cf68a4`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 332.1 MB (332148369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3339c9a829f78c58991d85925d25c01dc7908b2b5fae5182254b2d11515d01b1`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 701.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5026f862d773d6f14b549e130c488fdf18fe5cfe5f3ee9184f204e0d2e3c4a2c`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e6995e4b9e98d6ce37146a8a760dd7c751326f235a6b75c74d86cef7f3fa8`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ae20cf8498cb9148ad67e7623f7e98eb291063ae6fe1ff1effc2d6ef32931`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:00e4f0b5c91fe8d271b62325ab6765b3e156a75247e5354edb882af6f90ab41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39557319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4b325a03b484e39df870f29baf7c2303d8c1b49603d6c1f4f9341130fdabb5`

```dockerfile
```

-	Layers:
	-	`sha256:15a6a8f2e81412fde2f19a1891afa2ae42e27dd5384362adb54710ccb421854c`  
		Last Modified: Thu, 10 Jul 2025 22:12:25 GMT  
		Size: 39.5 MB (39530601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb215474ad0185c511cdcbe25322f7b4c0e8cc277bf7e78b2fdd6695285f962e`  
		Last Modified: Thu, 10 Jul 2025 22:12:26 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8261c7c667051c2548ebe60901b2a18d19eeacc33a349cad7aaba1a7a881bfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.6 MB (580590873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2b6b132fc3d7768653de7e11e8936eaacf5ca5eb4e0b498c93815300866c75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=C.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=16.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f139329725c25fb45908efd4d1b3f14835959b80ee921e82449f1b9c1c7e33`  
		Last Modified: Thu, 10 Jul 2025 22:15:54 GMT  
		Size: 216.9 MB (216918856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23980098e07377e4ec86a9b4771ba6b2bb8b503aab11c5bad6125b37692ef219`  
		Last Modified: Thu, 10 Jul 2025 19:19:12 GMT  
		Size: 2.6 MB (2635403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aa109192a5870c08a039d2b6126a8c339267745d089af8c0ea6f97226f365a`  
		Last Modified: Thu, 10 Jul 2025 19:19:12 GMT  
		Size: 479.0 KB (479042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef75f050913c558602a5ce34a4b61e82c29785f96522899eee0f65efb82fd05`  
		Last Modified: Thu, 10 Jul 2025 22:15:49 GMT  
		Size: 331.8 MB (331811007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf811f41225924fd084ca9305cccbd0a124bb1e0bc16369dba394711158927`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37efdcd3def2bc24566219168efb48c2d357c215f13ac0834f8d5710bb31d23`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1671d60bd9835024a9337c8525d2dde04ace7d6b127a1a198fdbc541227bf98`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54b50c045e31b92e133ccea4b31637e74f2258471fd82d9bc301f1a4360d472`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e63b1631277f4c5cb3c1922b1be771108ae7633b02e3da907798b0f5e8391fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39563937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86baea812e3aa70df5ddd4d341ee2426733278d2df0a7d217772a94bcabeb32`

```dockerfile
```

-	Layers:
	-	`sha256:9a18fdf752cb0114d024e3434a14ae3c23004fdd954e3f35130d34e67c3377a1`  
		Last Modified: Thu, 10 Jul 2025 22:13:02 GMT  
		Size: 39.5 MB (39537067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ee48fe1a9d8942d5bfe4a42f5441563700622f7e253bc3eefa00c31a262764`  
		Last Modified: Thu, 10 Jul 2025 22:13:03 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250710`

```console
$ docker pull odoo@sha256:3164b5dc56b190806fc5795bcc8d0047cd5528155535e18ba05dbdb29518b7bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250710` - linux; amd64

```console
$ docker pull odoo@sha256:cf9336a7f946d6a5f92151fd5d8446dc75745c4902c9b0947193d3a43ad7c210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.1 MB (585140148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e935082be1b2d273c82b36f310fc9b739be0310a86f28639f01644be07e3bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=C.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=16.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49064d53a2fab77e9bb6937622c490c40122e9754b82e884d3b42e99eba4d8c7`  
		Last Modified: Thu, 10 Jul 2025 22:12:53 GMT  
		Size: 219.6 MB (219627137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2a6d9421b08426be3da064f45a41e008f9e7c1e5c3883ef480fdc64c5a92f1`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 2.6 MB (2627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b4570317fbbc64a556932bcf87e7b601b7fdbbb3167a7f3378d55ab2ff730c`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 479.1 KB (479054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8f637e575f8813d0c94d4bcde1bdbea824780cbe37d648b188b94d5cf68a4`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 332.1 MB (332148369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3339c9a829f78c58991d85925d25c01dc7908b2b5fae5182254b2d11515d01b1`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 701.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5026f862d773d6f14b549e130c488fdf18fe5cfe5f3ee9184f204e0d2e3c4a2c`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e6995e4b9e98d6ce37146a8a760dd7c751326f235a6b75c74d86cef7f3fa8`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ae20cf8498cb9148ad67e7623f7e98eb291063ae6fe1ff1effc2d6ef32931`  
		Last Modified: Thu, 10 Jul 2025 19:09:55 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:00e4f0b5c91fe8d271b62325ab6765b3e156a75247e5354edb882af6f90ab41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39557319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4b325a03b484e39df870f29baf7c2303d8c1b49603d6c1f4f9341130fdabb5`

```dockerfile
```

-	Layers:
	-	`sha256:15a6a8f2e81412fde2f19a1891afa2ae42e27dd5384362adb54710ccb421854c`  
		Last Modified: Thu, 10 Jul 2025 22:12:25 GMT  
		Size: 39.5 MB (39530601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb215474ad0185c511cdcbe25322f7b4c0e8cc277bf7e78b2fdd6695285f962e`  
		Last Modified: Thu, 10 Jul 2025 22:12:26 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250710` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8261c7c667051c2548ebe60901b2a18d19eeacc33a349cad7aaba1a7a881bfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.6 MB (580590873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2b6b132fc3d7768653de7e11e8936eaacf5ca5eb4e0b498c93815300866c75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=C.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=16.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=19cd95eede623d4e0c544267af91a4bc14b204db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f139329725c25fb45908efd4d1b3f14835959b80ee921e82449f1b9c1c7e33`  
		Last Modified: Thu, 10 Jul 2025 22:15:54 GMT  
		Size: 216.9 MB (216918856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23980098e07377e4ec86a9b4771ba6b2bb8b503aab11c5bad6125b37692ef219`  
		Last Modified: Thu, 10 Jul 2025 19:19:12 GMT  
		Size: 2.6 MB (2635403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aa109192a5870c08a039d2b6126a8c339267745d089af8c0ea6f97226f365a`  
		Last Modified: Thu, 10 Jul 2025 19:19:12 GMT  
		Size: 479.0 KB (479042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef75f050913c558602a5ce34a4b61e82c29785f96522899eee0f65efb82fd05`  
		Last Modified: Thu, 10 Jul 2025 22:15:49 GMT  
		Size: 331.8 MB (331811007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf811f41225924fd084ca9305cccbd0a124bb1e0bc16369dba394711158927`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37efdcd3def2bc24566219168efb48c2d357c215f13ac0834f8d5710bb31d23`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1671d60bd9835024a9337c8525d2dde04ace7d6b127a1a198fdbc541227bf98`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54b50c045e31b92e133ccea4b31637e74f2258471fd82d9bc301f1a4360d472`  
		Last Modified: Thu, 10 Jul 2025 19:19:11 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:e63b1631277f4c5cb3c1922b1be771108ae7633b02e3da907798b0f5e8391fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39563937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86baea812e3aa70df5ddd4d341ee2426733278d2df0a7d217772a94bcabeb32`

```dockerfile
```

-	Layers:
	-	`sha256:9a18fdf752cb0114d024e3434a14ae3c23004fdd954e3f35130d34e67c3377a1`  
		Last Modified: Thu, 10 Jul 2025 22:13:02 GMT  
		Size: 39.5 MB (39537067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ee48fe1a9d8942d5bfe4a42f5441563700622f7e253bc3eefa00c31a262764`  
		Last Modified: Thu, 10 Jul 2025 22:13:03 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:b3ff10fe374835de4b650903c5e6400081b51112f819bf8d84936796281fe16e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:48f928efb0b43cd24a16479f1f0dac62e1e23f74c648e97a777e0bbd495cec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 MB (601419830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7875556b6aa56a1de0807e0d78a937b94692c59a925cce494c438726d0c239d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ece2f5344d18c0d805a6eb3b11480148c1caa58891be92d3266afe727b85e6`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 233.9 MB (233930681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d20cc40bb3cae664d9b9c26d6831b18d6d9f42303b592769b4e2abf1ddec3`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 2.5 MB (2523186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c2bc31151a72635368aca20ddbf5a30a03172812cbef0da98987c36da7845b`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 480.1 KB (480097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c9d7907298ca7558c169665f1d39d4ba19c022e6aace76f4c620366a317ed4`  
		Last Modified: Thu, 10 Jul 2025 22:13:10 GMT  
		Size: 334.9 MB (334947744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3ac2a47e870c620e454d086c6366031a856998e6d2a1b0caac8bf7aa21d37a`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3313e7cb048e81f40f89b0ec73fa6c14718e97f2bdbe139bf5a9dcbea4407021`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e327dcdfd2fbfe658fd73e2910e0f55e4a76593080628870b2af9f78924924d`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a055c29a0eb688c04344d922cdd5900ae38af8511bdc0b5277d6f0cb2975e86`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4cacdb7be6dda688f8d0149f506c44bf747d536318e730fbe88f6a0201f1997a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40483108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b983a9fe53591b7ac8248749e87cd7ebb75230bff215c23bb0c75957e3d7544`

```dockerfile
```

-	Layers:
	-	`sha256:0bd8aadd7864103631d895fe21eb5a4cd88760de7551707eb63fb971f871d104`  
		Last Modified: Thu, 10 Jul 2025 22:12:37 GMT  
		Size: 40.5 MB (40456273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9aa2e09d74f90aa5e849e21eee26502149d3bf752496e4eed552df85a989095`  
		Last Modified: Thu, 10 Jul 2025 22:12:38 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:23247f5a2535e037f39d2d05f488f4e20c356009eca3177d1e3ca7c850fc4079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596069487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640cf1993c671f0bb1657bdc4618df40e7c6b21c5ac41df31d6281f5ddf74b84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c86124df46151281b12e28b4a56b43a15472ecf23c2fb3eccc7233bc3c847`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 231.2 MB (231155283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7ee5a1beb01cd4f56f69aed4ce84327c4e136c5c04f9531a526a7f9934cf9`  
		Last Modified: Wed, 02 Jul 2025 07:25:46 GMT  
		Size: 2.5 MB (2516262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2529d3bfb7f973f508e180afefaf73063a3c6655fbaeb45d744a1c8366ad6d77`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 480.1 KB (480091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8e604554aeebe33aad0bfdb1fa8d22372cae4c17cd4ef09d60a1c81e2f9b9`  
		Last Modified: Thu, 10 Jul 2025 22:17:17 GMT  
		Size: 334.6 MB (334556143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8796163156e98461e732abf77846864503ed4d21e18f78d7055e6dc5ae061b2`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b1780bd7f6a6f927847536f0c103677eb5854a13a5353f2265872345d7148`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae7f73a6652fee8396addaeb74ace12b571869966423cfe979e08d8b645ccd9`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e354edc6a141783b71d8d9a8e1429f37af66d97160d5f89c1199162cb274be6`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:8824c5369424afbb2451fcb14b878e2f1577d98fd4ce90e19cd65c2c258a804e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40489767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7287b9f848069dda070c8108a7b2ba8169768cde28cfc63fd0c183abca435b0`

```dockerfile
```

-	Layers:
	-	`sha256:8a14dc15ab1fc27a1e1503a2968613106f382666af212bcdcc201b7b1bde6c96`  
		Last Modified: Thu, 10 Jul 2025 22:13:15 GMT  
		Size: 40.5 MB (40462780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524375745f8f6478581db3872a80454dfe4c0899389cb76db263c5acdc4c9187`  
		Last Modified: Thu, 10 Jul 2025 22:13:16 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:5a66fbb729b6a8aef5a142cc108acbc45d9d7004814d6a71541f69551194f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617699729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166a802cffc701f0815317ab4945b0546150ab73183516bdd025fe8befe6e6ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:39 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Fri, 20 Jun 2025 10:18:39 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6ea6d5109d4d1b0a3362e810a1cd03a8680dcebb1b35dd00b36949d86c3e3`  
		Last Modified: Wed, 02 Jul 2025 14:49:08 GMT  
		Size: 243.3 MB (243261706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5064b7f25f4525a7d9e2d3d4505d2351d777fcd398b6d2b1acd03d9360cb25b`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 2.8 MB (2841522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4813f1ddec64145879a01ab0e281abf700bc8755c273d520e1bb54bfb92fc3c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f359b8d1b6cde9279529b05f3981059243c8ca6963ce05223c51a87870a8ba26`  
		Last Modified: Thu, 10 Jul 2025 19:20:41 GMT  
		Size: 336.7 MB (336671332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857742385bb8ccba0f69d5f0f396c68104aaa11e6d137fa8b9a13ac306ceacc`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be1306dedd4cd68aa7c4f4eb988f5dd03c7f030358ba7a87e4f7aa082b63983`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b680a6d96f161b75b3f5441ca01c185f39c002efd1eeb44ef90fb45a61f8d6`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0066e9e38c3228b6ce74e28b8328ffd47f29669144db765dee8f604a9acae50`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e46d15e9ea6f4612cde8f45a1b99cc4fd83b360887aeab16b6fcd46f05c887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40491771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2dd9984047384ec257e4c13db90d184de99526095c05ec332a4a82aaa6e6e2`

```dockerfile
```

-	Layers:
	-	`sha256:e299ca11fd3b1769b1e27bd41ce320426043874da4bf58742a5d7255a0ff39bd`  
		Last Modified: Thu, 10 Jul 2025 22:13:55 GMT  
		Size: 40.5 MB (40464880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a46af16089a2beac684ea724cc94928aea9d1dcecf5bcc80436132b2638d42`  
		Last Modified: Thu, 10 Jul 2025 22:13:56 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:b3ff10fe374835de4b650903c5e6400081b51112f819bf8d84936796281fe16e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:48f928efb0b43cd24a16479f1f0dac62e1e23f74c648e97a777e0bbd495cec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 MB (601419830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7875556b6aa56a1de0807e0d78a937b94692c59a925cce494c438726d0c239d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ece2f5344d18c0d805a6eb3b11480148c1caa58891be92d3266afe727b85e6`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 233.9 MB (233930681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d20cc40bb3cae664d9b9c26d6831b18d6d9f42303b592769b4e2abf1ddec3`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 2.5 MB (2523186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c2bc31151a72635368aca20ddbf5a30a03172812cbef0da98987c36da7845b`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 480.1 KB (480097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c9d7907298ca7558c169665f1d39d4ba19c022e6aace76f4c620366a317ed4`  
		Last Modified: Thu, 10 Jul 2025 22:13:10 GMT  
		Size: 334.9 MB (334947744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3ac2a47e870c620e454d086c6366031a856998e6d2a1b0caac8bf7aa21d37a`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3313e7cb048e81f40f89b0ec73fa6c14718e97f2bdbe139bf5a9dcbea4407021`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e327dcdfd2fbfe658fd73e2910e0f55e4a76593080628870b2af9f78924924d`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a055c29a0eb688c04344d922cdd5900ae38af8511bdc0b5277d6f0cb2975e86`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4cacdb7be6dda688f8d0149f506c44bf747d536318e730fbe88f6a0201f1997a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40483108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b983a9fe53591b7ac8248749e87cd7ebb75230bff215c23bb0c75957e3d7544`

```dockerfile
```

-	Layers:
	-	`sha256:0bd8aadd7864103631d895fe21eb5a4cd88760de7551707eb63fb971f871d104`  
		Last Modified: Thu, 10 Jul 2025 22:12:37 GMT  
		Size: 40.5 MB (40456273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9aa2e09d74f90aa5e849e21eee26502149d3bf752496e4eed552df85a989095`  
		Last Modified: Thu, 10 Jul 2025 22:12:38 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:23247f5a2535e037f39d2d05f488f4e20c356009eca3177d1e3ca7c850fc4079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596069487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640cf1993c671f0bb1657bdc4618df40e7c6b21c5ac41df31d6281f5ddf74b84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c86124df46151281b12e28b4a56b43a15472ecf23c2fb3eccc7233bc3c847`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 231.2 MB (231155283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7ee5a1beb01cd4f56f69aed4ce84327c4e136c5c04f9531a526a7f9934cf9`  
		Last Modified: Wed, 02 Jul 2025 07:25:46 GMT  
		Size: 2.5 MB (2516262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2529d3bfb7f973f508e180afefaf73063a3c6655fbaeb45d744a1c8366ad6d77`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 480.1 KB (480091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8e604554aeebe33aad0bfdb1fa8d22372cae4c17cd4ef09d60a1c81e2f9b9`  
		Last Modified: Thu, 10 Jul 2025 22:17:17 GMT  
		Size: 334.6 MB (334556143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8796163156e98461e732abf77846864503ed4d21e18f78d7055e6dc5ae061b2`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b1780bd7f6a6f927847536f0c103677eb5854a13a5353f2265872345d7148`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae7f73a6652fee8396addaeb74ace12b571869966423cfe979e08d8b645ccd9`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e354edc6a141783b71d8d9a8e1429f37af66d97160d5f89c1199162cb274be6`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8824c5369424afbb2451fcb14b878e2f1577d98fd4ce90e19cd65c2c258a804e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40489767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7287b9f848069dda070c8108a7b2ba8169768cde28cfc63fd0c183abca435b0`

```dockerfile
```

-	Layers:
	-	`sha256:8a14dc15ab1fc27a1e1503a2968613106f382666af212bcdcc201b7b1bde6c96`  
		Last Modified: Thu, 10 Jul 2025 22:13:15 GMT  
		Size: 40.5 MB (40462780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524375745f8f6478581db3872a80454dfe4c0899389cb76db263c5acdc4c9187`  
		Last Modified: Thu, 10 Jul 2025 22:13:16 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5a66fbb729b6a8aef5a142cc108acbc45d9d7004814d6a71541f69551194f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617699729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166a802cffc701f0815317ab4945b0546150ab73183516bdd025fe8befe6e6ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:39 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Fri, 20 Jun 2025 10:18:39 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6ea6d5109d4d1b0a3362e810a1cd03a8680dcebb1b35dd00b36949d86c3e3`  
		Last Modified: Wed, 02 Jul 2025 14:49:08 GMT  
		Size: 243.3 MB (243261706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5064b7f25f4525a7d9e2d3d4505d2351d777fcd398b6d2b1acd03d9360cb25b`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 2.8 MB (2841522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4813f1ddec64145879a01ab0e281abf700bc8755c273d520e1bb54bfb92fc3c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f359b8d1b6cde9279529b05f3981059243c8ca6963ce05223c51a87870a8ba26`  
		Last Modified: Thu, 10 Jul 2025 19:20:41 GMT  
		Size: 336.7 MB (336671332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857742385bb8ccba0f69d5f0f396c68104aaa11e6d137fa8b9a13ac306ceacc`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be1306dedd4cd68aa7c4f4eb988f5dd03c7f030358ba7a87e4f7aa082b63983`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b680a6d96f161b75b3f5441ca01c185f39c002efd1eeb44ef90fb45a61f8d6`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0066e9e38c3228b6ce74e28b8328ffd47f29669144db765dee8f604a9acae50`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e46d15e9ea6f4612cde8f45a1b99cc4fd83b360887aeab16b6fcd46f05c887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40491771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2dd9984047384ec257e4c13db90d184de99526095c05ec332a4a82aaa6e6e2`

```dockerfile
```

-	Layers:
	-	`sha256:e299ca11fd3b1769b1e27bd41ce320426043874da4bf58742a5d7255a0ff39bd`  
		Last Modified: Thu, 10 Jul 2025 22:13:55 GMT  
		Size: 40.5 MB (40464880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a46af16089a2beac684ea724cc94928aea9d1dcecf5bcc80436132b2638d42`  
		Last Modified: Thu, 10 Jul 2025 22:13:56 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250710`

```console
$ docker pull odoo@sha256:b3ff10fe374835de4b650903c5e6400081b51112f819bf8d84936796281fe16e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250710` - linux; amd64

```console
$ docker pull odoo@sha256:48f928efb0b43cd24a16479f1f0dac62e1e23f74c648e97a777e0bbd495cec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 MB (601419830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7875556b6aa56a1de0807e0d78a937b94692c59a925cce494c438726d0c239d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ece2f5344d18c0d805a6eb3b11480148c1caa58891be92d3266afe727b85e6`  
		Last Modified: Thu, 10 Jul 2025 22:13:05 GMT  
		Size: 233.9 MB (233930681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d20cc40bb3cae664d9b9c26d6831b18d6d9f42303b592769b4e2abf1ddec3`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 2.5 MB (2523186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c2bc31151a72635368aca20ddbf5a30a03172812cbef0da98987c36da7845b`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 480.1 KB (480097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c9d7907298ca7558c169665f1d39d4ba19c022e6aace76f4c620366a317ed4`  
		Last Modified: Thu, 10 Jul 2025 22:13:10 GMT  
		Size: 334.9 MB (334947744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3ac2a47e870c620e454d086c6366031a856998e6d2a1b0caac8bf7aa21d37a`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3313e7cb048e81f40f89b0ec73fa6c14718e97f2bdbe139bf5a9dcbea4407021`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e327dcdfd2fbfe658fd73e2910e0f55e4a76593080628870b2af9f78924924d`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a055c29a0eb688c04344d922cdd5900ae38af8511bdc0b5277d6f0cb2975e86`  
		Last Modified: Thu, 10 Jul 2025 19:10:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:4cacdb7be6dda688f8d0149f506c44bf747d536318e730fbe88f6a0201f1997a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40483108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b983a9fe53591b7ac8248749e87cd7ebb75230bff215c23bb0c75957e3d7544`

```dockerfile
```

-	Layers:
	-	`sha256:0bd8aadd7864103631d895fe21eb5a4cd88760de7551707eb63fb971f871d104`  
		Last Modified: Thu, 10 Jul 2025 22:12:37 GMT  
		Size: 40.5 MB (40456273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9aa2e09d74f90aa5e849e21eee26502149d3bf752496e4eed552df85a989095`  
		Last Modified: Thu, 10 Jul 2025 22:12:38 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250710` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:23247f5a2535e037f39d2d05f488f4e20c356009eca3177d1e3ca7c850fc4079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596069487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640cf1993c671f0bb1657bdc4618df40e7c6b21c5ac41df31d6281f5ddf74b84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c86124df46151281b12e28b4a56b43a15472ecf23c2fb3eccc7233bc3c847`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 231.2 MB (231155283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7ee5a1beb01cd4f56f69aed4ce84327c4e136c5c04f9531a526a7f9934cf9`  
		Last Modified: Wed, 02 Jul 2025 07:25:46 GMT  
		Size: 2.5 MB (2516262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2529d3bfb7f973f508e180afefaf73063a3c6655fbaeb45d744a1c8366ad6d77`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 480.1 KB (480091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8e604554aeebe33aad0bfdb1fa8d22372cae4c17cd4ef09d60a1c81e2f9b9`  
		Last Modified: Thu, 10 Jul 2025 22:17:17 GMT  
		Size: 334.6 MB (334556143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8796163156e98461e732abf77846864503ed4d21e18f78d7055e6dc5ae061b2`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b1780bd7f6a6f927847536f0c103677eb5854a13a5353f2265872345d7148`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae7f73a6652fee8396addaeb74ace12b571869966423cfe979e08d8b645ccd9`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e354edc6a141783b71d8d9a8e1429f37af66d97160d5f89c1199162cb274be6`  
		Last Modified: Thu, 10 Jul 2025 19:15:36 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:8824c5369424afbb2451fcb14b878e2f1577d98fd4ce90e19cd65c2c258a804e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40489767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7287b9f848069dda070c8108a7b2ba8169768cde28cfc63fd0c183abca435b0`

```dockerfile
```

-	Layers:
	-	`sha256:8a14dc15ab1fc27a1e1503a2968613106f382666af212bcdcc201b7b1bde6c96`  
		Last Modified: Thu, 10 Jul 2025 22:13:15 GMT  
		Size: 40.5 MB (40462780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:524375745f8f6478581db3872a80454dfe4c0899389cb76db263c5acdc4c9187`  
		Last Modified: Thu, 10 Jul 2025 22:13:16 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250710` - linux; ppc64le

```console
$ docker pull odoo@sha256:5a66fbb729b6a8aef5a142cc108acbc45d9d7004814d6a71541f69551194f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617699729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166a802cffc701f0815317ab4945b0546150ab73183516bdd025fe8befe6e6ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:39 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Fri, 20 Jun 2025 10:18:39 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=17.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=97b1dd31e5b279d8d9bc9e880794e0f47dbf9f5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6ea6d5109d4d1b0a3362e810a1cd03a8680dcebb1b35dd00b36949d86c3e3`  
		Last Modified: Wed, 02 Jul 2025 14:49:08 GMT  
		Size: 243.3 MB (243261706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5064b7f25f4525a7d9e2d3d4505d2351d777fcd398b6d2b1acd03d9360cb25b`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 2.8 MB (2841522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4813f1ddec64145879a01ab0e281abf700bc8755c273d520e1bb54bfb92fc3c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f359b8d1b6cde9279529b05f3981059243c8ca6963ce05223c51a87870a8ba26`  
		Last Modified: Thu, 10 Jul 2025 19:20:41 GMT  
		Size: 336.7 MB (336671332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857742385bb8ccba0f69d5f0f396c68104aaa11e6d137fa8b9a13ac306ceacc`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be1306dedd4cd68aa7c4f4eb988f5dd03c7f030358ba7a87e4f7aa082b63983`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b680a6d96f161b75b3f5441ca01c185f39c002efd1eeb44ef90fb45a61f8d6`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0066e9e38c3228b6ce74e28b8328ffd47f29669144db765dee8f604a9acae50`  
		Last Modified: Thu, 10 Jul 2025 19:20:47 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e46d15e9ea6f4612cde8f45a1b99cc4fd83b360887aeab16b6fcd46f05c887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40491771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2dd9984047384ec257e4c13db90d184de99526095c05ec332a4a82aaa6e6e2`

```dockerfile
```

-	Layers:
	-	`sha256:e299ca11fd3b1769b1e27bd41ce320426043874da4bf58742a5d7255a0ff39bd`  
		Last Modified: Thu, 10 Jul 2025 22:13:55 GMT  
		Size: 40.5 MB (40464880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a46af16089a2beac684ea724cc94928aea9d1dcecf5bcc80436132b2638d42`  
		Last Modified: Thu, 10 Jul 2025 22:13:56 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:1d243f0f1448390c2863575efa6a78cc02b1d44586d8fb9ea472f8e216609845
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:7235a6200293f3b09b588260db22f01eb8f15e2707ca31454b85c0d047870d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672891570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b2f03bede647f3660252d5a30aca052baf7b6966a547a1eba5a39343d11ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244901ca41e14ba5483ed7a71a7160291b0e2aea5ea87f35308020331b7b6e61`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 254.7 MB (254704337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa4b6e720391d98b70199170e225510dcafb7a6dcfaf0219bf6805fe5f0382`  
		Last Modified: Thu, 10 Jul 2025 19:10:31 GMT  
		Size: 14.3 MB (14275280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df4e1506c3375c105ca74eaf606137870171d0c4a9ff3a7a8ad8230fd627e5`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 479.9 KB (479852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72566032ce57bc4d555557bbcb346658ac471d7e02b74e48e731c0ae80606ce`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 373.7 MB (373711300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e781d53e3fdadb21b4be21041d2f85e2efd37b841f72b745c289d0b6c29f7a2`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0bc51d9f5c4643e045d3ed5a41f09b056ea813b2d77ca9f39eb8c2f063fcef`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a27ef56270dc68267b4cc548d2780ff7d911b4ea8ec0acda33c50e132421b33`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8442acccb2f3fff8c4259fd44beb796adcf8a8620cfda47cc8b6d5299e2e5118`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:2edcb9a8a60e068117ab67e0a8b79dbd9e80e69a06582f00640121c9f2201a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60277621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef50aa61e059075d9bc1e05b3bc8ba4738319f12aea133082f788bff8939e2b`

```dockerfile
```

-	Layers:
	-	`sha256:1ce9280a7beb5424699aeeb9ab2e3fc1bb719cec76031aec71aee59f61973b88`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 60.3 MB (60250485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507377e1ca9cf7dd0dac06e9b339b0e8b2ed0cad6c0e8c4a8c4aba3b8e0818b2`  
		Last Modified: Thu, 10 Jul 2025 22:12:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d9da5f894869339fae75d41c649d14041e5a7a476d6c16338b4f2dd622472ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.1 MB (669077387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6ea9c76a4e66fdcd3c59c3ae07f6cb0b71e6b284d9cb16adc70653e44829fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e98f49a27a3036b9a25540180c28229b2b4a3073d9fa8905aee883806adf8f`  
		Last Modified: Thu, 10 Jul 2025 22:13:35 GMT  
		Size: 373.6 MB (373564206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270bed052c2dd54525956eb90ff719c0b89f33945940819f9bde14e44fb7a41`  
		Last Modified: Thu, 10 Jul 2025 19:11:55 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ec87eb7aaa98ca3f7872f0d0e95d3684c23fd6e0db748f24b5b52c206ae04a`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9d38ad71e0861da093153f63294b0a6e71835b85b917e3e94b76b0f8c7b9d`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ee093ea0550ae35a9f968c6580aaabe18fa6b19e8d7e713deb5f41fdbba47`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d5b27af6e8021cf4960e2b9b43920561f3b5d4bb4c5eb219a17e426f6fa72cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60285060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d9ce87d855ce7a470a9ef76ec4bf141bea8d7924431309b9467796a97a104`

```dockerfile
```

-	Layers:
	-	`sha256:534d20faa72e9539a6e82aa6c5a8d354b849745adf3f7bbb85dacc7bcad57a83`  
		Last Modified: Thu, 10 Jul 2025 22:14:21 GMT  
		Size: 60.3 MB (60257760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556b153458fb938af443f24c0bbb1ee2ebc81fd7ec66b0f97b1db47fa04f2c18`  
		Last Modified: Thu, 10 Jul 2025 22:14:22 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:10d452ba552846357307a1bf6548dc32cc63a96b33b2ae65e5a9042c092557df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.9 MB (688922308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7edd53da4bc8afde5c7499cdcc3b7fbdabbfde6f3f3ba6a322e08ec3ac08ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:18:14 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:18:18 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Thu, 19 Jun 2025 23:18:18 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b91774b9d3a456defc0d1c3602eae7a52c41ba6fc41639fdbf63dbb1c1b82e`  
		Last Modified: Thu, 10 Jul 2025 19:14:30 GMT  
		Size: 374.2 MB (374242554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2576ff59988ded3be714e6b9e68ea3da5012e99f2dcbd0fc3c9ecbc1dae2e`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3f0e891484cd875e25c56c717745497ffa0dcfb3a13689cdd8b54e8cef74d6`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c6933cfe9a6ae8e6978f3257b77e8925b9edb571e29816746de99d7fcb776`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32bf435553b3c3cd789da1822d3625c2a9c9e516732168b6440082cb4a79cbe`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b26d6f13842f72fec66f400481c9ed99f67b566f607b4408badbd0942c80142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5537110a95bdb82d36ea88e5b25951d3292d9be17deff3dc2733162de106a98c`

```dockerfile
```

-	Layers:
	-	`sha256:ad32489d4ce25ae09a998b4a8445be2e4486ed62663e52abeed7e49b2ffc5093`  
		Last Modified: Thu, 10 Jul 2025 22:15:44 GMT  
		Size: 60.3 MB (60258862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cb2a766695613c83613d57ff11e870a7755072cb912dc999bd7086531d8094`  
		Last Modified: Thu, 10 Jul 2025 22:15:45 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:1d243f0f1448390c2863575efa6a78cc02b1d44586d8fb9ea472f8e216609845
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:7235a6200293f3b09b588260db22f01eb8f15e2707ca31454b85c0d047870d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672891570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b2f03bede647f3660252d5a30aca052baf7b6966a547a1eba5a39343d11ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244901ca41e14ba5483ed7a71a7160291b0e2aea5ea87f35308020331b7b6e61`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 254.7 MB (254704337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa4b6e720391d98b70199170e225510dcafb7a6dcfaf0219bf6805fe5f0382`  
		Last Modified: Thu, 10 Jul 2025 19:10:31 GMT  
		Size: 14.3 MB (14275280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df4e1506c3375c105ca74eaf606137870171d0c4a9ff3a7a8ad8230fd627e5`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 479.9 KB (479852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72566032ce57bc4d555557bbcb346658ac471d7e02b74e48e731c0ae80606ce`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 373.7 MB (373711300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e781d53e3fdadb21b4be21041d2f85e2efd37b841f72b745c289d0b6c29f7a2`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0bc51d9f5c4643e045d3ed5a41f09b056ea813b2d77ca9f39eb8c2f063fcef`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a27ef56270dc68267b4cc548d2780ff7d911b4ea8ec0acda33c50e132421b33`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8442acccb2f3fff8c4259fd44beb796adcf8a8620cfda47cc8b6d5299e2e5118`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2edcb9a8a60e068117ab67e0a8b79dbd9e80e69a06582f00640121c9f2201a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60277621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef50aa61e059075d9bc1e05b3bc8ba4738319f12aea133082f788bff8939e2b`

```dockerfile
```

-	Layers:
	-	`sha256:1ce9280a7beb5424699aeeb9ab2e3fc1bb719cec76031aec71aee59f61973b88`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 60.3 MB (60250485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507377e1ca9cf7dd0dac06e9b339b0e8b2ed0cad6c0e8c4a8c4aba3b8e0818b2`  
		Last Modified: Thu, 10 Jul 2025 22:12:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d9da5f894869339fae75d41c649d14041e5a7a476d6c16338b4f2dd622472ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.1 MB (669077387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6ea9c76a4e66fdcd3c59c3ae07f6cb0b71e6b284d9cb16adc70653e44829fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e98f49a27a3036b9a25540180c28229b2b4a3073d9fa8905aee883806adf8f`  
		Last Modified: Thu, 10 Jul 2025 22:13:35 GMT  
		Size: 373.6 MB (373564206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270bed052c2dd54525956eb90ff719c0b89f33945940819f9bde14e44fb7a41`  
		Last Modified: Thu, 10 Jul 2025 19:11:55 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ec87eb7aaa98ca3f7872f0d0e95d3684c23fd6e0db748f24b5b52c206ae04a`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9d38ad71e0861da093153f63294b0a6e71835b85b917e3e94b76b0f8c7b9d`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ee093ea0550ae35a9f968c6580aaabe18fa6b19e8d7e713deb5f41fdbba47`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d5b27af6e8021cf4960e2b9b43920561f3b5d4bb4c5eb219a17e426f6fa72cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60285060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d9ce87d855ce7a470a9ef76ec4bf141bea8d7924431309b9467796a97a104`

```dockerfile
```

-	Layers:
	-	`sha256:534d20faa72e9539a6e82aa6c5a8d354b849745adf3f7bbb85dacc7bcad57a83`  
		Last Modified: Thu, 10 Jul 2025 22:14:21 GMT  
		Size: 60.3 MB (60257760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556b153458fb938af443f24c0bbb1ee2ebc81fd7ec66b0f97b1db47fa04f2c18`  
		Last Modified: Thu, 10 Jul 2025 22:14:22 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:10d452ba552846357307a1bf6548dc32cc63a96b33b2ae65e5a9042c092557df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.9 MB (688922308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7edd53da4bc8afde5c7499cdcc3b7fbdabbfde6f3f3ba6a322e08ec3ac08ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:18:14 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:18:18 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Thu, 19 Jun 2025 23:18:18 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b91774b9d3a456defc0d1c3602eae7a52c41ba6fc41639fdbf63dbb1c1b82e`  
		Last Modified: Thu, 10 Jul 2025 19:14:30 GMT  
		Size: 374.2 MB (374242554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2576ff59988ded3be714e6b9e68ea3da5012e99f2dcbd0fc3c9ecbc1dae2e`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3f0e891484cd875e25c56c717745497ffa0dcfb3a13689cdd8b54e8cef74d6`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c6933cfe9a6ae8e6978f3257b77e8925b9edb571e29816746de99d7fcb776`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32bf435553b3c3cd789da1822d3625c2a9c9e516732168b6440082cb4a79cbe`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b26d6f13842f72fec66f400481c9ed99f67b566f607b4408badbd0942c80142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5537110a95bdb82d36ea88e5b25951d3292d9be17deff3dc2733162de106a98c`

```dockerfile
```

-	Layers:
	-	`sha256:ad32489d4ce25ae09a998b4a8445be2e4486ed62663e52abeed7e49b2ffc5093`  
		Last Modified: Thu, 10 Jul 2025 22:15:44 GMT  
		Size: 60.3 MB (60258862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cb2a766695613c83613d57ff11e870a7755072cb912dc999bd7086531d8094`  
		Last Modified: Thu, 10 Jul 2025 22:15:45 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250710`

```console
$ docker pull odoo@sha256:1d243f0f1448390c2863575efa6a78cc02b1d44586d8fb9ea472f8e216609845
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250710` - linux; amd64

```console
$ docker pull odoo@sha256:7235a6200293f3b09b588260db22f01eb8f15e2707ca31454b85c0d047870d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672891570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b2f03bede647f3660252d5a30aca052baf7b6966a547a1eba5a39343d11ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244901ca41e14ba5483ed7a71a7160291b0e2aea5ea87f35308020331b7b6e61`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 254.7 MB (254704337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa4b6e720391d98b70199170e225510dcafb7a6dcfaf0219bf6805fe5f0382`  
		Last Modified: Thu, 10 Jul 2025 19:10:31 GMT  
		Size: 14.3 MB (14275280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df4e1506c3375c105ca74eaf606137870171d0c4a9ff3a7a8ad8230fd627e5`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 479.9 KB (479852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72566032ce57bc4d555557bbcb346658ac471d7e02b74e48e731c0ae80606ce`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 373.7 MB (373711300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e781d53e3fdadb21b4be21041d2f85e2efd37b841f72b745c289d0b6c29f7a2`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0bc51d9f5c4643e045d3ed5a41f09b056ea813b2d77ca9f39eb8c2f063fcef`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a27ef56270dc68267b4cc548d2780ff7d911b4ea8ec0acda33c50e132421b33`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8442acccb2f3fff8c4259fd44beb796adcf8a8620cfda47cc8b6d5299e2e5118`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:2edcb9a8a60e068117ab67e0a8b79dbd9e80e69a06582f00640121c9f2201a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60277621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef50aa61e059075d9bc1e05b3bc8ba4738319f12aea133082f788bff8939e2b`

```dockerfile
```

-	Layers:
	-	`sha256:1ce9280a7beb5424699aeeb9ab2e3fc1bb719cec76031aec71aee59f61973b88`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 60.3 MB (60250485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507377e1ca9cf7dd0dac06e9b339b0e8b2ed0cad6c0e8c4a8c4aba3b8e0818b2`  
		Last Modified: Thu, 10 Jul 2025 22:12:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250710` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d9da5f894869339fae75d41c649d14041e5a7a476d6c16338b4f2dd622472ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.1 MB (669077387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6ea9c76a4e66fdcd3c59c3ae07f6cb0b71e6b284d9cb16adc70653e44829fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e98f49a27a3036b9a25540180c28229b2b4a3073d9fa8905aee883806adf8f`  
		Last Modified: Thu, 10 Jul 2025 22:13:35 GMT  
		Size: 373.6 MB (373564206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270bed052c2dd54525956eb90ff719c0b89f33945940819f9bde14e44fb7a41`  
		Last Modified: Thu, 10 Jul 2025 19:11:55 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ec87eb7aaa98ca3f7872f0d0e95d3684c23fd6e0db748f24b5b52c206ae04a`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9d38ad71e0861da093153f63294b0a6e71835b85b917e3e94b76b0f8c7b9d`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ee093ea0550ae35a9f968c6580aaabe18fa6b19e8d7e713deb5f41fdbba47`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:d5b27af6e8021cf4960e2b9b43920561f3b5d4bb4c5eb219a17e426f6fa72cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60285060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d9ce87d855ce7a470a9ef76ec4bf141bea8d7924431309b9467796a97a104`

```dockerfile
```

-	Layers:
	-	`sha256:534d20faa72e9539a6e82aa6c5a8d354b849745adf3f7bbb85dacc7bcad57a83`  
		Last Modified: Thu, 10 Jul 2025 22:14:21 GMT  
		Size: 60.3 MB (60257760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556b153458fb938af443f24c0bbb1ee2ebc81fd7ec66b0f97b1db47fa04f2c18`  
		Last Modified: Thu, 10 Jul 2025 22:14:22 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250710` - linux; ppc64le

```console
$ docker pull odoo@sha256:10d452ba552846357307a1bf6548dc32cc63a96b33b2ae65e5a9042c092557df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.9 MB (688922308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7edd53da4bc8afde5c7499cdcc3b7fbdabbfde6f3f3ba6a322e08ec3ac08ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:18:14 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:18:18 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Thu, 19 Jun 2025 23:18:18 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b91774b9d3a456defc0d1c3602eae7a52c41ba6fc41639fdbf63dbb1c1b82e`  
		Last Modified: Thu, 10 Jul 2025 19:14:30 GMT  
		Size: 374.2 MB (374242554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2576ff59988ded3be714e6b9e68ea3da5012e99f2dcbd0fc3c9ecbc1dae2e`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3f0e891484cd875e25c56c717745497ffa0dcfb3a13689cdd8b54e8cef74d6`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c6933cfe9a6ae8e6978f3257b77e8925b9edb571e29816746de99d7fcb776`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32bf435553b3c3cd789da1822d3625c2a9c9e516732168b6440082cb4a79cbe`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250710` - unknown; unknown

```console
$ docker pull odoo@sha256:b26d6f13842f72fec66f400481c9ed99f67b566f607b4408badbd0942c80142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5537110a95bdb82d36ea88e5b25951d3292d9be17deff3dc2733162de106a98c`

```dockerfile
```

-	Layers:
	-	`sha256:ad32489d4ce25ae09a998b4a8445be2e4486ed62663e52abeed7e49b2ffc5093`  
		Last Modified: Thu, 10 Jul 2025 22:15:44 GMT  
		Size: 60.3 MB (60258862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cb2a766695613c83613d57ff11e870a7755072cb912dc999bd7086531d8094`  
		Last Modified: Thu, 10 Jul 2025 22:15:45 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:1d243f0f1448390c2863575efa6a78cc02b1d44586d8fb9ea472f8e216609845
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:7235a6200293f3b09b588260db22f01eb8f15e2707ca31454b85c0d047870d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672891570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b2f03bede647f3660252d5a30aca052baf7b6966a547a1eba5a39343d11ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:33 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:35 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Thu, 19 Jun 2025 23:16:36 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=amd64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244901ca41e14ba5483ed7a71a7160291b0e2aea5ea87f35308020331b7b6e61`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 254.7 MB (254704337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa4b6e720391d98b70199170e225510dcafb7a6dcfaf0219bf6805fe5f0382`  
		Last Modified: Thu, 10 Jul 2025 19:10:31 GMT  
		Size: 14.3 MB (14275280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df4e1506c3375c105ca74eaf606137870171d0c4a9ff3a7a8ad8230fd627e5`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 479.9 KB (479852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72566032ce57bc4d555557bbcb346658ac471d7e02b74e48e731c0ae80606ce`  
		Last Modified: Thu, 10 Jul 2025 22:13:04 GMT  
		Size: 373.7 MB (373711300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e781d53e3fdadb21b4be21041d2f85e2efd37b841f72b745c289d0b6c29f7a2`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0bc51d9f5c4643e045d3ed5a41f09b056ea813b2d77ca9f39eb8c2f063fcef`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a27ef56270dc68267b4cc548d2780ff7d911b4ea8ec0acda33c50e132421b33`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8442acccb2f3fff8c4259fd44beb796adcf8a8620cfda47cc8b6d5299e2e5118`  
		Last Modified: Thu, 10 Jul 2025 19:10:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2edcb9a8a60e068117ab67e0a8b79dbd9e80e69a06582f00640121c9f2201a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60277621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef50aa61e059075d9bc1e05b3bc8ba4738319f12aea133082f788bff8939e2b`

```dockerfile
```

-	Layers:
	-	`sha256:1ce9280a7beb5424699aeeb9ab2e3fc1bb719cec76031aec71aee59f61973b88`  
		Last Modified: Thu, 10 Jul 2025 22:12:54 GMT  
		Size: 60.3 MB (60250485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507377e1ca9cf7dd0dac06e9b339b0e8b2ed0cad6c0e8c4a8c4aba3b8e0818b2`  
		Last Modified: Thu, 10 Jul 2025 22:12:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d9da5f894869339fae75d41c649d14041e5a7a476d6c16338b4f2dd622472ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.1 MB (669077387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6ea9c76a4e66fdcd3c59c3ae07f6cb0b71e6b284d9cb16adc70653e44829fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:16:53 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:16:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:16:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:16:56 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 19 Jun 2025 23:16:56 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=arm64
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e98f49a27a3036b9a25540180c28229b2b4a3073d9fa8905aee883806adf8f`  
		Last Modified: Thu, 10 Jul 2025 22:13:35 GMT  
		Size: 373.6 MB (373564206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a270bed052c2dd54525956eb90ff719c0b89f33945940819f9bde14e44fb7a41`  
		Last Modified: Thu, 10 Jul 2025 19:11:55 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ec87eb7aaa98ca3f7872f0d0e95d3684c23fd6e0db748f24b5b52c206ae04a`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9d38ad71e0861da093153f63294b0a6e71835b85b917e3e94b76b0f8c7b9d`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ee093ea0550ae35a9f968c6580aaabe18fa6b19e8d7e713deb5f41fdbba47`  
		Last Modified: Thu, 10 Jul 2025 19:11:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d5b27af6e8021cf4960e2b9b43920561f3b5d4bb4c5eb219a17e426f6fa72cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60285060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d9ce87d855ce7a470a9ef76ec4bf141bea8d7924431309b9467796a97a104`

```dockerfile
```

-	Layers:
	-	`sha256:534d20faa72e9539a6e82aa6c5a8d354b849745adf3f7bbb85dacc7bcad57a83`  
		Last Modified: Thu, 10 Jul 2025 22:14:21 GMT  
		Size: 60.3 MB (60257760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556b153458fb938af443f24c0bbb1ee2ebc81fd7ec66b0f97b1db47fa04f2c18`  
		Last Modified: Thu, 10 Jul 2025 22:14:22 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:10d452ba552846357307a1bf6548dc32cc63a96b33b2ae65e5a9042c092557df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.9 MB (688922308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7edd53da4bc8afde5c7499cdcc3b7fbdabbfde6f3f3ba6a322e08ec3ac08ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 19 Jun 2025 23:18:14 GMT
ARG RELEASE
# Thu, 19 Jun 2025 23:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Jun 2025 23:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Jun 2025 23:18:18 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Thu, 19 Jun 2025 23:18:18 GMT
CMD ["/bin/bash"]
# Thu, 10 Jul 2025 14:32:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Jul 2025 14:32:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 10 Jul 2025 14:32:17 GMT
ARG TARGETARCH=ppc64le
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_VERSION=18.0
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_RELEASE=20250710
# Thu, 10 Jul 2025 14:32:17 GMT
ARG ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250710 ODOO_SHA=7859985576e247950959a2158c10af319e716e3e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Jul 2025 14:32:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 10 Jul 2025 14:32:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Jul 2025 14:32:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 10 Jul 2025 14:32:17 GMT
USER odoo
# Thu, 10 Jul 2025 14:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Jul 2025 14:32:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b91774b9d3a456defc0d1c3602eae7a52c41ba6fc41639fdbf63dbb1c1b82e`  
		Last Modified: Thu, 10 Jul 2025 19:14:30 GMT  
		Size: 374.2 MB (374242554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d2576ff59988ded3be714e6b9e68ea3da5012e99f2dcbd0fc3c9ecbc1dae2e`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3f0e891484cd875e25c56c717745497ffa0dcfb3a13689cdd8b54e8cef74d6`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c6933cfe9a6ae8e6978f3257b77e8925b9edb571e29816746de99d7fcb776`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32bf435553b3c3cd789da1822d3625c2a9c9e516732168b6440082cb4a79cbe`  
		Last Modified: Thu, 10 Jul 2025 19:14:46 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b26d6f13842f72fec66f400481c9ed99f67b566f607b4408badbd0942c80142b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5537110a95bdb82d36ea88e5b25951d3292d9be17deff3dc2733162de106a98c`

```dockerfile
```

-	Layers:
	-	`sha256:ad32489d4ce25ae09a998b4a8445be2e4486ed62663e52abeed7e49b2ffc5093`  
		Last Modified: Thu, 10 Jul 2025 22:15:44 GMT  
		Size: 60.3 MB (60258862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cb2a766695613c83613d57ff11e870a7755072cb912dc999bd7086531d8094`  
		Last Modified: Thu, 10 Jul 2025 22:15:45 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
