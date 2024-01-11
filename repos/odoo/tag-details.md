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
$ docker pull odoo@sha256:b5a80bf7a957a30804dcdf9b450426984be38905459b6f75cd121eebfe8d18c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:24d7463086e88729f4a978e622cb483048609d236ace6e2ee7e8feea31e27dbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563264702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255b914c896c9962db3e953bd998fb77e1b22e5f6f9122810b8bcb3fc421ab96`
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
# Thu, 11 Jan 2024 04:26:53 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 04:26:53 GMT
ARG ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
# Thu, 11 Jan 2024 04:28:04 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 04:28:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 04:28:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 04:28:07 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 04:28:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 04:28:08 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 04:28:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 04:28:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 04:28:08 GMT
USER odoo
# Thu, 11 Jan 2024 04:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:28:08 GMT
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
	-	`sha256:96ffe09794afb2b58ce2489a8ee7126a3ae9b55b2bba59e2a94b1cc7efec49b9`  
		Last Modified: Thu, 11 Jan 2024 04:29:47 GMT  
		Size: 308.5 MB (308461125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ba06c7a7f093982943d19333a4fb0769da89e68842a9093ada1f85a23dbb4`  
		Last Modified: Thu, 11 Jan 2024 04:29:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0854725078b46fc1c31d4dd5483b0dcefe0a76b91057820c86731b8fc71ebf`  
		Last Modified: Thu, 11 Jan 2024 04:29:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609679d1710e98f13749de2665ae756ad879be3160c293f329e7f5df71662264`  
		Last Modified: Thu, 11 Jan 2024 04:29:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd806359e3e01d7a3b483401001c0e78f494575bd8ec3246679b494aa02dee60`  
		Last Modified: Thu, 11 Jan 2024 04:29:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:b5a80bf7a957a30804dcdf9b450426984be38905459b6f75cd121eebfe8d18c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:24d7463086e88729f4a978e622cb483048609d236ace6e2ee7e8feea31e27dbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563264702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255b914c896c9962db3e953bd998fb77e1b22e5f6f9122810b8bcb3fc421ab96`
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
# Thu, 11 Jan 2024 04:26:53 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 04:26:53 GMT
ARG ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
# Thu, 11 Jan 2024 04:28:04 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 04:28:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 04:28:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 04:28:07 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=af62378df9c727be6480f4cbc842fee621405f95
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 04:28:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 04:28:08 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 04:28:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 04:28:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 04:28:08 GMT
USER odoo
# Thu, 11 Jan 2024 04:28:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:28:08 GMT
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
	-	`sha256:96ffe09794afb2b58ce2489a8ee7126a3ae9b55b2bba59e2a94b1cc7efec49b9`  
		Last Modified: Thu, 11 Jan 2024 04:29:47 GMT  
		Size: 308.5 MB (308461125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ba06c7a7f093982943d19333a4fb0769da89e68842a9093ada1f85a23dbb4`  
		Last Modified: Thu, 11 Jan 2024 04:29:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0854725078b46fc1c31d4dd5483b0dcefe0a76b91057820c86731b8fc71ebf`  
		Last Modified: Thu, 11 Jan 2024 04:29:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609679d1710e98f13749de2665ae756ad879be3160c293f329e7f5df71662264`  
		Last Modified: Thu, 11 Jan 2024 04:29:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd806359e3e01d7a3b483401001c0e78f494575bd8ec3246679b494aa02dee60`  
		Last Modified: Thu, 11 Jan 2024 04:29:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:4d15e19d56dd57e9fe0cc6ca29152884676c47f44dc53145c0e178e1c5235f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:09910d07c80de270fd4cb64d573ed79403eb2b9f32784e02cb91016be80b8f98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.8 MB (577758675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea3df020b4b5bef69b33a820da4817fdc546aec1b36b417d5fe8235b443bfe4`
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
# Thu, 11 Jan 2024 04:24:08 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 04:24:08 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 11 Jan 2024 04:25:29 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 04:25:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 04:25:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 04:25:34 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 04:25:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 04:25:35 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 04:25:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 04:25:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 04:25:35 GMT
USER odoo
# Thu, 11 Jan 2024 04:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:25:35 GMT
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
	-	`sha256:8894bc69b4071109661a33ec8780f0dbdfaf6d3a6c7120d701db90ea51c8ef8b`  
		Last Modified: Thu, 11 Jan 2024 04:29:02 GMT  
		Size: 323.6 MB (323642489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ae7e0821dc076c0f9deaec4a4f0c14d9e11feae9f88f9185d22f6a1edf48a`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7e9b3ed567a4657a9dd14ff7fdeb3043934a814f2290ba1baccaefab9319d1`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a212ad5a35843cb84e2873dae669a6dd680dd3642a2cd817fbd430dc1e4ba783`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c571c8161496a8f3948f43dd8d820ff67122a37fb061797c2ceec1e885c37ad4`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3b6dc3112c14927fb7f906166836f602a2aa7b2f506f14f66eefa7fcc425669
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573353528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd3691cf3f7fc641f3735d8007bff04b3fd0ca14c65235775075dea7583e4d8`
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
# Thu, 11 Jan 2024 06:33:35 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 06:33:35 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 11 Jan 2024 06:34:49 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 06:34:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 06:34:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 06:34:56 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 06:34:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 06:34:57 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 06:34:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 06:34:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 06:34:57 GMT
USER odoo
# Thu, 11 Jan 2024 06:34:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 06:34:57 GMT
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
	-	`sha256:ce82808a319b20e31e837d14f1539681829af0766878415ee60db2560c54311c`  
		Last Modified: Thu, 11 Jan 2024 06:35:49 GMT  
		Size: 323.3 MB (323282961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5303bd20d5f779b0487964b58367d1fec26ccf17359049513b24f5b2624e72c4`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d36b0c7affb21ffa6c11290bafbbc1a3fd59e8dfbd86a383a7896d4051d8a`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3337f394d41dad58ee21cc292276c9ae40ce2620a450c9a9f46478b0086a773d`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb0b4f84d6d02d8ecf9ca5a1fb25a408f757784ad4a4a079a24aac87582a276`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
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
$ docker pull odoo@sha256:4d15e19d56dd57e9fe0cc6ca29152884676c47f44dc53145c0e178e1c5235f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:09910d07c80de270fd4cb64d573ed79403eb2b9f32784e02cb91016be80b8f98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.8 MB (577758675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea3df020b4b5bef69b33a820da4817fdc546aec1b36b417d5fe8235b443bfe4`
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
# Thu, 11 Jan 2024 04:24:08 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 04:24:08 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 11 Jan 2024 04:25:29 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 04:25:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 04:25:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 04:25:34 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 04:25:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 04:25:35 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 04:25:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 04:25:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 04:25:35 GMT
USER odoo
# Thu, 11 Jan 2024 04:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:25:35 GMT
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
	-	`sha256:8894bc69b4071109661a33ec8780f0dbdfaf6d3a6c7120d701db90ea51c8ef8b`  
		Last Modified: Thu, 11 Jan 2024 04:29:02 GMT  
		Size: 323.6 MB (323642489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ae7e0821dc076c0f9deaec4a4f0c14d9e11feae9f88f9185d22f6a1edf48a`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7e9b3ed567a4657a9dd14ff7fdeb3043934a814f2290ba1baccaefab9319d1`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a212ad5a35843cb84e2873dae669a6dd680dd3642a2cd817fbd430dc1e4ba783`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c571c8161496a8f3948f43dd8d820ff67122a37fb061797c2ceec1e885c37ad4`  
		Last Modified: Thu, 11 Jan 2024 04:28:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3b6dc3112c14927fb7f906166836f602a2aa7b2f506f14f66eefa7fcc425669
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.4 MB (573353528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd3691cf3f7fc641f3735d8007bff04b3fd0ca14c65235775075dea7583e4d8`
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
# Thu, 11 Jan 2024 06:33:35 GMT
ARG ODOO_RELEASE=20240104
# Thu, 11 Jan 2024 06:33:35 GMT
ARG ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
# Thu, 11 Jan 2024 06:34:49 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 11 Jan 2024 06:34:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 11 Jan 2024 06:34:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 11 Jan 2024 06:34:56 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=b404b131e0898bbd33849fb69dc97412219e64a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 11 Jan 2024 06:34:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jan 2024 06:34:57 GMT
EXPOSE 8069 8071 8072
# Thu, 11 Jan 2024 06:34:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jan 2024 06:34:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 11 Jan 2024 06:34:57 GMT
USER odoo
# Thu, 11 Jan 2024 06:34:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 06:34:57 GMT
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
	-	`sha256:ce82808a319b20e31e837d14f1539681829af0766878415ee60db2560c54311c`  
		Last Modified: Thu, 11 Jan 2024 06:35:49 GMT  
		Size: 323.3 MB (323282961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5303bd20d5f779b0487964b58367d1fec26ccf17359049513b24f5b2624e72c4`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d36b0c7affb21ffa6c11290bafbbc1a3fd59e8dfbd86a383a7896d4051d8a`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3337f394d41dad58ee21cc292276c9ae40ce2620a450c9a9f46478b0086a773d`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb0b4f84d6d02d8ecf9ca5a1fb25a408f757784ad4a4a079a24aac87582a276`  
		Last Modified: Thu, 11 Jan 2024 06:35:20 GMT  
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
