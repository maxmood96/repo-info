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
$ docker pull odoo@sha256:8204f4ec2e43fd7da356490d82bd09d7f8bac7ea01bae4d80d1086f4d0488a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:34686e2e2e11aa291eb19dd7fa5fecdb5e76ba0869795832bdaa015994c2cee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596442551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a770ff11013f1e31263ebc64e0c24bc364e128e63ea312a8bf42942223666f`
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
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:37:20 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:37:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:37:24 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:37:25 GMT
USER odoo
# Tue, 16 Jan 2024 18:37:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:37:25 GMT
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
	-	`sha256:ab9312bd794422cccecb264eb665eb9d60e8e07f9e5dcfd762cdae2858b581c5`  
		Last Modified: Tue, 16 Jan 2024 18:41:26 GMT  
		Size: 329.3 MB (329275713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040fa2098f3c95eef1cd85963e35c1be2cb1d7813579c8db848019ca444eb32`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff7d4d6049c2b3b10f5d2836254c47a75878be3b16dae7efb9fadad5623912e`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6813d9b0620ed15ec31190029d7ee73762ec76ebb99b55dafd4555b615d3e3`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036555d3f0b2644cc421f7dc5f1ff4c983d9c17572a8e630103390836f0f2bf`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fea3c2e90c2f105a4f3e7c5a5cb866d01f6f294a570fc16d5a6b6f15b3abb6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591382864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5c91da6daa2abf3f05f79f785ac6e846571b16b7ff4b7ff878adb26b9e1716`
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
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:43:38 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:43:40 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:43:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:43:40 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:43:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:43:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:43:40 GMT
USER odoo
# Tue, 16 Jan 2024 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:40 GMT
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
	-	`sha256:8365cc03105765cbac69f6af6ab40ee50e70f99e8588525212a99b3109015265`  
		Last Modified: Tue, 16 Jan 2024 18:46:17 GMT  
		Size: 328.9 MB (328891032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8bebed78a1ea93f549f2bdb8ddadcdfcc0677a47e0e34e55e3eb433035df28`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1bdd1ab1c23fc5f02c8030847ffdba019119c85ad58893912478aac4027a56`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e854652194f0c7ba3c4140b0a0b3cd58cf3485c4facf6905a0f1539a0d8834`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b474447fb3a94bcc6d563776c31968090b5d60b27f31f29e84474c3d39ca07b`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:dbbb6a3f62e4b67c8bab0acd0ad7b5e83da24825c526ca3200e7f8e1c4feecc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.3 MB (613250150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1d8fe7f80def916c8545cb2ac53ce433c46c7e3e492030f5a2acff148f909e`
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
# Tue, 16 Jan 2024 21:07:22 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 21:07:23 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 21:10:14 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 21:10:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 21:10:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 21:10:30 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 21:10:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 21:10:32 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 21:10:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 21:10:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 21:10:33 GMT
USER odoo
# Tue, 16 Jan 2024 21:10:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 21:10:34 GMT
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
	-	`sha256:bfa1555dfde4bf4b3fa68a1574a42c3f42b468ef38401820282c8dd1e147f0a3`  
		Last Modified: Tue, 16 Jan 2024 21:14:34 GMT  
		Size: 331.0 MB (331031560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff56bc61b6a894d8e3d560eb176836b9c8021ff29b06085121947191a090afc`  
		Last Modified: Tue, 16 Jan 2024 21:13:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5af465af33c5605a111edfcb218528610d52d9a0caafe6d23ec4975e4cc6c1f`  
		Last Modified: Tue, 16 Jan 2024 21:13:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49bafd893b86d6b0750536bd48314dcc8ba4064ee354386844ee0febbda13f`  
		Last Modified: Tue, 16 Jan 2024 21:13:49 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6aa6a8247f20bceff46f306f6c68bb5e19871395168d375fb5e4bc8e59d72b`  
		Last Modified: Tue, 16 Jan 2024 21:13:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:8204f4ec2e43fd7da356490d82bd09d7f8bac7ea01bae4d80d1086f4d0488a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:34686e2e2e11aa291eb19dd7fa5fecdb5e76ba0869795832bdaa015994c2cee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596442551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a770ff11013f1e31263ebc64e0c24bc364e128e63ea312a8bf42942223666f`
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
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:37:20 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:37:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:37:24 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:37:25 GMT
USER odoo
# Tue, 16 Jan 2024 18:37:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:37:25 GMT
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
	-	`sha256:ab9312bd794422cccecb264eb665eb9d60e8e07f9e5dcfd762cdae2858b581c5`  
		Last Modified: Tue, 16 Jan 2024 18:41:26 GMT  
		Size: 329.3 MB (329275713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040fa2098f3c95eef1cd85963e35c1be2cb1d7813579c8db848019ca444eb32`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff7d4d6049c2b3b10f5d2836254c47a75878be3b16dae7efb9fadad5623912e`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6813d9b0620ed15ec31190029d7ee73762ec76ebb99b55dafd4555b615d3e3`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036555d3f0b2644cc421f7dc5f1ff4c983d9c17572a8e630103390836f0f2bf`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fea3c2e90c2f105a4f3e7c5a5cb866d01f6f294a570fc16d5a6b6f15b3abb6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591382864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5c91da6daa2abf3f05f79f785ac6e846571b16b7ff4b7ff878adb26b9e1716`
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
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:43:38 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:43:40 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:43:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:43:40 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:43:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:43:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:43:40 GMT
USER odoo
# Tue, 16 Jan 2024 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:40 GMT
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
	-	`sha256:8365cc03105765cbac69f6af6ab40ee50e70f99e8588525212a99b3109015265`  
		Last Modified: Tue, 16 Jan 2024 18:46:17 GMT  
		Size: 328.9 MB (328891032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8bebed78a1ea93f549f2bdb8ddadcdfcc0677a47e0e34e55e3eb433035df28`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1bdd1ab1c23fc5f02c8030847ffdba019119c85ad58893912478aac4027a56`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e854652194f0c7ba3c4140b0a0b3cd58cf3485c4facf6905a0f1539a0d8834`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b474447fb3a94bcc6d563776c31968090b5d60b27f31f29e84474c3d39ca07b`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:dbbb6a3f62e4b67c8bab0acd0ad7b5e83da24825c526ca3200e7f8e1c4feecc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.3 MB (613250150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1d8fe7f80def916c8545cb2ac53ce433c46c7e3e492030f5a2acff148f909e`
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
# Tue, 16 Jan 2024 21:07:22 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 21:07:23 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 21:10:14 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 21:10:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 21:10:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 21:10:30 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 21:10:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 21:10:32 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 21:10:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 21:10:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 21:10:33 GMT
USER odoo
# Tue, 16 Jan 2024 21:10:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 21:10:34 GMT
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
	-	`sha256:bfa1555dfde4bf4b3fa68a1574a42c3f42b468ef38401820282c8dd1e147f0a3`  
		Last Modified: Tue, 16 Jan 2024 21:14:34 GMT  
		Size: 331.0 MB (331031560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff56bc61b6a894d8e3d560eb176836b9c8021ff29b06085121947191a090afc`  
		Last Modified: Tue, 16 Jan 2024 21:13:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5af465af33c5605a111edfcb218528610d52d9a0caafe6d23ec4975e4cc6c1f`  
		Last Modified: Tue, 16 Jan 2024 21:13:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49bafd893b86d6b0750536bd48314dcc8ba4064ee354386844ee0febbda13f`  
		Last Modified: Tue, 16 Jan 2024 21:13:49 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6aa6a8247f20bceff46f306f6c68bb5e19871395168d375fb5e4bc8e59d72b`  
		Last Modified: Tue, 16 Jan 2024 21:13:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:8204f4ec2e43fd7da356490d82bd09d7f8bac7ea01bae4d80d1086f4d0488a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:34686e2e2e11aa291eb19dd7fa5fecdb5e76ba0869795832bdaa015994c2cee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596442551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a770ff11013f1e31263ebc64e0c24bc364e128e63ea312a8bf42942223666f`
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
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:37:20 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:37:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:37:24 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:37:25 GMT
USER odoo
# Tue, 16 Jan 2024 18:37:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:37:25 GMT
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
	-	`sha256:ab9312bd794422cccecb264eb665eb9d60e8e07f9e5dcfd762cdae2858b581c5`  
		Last Modified: Tue, 16 Jan 2024 18:41:26 GMT  
		Size: 329.3 MB (329275713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040fa2098f3c95eef1cd85963e35c1be2cb1d7813579c8db848019ca444eb32`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff7d4d6049c2b3b10f5d2836254c47a75878be3b16dae7efb9fadad5623912e`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6813d9b0620ed15ec31190029d7ee73762ec76ebb99b55dafd4555b615d3e3`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036555d3f0b2644cc421f7dc5f1ff4c983d9c17572a8e630103390836f0f2bf`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fea3c2e90c2f105a4f3e7c5a5cb866d01f6f294a570fc16d5a6b6f15b3abb6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591382864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5c91da6daa2abf3f05f79f785ac6e846571b16b7ff4b7ff878adb26b9e1716`
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
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:43:38 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:43:40 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:43:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:43:40 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:43:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:43:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:43:40 GMT
USER odoo
# Tue, 16 Jan 2024 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:40 GMT
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
	-	`sha256:8365cc03105765cbac69f6af6ab40ee50e70f99e8588525212a99b3109015265`  
		Last Modified: Tue, 16 Jan 2024 18:46:17 GMT  
		Size: 328.9 MB (328891032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8bebed78a1ea93f549f2bdb8ddadcdfcc0677a47e0e34e55e3eb433035df28`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1bdd1ab1c23fc5f02c8030847ffdba019119c85ad58893912478aac4027a56`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e854652194f0c7ba3c4140b0a0b3cd58cf3485c4facf6905a0f1539a0d8834`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b474447fb3a94bcc6d563776c31968090b5d60b27f31f29e84474c3d39ca07b`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:dbbb6a3f62e4b67c8bab0acd0ad7b5e83da24825c526ca3200e7f8e1c4feecc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.3 MB (613250150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1d8fe7f80def916c8545cb2ac53ce433c46c7e3e492030f5a2acff148f909e`
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
# Tue, 16 Jan 2024 21:07:22 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 21:07:23 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 21:10:14 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 21:10:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 21:10:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 21:10:30 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 21:10:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 21:10:32 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 21:10:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 21:10:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 21:10:33 GMT
USER odoo
# Tue, 16 Jan 2024 21:10:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 21:10:34 GMT
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
	-	`sha256:bfa1555dfde4bf4b3fa68a1574a42c3f42b468ef38401820282c8dd1e147f0a3`  
		Last Modified: Tue, 16 Jan 2024 21:14:34 GMT  
		Size: 331.0 MB (331031560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff56bc61b6a894d8e3d560eb176836b9c8021ff29b06085121947191a090afc`  
		Last Modified: Tue, 16 Jan 2024 21:13:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5af465af33c5605a111edfcb218528610d52d9a0caafe6d23ec4975e4cc6c1f`  
		Last Modified: Tue, 16 Jan 2024 21:13:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49bafd893b86d6b0750536bd48314dcc8ba4064ee354386844ee0febbda13f`  
		Last Modified: Tue, 16 Jan 2024 21:13:49 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6aa6a8247f20bceff46f306f6c68bb5e19871395168d375fb5e4bc8e59d72b`  
		Last Modified: Tue, 16 Jan 2024 21:13:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
