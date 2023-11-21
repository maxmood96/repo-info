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
$ docker pull odoo@sha256:cbbb37767064e27c470c3ca45ceedadc0338f95dfa708bd1613db8633c0638af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:1e556861e227141c43bf78491e48a21cdfd3e3c7e1444969fe4638baf069a279
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563030525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa56565ebb7654f7b53256ab74c0a8bd173cf1a5a5906a1bce38c83d338cbc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:09:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:10:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:07 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:10:07 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Nov 2023 06:10:07 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:10:07 GMT
ARG ODOO_SHA=e9b17c526485b15053924eba01c7dca4d8db9653
# Tue, 21 Nov 2023 06:11:17 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=e9b17c526485b15053924eba01c7dca4d8db9653
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:11:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:11:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:11:22 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=e9b17c526485b15053924eba01c7dca4d8db9653
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:11:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:11:22 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:11:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:11:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:11:22 GMT
USER odoo
# Tue, 21 Nov 2023 06:11:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:11:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28800da8ad810dcb3060b9a249d76f10fc059eb9ea15aa7bb1fcfd0755b607`  
		Last Modified: Tue, 21 Nov 2023 06:13:44 GMT  
		Size: 220.3 MB (220297479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd5e822cfaa6f1e0ff1254d563b0f9fae55e9a37a6461f685b61ba68642687e`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 2.6 MB (2625685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c2fe85ca0f057eeac7b5d2f65043d55dd0192357c143eca092e3fcdb6f1826`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 459.5 KB (459485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac0276657a26037c2063324cd1cfdcfc362da59c734dd6bc50d0c965345c06d`  
		Last Modified: Tue, 21 Nov 2023 06:13:52 GMT  
		Size: 308.2 MB (308227586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acfd2b44f360c1ba6da017542fe5306214e3431d646d8e2ff5de4ad23c4e7d3`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaebcb363f33d6f26deaebe35ecc811f40eef3f6dd69d0c3a81ee8289dc1edd0`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782b27b19fa33038485c6440498ad0dd8f41ca8f7a63497b9b0cac5dfd4c2a57`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d59808bd8428e50866dbf406aed85aa4a0f713af2f0660999ab6b28eb30fd5c`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:cbbb37767064e27c470c3ca45ceedadc0338f95dfa708bd1613db8633c0638af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:1e556861e227141c43bf78491e48a21cdfd3e3c7e1444969fe4638baf069a279
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563030525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa56565ebb7654f7b53256ab74c0a8bd173cf1a5a5906a1bce38c83d338cbc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:09:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:10:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:10:07 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:10:07 GMT
ENV ODOO_VERSION=15.0
# Tue, 21 Nov 2023 06:10:07 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:10:07 GMT
ARG ODOO_SHA=e9b17c526485b15053924eba01c7dca4d8db9653
# Tue, 21 Nov 2023 06:11:17 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=e9b17c526485b15053924eba01c7dca4d8db9653
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:11:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:11:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:11:22 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=e9b17c526485b15053924eba01c7dca4d8db9653
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:11:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:11:22 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:11:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:11:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:11:22 GMT
USER odoo
# Tue, 21 Nov 2023 06:11:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:11:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a28800da8ad810dcb3060b9a249d76f10fc059eb9ea15aa7bb1fcfd0755b607`  
		Last Modified: Tue, 21 Nov 2023 06:13:44 GMT  
		Size: 220.3 MB (220297479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd5e822cfaa6f1e0ff1254d563b0f9fae55e9a37a6461f685b61ba68642687e`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 2.6 MB (2625685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c2fe85ca0f057eeac7b5d2f65043d55dd0192357c143eca092e3fcdb6f1826`  
		Last Modified: Tue, 21 Nov 2023 06:13:20 GMT  
		Size: 459.5 KB (459485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac0276657a26037c2063324cd1cfdcfc362da59c734dd6bc50d0c965345c06d`  
		Last Modified: Tue, 21 Nov 2023 06:13:52 GMT  
		Size: 308.2 MB (308227586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acfd2b44f360c1ba6da017542fe5306214e3431d646d8e2ff5de4ad23c4e7d3`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaebcb363f33d6f26deaebe35ecc811f40eef3f6dd69d0c3a81ee8289dc1edd0`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782b27b19fa33038485c6440498ad0dd8f41ca8f7a63497b9b0cac5dfd4c2a57`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d59808bd8428e50866dbf406aed85aa4a0f713af2f0660999ab6b28eb30fd5c`  
		Last Modified: Tue, 21 Nov 2023 06:13:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:9f043f79da90cb52868c128617480a8f9768f4825033bef13e064af3808f9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:36c6fb2ab9a349bfb15d26a5de69965723de7c01a29272097102b821c06d7bca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577247493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db6e122b27014e9f24a5797ace9ee9cde4ab70d185735759102a21e73395941`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:06:00 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 06:07:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:07:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:25 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:07:25 GMT
ENV ODOO_VERSION=16.0
# Tue, 21 Nov 2023 06:07:25 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:07:25 GMT
ARG ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
# Tue, 21 Nov 2023 06:08:46 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:08:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:08:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:08:51 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:08:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:08:51 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:08:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:08:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:08:51 GMT
USER odoo
# Tue, 21 Nov 2023 06:08:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:08:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66dcf73708692fc6d6dee7d004e9c2f7d2fb47f905fbbc62dc61f2daffceb17`  
		Last Modified: Tue, 21 Nov 2023 06:12:58 GMT  
		Size: 219.6 MB (219606563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f096532668b80e067c70ebffa93b9ba9b5efa7080f7cf42b36ccb58a90e3508`  
		Last Modified: Tue, 21 Nov 2023 06:12:34 GMT  
		Size: 2.6 MB (2629834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ce0ca6176cbb017ef1b39cc6364b8f0620ac11996f8f6f959fb01195040a7b`  
		Last Modified: Tue, 21 Nov 2023 06:12:33 GMT  
		Size: 459.5 KB (459472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d02b50390db47496a7f9f64c58de1b57f352a85843ea061849cc8ab86777c3`  
		Last Modified: Tue, 21 Nov 2023 06:13:09 GMT  
		Size: 323.1 MB (323131333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eb1ccec3ba33f9b7f1e29cbbca291f714ae6669d0e6ba22e9cbae959329f`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6c457ea70f8f89b9b30e2307680ab0ad99c08a9ee46011f096d66d89e15a8`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf2949f5b2590d385a7bd9f562cfc95f173caf1f0815ed9e8bd6929f9e5d1aa`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41cac939acbc5358db8444ce12b1a4fa82fbe7ca90b8609160c854c9109845a`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:705cbdf873f05566bbea4e0f133b2f263164196eb2d941db744b01c0f70d5443
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572830628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dd8a18eb49a201baa9ea4477eaa5fee746dbc8dc009c05c010d51051739583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 21 Nov 2023 04:09:39 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:09:39 GMT
ARG ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
# Tue, 21 Nov 2023 04:11:06 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:11:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:11:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:11:14 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:11:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:11:14 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:11:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:11:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:11:15 GMT
USER odoo
# Tue, 21 Nov 2023 04:11:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:11:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9407019faecd870a2e511ae137e05316d5327b7a112db897900d2c3c5e33beb`  
		Last Modified: Tue, 21 Nov 2023 04:12:34 GMT  
		Size: 322.8 MB (322763119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509bf053d9d9d3479566f801c18e24b900d2bfe0dce8fc3336787f97b4a2f014`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a8439c4b181deb2c7ed26fa08a824fdf50ca8edfc5e98df5e5b2047b4464c`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea84d5d217e44ba938402be039d9d9d2ec77f3eeec92f0361cd443a2de60f4b`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebad2321a896b36656c3a82e4f3ab09f85d9f461be5d51a9a085ab043ae2af66`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:f3c0291c87b4d41b14f8f7ba13c451d1c4dd395c1340dde3a58781d9fe288d46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591769531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de32170d51259e1a67f56d19fc86f974ec6963e97f7e6bc8883900412a9943b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:37:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 04:37:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 04:37:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:37:34 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 04:40:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 04:40:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:40:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 04:40:39 GMT
ENV ODOO_VERSION=16.0
# Tue, 21 Nov 2023 04:40:40 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:40:40 GMT
ARG ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
# Tue, 21 Nov 2023 04:42:42 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:42:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:42:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:43:00 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:43:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:43:01 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:43:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:43:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:43:03 GMT
USER odoo
# Tue, 21 Nov 2023 04:43:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:43:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9412e97f56973d23e9dad0c3fcfd85b2446ed64817cf494fd8c0d7e8a361d2b6`  
		Last Modified: Tue, 21 Nov 2023 04:44:49 GMT  
		Size: 228.6 MB (228598187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a33d7cd62e6b8c2d2d1f1384daa821c3fbc171b6a3fb9296592372045d33751`  
		Last Modified: Tue, 21 Nov 2023 04:44:20 GMT  
		Size: 2.9 MB (2875641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656925877eaa583e8f5dde6fd482750adc09d25cdd8ac87e6345c0b308d1b97`  
		Last Modified: Tue, 21 Nov 2023 04:44:19 GMT  
		Size: 459.5 KB (459505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000712ccef34f00b423262b398f9b0cfac8de88db06af1052d39e27a9b9a8629`  
		Last Modified: Tue, 21 Nov 2023 04:45:01 GMT  
		Size: 324.5 MB (324540006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067ad1a11ec85e4670753fbcd15de011efa4aba85a5b823fd26a00f674b2ba1`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151364655400e569fce604eeb6bfd0df37fd6f9c25dde40dd56cb58177dd823d`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd938a0876e7fed002bcf91cd26ab3c81d26c90847be1e91631a4566fba75289`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78223175c5733a078aa9fc4e0e70650cb2f29cab6e5997c31805440dd4e14a90`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:9f043f79da90cb52868c128617480a8f9768f4825033bef13e064af3808f9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:36c6fb2ab9a349bfb15d26a5de69965723de7c01a29272097102b821c06d7bca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577247493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db6e122b27014e9f24a5797ace9ee9cde4ab70d185735759102a21e73395941`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:06:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 06:06:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 06:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 06:06:00 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 06:07:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 06:07:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:07:25 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 06:07:25 GMT
ENV ODOO_VERSION=16.0
# Tue, 21 Nov 2023 06:07:25 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:07:25 GMT
ARG ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
# Tue, 21 Nov 2023 06:08:46 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:08:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:08:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:08:51 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:08:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:08:51 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:08:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:08:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:08:51 GMT
USER odoo
# Tue, 21 Nov 2023 06:08:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:08:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66dcf73708692fc6d6dee7d004e9c2f7d2fb47f905fbbc62dc61f2daffceb17`  
		Last Modified: Tue, 21 Nov 2023 06:12:58 GMT  
		Size: 219.6 MB (219606563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f096532668b80e067c70ebffa93b9ba9b5efa7080f7cf42b36ccb58a90e3508`  
		Last Modified: Tue, 21 Nov 2023 06:12:34 GMT  
		Size: 2.6 MB (2629834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ce0ca6176cbb017ef1b39cc6364b8f0620ac11996f8f6f959fb01195040a7b`  
		Last Modified: Tue, 21 Nov 2023 06:12:33 GMT  
		Size: 459.5 KB (459472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d02b50390db47496a7f9f64c58de1b57f352a85843ea061849cc8ab86777c3`  
		Last Modified: Tue, 21 Nov 2023 06:13:09 GMT  
		Size: 323.1 MB (323131333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c211eb1ccec3ba33f9b7f1e29cbbca291f714ae6669d0e6ba22e9cbae959329f`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd6c457ea70f8f89b9b30e2307680ab0ad99c08a9ee46011f096d66d89e15a8`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf2949f5b2590d385a7bd9f562cfc95f173caf1f0815ed9e8bd6929f9e5d1aa`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41cac939acbc5358db8444ce12b1a4fa82fbe7ca90b8609160c854c9109845a`  
		Last Modified: Tue, 21 Nov 2023 06:12:31 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:705cbdf873f05566bbea4e0f133b2f263164196eb2d941db744b01c0f70d5443
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572830628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dd8a18eb49a201baa9ea4477eaa5fee746dbc8dc009c05c010d51051739583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 21 Nov 2023 04:09:39 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:09:39 GMT
ARG ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
# Tue, 21 Nov 2023 04:11:06 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:11:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:11:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:11:14 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:11:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:11:14 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:11:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:11:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:11:15 GMT
USER odoo
# Tue, 21 Nov 2023 04:11:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:11:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9407019faecd870a2e511ae137e05316d5327b7a112db897900d2c3c5e33beb`  
		Last Modified: Tue, 21 Nov 2023 04:12:34 GMT  
		Size: 322.8 MB (322763119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509bf053d9d9d3479566f801c18e24b900d2bfe0dce8fc3336787f97b4a2f014`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37a8439c4b181deb2c7ed26fa08a824fdf50ca8edfc5e98df5e5b2047b4464c`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea84d5d217e44ba938402be039d9d9d2ec77f3eeec92f0361cd443a2de60f4b`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebad2321a896b36656c3a82e4f3ab09f85d9f461be5d51a9a085ab043ae2af66`  
		Last Modified: Tue, 21 Nov 2023 04:12:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f3c0291c87b4d41b14f8f7ba13c451d1c4dd395c1340dde3a58781d9fe288d46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 MB (591769531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de32170d51259e1a67f56d19fc86f974ec6963e97f7e6bc8883900412a9943b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:37:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 04:37:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 04:37:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 04:37:34 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 04:40:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 04:40:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 04:40:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 04:40:39 GMT
ENV ODOO_VERSION=16.0
# Tue, 21 Nov 2023 04:40:40 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:40:40 GMT
ARG ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
# Tue, 21 Nov 2023 04:42:42 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:42:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:42:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:43:00 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=97b5f7e7d545b4c8f29b133b01d64f6049c88c78
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:43:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:43:01 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:43:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:43:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:43:03 GMT
USER odoo
# Tue, 21 Nov 2023 04:43:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:43:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9412e97f56973d23e9dad0c3fcfd85b2446ed64817cf494fd8c0d7e8a361d2b6`  
		Last Modified: Tue, 21 Nov 2023 04:44:49 GMT  
		Size: 228.6 MB (228598187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a33d7cd62e6b8c2d2d1f1384daa821c3fbc171b6a3fb9296592372045d33751`  
		Last Modified: Tue, 21 Nov 2023 04:44:20 GMT  
		Size: 2.9 MB (2875641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d656925877eaa583e8f5dde6fd482750adc09d25cdd8ac87e6345c0b308d1b97`  
		Last Modified: Tue, 21 Nov 2023 04:44:19 GMT  
		Size: 459.5 KB (459505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000712ccef34f00b423262b398f9b0cfac8de88db06af1052d39e27a9b9a8629`  
		Last Modified: Tue, 21 Nov 2023 04:45:01 GMT  
		Size: 324.5 MB (324540006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067ad1a11ec85e4670753fbcd15de011efa4aba85a5b823fd26a00f674b2ba1`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151364655400e569fce604eeb6bfd0df37fd6f9c25dde40dd56cb58177dd823d`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd938a0876e7fed002bcf91cd26ab3c81d26c90847be1e91631a4566fba75289`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78223175c5733a078aa9fc4e0e70650cb2f29cab6e5997c31805440dd4e14a90`  
		Last Modified: Tue, 21 Nov 2023 04:44:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:3738d94b2ca518112b559c319630e385791a6f0be75797d1f718f57640b72914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:9f57fa8946d9301694a786aa4bd0f4ecc934118e82ea410bd082348e1dc42d5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594449353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf44b22dd1a9318c88613d2a81cefd271379a74b9c3aa0fbb1e34763240c97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 06:03:51 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:03:51 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 06:05:46 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:05:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:05:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:05:51 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:05:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:05:51 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:05:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:05:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:05:52 GMT
USER odoo
# Tue, 21 Nov 2023 06:05:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:05:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b699250faaaa18113675f119e5bda24097c32b1886dca1d8bdacc634802fa`  
		Last Modified: Tue, 21 Nov 2023 06:12:18 GMT  
		Size: 325.0 MB (325019891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca808d5c34b2820247735cbb3f7da17d71cdb205be8cfc5b7099be424fabdfd5`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148accfa4e3bf0b22a62ac9819f89e571ff37b5dbf5d405c190af8c27073c28`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4359884d1352b92e45c161e763ad85dec0c7d0800f995aa829ec1201cfbe93`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3d79cacd98196061c6ab9ef939de4ab58f316cbe5885217dd1bd610055de4`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:081e643c5b1d024db510b0c7b35b43a07b0eb08674a4478ecbe7d3e690c79535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589252116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8213f8ac42992be9d7b335deb14e4cdcdf6332ab64b8112eb3c0e9011525a3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 04:07:16 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:07:16 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 04:09:26 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:09:35 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:09:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:09:35 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:09:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:09:35 GMT
USER odoo
# Tue, 21 Nov 2023 04:09:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:09:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0b61a08606390fbb30208a1c7ecb8e9f362c2e67348e7ca4e0a137f155bfdc`  
		Last Modified: Tue, 21 Nov 2023 04:11:53 GMT  
		Size: 324.6 MB (324631518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cadee43b1bf171bcee8f8a922aaacf7780d1bc3f22ffb8753b6026dedad8f6`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618075eb4ae57747ac5d18886eb478e1bde106ce7c8ffdb4ee962e649342551e`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a97278fdc7005daaf7f7481fbaf2ad6650a52d3727b57952d0ec091e402d89`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66f192450018011ce8cedb344714cdbafaa778844b51ca83c7bd59b6c3d6018`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:b7851ec4705b5e2f2dcec02962bd3a42780532177776f54b1142571adc4d25aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611662048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affaaac65f413cdf81476af3f1f0da82fcf20ee50c65def7443bbc7daef30c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 04:34:09 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:34:09 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 04:37:08 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:37:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:37:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:37:23 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:37:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:37:27 GMT
USER odoo
# Tue, 21 Nov 2023 04:37:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:37:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa87a1e6855f7991bb0b852407c1259aecc287aaa92688747b0a83a5914051`  
		Last Modified: Tue, 21 Nov 2023 04:44:03 GMT  
		Size: 326.8 MB (326785980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38fb051d6a2636dff68e579dd6d331587b6b1fd93ae93749396e6cc146d95f8`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a545be1ff4fa26725caea8d93009850670d90b06669c660fdae6f5cbf6c66fb`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b650a97009bfa1a8feff40fe14603e739226de430d8e283f5c353279aff92`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0565f9098b3ad31dd9b67f2af817bf716ca6c4d258d4f0f4a1a616e190f59df0`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:3738d94b2ca518112b559c319630e385791a6f0be75797d1f718f57640b72914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:9f57fa8946d9301694a786aa4bd0f4ecc934118e82ea410bd082348e1dc42d5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594449353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf44b22dd1a9318c88613d2a81cefd271379a74b9c3aa0fbb1e34763240c97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 06:03:51 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:03:51 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 06:05:46 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:05:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:05:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:05:51 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:05:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:05:51 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:05:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:05:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:05:52 GMT
USER odoo
# Tue, 21 Nov 2023 06:05:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:05:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b699250faaaa18113675f119e5bda24097c32b1886dca1d8bdacc634802fa`  
		Last Modified: Tue, 21 Nov 2023 06:12:18 GMT  
		Size: 325.0 MB (325019891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca808d5c34b2820247735cbb3f7da17d71cdb205be8cfc5b7099be424fabdfd5`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148accfa4e3bf0b22a62ac9819f89e571ff37b5dbf5d405c190af8c27073c28`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4359884d1352b92e45c161e763ad85dec0c7d0800f995aa829ec1201cfbe93`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3d79cacd98196061c6ab9ef939de4ab58f316cbe5885217dd1bd610055de4`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:081e643c5b1d024db510b0c7b35b43a07b0eb08674a4478ecbe7d3e690c79535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589252116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8213f8ac42992be9d7b335deb14e4cdcdf6332ab64b8112eb3c0e9011525a3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 04:07:16 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:07:16 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 04:09:26 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:09:35 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:09:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:09:35 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:09:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:09:35 GMT
USER odoo
# Tue, 21 Nov 2023 04:09:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:09:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0b61a08606390fbb30208a1c7ecb8e9f362c2e67348e7ca4e0a137f155bfdc`  
		Last Modified: Tue, 21 Nov 2023 04:11:53 GMT  
		Size: 324.6 MB (324631518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cadee43b1bf171bcee8f8a922aaacf7780d1bc3f22ffb8753b6026dedad8f6`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618075eb4ae57747ac5d18886eb478e1bde106ce7c8ffdb4ee962e649342551e`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a97278fdc7005daaf7f7481fbaf2ad6650a52d3727b57952d0ec091e402d89`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66f192450018011ce8cedb344714cdbafaa778844b51ca83c7bd59b6c3d6018`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b7851ec4705b5e2f2dcec02962bd3a42780532177776f54b1142571adc4d25aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611662048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affaaac65f413cdf81476af3f1f0da82fcf20ee50c65def7443bbc7daef30c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 04:34:09 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:34:09 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 04:37:08 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:37:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:37:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:37:23 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:37:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:37:27 GMT
USER odoo
# Tue, 21 Nov 2023 04:37:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:37:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa87a1e6855f7991bb0b852407c1259aecc287aaa92688747b0a83a5914051`  
		Last Modified: Tue, 21 Nov 2023 04:44:03 GMT  
		Size: 326.8 MB (326785980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38fb051d6a2636dff68e579dd6d331587b6b1fd93ae93749396e6cc146d95f8`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a545be1ff4fa26725caea8d93009850670d90b06669c660fdae6f5cbf6c66fb`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b650a97009bfa1a8feff40fe14603e739226de430d8e283f5c353279aff92`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0565f9098b3ad31dd9b67f2af817bf716ca6c4d258d4f0f4a1a616e190f59df0`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:3738d94b2ca518112b559c319630e385791a6f0be75797d1f718f57640b72914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:9f57fa8946d9301694a786aa4bd0f4ecc934118e82ea410bd082348e1dc42d5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594449353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf44b22dd1a9318c88613d2a81cefd271379a74b9c3aa0fbb1e34763240c97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 06:03:51 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 06:03:51 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 06:05:46 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 06:05:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 06:05:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 06:05:51 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 06:05:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 06:05:51 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 06:05:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 06:05:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 06:05:52 GMT
USER odoo
# Tue, 21 Nov 2023 06:05:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 06:05:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b699250faaaa18113675f119e5bda24097c32b1886dca1d8bdacc634802fa`  
		Last Modified: Tue, 21 Nov 2023 06:12:18 GMT  
		Size: 325.0 MB (325019891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca808d5c34b2820247735cbb3f7da17d71cdb205be8cfc5b7099be424fabdfd5`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9148accfa4e3bf0b22a62ac9819f89e571ff37b5dbf5d405c190af8c27073c28`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4359884d1352b92e45c161e763ad85dec0c7d0800f995aa829ec1201cfbe93`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3d79cacd98196061c6ab9ef939de4ab58f316cbe5885217dd1bd610055de4`  
		Last Modified: Tue, 21 Nov 2023 06:11:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:081e643c5b1d024db510b0c7b35b43a07b0eb08674a4478ecbe7d3e690c79535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589252116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8213f8ac42992be9d7b335deb14e4cdcdf6332ab64b8112eb3c0e9011525a3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 04:07:16 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:07:16 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 04:09:26 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:09:35 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:09:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:09:35 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:09:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:09:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:09:35 GMT
USER odoo
# Tue, 21 Nov 2023 04:09:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:09:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0b61a08606390fbb30208a1c7ecb8e9f362c2e67348e7ca4e0a137f155bfdc`  
		Last Modified: Tue, 21 Nov 2023 04:11:53 GMT  
		Size: 324.6 MB (324631518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cadee43b1bf171bcee8f8a922aaacf7780d1bc3f22ffb8753b6026dedad8f6`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618075eb4ae57747ac5d18886eb478e1bde106ce7c8ffdb4ee962e649342551e`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a97278fdc7005daaf7f7481fbaf2ad6650a52d3727b57952d0ec091e402d89`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66f192450018011ce8cedb344714cdbafaa778844b51ca83c7bd59b6c3d6018`  
		Last Modified: Tue, 21 Nov 2023 04:11:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:b7851ec4705b5e2f2dcec02962bd3a42780532177776f54b1142571adc4d25aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611662048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affaaac65f413cdf81476af3f1f0da82fcf20ee50c65def7443bbc7daef30c95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Nov 2023 04:34:09 GMT
ARG ODOO_RELEASE=20231120
# Tue, 21 Nov 2023 04:34:09 GMT
ARG ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
# Tue, 21 Nov 2023 04:37:08 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 21 Nov 2023 04:37:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 21 Nov 2023 04:37:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 21 Nov 2023 04:37:23 GMT
# ARGS: ODOO_RELEASE=20231120 ODOO_SHA=57b836de2901c4ec5e3de433eb9258024701d255
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 21 Nov 2023 04:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Nov 2023 04:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 21 Nov 2023 04:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Nov 2023 04:37:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 21 Nov 2023 04:37:27 GMT
USER odoo
# Tue, 21 Nov 2023 04:37:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Nov 2023 04:37:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa87a1e6855f7991bb0b852407c1259aecc287aaa92688747b0a83a5914051`  
		Last Modified: Tue, 21 Nov 2023 04:44:03 GMT  
		Size: 326.8 MB (326785980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38fb051d6a2636dff68e579dd6d331587b6b1fd93ae93749396e6cc146d95f8`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a545be1ff4fa26725caea8d93009850670d90b06669c660fdae6f5cbf6c66fb`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b650a97009bfa1a8feff40fe14603e739226de430d8e283f5c353279aff92`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0565f9098b3ad31dd9b67f2af817bf716ca6c4d258d4f0f4a1a616e190f59df0`  
		Last Modified: Tue, 21 Nov 2023 04:43:20 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
