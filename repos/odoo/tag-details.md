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
$ docker pull odoo@sha256:5169ddb3b87cff30cea27dcfce9139314e5dea70b10e42a827f01762cf70f93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:0792706f71355f041895197ad3e776f577277fd22cab6d9a7a0a893dc29891e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563140418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cc4b62b25aa258edddec3f2b0b0b41390fd2969197c1c593a125b158c69274`
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
# Fri, 15 Dec 2023 19:35:31 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:35:31 GMT
ARG ODOO_SHA=a67e5a8be2d8b5c2da4f95614782ab4bcc0a17ec
# Fri, 15 Dec 2023 19:36:44 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=a67e5a8be2d8b5c2da4f95614782ab4bcc0a17ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:36:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:36:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:36:49 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=a67e5a8be2d8b5c2da4f95614782ab4bcc0a17ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:36:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:36:49 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:36:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:36:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:36:49 GMT
USER odoo
# Fri, 15 Dec 2023 19:36:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:36:49 GMT
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
	-	`sha256:57a703f8024a34101b938db0db0397334678a236e07d2b635317620908c8bd96`  
		Last Modified: Fri, 15 Dec 2023 19:39:06 GMT  
		Size: 308.3 MB (308337482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65c6f6abb15c03b11c8be9678aade4b60d0af5b53778677ec55b2e413585f64`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2de21c2b8bf0ce9eae2b74c0a5f67eca804f566b19510bc13baa5022e12eb8`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60711fb41440263b3116fec430aac986831a53ae08d11ff0b73855836bc95322`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8b2a923d1a58472bcf2e33df0220f13354d4a0dd3863f0254a8dcf9f63b73`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:5169ddb3b87cff30cea27dcfce9139314e5dea70b10e42a827f01762cf70f93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:0792706f71355f041895197ad3e776f577277fd22cab6d9a7a0a893dc29891e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563140418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cc4b62b25aa258edddec3f2b0b0b41390fd2969197c1c593a125b158c69274`
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
# Fri, 15 Dec 2023 19:35:31 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:35:31 GMT
ARG ODOO_SHA=a67e5a8be2d8b5c2da4f95614782ab4bcc0a17ec
# Fri, 15 Dec 2023 19:36:44 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=a67e5a8be2d8b5c2da4f95614782ab4bcc0a17ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:36:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:36:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:36:49 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=a67e5a8be2d8b5c2da4f95614782ab4bcc0a17ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:36:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:36:49 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:36:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:36:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:36:49 GMT
USER odoo
# Fri, 15 Dec 2023 19:36:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:36:49 GMT
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
	-	`sha256:57a703f8024a34101b938db0db0397334678a236e07d2b635317620908c8bd96`  
		Last Modified: Fri, 15 Dec 2023 19:39:06 GMT  
		Size: 308.3 MB (308337482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65c6f6abb15c03b11c8be9678aade4b60d0af5b53778677ec55b2e413585f64`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2de21c2b8bf0ce9eae2b74c0a5f67eca804f566b19510bc13baa5022e12eb8`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60711fb41440263b3116fec430aac986831a53ae08d11ff0b73855836bc95322`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8b2a923d1a58472bcf2e33df0220f13354d4a0dd3863f0254a8dcf9f63b73`  
		Last Modified: Fri, 15 Dec 2023 19:38:34 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:71ae1700211b6d3387d9b33c0d915bd3e12fda64d5b895dc8a526090a9d07292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:19e2d2ddabe02e6fffbdee3f9d6734920dfbac7d0df0cc84626d8835ea0491c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.5 MB (577503235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c0d3c8248b836829417063e3f497d9460d0170adfc27cecb924916de2baa6`
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
# Fri, 15 Dec 2023 19:33:52 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:33:52 GMT
ARG ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
# Fri, 15 Dec 2023 19:35:13 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:35:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:35:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:35:18 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:35:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:35:18 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:35:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:35:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:35:19 GMT
USER odoo
# Fri, 15 Dec 2023 19:35:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:35:19 GMT
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
	-	`sha256:b398bea99bf8c83e634e8bddda6cfb44052f45cc0e905cb2ac39a51a3856796a`  
		Last Modified: Fri, 15 Dec 2023 19:38:25 GMT  
		Size: 323.4 MB (323387080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5647b0142c1e2b87c441cdfb34fb7b3d1217ab7451ed89edb44b73178014ab`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bd58eb2637e9b0c6d6a7584a9ffebd9f9962917ff504e9a22a52f6e697350b`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74e139ddb09b7f4d74053600ceec1c3a75d4f8cf88234e5a6e856c79d90f803`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd02a8fa4086aabd9fc6d3b2ad9f6e0faa4d76bbb63c97876c547a07f9a75b1`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a8f53468664cd1f8c249a638e4afa6d44c072861ea65f9865aeb911a8c359771
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (573029481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d876138dfea48b2e4bc427ae378ae82b69c8aa6809be60094d9d6e78e8ea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:24:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 10:24:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 10:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 10:24:03 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 10:25:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 10:25:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:25:16 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 10:25:16 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Dec 2023 19:59:18 GMT
ARG ODOO_RELEASE=20231208
# Fri, 08 Dec 2023 19:59:18 GMT
ARG ODOO_SHA=468d34eb1d78003d832515f7f2bbc0cc90ab1cc0
# Fri, 08 Dec 2023 20:00:31 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=468d34eb1d78003d832515f7f2bbc0cc90ab1cc0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Dec 2023 20:00:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Dec 2023 20:00:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Dec 2023 20:00:39 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=468d34eb1d78003d832515f7f2bbc0cc90ab1cc0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Dec 2023 20:00:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Dec 2023 20:00:39 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Dec 2023 20:00:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Dec 2023 20:00:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Dec 2023 20:00:39 GMT
USER odoo
# Fri, 08 Dec 2023 20:00:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Dec 2023 20:00:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ab9b0a137551e75078132a976e9e490b4eb1fc07fe87beb915c8f0be0988b`  
		Last Modified: Tue, 21 Nov 2023 10:27:07 GMT  
		Size: 216.9 MB (216908243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451f82e1e1d62729c32c647a135084aeea39e2eecdfab5f468e549adbe642a1`  
		Last Modified: Tue, 21 Nov 2023 10:26:50 GMT  
		Size: 2.6 MB (2634860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d5b0160b4770a0c5d2bbe136fec01bf9daa283a549aceba5449dcc1b0eb7a`  
		Last Modified: Tue, 21 Nov 2023 10:26:49 GMT  
		Size: 459.5 KB (459492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca6c9a31e3038c6c59c584514d3543a5ed04d65585417fad7bd1a08779fa67f`  
		Last Modified: Fri, 08 Dec 2023 20:02:21 GMT  
		Size: 323.0 MB (322960299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339dd557785899b6ce705230df2b02bbe26c15935e86053d6f2939fcfee59d90`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae721c673b10423a864878a5efcc2b65e3405e07d4c76dd34348a4bf805c0a`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ac15a8b5ddfe6eb46a71b3f7f59c5ef91d296d27f24ff38f7b859442b192e5`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad95cab6488c0bde41a53c09c33e0e8163c540a7d13e04f3b25273fc71872490`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:24c67dadf8be5c956cd25f59f1d72980a44d81badb38905ecb2f37f0633c0216
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1b2371017686992430eb718879dea7368f7f828f2d298a4b9e7e3deaed153c`
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
# Fri, 15 Dec 2023 19:38:47 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:38:47 GMT
ARG ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
# Fri, 15 Dec 2023 19:41:07 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:41:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:41:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:41:23 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:41:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:41:24 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:41:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:41:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:41:25 GMT
USER odoo
# Fri, 15 Dec 2023 19:41:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:41:26 GMT
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
	-	`sha256:13f8fa92895b64c4834b7ff3ee299080bc3976e7ea85211a4ea0999605f795bc`  
		Last Modified: Fri, 15 Dec 2023 19:43:33 GMT  
		Size: 324.8 MB (324787864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aa28b20f0f24f94ea91818d99d75eeef6dd040227466e246194e6fed65cb77`  
		Last Modified: Fri, 15 Dec 2023 19:42:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cbb9d1b434cb777d1f65623a9ea12dd9b109dd3e5be2c6da9dd89f0b1bc086`  
		Last Modified: Fri, 15 Dec 2023 19:42:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0916130b01370e099a5e97fd34804a9cff2b6ca6a3caa398c607e7d543f473bb`  
		Last Modified: Fri, 15 Dec 2023 19:42:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab79c5f227822466354cf40ccebe0bf09cdd6f32cec479e7234a2a73f9ff410`  
		Last Modified: Fri, 15 Dec 2023 19:42:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:71ae1700211b6d3387d9b33c0d915bd3e12fda64d5b895dc8a526090a9d07292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:19e2d2ddabe02e6fffbdee3f9d6734920dfbac7d0df0cc84626d8835ea0491c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.5 MB (577503235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5c0d3c8248b836829417063e3f497d9460d0170adfc27cecb924916de2baa6`
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
# Fri, 15 Dec 2023 19:33:52 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:33:52 GMT
ARG ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
# Fri, 15 Dec 2023 19:35:13 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:35:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:35:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:35:18 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:35:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:35:18 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:35:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:35:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:35:19 GMT
USER odoo
# Fri, 15 Dec 2023 19:35:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:35:19 GMT
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
	-	`sha256:b398bea99bf8c83e634e8bddda6cfb44052f45cc0e905cb2ac39a51a3856796a`  
		Last Modified: Fri, 15 Dec 2023 19:38:25 GMT  
		Size: 323.4 MB (323387080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5647b0142c1e2b87c441cdfb34fb7b3d1217ab7451ed89edb44b73178014ab`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bd58eb2637e9b0c6d6a7584a9ffebd9f9962917ff504e9a22a52f6e697350b`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74e139ddb09b7f4d74053600ceec1c3a75d4f8cf88234e5a6e856c79d90f803`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd02a8fa4086aabd9fc6d3b2ad9f6e0faa4d76bbb63c97876c547a07f9a75b1`  
		Last Modified: Fri, 15 Dec 2023 19:37:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a8f53468664cd1f8c249a638e4afa6d44c072861ea65f9865aeb911a8c359771
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.0 MB (573029481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d876138dfea48b2e4bc427ae378ae82b69c8aa6809be60094d9d6e78e8ea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:24:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Nov 2023 10:24:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Nov 2023 10:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 10:24:03 GMT
ARG TARGETARCH
# Tue, 21 Nov 2023 10:25:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Nov 2023 10:25:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:25:16 GMT
RUN npm install -g rtlcss
# Tue, 21 Nov 2023 10:25:16 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Dec 2023 19:59:18 GMT
ARG ODOO_RELEASE=20231208
# Fri, 08 Dec 2023 19:59:18 GMT
ARG ODOO_SHA=468d34eb1d78003d832515f7f2bbc0cc90ab1cc0
# Fri, 08 Dec 2023 20:00:31 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=468d34eb1d78003d832515f7f2bbc0cc90ab1cc0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Dec 2023 20:00:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Dec 2023 20:00:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Dec 2023 20:00:39 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=468d34eb1d78003d832515f7f2bbc0cc90ab1cc0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Dec 2023 20:00:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Dec 2023 20:00:39 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Dec 2023 20:00:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Dec 2023 20:00:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Dec 2023 20:00:39 GMT
USER odoo
# Fri, 08 Dec 2023 20:00:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Dec 2023 20:00:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ab9b0a137551e75078132a976e9e490b4eb1fc07fe87beb915c8f0be0988b`  
		Last Modified: Tue, 21 Nov 2023 10:27:07 GMT  
		Size: 216.9 MB (216908243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451f82e1e1d62729c32c647a135084aeea39e2eecdfab5f468e549adbe642a1`  
		Last Modified: Tue, 21 Nov 2023 10:26:50 GMT  
		Size: 2.6 MB (2634860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006d5b0160b4770a0c5d2bbe136fec01bf9daa283a549aceba5449dcc1b0eb7a`  
		Last Modified: Tue, 21 Nov 2023 10:26:49 GMT  
		Size: 459.5 KB (459492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca6c9a31e3038c6c59c584514d3543a5ed04d65585417fad7bd1a08779fa67f`  
		Last Modified: Fri, 08 Dec 2023 20:02:21 GMT  
		Size: 323.0 MB (322960299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339dd557785899b6ce705230df2b02bbe26c15935e86053d6f2939fcfee59d90`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae721c673b10423a864878a5efcc2b65e3405e07d4c76dd34348a4bf805c0a`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ac15a8b5ddfe6eb46a71b3f7f59c5ef91d296d27f24ff38f7b859442b192e5`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad95cab6488c0bde41a53c09c33e0e8163c540a7d13e04f3b25273fc71872490`  
		Last Modified: Fri, 08 Dec 2023 20:01:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:24c67dadf8be5c956cd25f59f1d72980a44d81badb38905ecb2f37f0633c0216
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 MB (592017390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1b2371017686992430eb718879dea7368f7f828f2d298a4b9e7e3deaed153c`
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
# Fri, 15 Dec 2023 19:38:47 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:38:47 GMT
ARG ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
# Fri, 15 Dec 2023 19:41:07 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:41:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:41:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:41:23 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=dd439ff587a574a886855a9901d83d312214cdaf
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:41:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:41:24 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:41:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:41:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:41:25 GMT
USER odoo
# Fri, 15 Dec 2023 19:41:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:41:26 GMT
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
	-	`sha256:13f8fa92895b64c4834b7ff3ee299080bc3976e7ea85211a4ea0999605f795bc`  
		Last Modified: Fri, 15 Dec 2023 19:43:33 GMT  
		Size: 324.8 MB (324787864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aa28b20f0f24f94ea91818d99d75eeef6dd040227466e246194e6fed65cb77`  
		Last Modified: Fri, 15 Dec 2023 19:42:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cbb9d1b434cb777d1f65623a9ea12dd9b109dd3e5be2c6da9dd89f0b1bc086`  
		Last Modified: Fri, 15 Dec 2023 19:42:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0916130b01370e099a5e97fd34804a9cff2b6ca6a3caa398c607e7d543f473bb`  
		Last Modified: Fri, 15 Dec 2023 19:42:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab79c5f227822466354cf40ccebe0bf09cdd6f32cec479e7234a2a73f9ff410`  
		Last Modified: Fri, 15 Dec 2023 19:42:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:a0b415c1fdfd59abba1d4e220d81ca328d3ecd0da911d2609f4179bd7064a8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:a63b8294f9531af736a4eb55241cc0cb73e8824cc8376685d5ab495b7ebd1815
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593762355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c49abd517fb4d3335a641a900c0ccd923fec7515397963aa61b7bc477649ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:47:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 04:47:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 04:47:37 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 04:47:38 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 04:50:45 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 04:50:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:50:59 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 04:50:59 GMT
ENV ODOO_VERSION=17.0
# Fri, 15 Dec 2023 19:31:44 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:31:44 GMT
ARG ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
# Fri, 15 Dec 2023 19:33:39 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:33:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:33:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:33:44 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:33:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:33:44 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:33:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:33:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:33:44 GMT
USER odoo
# Fri, 15 Dec 2023 19:33:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:33:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b6d74eb5ad38b6aacfcfa4daf56cc8c38f636f6a9ddc69a04479cc6ac5c9d6`  
		Last Modified: Sat, 02 Dec 2023 04:54:11 GMT  
		Size: 233.7 MB (233729758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d621136e37a3ed7ade9ae6cb3ea6e0f4a6e19048001676d922e096d79dd1`  
		Last Modified: Sat, 02 Dec 2023 04:53:45 GMT  
		Size: 2.5 MB (2526589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c0ff2e7c8fdf34a67f3c215228454c4fab667f328176b9dbc46170300ae6c`  
		Last Modified: Sat, 02 Dec 2023 04:53:44 GMT  
		Size: 461.1 KB (461067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bb900e7ce3e56db3961f253decb8cd5d6c91698e44673c4f64af1e41d3cdab`  
		Last Modified: Fri, 15 Dec 2023 19:37:38 GMT  
		Size: 326.6 MB (326596150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a276cc93bd6a28c2e11c99d0b5876eb1952058e587cd7152c0329e36c2a76`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a99a931f8cf2d09fe9eb08ddc7533df69c59879dbdf08000ad86c24ed67e01`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7337e2afe2dc9fe51126d435160f5f849431de576e3e9fec13c8d8128b848093`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bd190209fd816138b299aeb0dac8e0b42fc2313bbb0881cddc2b576100c428`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9c7e9fdb15ab0037c886505db0118ab7d08bb21b16d81e7d3c5e70b50c371f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.4 MB (588406780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84651aaaa6020e29b8c8118ee6af5f20b340172c546510e770d46771eb272c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:15:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 06:15:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 06:15:40 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 06:15:40 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 06:18:17 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 06:18:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:18:32 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 06:18:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Dec 2023 19:56:55 GMT
ARG ODOO_RELEASE=20231208
# Fri, 08 Dec 2023 19:56:55 GMT
ARG ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
# Fri, 08 Dec 2023 19:59:08 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Dec 2023 19:59:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Dec 2023 19:59:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Dec 2023 19:59:15 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Dec 2023 19:59:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Dec 2023 19:59:15 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Dec 2023 19:59:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Dec 2023 19:59:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Dec 2023 19:59:16 GMT
USER odoo
# Fri, 08 Dec 2023 19:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Dec 2023 19:59:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2fbd5e011298a1d82b09d9b103b3c85586d12025686fb197205c02c5e340a2`  
		Last Modified: Sat, 02 Dec 2023 06:21:02 GMT  
		Size: 231.1 MB (231107816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c833560543c45eaf5583c723b991238f3600ac24ba07a362da30f82f6be8dc6`  
		Last Modified: Sat, 02 Dec 2023 06:20:43 GMT  
		Size: 2.5 MB (2520301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1617b34d74ba2e5b95ad66ee5cbc43579012bff1caa24cc6327fee160dc62cc`  
		Last Modified: Sat, 02 Dec 2023 06:20:43 GMT  
		Size: 461.1 KB (461073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d4b1aabad0bc38d42fcf94bd4a2972bb665d0103933d13ec5194d3351cdb8`  
		Last Modified: Fri, 08 Dec 2023 20:01:41 GMT  
		Size: 325.9 MB (325915185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b54be8f355648f9e799b7b1cca832d7d3e561a3c40cdab8c79eb66abf7a499`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51531d7f1ff1834ff7ffe2de8652d8e0c94d6624cd3080dfc420aa3b26bbf9bb`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1427aa84d3d480ff14462ba1b91108d72011ea1496dbc121ef55f0026550fe84`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065449cd7b89b82483c096451cf6c72014dd766ebecd2f7d6047550013815dc4`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:8f93498227ce95872600f724a2a29041511bc4a7332b540b73fa6e9afc709520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610577108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3489e88b86852152fb33de09b5ca08880c041bb25a9354fad5a062dd4766ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 08:12:00 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:12:03 GMT
ADD file:80047e51fa5311c19317ab688acec0517d98f1cbf74fa4c22a7105e80ebaf610 in / 
# Fri, 01 Dec 2023 08:12:04 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:09:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 05:09:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 05:09:22 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 05:09:22 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 05:13:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 05:13:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:13:39 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 05:13:40 GMT
ENV ODOO_VERSION=17.0
# Fri, 15 Dec 2023 19:34:38 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:34:38 GMT
ARG ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
# Fri, 15 Dec 2023 19:38:17 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:38:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:38:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:38:31 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:38:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:38:32 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:38:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:38:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:38:35 GMT
USER odoo
# Fri, 15 Dec 2023 19:38:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c3606768af36fe4984cee7cfc0c9d919a7adf83ac4c1849c30da06916b9ec921`  
		Last Modified: Sat, 02 Dec 2023 04:49:10 GMT  
		Size: 35.7 MB (35662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cab7e6a789250f903ab04c7af36f05cd95ad421f0010687d51d44f865da474e`  
		Last Modified: Sat, 02 Dec 2023 05:17:45 GMT  
		Size: 243.3 MB (243295005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18f49b132cf82e3cdcec078326873093460ffc189fa35b8d1f0e19e565cfc8`  
		Last Modified: Sat, 02 Dec 2023 05:17:14 GMT  
		Size: 2.8 MB (2803163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d21ff7071f1369530b67a6fb2780158786764eba5660a64fcde9124c5fe65`  
		Last Modified: Sat, 02 Dec 2023 05:17:13 GMT  
		Size: 461.2 KB (461214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0a7bc3530ba030477d500024a24c2f552d3a077012d7ae4f8f65e8d3010bbf`  
		Last Modified: Fri, 15 Dec 2023 19:42:37 GMT  
		Size: 328.4 MB (328352525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09520552b4a4cfff2e2a5bf2e4d3d701ae6dfab035c358bbd16d604644a8df`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1a2e3d1ad0eb5ed45ef535d08041edb754624bbc8ffbd630110a199b563dcc`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f19db4d5add10d1510fd0c4a26e7497ad4288cf5daf9a6abd5b3b666daff48`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61992da5ba5f9038e35d9be6159557f05856f8c55765ae7cedcee3962afbdcae`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:a0b415c1fdfd59abba1d4e220d81ca328d3ecd0da911d2609f4179bd7064a8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:a63b8294f9531af736a4eb55241cc0cb73e8824cc8376685d5ab495b7ebd1815
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593762355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c49abd517fb4d3335a641a900c0ccd923fec7515397963aa61b7bc477649ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:47:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 04:47:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 04:47:37 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 04:47:38 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 04:50:45 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 04:50:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:50:59 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 04:50:59 GMT
ENV ODOO_VERSION=17.0
# Fri, 15 Dec 2023 19:31:44 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:31:44 GMT
ARG ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
# Fri, 15 Dec 2023 19:33:39 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:33:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:33:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:33:44 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:33:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:33:44 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:33:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:33:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:33:44 GMT
USER odoo
# Fri, 15 Dec 2023 19:33:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:33:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b6d74eb5ad38b6aacfcfa4daf56cc8c38f636f6a9ddc69a04479cc6ac5c9d6`  
		Last Modified: Sat, 02 Dec 2023 04:54:11 GMT  
		Size: 233.7 MB (233729758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d621136e37a3ed7ade9ae6cb3ea6e0f4a6e19048001676d922e096d79dd1`  
		Last Modified: Sat, 02 Dec 2023 04:53:45 GMT  
		Size: 2.5 MB (2526589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c0ff2e7c8fdf34a67f3c215228454c4fab667f328176b9dbc46170300ae6c`  
		Last Modified: Sat, 02 Dec 2023 04:53:44 GMT  
		Size: 461.1 KB (461067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bb900e7ce3e56db3961f253decb8cd5d6c91698e44673c4f64af1e41d3cdab`  
		Last Modified: Fri, 15 Dec 2023 19:37:38 GMT  
		Size: 326.6 MB (326596150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a276cc93bd6a28c2e11c99d0b5876eb1952058e587cd7152c0329e36c2a76`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a99a931f8cf2d09fe9eb08ddc7533df69c59879dbdf08000ad86c24ed67e01`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7337e2afe2dc9fe51126d435160f5f849431de576e3e9fec13c8d8128b848093`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bd190209fd816138b299aeb0dac8e0b42fc2313bbb0881cddc2b576100c428`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9c7e9fdb15ab0037c886505db0118ab7d08bb21b16d81e7d3c5e70b50c371f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.4 MB (588406780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84651aaaa6020e29b8c8118ee6af5f20b340172c546510e770d46771eb272c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:15:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 06:15:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 06:15:40 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 06:15:40 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 06:18:17 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 06:18:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:18:32 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 06:18:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Dec 2023 19:56:55 GMT
ARG ODOO_RELEASE=20231208
# Fri, 08 Dec 2023 19:56:55 GMT
ARG ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
# Fri, 08 Dec 2023 19:59:08 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Dec 2023 19:59:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Dec 2023 19:59:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Dec 2023 19:59:15 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Dec 2023 19:59:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Dec 2023 19:59:15 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Dec 2023 19:59:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Dec 2023 19:59:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Dec 2023 19:59:16 GMT
USER odoo
# Fri, 08 Dec 2023 19:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Dec 2023 19:59:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2fbd5e011298a1d82b09d9b103b3c85586d12025686fb197205c02c5e340a2`  
		Last Modified: Sat, 02 Dec 2023 06:21:02 GMT  
		Size: 231.1 MB (231107816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c833560543c45eaf5583c723b991238f3600ac24ba07a362da30f82f6be8dc6`  
		Last Modified: Sat, 02 Dec 2023 06:20:43 GMT  
		Size: 2.5 MB (2520301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1617b34d74ba2e5b95ad66ee5cbc43579012bff1caa24cc6327fee160dc62cc`  
		Last Modified: Sat, 02 Dec 2023 06:20:43 GMT  
		Size: 461.1 KB (461073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d4b1aabad0bc38d42fcf94bd4a2972bb665d0103933d13ec5194d3351cdb8`  
		Last Modified: Fri, 08 Dec 2023 20:01:41 GMT  
		Size: 325.9 MB (325915185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b54be8f355648f9e799b7b1cca832d7d3e561a3c40cdab8c79eb66abf7a499`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51531d7f1ff1834ff7ffe2de8652d8e0c94d6624cd3080dfc420aa3b26bbf9bb`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1427aa84d3d480ff14462ba1b91108d72011ea1496dbc121ef55f0026550fe84`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065449cd7b89b82483c096451cf6c72014dd766ebecd2f7d6047550013815dc4`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:8f93498227ce95872600f724a2a29041511bc4a7332b540b73fa6e9afc709520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610577108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3489e88b86852152fb33de09b5ca08880c041bb25a9354fad5a062dd4766ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 08:12:00 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:12:03 GMT
ADD file:80047e51fa5311c19317ab688acec0517d98f1cbf74fa4c22a7105e80ebaf610 in / 
# Fri, 01 Dec 2023 08:12:04 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:09:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 05:09:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 05:09:22 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 05:09:22 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 05:13:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 05:13:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:13:39 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 05:13:40 GMT
ENV ODOO_VERSION=17.0
# Fri, 15 Dec 2023 19:34:38 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:34:38 GMT
ARG ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
# Fri, 15 Dec 2023 19:38:17 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:38:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:38:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:38:31 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:38:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:38:32 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:38:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:38:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:38:35 GMT
USER odoo
# Fri, 15 Dec 2023 19:38:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c3606768af36fe4984cee7cfc0c9d919a7adf83ac4c1849c30da06916b9ec921`  
		Last Modified: Sat, 02 Dec 2023 04:49:10 GMT  
		Size: 35.7 MB (35662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cab7e6a789250f903ab04c7af36f05cd95ad421f0010687d51d44f865da474e`  
		Last Modified: Sat, 02 Dec 2023 05:17:45 GMT  
		Size: 243.3 MB (243295005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18f49b132cf82e3cdcec078326873093460ffc189fa35b8d1f0e19e565cfc8`  
		Last Modified: Sat, 02 Dec 2023 05:17:14 GMT  
		Size: 2.8 MB (2803163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d21ff7071f1369530b67a6fb2780158786764eba5660a64fcde9124c5fe65`  
		Last Modified: Sat, 02 Dec 2023 05:17:13 GMT  
		Size: 461.2 KB (461214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0a7bc3530ba030477d500024a24c2f552d3a077012d7ae4f8f65e8d3010bbf`  
		Last Modified: Fri, 15 Dec 2023 19:42:37 GMT  
		Size: 328.4 MB (328352525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09520552b4a4cfff2e2a5bf2e4d3d701ae6dfab035c358bbd16d604644a8df`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1a2e3d1ad0eb5ed45ef535d08041edb754624bbc8ffbd630110a199b563dcc`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f19db4d5add10d1510fd0c4a26e7497ad4288cf5daf9a6abd5b3b666daff48`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61992da5ba5f9038e35d9be6159557f05856f8c55765ae7cedcee3962afbdcae`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:a0b415c1fdfd59abba1d4e220d81ca328d3ecd0da911d2609f4179bd7064a8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:a63b8294f9531af736a4eb55241cc0cb73e8824cc8376685d5ab495b7ebd1815
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593762355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c49abd517fb4d3335a641a900c0ccd923fec7515397963aa61b7bc477649ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:47:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 04:47:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 04:47:37 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 04:47:38 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 04:50:45 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 04:50:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 04:50:59 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 04:50:59 GMT
ENV ODOO_VERSION=17.0
# Fri, 15 Dec 2023 19:31:44 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:31:44 GMT
ARG ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
# Fri, 15 Dec 2023 19:33:39 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:33:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:33:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:33:44 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:33:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:33:44 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:33:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:33:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:33:44 GMT
USER odoo
# Fri, 15 Dec 2023 19:33:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:33:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b6d74eb5ad38b6aacfcfa4daf56cc8c38f636f6a9ddc69a04479cc6ac5c9d6`  
		Last Modified: Sat, 02 Dec 2023 04:54:11 GMT  
		Size: 233.7 MB (233729758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf80d621136e37a3ed7ade9ae6cb3ea6e0f4a6e19048001676d922e096d79dd1`  
		Last Modified: Sat, 02 Dec 2023 04:53:45 GMT  
		Size: 2.5 MB (2526589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c0ff2e7c8fdf34a67f3c215228454c4fab667f328176b9dbc46170300ae6c`  
		Last Modified: Sat, 02 Dec 2023 04:53:44 GMT  
		Size: 461.1 KB (461067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bb900e7ce3e56db3961f253decb8cd5d6c91698e44673c4f64af1e41d3cdab`  
		Last Modified: Fri, 15 Dec 2023 19:37:38 GMT  
		Size: 326.6 MB (326596150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a276cc93bd6a28c2e11c99d0b5876eb1952058e587cd7152c0329e36c2a76`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a99a931f8cf2d09fe9eb08ddc7533df69c59879dbdf08000ad86c24ed67e01`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7337e2afe2dc9fe51126d435160f5f849431de576e3e9fec13c8d8128b848093`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bd190209fd816138b299aeb0dac8e0b42fc2313bbb0881cddc2b576100c428`  
		Last Modified: Fri, 15 Dec 2023 19:37:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9c7e9fdb15ab0037c886505db0118ab7d08bb21b16d81e7d3c5e70b50c371f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.4 MB (588406780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84651aaaa6020e29b8c8118ee6af5f20b340172c546510e770d46771eb272c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:15:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 06:15:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 06:15:40 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 06:15:40 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 06:18:17 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 06:18:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:18:32 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 06:18:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Dec 2023 19:56:55 GMT
ARG ODOO_RELEASE=20231208
# Fri, 08 Dec 2023 19:56:55 GMT
ARG ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
# Fri, 08 Dec 2023 19:59:08 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Dec 2023 19:59:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Dec 2023 19:59:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Dec 2023 19:59:15 GMT
# ARGS: ODOO_RELEASE=20231208 ODOO_SHA=22fee8e6b6f6e61236198eca5b01e2ebd223844d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Dec 2023 19:59:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Dec 2023 19:59:15 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Dec 2023 19:59:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Dec 2023 19:59:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Dec 2023 19:59:16 GMT
USER odoo
# Fri, 08 Dec 2023 19:59:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Dec 2023 19:59:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2fbd5e011298a1d82b09d9b103b3c85586d12025686fb197205c02c5e340a2`  
		Last Modified: Sat, 02 Dec 2023 06:21:02 GMT  
		Size: 231.1 MB (231107816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c833560543c45eaf5583c723b991238f3600ac24ba07a362da30f82f6be8dc6`  
		Last Modified: Sat, 02 Dec 2023 06:20:43 GMT  
		Size: 2.5 MB (2520301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1617b34d74ba2e5b95ad66ee5cbc43579012bff1caa24cc6327fee160dc62cc`  
		Last Modified: Sat, 02 Dec 2023 06:20:43 GMT  
		Size: 461.1 KB (461073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d4b1aabad0bc38d42fcf94bd4a2972bb665d0103933d13ec5194d3351cdb8`  
		Last Modified: Fri, 08 Dec 2023 20:01:41 GMT  
		Size: 325.9 MB (325915185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b54be8f355648f9e799b7b1cca832d7d3e561a3c40cdab8c79eb66abf7a499`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51531d7f1ff1834ff7ffe2de8652d8e0c94d6624cd3080dfc420aa3b26bbf9bb`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1427aa84d3d480ff14462ba1b91108d72011ea1496dbc121ef55f0026550fe84`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065449cd7b89b82483c096451cf6c72014dd766ebecd2f7d6047550013815dc4`  
		Last Modified: Fri, 08 Dec 2023 20:01:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:8f93498227ce95872600f724a2a29041511bc4a7332b540b73fa6e9afc709520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610577108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3489e88b86852152fb33de09b5ca08880c041bb25a9354fad5a062dd4766ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 01 Dec 2023 08:12:00 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:12:03 GMT
ADD file:80047e51fa5311c19317ab688acec0517d98f1cbf74fa4c22a7105e80ebaf610 in / 
# Fri, 01 Dec 2023 08:12:04 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:09:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 02 Dec 2023 05:09:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 02 Dec 2023 05:09:22 GMT
ENV LANG=en_US.UTF-8
# Sat, 02 Dec 2023 05:09:22 GMT
ARG TARGETARCH
# Sat, 02 Dec 2023 05:13:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 02 Dec 2023 05:13:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:13:39 GMT
RUN npm install -g rtlcss
# Sat, 02 Dec 2023 05:13:40 GMT
ENV ODOO_VERSION=17.0
# Fri, 15 Dec 2023 19:34:38 GMT
ARG ODOO_RELEASE=20231215
# Fri, 15 Dec 2023 19:34:38 GMT
ARG ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
# Fri, 15 Dec 2023 19:38:17 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 Dec 2023 19:38:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 15 Dec 2023 19:38:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 Dec 2023 19:38:31 GMT
# ARGS: ODOO_RELEASE=20231215 ODOO_SHA=e5073e19f71cbf056e2e647aa667d95b6f903901
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 Dec 2023 19:38:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 Dec 2023 19:38:32 GMT
EXPOSE 8069 8071 8072
# Fri, 15 Dec 2023 19:38:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 Dec 2023 19:38:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 Dec 2023 19:38:35 GMT
USER odoo
# Fri, 15 Dec 2023 19:38:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Dec 2023 19:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c3606768af36fe4984cee7cfc0c9d919a7adf83ac4c1849c30da06916b9ec921`  
		Last Modified: Sat, 02 Dec 2023 04:49:10 GMT  
		Size: 35.7 MB (35662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cab7e6a789250f903ab04c7af36f05cd95ad421f0010687d51d44f865da474e`  
		Last Modified: Sat, 02 Dec 2023 05:17:45 GMT  
		Size: 243.3 MB (243295005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd18f49b132cf82e3cdcec078326873093460ffc189fa35b8d1f0e19e565cfc8`  
		Last Modified: Sat, 02 Dec 2023 05:17:14 GMT  
		Size: 2.8 MB (2803163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d21ff7071f1369530b67a6fb2780158786764eba5660a64fcde9124c5fe65`  
		Last Modified: Sat, 02 Dec 2023 05:17:13 GMT  
		Size: 461.2 KB (461214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0a7bc3530ba030477d500024a24c2f552d3a077012d7ae4f8f65e8d3010bbf`  
		Last Modified: Fri, 15 Dec 2023 19:42:37 GMT  
		Size: 328.4 MB (328352525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a09520552b4a4cfff2e2a5bf2e4d3d701ae6dfab035c358bbd16d604644a8df`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1a2e3d1ad0eb5ed45ef535d08041edb754624bbc8ffbd630110a199b563dcc`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f19db4d5add10d1510fd0c4a26e7497ad4288cf5daf9a6abd5b3b666daff48`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61992da5ba5f9038e35d9be6159557f05856f8c55765ae7cedcee3962afbdcae`  
		Last Modified: Fri, 15 Dec 2023 19:41:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
