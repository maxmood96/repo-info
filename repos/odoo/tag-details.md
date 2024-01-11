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
$ docker pull odoo@sha256:4257fdbf245818efbdaba3f8cd70960cf94ccf4a53aa75a9b22dadd4368edb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:18caf5e2f61e4a1d66feda286018eea758fdc4346ea0c68b0133a9ade21b1fba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563264982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08915dc1b3726ce61e073cf70d5ec2115b8d8b20eb084e93313179a6a6b9694d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:59 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Dec 2023 02:31:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Dec 2023 02:31:59 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:36:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 19 Dec 2023 02:36:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:36:11 GMT
RUN npm install -g rtlcss
# Tue, 19 Dec 2023 02:36:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 04 Jan 2024 21:09:10 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:09:10 GMT
ARG ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
# Thu, 04 Jan 2024 21:10:22 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:10:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:10:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:10:27 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:10:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:10:27 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:10:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:10:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:10:27 GMT
USER odoo
# Thu, 04 Jan 2024 21:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:10:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d5d69e2605b2bccd82e2df0551e09fb8dc42447b60a2bc93b59aa605c3591c`  
		Last Modified: Tue, 19 Dec 2023 02:38:55 GMT  
		Size: 220.3 MB (220298621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1ef12f1e24c3c6833763c9d4f4161f145a75c469ea11118c3d89f26cb5da`  
		Last Modified: Tue, 19 Dec 2023 02:38:30 GMT  
		Size: 2.6 MB (2625731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8705a2eadf4550b011bb15758e88dfa0da3ae5e3cc226a651ae08f0cccd49ae`  
		Last Modified: Tue, 19 Dec 2023 02:38:30 GMT  
		Size: 459.6 KB (459552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d844b283e8c6e3e89385c2ef3df567da695bf37c70724e6fbcef8cdbb93c9c97`  
		Last Modified: Thu, 04 Jan 2024 21:12:52 GMT  
		Size: 308.5 MB (308460739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062924091b4216b255990c9b871ab93c8cf5e07df79395eb4acc34d4a981b611`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028597b03d83c131967578096fee4c50587721f8ad78bb380b695aa2f43bab8b`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9be1abb440d0df0a3881211c8f4e60cbe4abfb523dee086dc5831898f62e7a`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1551ca54e35fd752f611f256e0efbfad9bdba4b10d9e22fbdc2b888ec7371020`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:4257fdbf245818efbdaba3f8cd70960cf94ccf4a53aa75a9b22dadd4368edb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:18caf5e2f61e4a1d66feda286018eea758fdc4346ea0c68b0133a9ade21b1fba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563264982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08915dc1b3726ce61e073cf70d5ec2115b8d8b20eb084e93313179a6a6b9694d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:59 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Dec 2023 02:31:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Dec 2023 02:31:59 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:36:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 19 Dec 2023 02:36:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:36:11 GMT
RUN npm install -g rtlcss
# Tue, 19 Dec 2023 02:36:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 04 Jan 2024 21:09:10 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:09:10 GMT
ARG ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
# Thu, 04 Jan 2024 21:10:22 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:10:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:10:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:10:27 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:10:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:10:27 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:10:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:10:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:10:27 GMT
USER odoo
# Thu, 04 Jan 2024 21:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:10:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d5d69e2605b2bccd82e2df0551e09fb8dc42447b60a2bc93b59aa605c3591c`  
		Last Modified: Tue, 19 Dec 2023 02:38:55 GMT  
		Size: 220.3 MB (220298621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1ef12f1e24c3c6833763c9d4f4161f145a75c469ea11118c3d89f26cb5da`  
		Last Modified: Tue, 19 Dec 2023 02:38:30 GMT  
		Size: 2.6 MB (2625731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8705a2eadf4550b011bb15758e88dfa0da3ae5e3cc226a651ae08f0cccd49ae`  
		Last Modified: Tue, 19 Dec 2023 02:38:30 GMT  
		Size: 459.6 KB (459552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d844b283e8c6e3e89385c2ef3df567da695bf37c70724e6fbcef8cdbb93c9c97`  
		Last Modified: Thu, 04 Jan 2024 21:12:52 GMT  
		Size: 308.5 MB (308460739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062924091b4216b255990c9b871ab93c8cf5e07df79395eb4acc34d4a981b611`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028597b03d83c131967578096fee4c50587721f8ad78bb380b695aa2f43bab8b`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9be1abb440d0df0a3881211c8f4e60cbe4abfb523dee086dc5831898f62e7a`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1551ca54e35fd752f611f256e0efbfad9bdba4b10d9e22fbdc2b888ec7371020`  
		Last Modified: Thu, 04 Jan 2024 21:12:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:6a6bd3663e03f5131016ddda37282c3fb366b88dd8a7a50832ad15f7d4326188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:9b0eae5f92d511274b0f770bb01e09af24dec4a8316300e01a74411ecf5a6ffd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.8 MB (577761185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ac4f68c034cdd95088b311733c43ed0e933e807a4057c01e99e92c5e394f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:59 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Dec 2023 02:31:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Dec 2023 02:31:59 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:31:59 GMT
ARG TARGETARCH
# Tue, 19 Dec 2023 02:33:11 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 19 Dec 2023 02:33:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:23 GMT
RUN npm install -g rtlcss
# Tue, 19 Dec 2023 02:33:24 GMT
ENV ODOO_VERSION=16.0
# Thu, 04 Jan 2024 21:07:31 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:07:31 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 04 Jan 2024 21:08:54 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:08:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:08:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:08:59 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:08:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:08:59 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:08:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:08:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:08:59 GMT
USER odoo
# Thu, 04 Jan 2024 21:08:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:08:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21397601f383856bad1be67c360c70e98e2164b6d334345340ef77aab8d01277`  
		Last Modified: Tue, 19 Dec 2023 02:38:06 GMT  
		Size: 219.6 MB (219606068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a886ed10d0ec268c641a802cb8a7cd4bb0276e9f273a6d084fb8d663d99492e9`  
		Last Modified: Tue, 19 Dec 2023 02:37:41 GMT  
		Size: 2.6 MB (2629859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3109584422e3b3ffbbfc68a4bf5323d9a355db5e6aeeeefbd90a419167213c1`  
		Last Modified: Tue, 19 Dec 2023 02:37:41 GMT  
		Size: 459.6 KB (459559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b96cd3ce2d032c5c9b0520239960dcdddbc1f47377857a1569932fb76de3f78`  
		Last Modified: Thu, 04 Jan 2024 21:12:09 GMT  
		Size: 323.6 MB (323645365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b98bb3c67dea8776655d0800c7726b9f2b29a7c2da155c16ea305290a4d8c5`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fc724203099b53e6f44f190372255f98d47cd4d7885792a798443c666ef4a0`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fef4c374432b3a459e7bcfc764ff1c9da6e83cbd8310867b4c932445018cad3`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f8cf22e7c707bfdc0b7cbdb0889953c908f6c68142b25c677d2ccae892349b`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d78c417757e8b6a7c9d1f5e86fef0770ddf08057a050ad33449eac3211f4736e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573351812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd18c1e9cada18b08be9f4a2d2e006506ccc037dfe71c1a77d1c4fd4ce1b3043`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:22:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Dec 2023 03:22:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Dec 2023 03:22:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 03:22:45 GMT
ARG TARGETARCH
# Tue, 19 Dec 2023 03:23:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 19 Dec 2023 03:23:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:24:00 GMT
RUN npm install -g rtlcss
# Tue, 19 Dec 2023 03:24:00 GMT
ENV ODOO_VERSION=16.0
# Thu, 04 Jan 2024 21:11:41 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:11:41 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 04 Jan 2024 21:13:00 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:13:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:13:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:13:08 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:13:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:13:08 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:13:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:13:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:13:09 GMT
USER odoo
# Thu, 04 Jan 2024 21:13:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:13:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ad9b105863f2fc14a5eef7551b0e02b42125be8cf06d2b399cca8dd47b9024`  
		Last Modified: Tue, 19 Dec 2023 03:25:50 GMT  
		Size: 216.9 MB (216906264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585aa02a509f7adac375bec76b48202f6c03b9204aeeda420abd6a05fd26b625`  
		Last Modified: Tue, 19 Dec 2023 03:25:32 GMT  
		Size: 2.6 MB (2634790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7efcf8969b0a1f21c021a830c4005ce948c2d74c14f20ee46a0c716d9a9406`  
		Last Modified: Tue, 19 Dec 2023 03:25:32 GMT  
		Size: 459.6 KB (459615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39864f7de5e477d4dfb0d0c352d686b67812df67e69a73a1a6102e10ae9068b`  
		Last Modified: Thu, 04 Jan 2024 21:14:37 GMT  
		Size: 323.3 MB (323284635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a1b697966e4035852843b44d30ba78874866ea008fc1fe7ad7ba474e601ba6`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b168e28fcadc6a814d2125df1bcdbf145176de81bad9a90eebd7d60efcfc3a`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8655d8577e4f4033b23cd00e5e7fa8ed3a5dd8e1352597d616126d1f0ae01f`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58012a4694966a381c69b0459f5b07acc8d099163fe16b2819dcc56599512f4`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:5eef172dfc9ddcbbd443fab03e1916608d59e6c1d8de9569fb67999c93a1b19c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592310873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b5f1043ba3b4f146b902485193e734bb02cd369cc5da43d3316d6f66ad87a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:56:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 03:56:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 03:56:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 03:56:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 03:59:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 03:59:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:59:44 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 03:59:45 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jan 2024 03:59:45 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 03:59:46 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 11 Jan 2024 04:02:09 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 04:02:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 04:02:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 04:02:24 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 04:02:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 04:02:26 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 04:02:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 04:02:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 04:02:28 GMT
USER odoo
# Thu, 11 Jan 2024 04:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:02:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98645df03fa753cd35df386c12a15edceb4284519ed070b82144681b10101c7`  
		Last Modified: Thu, 11 Jan 2024 04:03:17 GMT  
		Size: 228.6 MB (228601149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e8f09bc42c4ab2ba211885268c12651fd157357bc388a9ace0b59c705a2d22`  
		Last Modified: Thu, 11 Jan 2024 04:02:47 GMT  
		Size: 2.9 MB (2875618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5ba7386839331811e9baf6be69016dc74bc0b395e5d441677af7b58038dff5`  
		Last Modified: Thu, 11 Jan 2024 04:02:46 GMT  
		Size: 460.4 KB (460388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54728c2a7648f1e3d157ba509b0a122fc6907750e83132b727cf0d946e9320e6`  
		Last Modified: Thu, 11 Jan 2024 04:03:30 GMT  
		Size: 325.1 MB (325077448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f646906d36e6ce7633381af7974bc97093e14d6f71f0567365f4ab7a72262b5e`  
		Last Modified: Thu, 11 Jan 2024 04:02:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaad691bd9b87320ec4907a43ebeee482631201cb2aa28dc670248a67aff681`  
		Last Modified: Thu, 11 Jan 2024 04:02:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90f479fbf932e2a6b7f302497f29541643ffa96ccfa397971c2b2236470206f`  
		Last Modified: Thu, 11 Jan 2024 04:02:44 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7111b9f78ae35c050f668a191b43cbae158cfd4bc45c869e13eebb7404e370`  
		Last Modified: Thu, 11 Jan 2024 04:02:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:6a6bd3663e03f5131016ddda37282c3fb366b88dd8a7a50832ad15f7d4326188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:9b0eae5f92d511274b0f770bb01e09af24dec4a8316300e01a74411ecf5a6ffd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.8 MB (577761185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ac4f68c034cdd95088b311733c43ed0e933e807a4057c01e99e92c5e394f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:59 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Dec 2023 02:31:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Dec 2023 02:31:59 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:31:59 GMT
ARG TARGETARCH
# Tue, 19 Dec 2023 02:33:11 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 19 Dec 2023 02:33:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:23 GMT
RUN npm install -g rtlcss
# Tue, 19 Dec 2023 02:33:24 GMT
ENV ODOO_VERSION=16.0
# Thu, 04 Jan 2024 21:07:31 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:07:31 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 04 Jan 2024 21:08:54 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:08:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:08:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:08:59 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:08:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:08:59 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:08:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:08:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:08:59 GMT
USER odoo
# Thu, 04 Jan 2024 21:08:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:08:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21397601f383856bad1be67c360c70e98e2164b6d334345340ef77aab8d01277`  
		Last Modified: Tue, 19 Dec 2023 02:38:06 GMT  
		Size: 219.6 MB (219606068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a886ed10d0ec268c641a802cb8a7cd4bb0276e9f273a6d084fb8d663d99492e9`  
		Last Modified: Tue, 19 Dec 2023 02:37:41 GMT  
		Size: 2.6 MB (2629859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3109584422e3b3ffbbfc68a4bf5323d9a355db5e6aeeeefbd90a419167213c1`  
		Last Modified: Tue, 19 Dec 2023 02:37:41 GMT  
		Size: 459.6 KB (459559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b96cd3ce2d032c5c9b0520239960dcdddbc1f47377857a1569932fb76de3f78`  
		Last Modified: Thu, 04 Jan 2024 21:12:09 GMT  
		Size: 323.6 MB (323645365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b98bb3c67dea8776655d0800c7726b9f2b29a7c2da155c16ea305290a4d8c5`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fc724203099b53e6f44f190372255f98d47cd4d7885792a798443c666ef4a0`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fef4c374432b3a459e7bcfc764ff1c9da6e83cbd8310867b4c932445018cad3`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f8cf22e7c707bfdc0b7cbdb0889953c908f6c68142b25c677d2ccae892349b`  
		Last Modified: Thu, 04 Jan 2024 21:11:31 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d78c417757e8b6a7c9d1f5e86fef0770ddf08057a050ad33449eac3211f4736e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573351812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd18c1e9cada18b08be9f4a2d2e006506ccc037dfe71c1a77d1c4fd4ce1b3043`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:22:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Dec 2023 03:22:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Dec 2023 03:22:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 03:22:45 GMT
ARG TARGETARCH
# Tue, 19 Dec 2023 03:23:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 19 Dec 2023 03:23:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:24:00 GMT
RUN npm install -g rtlcss
# Tue, 19 Dec 2023 03:24:00 GMT
ENV ODOO_VERSION=16.0
# Thu, 04 Jan 2024 21:11:41 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:11:41 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 04 Jan 2024 21:13:00 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:13:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:13:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:13:08 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:13:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:13:08 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:13:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:13:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:13:09 GMT
USER odoo
# Thu, 04 Jan 2024 21:13:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:13:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ad9b105863f2fc14a5eef7551b0e02b42125be8cf06d2b399cca8dd47b9024`  
		Last Modified: Tue, 19 Dec 2023 03:25:50 GMT  
		Size: 216.9 MB (216906264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585aa02a509f7adac375bec76b48202f6c03b9204aeeda420abd6a05fd26b625`  
		Last Modified: Tue, 19 Dec 2023 03:25:32 GMT  
		Size: 2.6 MB (2634790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7efcf8969b0a1f21c021a830c4005ce948c2d74c14f20ee46a0c716d9a9406`  
		Last Modified: Tue, 19 Dec 2023 03:25:32 GMT  
		Size: 459.6 KB (459615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39864f7de5e477d4dfb0d0c352d686b67812df67e69a73a1a6102e10ae9068b`  
		Last Modified: Thu, 04 Jan 2024 21:14:37 GMT  
		Size: 323.3 MB (323284635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a1b697966e4035852843b44d30ba78874866ea008fc1fe7ad7ba474e601ba6`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b168e28fcadc6a814d2125df1bcdbf145176de81bad9a90eebd7d60efcfc3a`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8655d8577e4f4033b23cd00e5e7fa8ed3a5dd8e1352597d616126d1f0ae01f`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58012a4694966a381c69b0459f5b07acc8d099163fe16b2819dcc56599512f4`  
		Last Modified: Thu, 04 Jan 2024 21:14:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5eef172dfc9ddcbbd443fab03e1916608d59e6c1d8de9569fb67999c93a1b19c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.3 MB (592310873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8b5f1043ba3b4f146b902485193e734bb02cd369cc5da43d3316d6f66ad87a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:56:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 03:56:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 03:56:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 03:56:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 03:59:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 03:59:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:59:44 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 03:59:45 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jan 2024 03:59:45 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 03:59:46 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 11 Jan 2024 04:02:09 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 04:02:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 04:02:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 04:02:24 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 04:02:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 04:02:26 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 04:02:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 04:02:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 04:02:28 GMT
USER odoo
# Thu, 11 Jan 2024 04:02:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:02:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98645df03fa753cd35df386c12a15edceb4284519ed070b82144681b10101c7`  
		Last Modified: Thu, 11 Jan 2024 04:03:17 GMT  
		Size: 228.6 MB (228601149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e8f09bc42c4ab2ba211885268c12651fd157357bc388a9ace0b59c705a2d22`  
		Last Modified: Thu, 11 Jan 2024 04:02:47 GMT  
		Size: 2.9 MB (2875618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5ba7386839331811e9baf6be69016dc74bc0b395e5d441677af7b58038dff5`  
		Last Modified: Thu, 11 Jan 2024 04:02:46 GMT  
		Size: 460.4 KB (460388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54728c2a7648f1e3d157ba509b0a122fc6907750e83132b727cf0d946e9320e6`  
		Last Modified: Thu, 11 Jan 2024 04:03:30 GMT  
		Size: 325.1 MB (325077448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f646906d36e6ce7633381af7974bc97093e14d6f71f0567365f4ab7a72262b5e`  
		Last Modified: Thu, 11 Jan 2024 04:02:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaad691bd9b87320ec4907a43ebeee482631201cb2aa28dc670248a67aff681`  
		Last Modified: Thu, 11 Jan 2024 04:02:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90f479fbf932e2a6b7f302497f29541643ffa96ccfa397971c2b2236470206f`  
		Last Modified: Thu, 11 Jan 2024 04:02:44 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7111b9f78ae35c050f668a191b43cbae158cfd4bc45c869e13eebb7404e370`  
		Last Modified: Thu, 11 Jan 2024 04:02:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:463baaa507dc8b6d62486dfd34589e6014f8f2735927b7c205ef42d83b563443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:cb62da0aaea917a6ef53e457e4b4113da46b60fc95d06e72f946d75f1f1eaaad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596401656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e2a8d99256a928d6c814584cf9c97901b623a06b113a8a21ba7c376e544fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:29:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 09:29:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 09:29:57 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 09:29:57 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 09:32:06 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 09:32:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:32:18 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 09:32:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 21:05:22 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:05:22 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 21:07:19 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:07:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:07:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:07:25 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:07:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:07:25 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:07:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:07:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:07:25 GMT
USER odoo
# Thu, 04 Jan 2024 21:07:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:07:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89681bc3d92fa58300c17f37a8c00221342b77325e00deb20e71ea410071d500`  
		Last Modified: Sat, 16 Dec 2023 09:34:46 GMT  
		Size: 233.7 MB (233730172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a3dc4306b241f9806eface9e5fe3c10ef771e41f03509a141414da8bb7c04`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 2.5 MB (2526485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746699b2b8c3aebf90f574a4692f492e2e617506c92d7a00874d79e4fddaf014`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b649d1972addc355aeac03251b960480b383859922d709ccbd2fc91e93cfd`  
		Last Modified: Thu, 04 Jan 2024 21:11:20 GMT  
		Size: 329.2 MB (329234819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f962cb53e5d611aea7cd0af144701cc13a08a2e8b7e07000234144678d8e8c`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaa5efbac844aae50891ecb81a4d2164862e1d5af3ae1d3b4fd79e5f204332b`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85107f9250c2e57e424d2cac941f24ccaecd2155bb9fa0468f5a82b5fa253e`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c259e9b1973dfcb04ef1ce9d24cec72aac2b6f600139f6ac1d82d95028d4b5a8`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1fb6c38ec3cb38c387c2af50c5dbe74c32c67af4a1182dff9005c93c74cf1f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591320520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06002113d5d47f707538c2065c32bb2e5d5c9476daf414b5e04b6a64e6ddd55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:59:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 10:59:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 10:59:32 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 10:59:32 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:01:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:02:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:02:09 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:02:09 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 21:09:18 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:09:18 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 21:11:28 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:11:30 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:11:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:11:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:11:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:11:31 GMT
USER odoo
# Thu, 04 Jan 2024 21:11:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:11:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed064f4459a4f1ab48040e16f6b55972797bd014de0d33737d676d7a1a25db4`  
		Last Modified: Sat, 16 Dec 2023 11:04:40 GMT  
		Size: 231.1 MB (231107542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217c6a3bbcbbb21c659f79f47bd7f96d743d57cfd0fe0b1678b81f7ff769a77`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 2.5 MB (2520464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce39a7573fc5d23b0ecb7a2dc95f9c6c6ea441c6712f6c192b2807e2aa72feb`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 461.1 KB (461075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a004190bbed69b91ab59eecc4bae57cc79121a7270f8514b91ea2bf15bf2cda`  
		Last Modified: Thu, 04 Jan 2024 21:13:56 GMT  
		Size: 328.8 MB (328828687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a25661ed080ac4a8f0b6dd56469807de2349b4145a20054ab45d64c0ffcf7`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d4d5fc55e77dc509d870870a9e8355c28395230b6907e1232233ff8b725bf4`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c84fbbceb0fdda9313add328741ff6389a1e2062d6b507fda9605508dfe5967`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41fb138585cd23cc7320050f622bae87d765251c31d5d046088051c512df898`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:7fe7fe925fab08ac8ef939ca19bba24340b8163a26807cda0e12d23be1ef0a58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613189453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073370c528f7a6b6e027696d4d13f6c57d45bc4e7087d70b699d1748855d9c76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:18:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 11:18:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 11:18:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 11:18:23 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:22:08 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:22:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:22:30 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:22:30 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 20:39:57 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 20:39:58 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 20:43:11 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 20:43:29 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 20:43:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 20:43:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 20:43:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 20:43:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 20:43:32 GMT
USER odoo
# Thu, 04 Jan 2024 20:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 20:43:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc829e9bac0988cf5b8041cc64556998568034e96cd72e93b700c2ac4d3f6330`  
		Last Modified: Sat, 16 Dec 2023 11:26:30 GMT  
		Size: 243.3 MB (243296411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77915009472ee87b9142650dd27d791d648dc1cb35fd84a5b5e471802c2476ab`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b76a07b6810b56620d5e557ab7a8e64c61a46a1af3a1452dc22677cd585e67`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 461.2 KB (461168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280397ddd60459cc8aaccada3a3e2dbaee17a792d80e29704706d28e00631371`  
		Last Modified: Thu, 04 Jan 2024 20:47:38 GMT  
		Size: 331.0 MB (330970863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3cb092fd02e8e0e54aa4e1cb3f55d5bc88ab2bcb659ddfd3d4bdf082963733`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1423ad8516811b7707b8770003a0e47af59b799e3d4120a56dfb3376fd77bf`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d518f7ee4905a3980f6fc47020d7368b1a206e8f39e19eb220a69035123545b3`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b109be03f47c8824d4ede96171b9dc3bf26949515e105f259ca6242e8dcb29a`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:463baaa507dc8b6d62486dfd34589e6014f8f2735927b7c205ef42d83b563443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:cb62da0aaea917a6ef53e457e4b4113da46b60fc95d06e72f946d75f1f1eaaad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596401656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e2a8d99256a928d6c814584cf9c97901b623a06b113a8a21ba7c376e544fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:29:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 09:29:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 09:29:57 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 09:29:57 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 09:32:06 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 09:32:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:32:18 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 09:32:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 21:05:22 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:05:22 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 21:07:19 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:07:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:07:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:07:25 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:07:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:07:25 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:07:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:07:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:07:25 GMT
USER odoo
# Thu, 04 Jan 2024 21:07:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:07:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89681bc3d92fa58300c17f37a8c00221342b77325e00deb20e71ea410071d500`  
		Last Modified: Sat, 16 Dec 2023 09:34:46 GMT  
		Size: 233.7 MB (233730172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a3dc4306b241f9806eface9e5fe3c10ef771e41f03509a141414da8bb7c04`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 2.5 MB (2526485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746699b2b8c3aebf90f574a4692f492e2e617506c92d7a00874d79e4fddaf014`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b649d1972addc355aeac03251b960480b383859922d709ccbd2fc91e93cfd`  
		Last Modified: Thu, 04 Jan 2024 21:11:20 GMT  
		Size: 329.2 MB (329234819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f962cb53e5d611aea7cd0af144701cc13a08a2e8b7e07000234144678d8e8c`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaa5efbac844aae50891ecb81a4d2164862e1d5af3ae1d3b4fd79e5f204332b`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85107f9250c2e57e424d2cac941f24ccaecd2155bb9fa0468f5a82b5fa253e`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c259e9b1973dfcb04ef1ce9d24cec72aac2b6f600139f6ac1d82d95028d4b5a8`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1fb6c38ec3cb38c387c2af50c5dbe74c32c67af4a1182dff9005c93c74cf1f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591320520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06002113d5d47f707538c2065c32bb2e5d5c9476daf414b5e04b6a64e6ddd55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:59:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 10:59:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 10:59:32 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 10:59:32 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:01:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:02:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:02:09 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:02:09 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 21:09:18 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:09:18 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 21:11:28 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:11:30 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:11:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:11:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:11:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:11:31 GMT
USER odoo
# Thu, 04 Jan 2024 21:11:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:11:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed064f4459a4f1ab48040e16f6b55972797bd014de0d33737d676d7a1a25db4`  
		Last Modified: Sat, 16 Dec 2023 11:04:40 GMT  
		Size: 231.1 MB (231107542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217c6a3bbcbbb21c659f79f47bd7f96d743d57cfd0fe0b1678b81f7ff769a77`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 2.5 MB (2520464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce39a7573fc5d23b0ecb7a2dc95f9c6c6ea441c6712f6c192b2807e2aa72feb`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 461.1 KB (461075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a004190bbed69b91ab59eecc4bae57cc79121a7270f8514b91ea2bf15bf2cda`  
		Last Modified: Thu, 04 Jan 2024 21:13:56 GMT  
		Size: 328.8 MB (328828687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a25661ed080ac4a8f0b6dd56469807de2349b4145a20054ab45d64c0ffcf7`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d4d5fc55e77dc509d870870a9e8355c28395230b6907e1232233ff8b725bf4`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c84fbbceb0fdda9313add328741ff6389a1e2062d6b507fda9605508dfe5967`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41fb138585cd23cc7320050f622bae87d765251c31d5d046088051c512df898`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:7fe7fe925fab08ac8ef939ca19bba24340b8163a26807cda0e12d23be1ef0a58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613189453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073370c528f7a6b6e027696d4d13f6c57d45bc4e7087d70b699d1748855d9c76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:18:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 11:18:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 11:18:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 11:18:23 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:22:08 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:22:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:22:30 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:22:30 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 20:39:57 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 20:39:58 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 20:43:11 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 20:43:29 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 20:43:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 20:43:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 20:43:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 20:43:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 20:43:32 GMT
USER odoo
# Thu, 04 Jan 2024 20:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 20:43:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc829e9bac0988cf5b8041cc64556998568034e96cd72e93b700c2ac4d3f6330`  
		Last Modified: Sat, 16 Dec 2023 11:26:30 GMT  
		Size: 243.3 MB (243296411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77915009472ee87b9142650dd27d791d648dc1cb35fd84a5b5e471802c2476ab`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b76a07b6810b56620d5e557ab7a8e64c61a46a1af3a1452dc22677cd585e67`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 461.2 KB (461168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280397ddd60459cc8aaccada3a3e2dbaee17a792d80e29704706d28e00631371`  
		Last Modified: Thu, 04 Jan 2024 20:47:38 GMT  
		Size: 331.0 MB (330970863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3cb092fd02e8e0e54aa4e1cb3f55d5bc88ab2bcb659ddfd3d4bdf082963733`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1423ad8516811b7707b8770003a0e47af59b799e3d4120a56dfb3376fd77bf`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d518f7ee4905a3980f6fc47020d7368b1a206e8f39e19eb220a69035123545b3`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b109be03f47c8824d4ede96171b9dc3bf26949515e105f259ca6242e8dcb29a`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:463baaa507dc8b6d62486dfd34589e6014f8f2735927b7c205ef42d83b563443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:cb62da0aaea917a6ef53e457e4b4113da46b60fc95d06e72f946d75f1f1eaaad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596401656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e2a8d99256a928d6c814584cf9c97901b623a06b113a8a21ba7c376e544fed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:29:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 09:29:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 09:29:57 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 09:29:57 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 09:32:06 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 09:32:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:32:18 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 09:32:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 21:05:22 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:05:22 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 21:07:19 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:07:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:07:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:07:25 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:07:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:07:25 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:07:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:07:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:07:25 GMT
USER odoo
# Thu, 04 Jan 2024 21:07:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:07:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89681bc3d92fa58300c17f37a8c00221342b77325e00deb20e71ea410071d500`  
		Last Modified: Sat, 16 Dec 2023 09:34:46 GMT  
		Size: 233.7 MB (233730172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a3dc4306b241f9806eface9e5fe3c10ef771e41f03509a141414da8bb7c04`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 2.5 MB (2526485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746699b2b8c3aebf90f574a4692f492e2e617506c92d7a00874d79e4fddaf014`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59b649d1972addc355aeac03251b960480b383859922d709ccbd2fc91e93cfd`  
		Last Modified: Thu, 04 Jan 2024 21:11:20 GMT  
		Size: 329.2 MB (329234819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f962cb53e5d611aea7cd0af144701cc13a08a2e8b7e07000234144678d8e8c`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaa5efbac844aae50891ecb81a4d2164862e1d5af3ae1d3b4fd79e5f204332b`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e85107f9250c2e57e424d2cac941f24ccaecd2155bb9fa0468f5a82b5fa253e`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c259e9b1973dfcb04ef1ce9d24cec72aac2b6f600139f6ac1d82d95028d4b5a8`  
		Last Modified: Thu, 04 Jan 2024 21:10:42 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1fb6c38ec3cb38c387c2af50c5dbe74c32c67af4a1182dff9005c93c74cf1f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591320520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06002113d5d47f707538c2065c32bb2e5d5c9476daf414b5e04b6a64e6ddd55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:59:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 10:59:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 10:59:32 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 10:59:32 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:01:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:02:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:02:09 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:02:09 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 21:09:18 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 21:09:18 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 21:11:28 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 21:11:30 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 21:11:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 21:11:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 21:11:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 21:11:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 21:11:31 GMT
USER odoo
# Thu, 04 Jan 2024 21:11:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 21:11:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed064f4459a4f1ab48040e16f6b55972797bd014de0d33737d676d7a1a25db4`  
		Last Modified: Sat, 16 Dec 2023 11:04:40 GMT  
		Size: 231.1 MB (231107542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217c6a3bbcbbb21c659f79f47bd7f96d743d57cfd0fe0b1678b81f7ff769a77`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 2.5 MB (2520464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce39a7573fc5d23b0ecb7a2dc95f9c6c6ea441c6712f6c192b2807e2aa72feb`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 461.1 KB (461075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a004190bbed69b91ab59eecc4bae57cc79121a7270f8514b91ea2bf15bf2cda`  
		Last Modified: Thu, 04 Jan 2024 21:13:56 GMT  
		Size: 328.8 MB (328828687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196a25661ed080ac4a8f0b6dd56469807de2349b4145a20054ab45d64c0ffcf7`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d4d5fc55e77dc509d870870a9e8355c28395230b6907e1232233ff8b725bf4`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c84fbbceb0fdda9313add328741ff6389a1e2062d6b507fda9605508dfe5967`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41fb138585cd23cc7320050f622bae87d765251c31d5d046088051c512df898`  
		Last Modified: Thu, 04 Jan 2024 21:13:26 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:7fe7fe925fab08ac8ef939ca19bba24340b8163a26807cda0e12d23be1ef0a58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613189453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073370c528f7a6b6e027696d4d13f6c57d45bc4e7087d70b699d1748855d9c76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:18:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 11:18:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 11:18:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 11:18:23 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:22:08 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:22:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:22:30 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:22:30 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 20:39:57 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 20:39:58 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 20:43:11 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 20:43:29 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 20:43:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 20:43:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 20:43:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 20:43:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 20:43:32 GMT
USER odoo
# Thu, 04 Jan 2024 20:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 20:43:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc829e9bac0988cf5b8041cc64556998568034e96cd72e93b700c2ac4d3f6330`  
		Last Modified: Sat, 16 Dec 2023 11:26:30 GMT  
		Size: 243.3 MB (243296411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77915009472ee87b9142650dd27d791d648dc1cb35fd84a5b5e471802c2476ab`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b76a07b6810b56620d5e557ab7a8e64c61a46a1af3a1452dc22677cd585e67`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 461.2 KB (461168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280397ddd60459cc8aaccada3a3e2dbaee17a792d80e29704706d28e00631371`  
		Last Modified: Thu, 04 Jan 2024 20:47:38 GMT  
		Size: 331.0 MB (330970863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3cb092fd02e8e0e54aa4e1cb3f55d5bc88ab2bcb659ddfd3d4bdf082963733`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1423ad8516811b7707b8770003a0e47af59b799e3d4120a56dfb3376fd77bf`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d518f7ee4905a3980f6fc47020d7368b1a206e8f39e19eb220a69035123545b3`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b109be03f47c8824d4ede96171b9dc3bf26949515e105f259ca6242e8dcb29a`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
