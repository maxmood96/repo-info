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
$ docker pull odoo@sha256:67050fdf8b20d75dd38dfca1a8d081f8ba5ae16e3f4b652cbbc7a5fcdf22b6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:982d3871f201ee1efef8767652ab17778d48d3bd03335f23a144d6d53ca15999
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563327397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e67d629c108404a3ddd86fc2b00cc0740e66f70def4819b13af56b59853eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:26:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:26:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:26:52 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:26:52 GMT
ENV ODOO_VERSION=15.0
# Tue, 16 Jan 2024 18:39:15 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:39:15 GMT
ARG ODOO_SHA=40649ca80d22575f9a2714f1bc7a9f1e849b7523
# Tue, 16 Jan 2024 18:40:31 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=40649ca80d22575f9a2714f1bc7a9f1e849b7523
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:40:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:40:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:40:35 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=40649ca80d22575f9a2714f1bc7a9f1e849b7523
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:40:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:40:36 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:40:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:40:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:40:36 GMT
USER odoo
# Tue, 16 Jan 2024 18:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a83c2ab42e477bbdeab88e23116d73788d2604ce89f63469bc9302abf2e18b`  
		Last Modified: Thu, 11 Jan 2024 04:29:38 GMT  
		Size: 220.3 MB (220297108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54740ee11b9fd73c810f20945af2e0b18c9b13581db15932f1f74f390bb71168`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 2.6 MB (2625737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fadd9b941961b874f97fbea1796d285ded2c1242c1c5cf5154539ea4ee5cd58`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 460.3 KB (460317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123e6a9085f518071eceef24fad1616fccda50e4845054894ed8d179e4cf4f4`  
		Last Modified: Tue, 16 Jan 2024 18:42:58 GMT  
		Size: 308.5 MB (308523820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6a2ba8d723e5d380ea3ce79cfe8bcebae7a5fd111502519c23c9d0b2f63ce`  
		Last Modified: Tue, 16 Jan 2024 18:42:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bcd992df75edb1bc7efd3929be97ea310bb2c137573390957fa18ddc9926dd`  
		Last Modified: Tue, 16 Jan 2024 18:42:25 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8f7ef9f0a17adb05962841120a0bc9e332a3f85a335befc8a142e124f713a`  
		Last Modified: Tue, 16 Jan 2024 18:42:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcee375ac9590a21bf9c5e416302411ff6dae012726d8d8eba6a9334a978c9df`  
		Last Modified: Tue, 16 Jan 2024 18:42:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:67050fdf8b20d75dd38dfca1a8d081f8ba5ae16e3f4b652cbbc7a5fcdf22b6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:982d3871f201ee1efef8767652ab17778d48d3bd03335f23a144d6d53ca15999
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563327397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e67d629c108404a3ddd86fc2b00cc0740e66f70def4819b13af56b59853eda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:26:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:26:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:26:52 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:26:52 GMT
ENV ODOO_VERSION=15.0
# Tue, 16 Jan 2024 18:39:15 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:39:15 GMT
ARG ODOO_SHA=40649ca80d22575f9a2714f1bc7a9f1e849b7523
# Tue, 16 Jan 2024 18:40:31 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=40649ca80d22575f9a2714f1bc7a9f1e849b7523
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:40:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:40:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:40:35 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=40649ca80d22575f9a2714f1bc7a9f1e849b7523
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:40:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:40:36 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:40:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:40:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:40:36 GMT
USER odoo
# Tue, 16 Jan 2024 18:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a83c2ab42e477bbdeab88e23116d73788d2604ce89f63469bc9302abf2e18b`  
		Last Modified: Thu, 11 Jan 2024 04:29:38 GMT  
		Size: 220.3 MB (220297108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54740ee11b9fd73c810f20945af2e0b18c9b13581db15932f1f74f390bb71168`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 2.6 MB (2625737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fadd9b941961b874f97fbea1796d285ded2c1242c1c5cf5154539ea4ee5cd58`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 460.3 KB (460317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d123e6a9085f518071eceef24fad1616fccda50e4845054894ed8d179e4cf4f4`  
		Last Modified: Tue, 16 Jan 2024 18:42:58 GMT  
		Size: 308.5 MB (308523820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd6a2ba8d723e5d380ea3ce79cfe8bcebae7a5fd111502519c23c9d0b2f63ce`  
		Last Modified: Tue, 16 Jan 2024 18:42:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bcd992df75edb1bc7efd3929be97ea310bb2c137573390957fa18ddc9926dd`  
		Last Modified: Tue, 16 Jan 2024 18:42:25 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8f7ef9f0a17adb05962841120a0bc9e332a3f85a335befc8a142e124f713a`  
		Last Modified: Tue, 16 Jan 2024 18:42:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcee375ac9590a21bf9c5e416302411ff6dae012726d8d8eba6a9334a978c9df`  
		Last Modified: Tue, 16 Jan 2024 18:42:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:974192e2fbcaf5cdad00a910fec0860f051aee1fa3dcc6edb1076d52316844dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:1df98166c0ef69b903529938c5cc917f79c75bcbc5685ae11ad2820989047bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577905224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d490df77692fd9f636d7b21d3db0b6b4d5367153ed0c816a2f5cabeec8a2a73c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:22:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 04:23:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:24:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:24:08 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:24:08 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Jan 2024 18:37:36 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:37:36 GMT
ARG ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
# Tue, 16 Jan 2024 18:39:01 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:39:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:39:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:39:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:39:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:39:05 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:39:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:39:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:39:05 GMT
USER odoo
# Tue, 16 Jan 2024 18:39:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86654a69bafa33531b4fcae19511db74ec083ee8a32a4e5f68400b666ea91d3`  
		Last Modified: Thu, 11 Jan 2024 04:28:50 GMT  
		Size: 219.6 MB (219605557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ade87532781cb4a4f46880be8dc7fdde9c138904bb8d31a486c98f76224e59b`  
		Last Modified: Thu, 11 Jan 2024 04:28:26 GMT  
		Size: 2.6 MB (2629862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d092994f2bb47b54ec61d78cd536111b7c2aed38ff9c54d904acfa556f832abe`  
		Last Modified: Thu, 11 Jan 2024 04:28:25 GMT  
		Size: 460.4 KB (460351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100f3437aeb34542f64e7d085e319370d14e23838ba78445cd5d2c25a0b1465f`  
		Last Modified: Tue, 16 Jan 2024 18:42:15 GMT  
		Size: 323.8 MB (323789040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ae83c5eb1c2d832b72d89125bf41e81064bafe881cc87e68b18e355b3d2e93`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5693bde1d6490ccc0e11cc85c3876190e52eb6887f694acb988eb5226837768`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cac09f53e84bbd72256ac9f0c24f5dbda6621e6b337cf1c335c5800af3a5ef5`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc3cd7172beaa2c0a0e732ff09d742a66dde9d8abb465c54cef02e0d36dc46e`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2e6ac036bfa3982414e1a0243a3be4a121650e4fff35492a8a37fd1da9aca5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.5 MB (573465442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5749d34b919bbd037bc335b42c4d34e84d78602d7c2e50a4d1f64c445845a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:32:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 06:32:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 06:32:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 06:32:19 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 06:33:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 06:33:33 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:33:34 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 06:33:34 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Jan 2024 18:43:52 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:43:52 GMT
ARG ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
# Tue, 16 Jan 2024 18:45:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:45:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:45:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:45:13 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:45:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:45:13 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:45:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:45:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:45:13 GMT
USER odoo
# Tue, 16 Jan 2024 18:45:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:45:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843638cd2bb45ed1fac36d25687a35e96bac688f9925d94266efe7a01b02dbc2`  
		Last Modified: Thu, 11 Jan 2024 06:35:43 GMT  
		Size: 216.9 MB (216908953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ecca8e8834b331b36f9b4440b200f5387f9e128237d075371a1088530fe7b2`  
		Last Modified: Thu, 11 Jan 2024 06:35:23 GMT  
		Size: 2.6 MB (2634821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ce5b97e9a663db05af8bf4aac7112926f555fdc5b3f95caede4a11d02a935d`  
		Last Modified: Thu, 11 Jan 2024 06:35:22 GMT  
		Size: 460.3 KB (460316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429337b49b7fbf49899c27520c61b63bf29e792f14796db2abe1b56fd86b14b`  
		Last Modified: Tue, 16 Jan 2024 18:46:58 GMT  
		Size: 323.4 MB (323394877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332654ed93f90d9401125c4bb7c878aba858cb7560ceab0c430b971efc84ca20`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6b9df0018a595c8e216bfcd577cf89edd884c84118448a1e04006e706feda5`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d23efc6efef627742735df53c93a9104a53810b8a3ebf4c92eb5932d2e95a05`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445a213319ab101835ce5d7ac580aa3c3582ec2bb3b11308915d117ab46098a3`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:63cd685b642ed3db3b8566c3a4d8acbc16a325fec855941779262391138b3a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.4 MB (592417463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928b3e0d462e95d25b5b8bfca3ca15145067ad44f2c8a8a102bb7e374fab7184`
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
# Tue, 16 Jan 2024 21:10:47 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 21:10:47 GMT
ARG ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
# Tue, 16 Jan 2024 21:13:04 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 21:13:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 21:13:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 21:13:23 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 21:13:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 21:13:25 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 21:13:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 21:13:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 21:13:28 GMT
USER odoo
# Tue, 16 Jan 2024 21:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 21:13:29 GMT
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
	-	`sha256:7a5de735002f0b8b9346226cc209ab2def0826552ac6daac7107956a599943a9`  
		Last Modified: Tue, 16 Jan 2024 21:15:32 GMT  
		Size: 325.2 MB (325184041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c906e54f027af7d00e2710733293c604b43f601bf7bff77baf5ddde99f1d4a11`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e6d19ca3e05b68657957012a59324a8e9724bbc25923cf20ecc2968639365`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b965f0da8e67368e1ccfdb6c506efa022d5a8375f41375ecb792383a85cc94`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acd80ddd5e968abd44c5ef300d4480b6c9c6be82357a002e3edb02bebe85dad`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:974192e2fbcaf5cdad00a910fec0860f051aee1fa3dcc6edb1076d52316844dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:1df98166c0ef69b903529938c5cc917f79c75bcbc5685ae11ad2820989047bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577905224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d490df77692fd9f636d7b21d3db0b6b4d5367153ed0c816a2f5cabeec8a2a73c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:22:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 04:23:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:24:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:24:08 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:24:08 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Jan 2024 18:37:36 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:37:36 GMT
ARG ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
# Tue, 16 Jan 2024 18:39:01 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:39:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:39:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:39:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:39:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:39:05 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:39:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:39:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:39:05 GMT
USER odoo
# Tue, 16 Jan 2024 18:39:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:39:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86654a69bafa33531b4fcae19511db74ec083ee8a32a4e5f68400b666ea91d3`  
		Last Modified: Thu, 11 Jan 2024 04:28:50 GMT  
		Size: 219.6 MB (219605557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ade87532781cb4a4f46880be8dc7fdde9c138904bb8d31a486c98f76224e59b`  
		Last Modified: Thu, 11 Jan 2024 04:28:26 GMT  
		Size: 2.6 MB (2629862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d092994f2bb47b54ec61d78cd536111b7c2aed38ff9c54d904acfa556f832abe`  
		Last Modified: Thu, 11 Jan 2024 04:28:25 GMT  
		Size: 460.4 KB (460351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100f3437aeb34542f64e7d085e319370d14e23838ba78445cd5d2c25a0b1465f`  
		Last Modified: Tue, 16 Jan 2024 18:42:15 GMT  
		Size: 323.8 MB (323789040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ae83c5eb1c2d832b72d89125bf41e81064bafe881cc87e68b18e355b3d2e93`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5693bde1d6490ccc0e11cc85c3876190e52eb6887f694acb988eb5226837768`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cac09f53e84bbd72256ac9f0c24f5dbda6621e6b337cf1c335c5800af3a5ef5`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc3cd7172beaa2c0a0e732ff09d742a66dde9d8abb465c54cef02e0d36dc46e`  
		Last Modified: Tue, 16 Jan 2024 18:41:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2e6ac036bfa3982414e1a0243a3be4a121650e4fff35492a8a37fd1da9aca5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.5 MB (573465442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5749d34b919bbd037bc335b42c4d34e84d78602d7c2e50a4d1f64c445845a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:32:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 06:32:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 06:32:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 06:32:19 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 06:33:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 06:33:33 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:33:34 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 06:33:34 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Jan 2024 18:43:52 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:43:52 GMT
ARG ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
# Tue, 16 Jan 2024 18:45:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:45:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:45:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:45:13 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:45:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:45:13 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:45:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:45:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:45:13 GMT
USER odoo
# Tue, 16 Jan 2024 18:45:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:45:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843638cd2bb45ed1fac36d25687a35e96bac688f9925d94266efe7a01b02dbc2`  
		Last Modified: Thu, 11 Jan 2024 06:35:43 GMT  
		Size: 216.9 MB (216908953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ecca8e8834b331b36f9b4440b200f5387f9e128237d075371a1088530fe7b2`  
		Last Modified: Thu, 11 Jan 2024 06:35:23 GMT  
		Size: 2.6 MB (2634821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ce5b97e9a663db05af8bf4aac7112926f555fdc5b3f95caede4a11d02a935d`  
		Last Modified: Thu, 11 Jan 2024 06:35:22 GMT  
		Size: 460.3 KB (460316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0429337b49b7fbf49899c27520c61b63bf29e792f14796db2abe1b56fd86b14b`  
		Last Modified: Tue, 16 Jan 2024 18:46:58 GMT  
		Size: 323.4 MB (323394877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332654ed93f90d9401125c4bb7c878aba858cb7560ceab0c430b971efc84ca20`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6b9df0018a595c8e216bfcd577cf89edd884c84118448a1e04006e706feda5`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d23efc6efef627742735df53c93a9104a53810b8a3ebf4c92eb5932d2e95a05`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445a213319ab101835ce5d7ac580aa3c3582ec2bb3b11308915d117ab46098a3`  
		Last Modified: Tue, 16 Jan 2024 18:46:29 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:63cd685b642ed3db3b8566c3a4d8acbc16a325fec855941779262391138b3a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.4 MB (592417463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928b3e0d462e95d25b5b8bfca3ca15145067ad44f2c8a8a102bb7e374fab7184`
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
# Tue, 16 Jan 2024 21:10:47 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 21:10:47 GMT
ARG ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
# Tue, 16 Jan 2024 21:13:04 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 21:13:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 21:13:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 21:13:23 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9a0630da934549f3e514ae2b75c24351b99a2300
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 21:13:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 21:13:25 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 21:13:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 21:13:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 21:13:28 GMT
USER odoo
# Tue, 16 Jan 2024 21:13:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 21:13:29 GMT
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
	-	`sha256:7a5de735002f0b8b9346226cc209ab2def0826552ac6daac7107956a599943a9`  
		Last Modified: Tue, 16 Jan 2024 21:15:32 GMT  
		Size: 325.2 MB (325184041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c906e54f027af7d00e2710733293c604b43f601bf7bff77baf5ddde99f1d4a11`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e6d19ca3e05b68657957012a59324a8e9724bbc25923cf20ecc2968639365`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b965f0da8e67368e1ccfdb6c506efa022d5a8375f41375ecb792383a85cc94`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acd80ddd5e968abd44c5ef300d4480b6c9c6be82357a002e3edb02bebe85dad`  
		Last Modified: Tue, 16 Jan 2024 21:14:47 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:cedd12e5ee13c7bdc8591735098d083e9dadc88e6bbf49c2f95f2394f6fb4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:f53d796cbc5c47e4a0521fa608339a296d702a2343729434333451059b1241d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596444727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a27fdb4c82a344205d6e4de1ccb831ca53d14c716da171642be05f070187c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:11:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:11:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:11:12 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:13:00 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:13:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:13:13 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:13:13 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:15:00 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:15:04 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:15:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:15:04 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:15:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:15:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:15:05 GMT
USER odoo
# Wed, 17 Jan 2024 08:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:15:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a19db281065cfaaff50a903f954cd8cd0ab77efd9751ee9c2bd36ef33cd941`  
		Last Modified: Wed, 17 Jan 2024 08:16:00 GMT  
		Size: 233.7 MB (233730319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498266485268b12f1ed92ca683caf8de575184ea4c681cb8b806a9f9d4d7bd9`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 2.5 MB (2526563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692263bc03dc29d26ef3660e4aa016c65b762f3ef32bc7f072ef5fd882b670ff`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65258011f7d95bc5c6666ff8b962a40af90eced980825c3fb9e8e1c3b2745265`  
		Last Modified: Wed, 17 Jan 2024 08:16:10 GMT  
		Size: 329.3 MB (329276798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebb976892adf6ad32a733852a334284401fba552da4b4bbc85fd6ae234e67c3`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce93c83bae47703bebe7594c6628caf21477aec318f388692bfa6a858fea849`  
		Last Modified: Wed, 17 Jan 2024 08:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df82699b4af6ed000dea119fba0cd353c552b1b3eab89193b41cba2f75d4d7`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7624844c3f8dd7be7303cd388326c370239754d6b1f700b005871f7127685`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f93ea522fb7d417657956707f082054e12456dd689b9d9d9a2d22a5a33c66a45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591381814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893d324f528244ba33334492efe7c97cd54996716de48d2fb51890d941c1318`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:43:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 07:43:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 07:43:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 07:43:08 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 07:45:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 07:45:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:45:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 07:45:29 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 07:47:17 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 07:47:25 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 07:47:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 07:47:25 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 07:47:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 07:47:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 07:47:25 GMT
USER odoo
# Wed, 17 Jan 2024 07:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 07:47:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b02358e221961189c89c25333bfd0ef1760807bc50d71f914a02039d400a50`  
		Last Modified: Wed, 17 Jan 2024 07:48:02 GMT  
		Size: 231.1 MB (231110379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e38938c1ef4955deb704dcf4973073668ce7eff75a9034b6a7ea8d7a4d458`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 2.5 MB (2519326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e6bddb24b8b00fae6832e4428a94c80b5a6b8ff0e710477bed35dcb3ef4565`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 461.4 KB (461390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce00313e2b01b8c4fa486aa894e7cf16f9256dfdc0cdb3f682e1633b60243c35`  
		Last Modified: Wed, 17 Jan 2024 07:48:08 GMT  
		Size: 328.9 MB (328888639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32acc1437d8329f75c61fbfc9f603dd3f19c2e56c219c015c38d02dbcf39b9`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970a9c4b96fe43a59e8d6a22ee80e126cc78a763ae635a80dc9829801c152dd6`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab67f1b70a5388d5e9a34c0920854bcdfd3dfa7f2d9a2d2523f971755dad42`  
		Last Modified: Wed, 17 Jan 2024 07:47:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85acac7286096ee325dc43e633e96f6034f6fb3251f948ae1ffab896c474960`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:599f5987c233ee7ccb129cc9e3d131e8419a506d99309b169d7d99e8619510bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613241916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba4b7f923dbb6ea7ce06e12639aa0d1453ae0a44e65b2bd8ee5366fe85852a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:00:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:00:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:00:33 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:05:34 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:05:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:01 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:06:01 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 08:06:02 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:06:03 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:09:42 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:10:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:10:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:10:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:10:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:10:09 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:10:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:10:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:10:12 GMT
USER odoo
# Wed, 17 Jan 2024 08:10:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:10:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcb20763fdcfb23eafb90744955b7c8403e4c9f4e0eb528e5e52f5966a7fbd`  
		Last Modified: Wed, 17 Jan 2024 08:11:11 GMT  
		Size: 243.3 MB (243285415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb20cbe165f4e4451478c82ca6213daeab6f98bea1bcaa439eb5e081dfd17d`  
		Last Modified: Wed, 17 Jan 2024 08:10:38 GMT  
		Size: 2.8 MB (2803440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0410b6743b107a0ae4ccbab9d310eacd59731c7b95cf9a6504fed01785d284`  
		Last Modified: Wed, 17 Jan 2024 08:10:37 GMT  
		Size: 461.4 KB (461416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fe56ab53c64fbdf9020abe3e89235aa40ed426c26ed0ed8165f08ff03400f9`  
		Last Modified: Wed, 17 Jan 2024 08:11:21 GMT  
		Size: 331.0 MB (331032028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60795f77f852574e13f4810508b00822403d952c6eb71aaa35dc1d7dbeda87ab`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09571254666376b6590d9a901532820a2d9a778e069216a1d55522178e2387a`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a408b5878f9af846a86a508843791fa9a33902a2fbbe7f8b8c1402fd3b8e98`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e2fc9c7139428c40f7d6ae7c4253fc7b268be29493c4735f868667201ed64`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cedd12e5ee13c7bdc8591735098d083e9dadc88e6bbf49c2f95f2394f6fb4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:f53d796cbc5c47e4a0521fa608339a296d702a2343729434333451059b1241d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596444727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a27fdb4c82a344205d6e4de1ccb831ca53d14c716da171642be05f070187c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:11:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:11:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:11:12 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:13:00 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:13:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:13:13 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:13:13 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:15:00 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:15:04 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:15:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:15:04 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:15:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:15:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:15:05 GMT
USER odoo
# Wed, 17 Jan 2024 08:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:15:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a19db281065cfaaff50a903f954cd8cd0ab77efd9751ee9c2bd36ef33cd941`  
		Last Modified: Wed, 17 Jan 2024 08:16:00 GMT  
		Size: 233.7 MB (233730319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498266485268b12f1ed92ca683caf8de575184ea4c681cb8b806a9f9d4d7bd9`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 2.5 MB (2526563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692263bc03dc29d26ef3660e4aa016c65b762f3ef32bc7f072ef5fd882b670ff`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65258011f7d95bc5c6666ff8b962a40af90eced980825c3fb9e8e1c3b2745265`  
		Last Modified: Wed, 17 Jan 2024 08:16:10 GMT  
		Size: 329.3 MB (329276798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebb976892adf6ad32a733852a334284401fba552da4b4bbc85fd6ae234e67c3`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce93c83bae47703bebe7594c6628caf21477aec318f388692bfa6a858fea849`  
		Last Modified: Wed, 17 Jan 2024 08:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df82699b4af6ed000dea119fba0cd353c552b1b3eab89193b41cba2f75d4d7`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7624844c3f8dd7be7303cd388326c370239754d6b1f700b005871f7127685`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f93ea522fb7d417657956707f082054e12456dd689b9d9d9a2d22a5a33c66a45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591381814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893d324f528244ba33334492efe7c97cd54996716de48d2fb51890d941c1318`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:43:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 07:43:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 07:43:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 07:43:08 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 07:45:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 07:45:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:45:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 07:45:29 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 07:47:17 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 07:47:25 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 07:47:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 07:47:25 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 07:47:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 07:47:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 07:47:25 GMT
USER odoo
# Wed, 17 Jan 2024 07:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 07:47:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b02358e221961189c89c25333bfd0ef1760807bc50d71f914a02039d400a50`  
		Last Modified: Wed, 17 Jan 2024 07:48:02 GMT  
		Size: 231.1 MB (231110379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e38938c1ef4955deb704dcf4973073668ce7eff75a9034b6a7ea8d7a4d458`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 2.5 MB (2519326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e6bddb24b8b00fae6832e4428a94c80b5a6b8ff0e710477bed35dcb3ef4565`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 461.4 KB (461390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce00313e2b01b8c4fa486aa894e7cf16f9256dfdc0cdb3f682e1633b60243c35`  
		Last Modified: Wed, 17 Jan 2024 07:48:08 GMT  
		Size: 328.9 MB (328888639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32acc1437d8329f75c61fbfc9f603dd3f19c2e56c219c015c38d02dbcf39b9`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970a9c4b96fe43a59e8d6a22ee80e126cc78a763ae635a80dc9829801c152dd6`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab67f1b70a5388d5e9a34c0920854bcdfd3dfa7f2d9a2d2523f971755dad42`  
		Last Modified: Wed, 17 Jan 2024 07:47:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85acac7286096ee325dc43e633e96f6034f6fb3251f948ae1ffab896c474960`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:599f5987c233ee7ccb129cc9e3d131e8419a506d99309b169d7d99e8619510bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613241916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba4b7f923dbb6ea7ce06e12639aa0d1453ae0a44e65b2bd8ee5366fe85852a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:00:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:00:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:00:33 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:05:34 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:05:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:01 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:06:01 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 08:06:02 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:06:03 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:09:42 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:10:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:10:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:10:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:10:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:10:09 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:10:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:10:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:10:12 GMT
USER odoo
# Wed, 17 Jan 2024 08:10:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:10:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcb20763fdcfb23eafb90744955b7c8403e4c9f4e0eb528e5e52f5966a7fbd`  
		Last Modified: Wed, 17 Jan 2024 08:11:11 GMT  
		Size: 243.3 MB (243285415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb20cbe165f4e4451478c82ca6213daeab6f98bea1bcaa439eb5e081dfd17d`  
		Last Modified: Wed, 17 Jan 2024 08:10:38 GMT  
		Size: 2.8 MB (2803440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0410b6743b107a0ae4ccbab9d310eacd59731c7b95cf9a6504fed01785d284`  
		Last Modified: Wed, 17 Jan 2024 08:10:37 GMT  
		Size: 461.4 KB (461416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fe56ab53c64fbdf9020abe3e89235aa40ed426c26ed0ed8165f08ff03400f9`  
		Last Modified: Wed, 17 Jan 2024 08:11:21 GMT  
		Size: 331.0 MB (331032028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60795f77f852574e13f4810508b00822403d952c6eb71aaa35dc1d7dbeda87ab`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09571254666376b6590d9a901532820a2d9a778e069216a1d55522178e2387a`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a408b5878f9af846a86a508843791fa9a33902a2fbbe7f8b8c1402fd3b8e98`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e2fc9c7139428c40f7d6ae7c4253fc7b268be29493c4735f868667201ed64`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:cedd12e5ee13c7bdc8591735098d083e9dadc88e6bbf49c2f95f2394f6fb4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f53d796cbc5c47e4a0521fa608339a296d702a2343729434333451059b1241d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596444727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a27fdb4c82a344205d6e4de1ccb831ca53d14c716da171642be05f070187c27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:11:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:11:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:11:12 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:13:00 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:13:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:13:13 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:13:13 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:15:00 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:15:04 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:15:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:15:04 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:15:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:15:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:15:05 GMT
USER odoo
# Wed, 17 Jan 2024 08:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:15:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a19db281065cfaaff50a903f954cd8cd0ab77efd9751ee9c2bd36ef33cd941`  
		Last Modified: Wed, 17 Jan 2024 08:16:00 GMT  
		Size: 233.7 MB (233730319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498266485268b12f1ed92ca683caf8de575184ea4c681cb8b806a9f9d4d7bd9`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 2.5 MB (2526563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692263bc03dc29d26ef3660e4aa016c65b762f3ef32bc7f072ef5fd882b670ff`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65258011f7d95bc5c6666ff8b962a40af90eced980825c3fb9e8e1c3b2745265`  
		Last Modified: Wed, 17 Jan 2024 08:16:10 GMT  
		Size: 329.3 MB (329276798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebb976892adf6ad32a733852a334284401fba552da4b4bbc85fd6ae234e67c3`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce93c83bae47703bebe7594c6628caf21477aec318f388692bfa6a858fea849`  
		Last Modified: Wed, 17 Jan 2024 08:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df82699b4af6ed000dea119fba0cd353c552b1b3eab89193b41cba2f75d4d7`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7624844c3f8dd7be7303cd388326c370239754d6b1f700b005871f7127685`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f93ea522fb7d417657956707f082054e12456dd689b9d9d9a2d22a5a33c66a45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591381814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893d324f528244ba33334492efe7c97cd54996716de48d2fb51890d941c1318`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:43:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 07:43:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 07:43:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 07:43:08 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 07:45:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 07:45:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:45:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 07:45:29 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 07:47:17 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 07:47:25 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 07:47:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 07:47:25 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 07:47:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 07:47:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 07:47:25 GMT
USER odoo
# Wed, 17 Jan 2024 07:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 07:47:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b02358e221961189c89c25333bfd0ef1760807bc50d71f914a02039d400a50`  
		Last Modified: Wed, 17 Jan 2024 07:48:02 GMT  
		Size: 231.1 MB (231110379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e38938c1ef4955deb704dcf4973073668ce7eff75a9034b6a7ea8d7a4d458`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 2.5 MB (2519326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e6bddb24b8b00fae6832e4428a94c80b5a6b8ff0e710477bed35dcb3ef4565`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 461.4 KB (461390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce00313e2b01b8c4fa486aa894e7cf16f9256dfdc0cdb3f682e1633b60243c35`  
		Last Modified: Wed, 17 Jan 2024 07:48:08 GMT  
		Size: 328.9 MB (328888639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32acc1437d8329f75c61fbfc9f603dd3f19c2e56c219c015c38d02dbcf39b9`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970a9c4b96fe43a59e8d6a22ee80e126cc78a763ae635a80dc9829801c152dd6`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab67f1b70a5388d5e9a34c0920854bcdfd3dfa7f2d9a2d2523f971755dad42`  
		Last Modified: Wed, 17 Jan 2024 07:47:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85acac7286096ee325dc43e633e96f6034f6fb3251f948ae1ffab896c474960`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:599f5987c233ee7ccb129cc9e3d131e8419a506d99309b169d7d99e8619510bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613241916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba4b7f923dbb6ea7ce06e12639aa0d1453ae0a44e65b2bd8ee5366fe85852a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:00:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:00:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:00:33 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:05:34 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:05:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:01 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:06:01 GMT
ENV ODOO_VERSION=17.0
# Wed, 17 Jan 2024 08:06:02 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:06:03 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:09:42 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:10:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:10:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:10:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:10:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:10:09 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:10:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:10:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:10:12 GMT
USER odoo
# Wed, 17 Jan 2024 08:10:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:10:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcb20763fdcfb23eafb90744955b7c8403e4c9f4e0eb528e5e52f5966a7fbd`  
		Last Modified: Wed, 17 Jan 2024 08:11:11 GMT  
		Size: 243.3 MB (243285415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb20cbe165f4e4451478c82ca6213daeab6f98bea1bcaa439eb5e081dfd17d`  
		Last Modified: Wed, 17 Jan 2024 08:10:38 GMT  
		Size: 2.8 MB (2803440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0410b6743b107a0ae4ccbab9d310eacd59731c7b95cf9a6504fed01785d284`  
		Last Modified: Wed, 17 Jan 2024 08:10:37 GMT  
		Size: 461.4 KB (461416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fe56ab53c64fbdf9020abe3e89235aa40ed426c26ed0ed8165f08ff03400f9`  
		Last Modified: Wed, 17 Jan 2024 08:11:21 GMT  
		Size: 331.0 MB (331032028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60795f77f852574e13f4810508b00822403d952c6eb71aaa35dc1d7dbeda87ab`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09571254666376b6590d9a901532820a2d9a778e069216a1d55522178e2387a`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a408b5878f9af846a86a508843791fa9a33902a2fbbe7f8b8c1402fd3b8e98`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e2fc9c7139428c40f7d6ae7c4253fc7b268be29493c4735f868667201ed64`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
