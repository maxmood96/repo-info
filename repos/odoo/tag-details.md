<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:e955595aa804e19eb53f2cb674ca633124eb98349f762588460566d0750bde3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:24d49635fd6f47fba3fe9399913d1202ba6b3736e04a339b655dc1c6f6e75197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.6 MB (563639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd6b62a20107238d96978857a017663c4b02afa3a8454b377ca88d097424519`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:22:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:22:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:22:12 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:22:12 GMT
ENV ODOO_VERSION=15.0
# Fri, 16 Feb 2024 19:56:36 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:56:36 GMT
ARG ODOO_SHA=828692cbc07440e9734f7662ec74b1417b15d01d
# Fri, 16 Feb 2024 19:57:48 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=828692cbc07440e9734f7662ec74b1417b15d01d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:57:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:57:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:57:53 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=828692cbc07440e9734f7662ec74b1417b15d01d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:57:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:57:53 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:57:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:57:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:57:54 GMT
USER odoo
# Fri, 16 Feb 2024 19:57:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:57:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503d586dde6058081085a71407e0daec70122616b9a175f52944fcf0f6cae634`  
		Last Modified: Tue, 13 Feb 2024 11:24:56 GMT  
		Size: 220.3 MB (220291578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fd8ca8a48200ac393e61d324250d6da85bc0dfaa29c83841e7b384b4ae90dd`  
		Last Modified: Tue, 13 Feb 2024 11:24:31 GMT  
		Size: 2.6 MB (2625899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d81bf30e1590e8be1f898a405b5ae2775c64d0de45831fcd3fbb2241409a1`  
		Last Modified: Tue, 13 Feb 2024 11:24:32 GMT  
		Size: 462.9 KB (462933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc436212910aac8c1c88aba720a3e70c967caa99572552c2df2414a3b18b801`  
		Last Modified: Fri, 16 Feb 2024 20:00:20 GMT  
		Size: 308.8 MB (308834664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50335bb60e909f5dcf37d48701896d49d3480893d72c6355b08896a54121659d`  
		Last Modified: Fri, 16 Feb 2024 19:59:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51906d1b4a77ea5651e29ed3418fdf3f27f28ca18d3db477c4360f8f772af8fa`  
		Last Modified: Fri, 16 Feb 2024 19:59:46 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ba8c717909c3cd9297dab44bccd0fcbfce17788ec45d1127d5984f82dabe7b`  
		Last Modified: Fri, 16 Feb 2024 19:59:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d8a8e366745db5f1ee0fe1fa8a88faf7cf53dd4e521eca35e0f62805ce2641`  
		Last Modified: Fri, 16 Feb 2024 19:59:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:e955595aa804e19eb53f2cb674ca633124eb98349f762588460566d0750bde3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:24d49635fd6f47fba3fe9399913d1202ba6b3736e04a339b655dc1c6f6e75197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.6 MB (563639961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd6b62a20107238d96978857a017663c4b02afa3a8454b377ca88d097424519`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:22:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:22:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:22:12 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:22:12 GMT
ENV ODOO_VERSION=15.0
# Fri, 16 Feb 2024 19:56:36 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:56:36 GMT
ARG ODOO_SHA=828692cbc07440e9734f7662ec74b1417b15d01d
# Fri, 16 Feb 2024 19:57:48 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=828692cbc07440e9734f7662ec74b1417b15d01d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:57:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:57:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:57:53 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=828692cbc07440e9734f7662ec74b1417b15d01d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:57:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:57:53 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:57:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:57:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:57:54 GMT
USER odoo
# Fri, 16 Feb 2024 19:57:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:57:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503d586dde6058081085a71407e0daec70122616b9a175f52944fcf0f6cae634`  
		Last Modified: Tue, 13 Feb 2024 11:24:56 GMT  
		Size: 220.3 MB (220291578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fd8ca8a48200ac393e61d324250d6da85bc0dfaa29c83841e7b384b4ae90dd`  
		Last Modified: Tue, 13 Feb 2024 11:24:31 GMT  
		Size: 2.6 MB (2625899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d81bf30e1590e8be1f898a405b5ae2775c64d0de45831fcd3fbb2241409a1`  
		Last Modified: Tue, 13 Feb 2024 11:24:32 GMT  
		Size: 462.9 KB (462933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc436212910aac8c1c88aba720a3e70c967caa99572552c2df2414a3b18b801`  
		Last Modified: Fri, 16 Feb 2024 20:00:20 GMT  
		Size: 308.8 MB (308834664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50335bb60e909f5dcf37d48701896d49d3480893d72c6355b08896a54121659d`  
		Last Modified: Fri, 16 Feb 2024 19:59:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51906d1b4a77ea5651e29ed3418fdf3f27f28ca18d3db477c4360f8f772af8fa`  
		Last Modified: Fri, 16 Feb 2024 19:59:46 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ba8c717909c3cd9297dab44bccd0fcbfce17788ec45d1127d5984f82dabe7b`  
		Last Modified: Fri, 16 Feb 2024 19:59:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d8a8e366745db5f1ee0fe1fa8a88faf7cf53dd4e521eca35e0f62805ce2641`  
		Last Modified: Fri, 16 Feb 2024 19:59:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:dbb6fb15586208152982c0bbe8f960bec2881feeb9742a532f32e70c9e3de733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:af72cc4197753b588538782b531ee9e9850b3b79e2867f7358399beef647fad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582346321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a560f442cd0dd365d61dfcbb5b61463a4ca9cfd107bbfd89162a046d89054c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:18:16 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 11:19:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:19:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:19:35 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:19:36 GMT
ENV ODOO_VERSION=16.0
# Fri, 16 Feb 2024 19:54:57 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:54:57 GMT
ARG ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
# Fri, 16 Feb 2024 19:56:21 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:56:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:56:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:56:25 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:56:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:56:26 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:56:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:56:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:56:26 GMT
USER odoo
# Fri, 16 Feb 2024 19:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:56:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f8764e315ffe4d9162112c693dc2de9180d54741bcc86a94a2e8dc63796`  
		Last Modified: Tue, 13 Feb 2024 11:24:08 GMT  
		Size: 219.6 MB (219603078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c251911a36e7b29cdc68e2e6ad3c227877483a27881808128a45cdf7f29cd97`  
		Last Modified: Tue, 13 Feb 2024 11:23:43 GMT  
		Size: 2.6 MB (2629960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b94be8a611fcadb8c1bb3ac916cbf8b7c765cb563396dcb2461b5150d88e9`  
		Last Modified: Tue, 13 Feb 2024 11:23:44 GMT  
		Size: 462.9 KB (462884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed175f9313b9bd49067a90541cff049d806c00e47cc5c692e65a10d3f32953a6`  
		Last Modified: Fri, 16 Feb 2024 19:59:36 GMT  
		Size: 328.2 MB (328225515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c01fec7da1418be92101ea8edc0e6353863976876f10f39fe4d88394b9f83d`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b085d40e50b63262fae8ac2bf3ea170151e8f06778e8687e4b5ef671c43190b4`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccdb79c7330ebf6b1db2de30be5c3d82a3bf05e32f31a8f4b8f5bd9b802b594`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20d920788170eccd49059c0b3021bb6fe50252122d861fc35cfd302ea33bc68`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a71d9310fcbd26ec7c9a99e2c8d8a5ca70624e4dbac3705a942afabc0e826e4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577921635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9578e33775436e90ab8d6943f480715b418e460e7318d5a7d560d47210b841ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:47:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 02:47:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 02:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 02:47:36 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 02:48:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 02:48:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:48:53 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 02:48:53 GMT
ENV ODOO_VERSION=16.0
# Fri, 16 Feb 2024 20:13:41 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 20:13:41 GMT
ARG ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
# Fri, 16 Feb 2024 20:14:56 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 20:15:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 20:15:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 20:15:04 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 20:15:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 20:15:04 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 20:15:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 20:15:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 20:15:04 GMT
USER odoo
# Fri, 16 Feb 2024 20:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 20:15:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2f618c4954544d5a1d56ef7354df8c3a0a52e4c057e074c37924915ca2fd1`  
		Last Modified: Tue, 13 Feb 2024 02:50:56 GMT  
		Size: 216.9 MB (216902917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473596c65e4b7b8b68f3b2d5b8b44b1d170a7c2d419f7047936e9222e56adb`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 2.6 MB (2635157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628656e229343de1b693a2b98cf92fb4f3b3bb43b28acb4438d79491525761f`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 462.9 KB (462916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f438fc70b7ac2cdb3dcb1e8a2471a9d49a65fb724be569fe11aa630d5cfa5f18`  
		Last Modified: Fri, 16 Feb 2024 20:16:36 GMT  
		Size: 327.8 MB (327847101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8013059648fdd2611c26320241da2108036272b5f0e2f10d21f24845ae675ade`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d95425cc6ad3ff566165e1cf50d42dafc3331a2eb9610fa45c5c5d6a0f9a24b`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92ce857386232b684f914b753480fb7f24d342489e70e79d6b54f414354286`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624704f6588173155ddfdd5073d7bc0f73d03a708ec41ff18e38644398202931`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:1b63e35a17b31a829114dea5b255d9d5a313fe49fb72fc417fd1e2da0f52de16
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596892270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc011e9e83b68fa780274e7945756db7739c5392390f08932917af07cbd9b5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:09:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 04:09:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 04:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 04:09:40 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 04:13:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 04:13:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:13:49 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 04:13:49 GMT
ENV ODOO_VERSION=16.0
# Fri, 16 Feb 2024 19:19:37 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:19:37 GMT
ARG ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
# Fri, 16 Feb 2024 19:21:36 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:21:44 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:21:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:21:46 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:21:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:21:47 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:21:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:21:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:21:48 GMT
USER odoo
# Fri, 16 Feb 2024 19:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:21:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47bb6241f7f89a639b08014441cb2820f9f7f4509216e43e8bbd6357c7bda0`  
		Last Modified: Tue, 13 Feb 2024 04:18:30 GMT  
		Size: 228.6 MB (228600171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9749dac12780aa7b6979dc392d78966a3978c3a71436c61a00cc276c9b3ab`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 2.9 MB (2875930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38c3b73d7742aebbefe4d2d4b68642d916e808d2f230032f15cc77e6bb0c9`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 463.0 KB (462957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18893cbce343ba6a522f94dfe7858789d14db2b49fa51be8522b3f1a3a466c6`  
		Last Modified: Fri, 16 Feb 2024 19:23:54 GMT  
		Size: 329.7 MB (329652950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72faa56cc4586770ecf1567223397bdd05a7b46f66babf7c8a246f67c8f9117c`  
		Last Modified: Fri, 16 Feb 2024 19:23:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22f437490cfe14dbb014bc0502cf30fe2b9f51fa425bfae54b6f7ab17fc4136`  
		Last Modified: Fri, 16 Feb 2024 19:23:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a600e16383ea100352500c34682d836760500b7a2291a0929a8affc616e03c`  
		Last Modified: Fri, 16 Feb 2024 19:23:08 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d3c2e652d01a1a4cb02d85a9d472b1be81afa7572fc9f7b550ece91a7da55`  
		Last Modified: Fri, 16 Feb 2024 19:23:08 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:dbb6fb15586208152982c0bbe8f960bec2881feeb9742a532f32e70c9e3de733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:af72cc4197753b588538782b531ee9e9850b3b79e2867f7358399beef647fad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.3 MB (582346321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a560f442cd0dd365d61dfcbb5b61463a4ca9cfd107bbfd89162a046d89054c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:18:16 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 11:19:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:19:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:19:35 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:19:36 GMT
ENV ODOO_VERSION=16.0
# Fri, 16 Feb 2024 19:54:57 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:54:57 GMT
ARG ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
# Fri, 16 Feb 2024 19:56:21 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:56:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:56:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:56:25 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:56:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:56:26 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:56:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:56:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:56:26 GMT
USER odoo
# Fri, 16 Feb 2024 19:56:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:56:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f8764e315ffe4d9162112c693dc2de9180d54741bcc86a94a2e8dc63796`  
		Last Modified: Tue, 13 Feb 2024 11:24:08 GMT  
		Size: 219.6 MB (219603078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c251911a36e7b29cdc68e2e6ad3c227877483a27881808128a45cdf7f29cd97`  
		Last Modified: Tue, 13 Feb 2024 11:23:43 GMT  
		Size: 2.6 MB (2629960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b94be8a611fcadb8c1bb3ac916cbf8b7c765cb563396dcb2461b5150d88e9`  
		Last Modified: Tue, 13 Feb 2024 11:23:44 GMT  
		Size: 462.9 KB (462884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed175f9313b9bd49067a90541cff049d806c00e47cc5c692e65a10d3f32953a6`  
		Last Modified: Fri, 16 Feb 2024 19:59:36 GMT  
		Size: 328.2 MB (328225515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c01fec7da1418be92101ea8edc0e6353863976876f10f39fe4d88394b9f83d`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b085d40e50b63262fae8ac2bf3ea170151e8f06778e8687e4b5ef671c43190b4`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccdb79c7330ebf6b1db2de30be5c3d82a3bf05e32f31a8f4b8f5bd9b802b594`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20d920788170eccd49059c0b3021bb6fe50252122d861fc35cfd302ea33bc68`  
		Last Modified: Fri, 16 Feb 2024 19:58:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a71d9310fcbd26ec7c9a99e2c8d8a5ca70624e4dbac3705a942afabc0e826e4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577921635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9578e33775436e90ab8d6943f480715b418e460e7318d5a7d560d47210b841ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:47:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 02:47:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 02:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 02:47:36 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 02:48:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 02:48:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:48:53 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 02:48:53 GMT
ENV ODOO_VERSION=16.0
# Fri, 16 Feb 2024 20:13:41 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 20:13:41 GMT
ARG ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
# Fri, 16 Feb 2024 20:14:56 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 20:15:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 20:15:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 20:15:04 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 20:15:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 20:15:04 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 20:15:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 20:15:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 20:15:04 GMT
USER odoo
# Fri, 16 Feb 2024 20:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 20:15:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2f618c4954544d5a1d56ef7354df8c3a0a52e4c057e074c37924915ca2fd1`  
		Last Modified: Tue, 13 Feb 2024 02:50:56 GMT  
		Size: 216.9 MB (216902917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473596c65e4b7b8b68f3b2d5b8b44b1d170a7c2d419f7047936e9222e56adb`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 2.6 MB (2635157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628656e229343de1b693a2b98cf92fb4f3b3bb43b28acb4438d79491525761f`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 462.9 KB (462916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f438fc70b7ac2cdb3dcb1e8a2471a9d49a65fb724be569fe11aa630d5cfa5f18`  
		Last Modified: Fri, 16 Feb 2024 20:16:36 GMT  
		Size: 327.8 MB (327847101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8013059648fdd2611c26320241da2108036272b5f0e2f10d21f24845ae675ade`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d95425cc6ad3ff566165e1cf50d42dafc3331a2eb9610fa45c5c5d6a0f9a24b`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92ce857386232b684f914b753480fb7f24d342489e70e79d6b54f414354286`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624704f6588173155ddfdd5073d7bc0f73d03a708ec41ff18e38644398202931`  
		Last Modified: Fri, 16 Feb 2024 20:16:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1b63e35a17b31a829114dea5b255d9d5a313fe49fb72fc417fd1e2da0f52de16
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596892270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc011e9e83b68fa780274e7945756db7739c5392390f08932917af07cbd9b5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:09:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 04:09:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 04:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 04:09:40 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 04:13:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 04:13:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:13:49 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 04:13:49 GMT
ENV ODOO_VERSION=16.0
# Fri, 16 Feb 2024 19:19:37 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:19:37 GMT
ARG ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
# Fri, 16 Feb 2024 19:21:36 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:21:44 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:21:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:21:46 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=550f2316a535d426556efc2fc2326a7063fa4cbe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:21:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:21:47 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:21:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:21:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:21:48 GMT
USER odoo
# Fri, 16 Feb 2024 19:21:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:21:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47bb6241f7f89a639b08014441cb2820f9f7f4509216e43e8bbd6357c7bda0`  
		Last Modified: Tue, 13 Feb 2024 04:18:30 GMT  
		Size: 228.6 MB (228600171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9749dac12780aa7b6979dc392d78966a3978c3a71436c61a00cc276c9b3ab`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 2.9 MB (2875930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38c3b73d7742aebbefe4d2d4b68642d916e808d2f230032f15cc77e6bb0c9`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 463.0 KB (462957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18893cbce343ba6a522f94dfe7858789d14db2b49fa51be8522b3f1a3a466c6`  
		Last Modified: Fri, 16 Feb 2024 19:23:54 GMT  
		Size: 329.7 MB (329652950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72faa56cc4586770ecf1567223397bdd05a7b46f66babf7c8a246f67c8f9117c`  
		Last Modified: Fri, 16 Feb 2024 19:23:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22f437490cfe14dbb014bc0502cf30fe2b9f51fa425bfae54b6f7ab17fc4136`  
		Last Modified: Fri, 16 Feb 2024 19:23:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a600e16383ea100352500c34682d836760500b7a2291a0929a8affc616e03c`  
		Last Modified: Fri, 16 Feb 2024 19:23:08 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d3c2e652d01a1a4cb02d85a9d472b1be81afa7572fc9f7b550ece91a7da55`  
		Last Modified: Fri, 16 Feb 2024 19:23:08 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:df9d92ed7530f4f858ca068e84770426315b3cb2444d0babf0bed834657a9c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:5be890524a2d295b05f1f307e7361884267aced83013c3c64d8351ee300e7576
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597906347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54751c91f8cf69da5ea7666db0e9f28477710651c8efbbf1063a4271b9fb58ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 19:52:48 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:52:48 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 19:54:44 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:54:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:54:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:54:48 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:54:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:54:49 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:54:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:54:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:54:49 GMT
USER odoo
# Fri, 16 Feb 2024 19:54:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:54:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce935f6616b14435af6d87b9ef332a9a7796c8662c1e294b13a68a30feb2c57b`  
		Last Modified: Fri, 16 Feb 2024 19:58:46 GMT  
		Size: 330.7 MB (330729005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed71c16a58aab299e75fc7cd38e48bf59a57f4d2b5b719d2b0dcbbd10d21ce`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345c9b22f8f37e61f1862a7551806e4d6694eae3c59521dab112a6e585bf848`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033e6de637697b689b89ecc89fc46fae6176f8ed99ae1e75b0fb48790f87a744`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4525b6e0513eb2b2f11010516700eacb6835e85a2ae3926eedfd77da57c06c7`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9c27c7b781c4c4d4f3500d93db72c90ca3b3a58c9aa955072f17ca35afc75b0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 MB (592847688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb11da2614093cc1597dacc9dc74df36931e14dafa8420c9e1605aa32fee8fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 20:11:18 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 20:11:18 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 20:13:21 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 20:13:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 20:13:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 20:13:29 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 20:13:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 20:13:29 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 20:13:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 20:13:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 20:13:29 GMT
USER odoo
# Fri, 16 Feb 2024 20:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 20:13:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe1c8b3874a580a9e13a2eeeb565a1ed204f59cff628e7a73cdef8efccfcf50`  
		Last Modified: Fri, 16 Feb 2024 20:15:55 GMT  
		Size: 330.3 MB (330340178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524f67a62f12809a68f7b488f1c1384d61b726cc32c6c3868b7c6744e62b6052`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e479167af002f7219015a2bd6f23b64043bab5a080f3220df416eb7a133ac3`  
		Last Modified: Fri, 16 Feb 2024 20:15:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75116801f1cbec1918886029fd42104b485c39a2d6a714d596e695fc9aae4fb`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4f6bc2f0c3677b758c2e9461007d3d2d8e6a9cf928484e0202bd6270025af`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:de24da148b3e34d39d73b637497d228f0d31e3841908281eb0dbc90c810718cc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614677562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf5c2a68c7c362bdc071f089ef52a2dd24b597e5133a0b2f2c716cd82f2ce98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 19:16:42 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:16:43 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 19:19:03 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:19:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:19:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:19:17 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:19:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:19:18 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:19:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:19:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:19:19 GMT
USER odoo
# Fri, 16 Feb 2024 19:19:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cfbee5283e0a815ee4192fa0b8866d13a393e3a5c4501956c64c4b03130f8b`  
		Last Modified: Fri, 16 Feb 2024 19:22:56 GMT  
		Size: 332.5 MB (332480606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda13d77f351e529f623245c7eb1ed5f8943875afbb0f92f342a0228fa537144`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3cbb36aa0ddbfc608e38c250b14025d06b4411e04d42670508ddeddba8d93a`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5334ab2a2363896f605b286926a20a01ca35b0de972817e22c184d9e606fb`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de62373de2fc89905d2c9f62d027d009d21757e67f802357db626c27a6c13d7`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:df9d92ed7530f4f858ca068e84770426315b3cb2444d0babf0bed834657a9c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:5be890524a2d295b05f1f307e7361884267aced83013c3c64d8351ee300e7576
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597906347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54751c91f8cf69da5ea7666db0e9f28477710651c8efbbf1063a4271b9fb58ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 19:52:48 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:52:48 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 19:54:44 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:54:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:54:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:54:48 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:54:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:54:49 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:54:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:54:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:54:49 GMT
USER odoo
# Fri, 16 Feb 2024 19:54:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:54:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce935f6616b14435af6d87b9ef332a9a7796c8662c1e294b13a68a30feb2c57b`  
		Last Modified: Fri, 16 Feb 2024 19:58:46 GMT  
		Size: 330.7 MB (330729005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed71c16a58aab299e75fc7cd38e48bf59a57f4d2b5b719d2b0dcbbd10d21ce`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345c9b22f8f37e61f1862a7551806e4d6694eae3c59521dab112a6e585bf848`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033e6de637697b689b89ecc89fc46fae6176f8ed99ae1e75b0fb48790f87a744`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4525b6e0513eb2b2f11010516700eacb6835e85a2ae3926eedfd77da57c06c7`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9c27c7b781c4c4d4f3500d93db72c90ca3b3a58c9aa955072f17ca35afc75b0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 MB (592847688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb11da2614093cc1597dacc9dc74df36931e14dafa8420c9e1605aa32fee8fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 20:11:18 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 20:11:18 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 20:13:21 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 20:13:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 20:13:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 20:13:29 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 20:13:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 20:13:29 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 20:13:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 20:13:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 20:13:29 GMT
USER odoo
# Fri, 16 Feb 2024 20:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 20:13:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe1c8b3874a580a9e13a2eeeb565a1ed204f59cff628e7a73cdef8efccfcf50`  
		Last Modified: Fri, 16 Feb 2024 20:15:55 GMT  
		Size: 330.3 MB (330340178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524f67a62f12809a68f7b488f1c1384d61b726cc32c6c3868b7c6744e62b6052`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e479167af002f7219015a2bd6f23b64043bab5a080f3220df416eb7a133ac3`  
		Last Modified: Fri, 16 Feb 2024 20:15:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75116801f1cbec1918886029fd42104b485c39a2d6a714d596e695fc9aae4fb`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4f6bc2f0c3677b758c2e9461007d3d2d8e6a9cf928484e0202bd6270025af`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:de24da148b3e34d39d73b637497d228f0d31e3841908281eb0dbc90c810718cc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614677562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf5c2a68c7c362bdc071f089ef52a2dd24b597e5133a0b2f2c716cd82f2ce98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 19:16:42 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:16:43 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 19:19:03 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:19:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:19:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:19:17 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:19:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:19:18 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:19:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:19:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:19:19 GMT
USER odoo
# Fri, 16 Feb 2024 19:19:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cfbee5283e0a815ee4192fa0b8866d13a393e3a5c4501956c64c4b03130f8b`  
		Last Modified: Fri, 16 Feb 2024 19:22:56 GMT  
		Size: 332.5 MB (332480606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda13d77f351e529f623245c7eb1ed5f8943875afbb0f92f342a0228fa537144`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3cbb36aa0ddbfc608e38c250b14025d06b4411e04d42670508ddeddba8d93a`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5334ab2a2363896f605b286926a20a01ca35b0de972817e22c184d9e606fb`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de62373de2fc89905d2c9f62d027d009d21757e67f802357db626c27a6c13d7`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:df9d92ed7530f4f858ca068e84770426315b3cb2444d0babf0bed834657a9c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:5be890524a2d295b05f1f307e7361884267aced83013c3c64d8351ee300e7576
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597906347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54751c91f8cf69da5ea7666db0e9f28477710651c8efbbf1063a4271b9fb58ee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 19:52:48 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:52:48 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 19:54:44 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:54:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:54:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:54:48 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:54:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:54:49 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:54:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:54:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:54:49 GMT
USER odoo
# Fri, 16 Feb 2024 19:54:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:54:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce935f6616b14435af6d87b9ef332a9a7796c8662c1e294b13a68a30feb2c57b`  
		Last Modified: Fri, 16 Feb 2024 19:58:46 GMT  
		Size: 330.7 MB (330729005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ed71c16a58aab299e75fc7cd38e48bf59a57f4d2b5b719d2b0dcbbd10d21ce`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2345c9b22f8f37e61f1862a7551806e4d6694eae3c59521dab112a6e585bf848`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033e6de637697b689b89ecc89fc46fae6176f8ed99ae1e75b0fb48790f87a744`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4525b6e0513eb2b2f11010516700eacb6835e85a2ae3926eedfd77da57c06c7`  
		Last Modified: Fri, 16 Feb 2024 19:58:07 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9c27c7b781c4c4d4f3500d93db72c90ca3b3a58c9aa955072f17ca35afc75b0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 MB (592847688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb11da2614093cc1597dacc9dc74df36931e14dafa8420c9e1605aa32fee8fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 20:11:18 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 20:11:18 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 20:13:21 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 20:13:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 20:13:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 20:13:29 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 20:13:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 20:13:29 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 20:13:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 20:13:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 20:13:29 GMT
USER odoo
# Fri, 16 Feb 2024 20:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 20:13:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe1c8b3874a580a9e13a2eeeb565a1ed204f59cff628e7a73cdef8efccfcf50`  
		Last Modified: Fri, 16 Feb 2024 20:15:55 GMT  
		Size: 330.3 MB (330340178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524f67a62f12809a68f7b488f1c1384d61b726cc32c6c3868b7c6744e62b6052`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e479167af002f7219015a2bd6f23b64043bab5a080f3220df416eb7a133ac3`  
		Last Modified: Fri, 16 Feb 2024 20:15:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75116801f1cbec1918886029fd42104b485c39a2d6a714d596e695fc9aae4fb`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4f6bc2f0c3677b758c2e9461007d3d2d8e6a9cf928484e0202bd6270025af`  
		Last Modified: Fri, 16 Feb 2024 20:15:24 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:de24da148b3e34d39d73b637497d228f0d31e3841908281eb0dbc90c810718cc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614677562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf5c2a68c7c362bdc071f089ef52a2dd24b597e5133a0b2f2c716cd82f2ce98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 19:16:42 GMT
ARG ODOO_RELEASE=20240216
# Fri, 16 Feb 2024 19:16:43 GMT
ARG ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
# Fri, 16 Feb 2024 19:19:03 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 19:19:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 19:19:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 19:19:17 GMT
# ARGS: ODOO_RELEASE=20240216 ODOO_SHA=a7d92964cf77023326396e666973e284fe7a3a9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 19:19:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 19:19:18 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 19:19:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 19:19:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 19:19:19 GMT
USER odoo
# Fri, 16 Feb 2024 19:19:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 19:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cfbee5283e0a815ee4192fa0b8866d13a393e3a5c4501956c64c4b03130f8b`  
		Last Modified: Fri, 16 Feb 2024 19:22:56 GMT  
		Size: 332.5 MB (332480606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda13d77f351e529f623245c7eb1ed5f8943875afbb0f92f342a0228fa537144`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3cbb36aa0ddbfc608e38c250b14025d06b4411e04d42670508ddeddba8d93a`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a5334ab2a2363896f605b286926a20a01ca35b0de972817e22c184d9e606fb`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de62373de2fc89905d2c9f62d027d009d21757e67f802357db626c27a6c13d7`  
		Last Modified: Fri, 16 Feb 2024 19:22:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
