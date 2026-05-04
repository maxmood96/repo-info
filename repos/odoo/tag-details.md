<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260504`](#odoo170-20260504)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260504`](#odoo180-20260504)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260504`](#odoo190-20260504)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:1f6c016a2bb2bde7342f4f53daf7336f9dcffb05a1e725df26097c5ce98d074b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:5220e88e86331a6959bb96c9f16e3bdb29875888ded32f9bbdc2db8c7a9032dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.3 MB (610287984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39756fb0dbf041787616d9159c4a922d6b36a05f9408ebf3148fd6679730722`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:09 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:09 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:17 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Apr 2026 17:21:17 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:17 GMT
ARG ODOO_SHA=b1ba76d03b56bed48bd25da72b5d9de9e1278b27
# Tue, 21 Apr 2026 17:22:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=b1ba76d03b56bed48bd25da72b5d9de9e1278b27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=b1ba76d03b56bed48bd25da72b5d9de9e1278b27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1501a282f0d6a0e9b308acdf314e5e602c7d86d02347f30844a11783671e77`  
		Last Modified: Tue, 21 Apr 2026 17:23:39 GMT  
		Size: 233.8 MB (233832184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc46703321cfe0196c79d75f84d961b5fad206a5461f9408581e6986742062`  
		Last Modified: Tue, 21 Apr 2026 17:23:27 GMT  
		Size: 2.6 MB (2603678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0b839ee1c092db591af3d018a89fe96ae6345f4af966ecf0de794e8e3cca8`  
		Last Modified: Tue, 21 Apr 2026 17:23:27 GMT  
		Size: 481.6 KB (481551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bef3f48c65bd2413b143d5e3190a275c89953d89e312411b8b96e0acc5a819`  
		Last Modified: Tue, 21 Apr 2026 17:23:40 GMT  
		Size: 343.6 MB (343631640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a14b3ebcedee2aea3f2064bfb7cbb737436ee18163a6ab241efe24d9aa95d70`  
		Last Modified: Tue, 21 Apr 2026 17:23:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aafbf4213787fdb9d87507a28a2e24733a2c9104f4a1b383dbb6880b1b9b63`  
		Last Modified: Tue, 21 Apr 2026 17:23:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f628b36b2c149f5fcb08193d5ca37f2739a9407b7e26247834970c158bb54`  
		Last Modified: Tue, 21 Apr 2026 17:23:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241454f0bd415675cb0d80ade2e25837923ce5ac4ed0fcb9f93e97926bd99d82`  
		Last Modified: Tue, 21 Apr 2026 17:23:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:5703ef352d5a4073e5b5549cf09d87b021791bda2531f1687b6f2dbe6ae39cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42904232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4559e73ea5fa7194c9dc4961885503e97e935a60c003374742a31138dec6b`

```dockerfile
```

-	Layers:
	-	`sha256:9f331715b5b347a8c19b82b20f771e260cbc1a0f4b1030025dd1d7c8873fb3a4`  
		Last Modified: Tue, 21 Apr 2026 17:23:30 GMT  
		Size: 42.9 MB (42877440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed2f6e07ab34e0d10efd23a4f953324c867e0397906618d259d331fe8044ad3`  
		Last Modified: Tue, 21 Apr 2026 17:23:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:436f787cb65d226ad7b4ebcdb0afad5570d92bf089e9653154565bd45c3e4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605274803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c41ce03faa12004338e59acd4328de63e7de2a79fff13d6d9bc5d30fd9d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:17 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:31 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:31 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:31 GMT
USER odoo
# Mon, 04 May 2026 20:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea59999641de59431037ca45a7bff25898c1b54dda0cea66b896eee9edba31c`  
		Last Modified: Mon, 04 May 2026 20:58:11 GMT  
		Size: 231.2 MB (231202109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e023a7d4e854b293eaaf9af326db95df181fadb3d7c3ebe1d3242ff1e977a1`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 2.6 MB (2598189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff26802bed98b8e6c8a44783691cd7f34b94cf7e3a676835c3a2e86827a15d0`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 484.0 KB (484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197540263cb05b1d2a3ba789fa3e02c026c42823ae543a0b784dad5541935c3`  
		Last Modified: Mon, 04 May 2026 20:58:16 GMT  
		Size: 343.4 MB (343381521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc04332b9e6d324b7c774b8d6ec3af2d44f140b7dce7272a6c7dadb04201a9`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215d70cd3f71c87e08a7bd6c89437273ee940c0e178776e7928f443cd5be40e`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36018947d52acd91d4ce275a6470517432e0ca66620b0572b9d803b8358302c3`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f49ad7b2b14ecce6c48cc6b3bfbe70f87184f19e372ab9c9bcd26897b481f`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1a7dee8e69d35bbf9e777d2c90a0b3d11c6a55334c094792d5b6a1025d4af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42911559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd91dbb69006c59d7a87b308d36b666122abd383422b429d976123ddd031234`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f7ec0101ee208525b5cddc5ef91270681bdbca1759373a1483faa486cbda7`  
		Last Modified: Mon, 04 May 2026 20:57:55 GMT  
		Size: 42.9 MB (42884616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0b27109c15adb36fa43396ef4ad7e01fbdb3e752b04d242d9f83285a2b1daf`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:1f6c016a2bb2bde7342f4f53daf7336f9dcffb05a1e725df26097c5ce98d074b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:5220e88e86331a6959bb96c9f16e3bdb29875888ded32f9bbdc2db8c7a9032dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.3 MB (610287984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39756fb0dbf041787616d9159c4a922d6b36a05f9408ebf3148fd6679730722`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:09 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:09 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:09 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:17 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Apr 2026 17:21:17 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:17 GMT
ARG ODOO_SHA=b1ba76d03b56bed48bd25da72b5d9de9e1278b27
# Tue, 21 Apr 2026 17:22:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=b1ba76d03b56bed48bd25da72b5d9de9e1278b27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=b1ba76d03b56bed48bd25da72b5d9de9e1278b27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:19 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1501a282f0d6a0e9b308acdf314e5e602c7d86d02347f30844a11783671e77`  
		Last Modified: Tue, 21 Apr 2026 17:23:39 GMT  
		Size: 233.8 MB (233832184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cc46703321cfe0196c79d75f84d961b5fad206a5461f9408581e6986742062`  
		Last Modified: Tue, 21 Apr 2026 17:23:27 GMT  
		Size: 2.6 MB (2603678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0b839ee1c092db591af3d018a89fe96ae6345f4af966ecf0de794e8e3cca8`  
		Last Modified: Tue, 21 Apr 2026 17:23:27 GMT  
		Size: 481.6 KB (481551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bef3f48c65bd2413b143d5e3190a275c89953d89e312411b8b96e0acc5a819`  
		Last Modified: Tue, 21 Apr 2026 17:23:40 GMT  
		Size: 343.6 MB (343631640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a14b3ebcedee2aea3f2064bfb7cbb737436ee18163a6ab241efe24d9aa95d70`  
		Last Modified: Tue, 21 Apr 2026 17:23:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aafbf4213787fdb9d87507a28a2e24733a2c9104f4a1b383dbb6880b1b9b63`  
		Last Modified: Tue, 21 Apr 2026 17:23:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f628b36b2c149f5fcb08193d5ca37f2739a9407b7e26247834970c158bb54`  
		Last Modified: Tue, 21 Apr 2026 17:23:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241454f0bd415675cb0d80ade2e25837923ce5ac4ed0fcb9f93e97926bd99d82`  
		Last Modified: Tue, 21 Apr 2026 17:23:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5703ef352d5a4073e5b5549cf09d87b021791bda2531f1687b6f2dbe6ae39cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42904232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4559e73ea5fa7194c9dc4961885503e97e935a60c003374742a31138dec6b`

```dockerfile
```

-	Layers:
	-	`sha256:9f331715b5b347a8c19b82b20f771e260cbc1a0f4b1030025dd1d7c8873fb3a4`  
		Last Modified: Tue, 21 Apr 2026 17:23:30 GMT  
		Size: 42.9 MB (42877440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed2f6e07ab34e0d10efd23a4f953324c867e0397906618d259d331fe8044ad3`  
		Last Modified: Tue, 21 Apr 2026 17:23:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:436f787cb65d226ad7b4ebcdb0afad5570d92bf089e9653154565bd45c3e4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605274803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c41ce03faa12004338e59acd4328de63e7de2a79fff13d6d9bc5d30fd9d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:17 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:31 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:31 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:31 GMT
USER odoo
# Mon, 04 May 2026 20:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea59999641de59431037ca45a7bff25898c1b54dda0cea66b896eee9edba31c`  
		Last Modified: Mon, 04 May 2026 20:58:11 GMT  
		Size: 231.2 MB (231202109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e023a7d4e854b293eaaf9af326db95df181fadb3d7c3ebe1d3242ff1e977a1`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 2.6 MB (2598189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff26802bed98b8e6c8a44783691cd7f34b94cf7e3a676835c3a2e86827a15d0`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 484.0 KB (484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197540263cb05b1d2a3ba789fa3e02c026c42823ae543a0b784dad5541935c3`  
		Last Modified: Mon, 04 May 2026 20:58:16 GMT  
		Size: 343.4 MB (343381521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc04332b9e6d324b7c774b8d6ec3af2d44f140b7dce7272a6c7dadb04201a9`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215d70cd3f71c87e08a7bd6c89437273ee940c0e178776e7928f443cd5be40e`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36018947d52acd91d4ce275a6470517432e0ca66620b0572b9d803b8358302c3`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f49ad7b2b14ecce6c48cc6b3bfbe70f87184f19e372ab9c9bcd26897b481f`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1a7dee8e69d35bbf9e777d2c90a0b3d11c6a55334c094792d5b6a1025d4af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42911559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd91dbb69006c59d7a87b308d36b666122abd383422b429d976123ddd031234`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f7ec0101ee208525b5cddc5ef91270681bdbca1759373a1483faa486cbda7`  
		Last Modified: Mon, 04 May 2026 20:57:55 GMT  
		Size: 42.9 MB (42884616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0b27109c15adb36fa43396ef4ad7e01fbdb3e752b04d242d9f83285a2b1daf`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260504`

```console
$ docker pull odoo@sha256:c04ade07db259b1e31bf9100486806366c5839a0c7200d27b53c9db6b1a21b2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260504` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:436f787cb65d226ad7b4ebcdb0afad5570d92bf089e9653154565bd45c3e4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605274803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c41ce03faa12004338e59acd4328de63e7de2a79fff13d6d9bc5d30fd9d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:17 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:31 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:31 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:31 GMT
USER odoo
# Mon, 04 May 2026 20:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea59999641de59431037ca45a7bff25898c1b54dda0cea66b896eee9edba31c`  
		Last Modified: Mon, 04 May 2026 20:58:11 GMT  
		Size: 231.2 MB (231202109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e023a7d4e854b293eaaf9af326db95df181fadb3d7c3ebe1d3242ff1e977a1`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 2.6 MB (2598189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff26802bed98b8e6c8a44783691cd7f34b94cf7e3a676835c3a2e86827a15d0`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 484.0 KB (484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197540263cb05b1d2a3ba789fa3e02c026c42823ae543a0b784dad5541935c3`  
		Last Modified: Mon, 04 May 2026 20:58:16 GMT  
		Size: 343.4 MB (343381521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc04332b9e6d324b7c774b8d6ec3af2d44f140b7dce7272a6c7dadb04201a9`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215d70cd3f71c87e08a7bd6c89437273ee940c0e178776e7928f443cd5be40e`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36018947d52acd91d4ce275a6470517432e0ca66620b0572b9d803b8358302c3`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f49ad7b2b14ecce6c48cc6b3bfbe70f87184f19e372ab9c9bcd26897b481f`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:1a7dee8e69d35bbf9e777d2c90a0b3d11c6a55334c094792d5b6a1025d4af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42911559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd91dbb69006c59d7a87b308d36b666122abd383422b429d976123ddd031234`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f7ec0101ee208525b5cddc5ef91270681bdbca1759373a1483faa486cbda7`  
		Last Modified: Mon, 04 May 2026 20:57:55 GMT  
		Size: 42.9 MB (42884616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0b27109c15adb36fa43396ef4ad7e01fbdb3e752b04d242d9f83285a2b1daf`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:64ac2117b1ff8e501cf957bdac25f3f033db72e0bc01e52c0cb1c58e4875fc12
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
$ docker pull odoo@sha256:eb9a47a64f7dcd08957774124f135aac5378de425fce0c414ffaf7af4ed685ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.4 MB (684396522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2f9b4543860573b1e8196c2b886b519076c0664168d06ff5ddb1a8d67431e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:30 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:30 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:38 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:39 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:39 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Apr 2026 17:21:39 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:39 GMT
ARG ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
# Tue, 21 Apr 2026 17:22:31 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a2c1d53bcff5e02d3786ca6fd088d70400b8050d967b3b23ed7bee11fa6fd1`  
		Last Modified: Tue, 21 Apr 2026 17:24:19 GMT  
		Size: 254.6 MB (254569151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51529edcd55198c332cb9977fb3e6705bb027bb2c66be3df50cd30a3668a677`  
		Last Modified: Tue, 21 Apr 2026 17:24:10 GMT  
		Size: 14.4 MB (14359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75439a0797ae96daaaf54d35f49913a7b5d645582a3c44b05a152a8986587e91`  
		Last Modified: Tue, 21 Apr 2026 17:24:09 GMT  
		Size: 481.3 KB (481283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f041afb3f818336dae61719c3c742d12770b2641da20a28f68517d565b2d3c82`  
		Last Modified: Tue, 21 Apr 2026 17:24:21 GMT  
		Size: 385.3 MB (385250701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dcdf076d181637f247a0fdda02c85ee46654fe6df965260471fb0b299d913f`  
		Last Modified: Tue, 21 Apr 2026 17:24:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d31c53a929751a5ca644f1c2f83d03caa4c100794a77d152f535823c0d3de2`  
		Last Modified: Tue, 21 Apr 2026 17:24:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1369461b44a80175b1412e4f4644badf348963011b5420183bd6cf1430ee1df2`  
		Last Modified: Tue, 21 Apr 2026 17:24:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7130400d21d9596a8e3dc410dc5468453f03646af36c64084ea8aeef6118fe`  
		Last Modified: Tue, 21 Apr 2026 17:24:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:ff37eca78bb2e22e67d9f7c5568bf88f906fe2729aadee37860d6a7ea42fa214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62267066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d542ff718c30ff2b88139264f55997738831a0aa5f0be59b7f0233a6c09525`

```dockerfile
```

-	Layers:
	-	`sha256:51e0920c5345c038d53854c1bdf066a4481af2f9d36715990f425ef0727332a3`  
		Last Modified: Tue, 21 Apr 2026 17:24:12 GMT  
		Size: 62.2 MB (62240267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1023b9760a6668fb8f481375cb8aaffca821ac79bf59f0d13109ae45c85ce6ad`  
		Last Modified: Tue, 21 Apr 2026 17:24:09 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:deb8312d6161d461367767ebe3e3d8287b5d4ddaa6056357332998cf8969b4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d50f1bef7b1ef23dcf31832b6ab4a147b2e749e979d51a98b04efb392b92b83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:57:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:57:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:57:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:57:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:57:18 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 20:58:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:58:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:58:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:58:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:58:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:58:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:58:27 GMT
USER odoo
# Mon, 04 May 2026 20:58:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:58:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06020f82bad6429dda80a5580e2edc922996244bfee4917f7d228f01d5005873`  
		Last Modified: Mon, 04 May 2026 21:00:46 GMT  
		Size: 252.0 MB (252027487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1375dc07ba914d2b5dd39fdf995ee7f4f36236976c8cba239eb754a86ce73`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 14.3 MB (14340777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f76573893a6df9475dd7328f8d5a2ec41556adbbf097a677679c3e396c6d0`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 483.8 KB (483781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da4bcf5509ea1436c286e21e10695d5c06263c11af710f78e4f1211e554814`  
		Last Modified: Mon, 04 May 2026 21:00:49 GMT  
		Size: 385.4 MB (385420382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ff6a3e6deda43a3e5e69e9896c2f20610ca5f49693049cfc4ed438eee76b4`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b2656f3617c78bc8a6f3fff8f99e51a281c6b9dbcd1702cb82881ffad60af`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8f2b7c0ca15824469119a7424b0e5e1fa450444b3b046b72a383eec35620f`  
		Last Modified: Mon, 04 May 2026 21:00:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f1100602f83d9866a405c8bfabfd366b8faf0cd25c2c560ca6caaa7f799b4b`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b9864d920f62cb996d47d41f9beda0ac6a42785ea99a59f0972ca3fa7e37b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8372b847d45130854effa92658e61c7edaf48ddbfd30bdd2b084f81f151952c3`

```dockerfile
```

-	Layers:
	-	`sha256:76ce18f183b90ed66db82ceded4f57c2be3d5b817adaceefa3e55cb25d4f77e7`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 62.3 MB (62254468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322109be1c7e63c7edb9fd92c67d90a20aadc34f947ac13e8e81d50c19c65b0`  
		Last Modified: Mon, 04 May 2026 21:00:31 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:9825ceb1c3205868cc05a7b0b8b91fd37a53d7661e6ba935b402ad7d66bba27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.6 MB (700590668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e7d0166cb24f4788ee4dd648d31f3d9d715dfbff05dfbd52629dfeb4156b3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260421
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
# Tue, 21 Apr 2026 17:24:05 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:24:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:24:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:24:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:24:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:24:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:24:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:24:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:24:10 GMT
USER odoo
# Tue, 21 Apr 2026 17:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:24:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e589bc94427b982b2e114479ba676714b4da86fbaf472ee8d2a4780d881918`  
		Last Modified: Tue, 21 Apr 2026 17:29:20 GMT  
		Size: 385.8 MB (385788454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50e1aba470ac784199f29882a4435c8b426c3f6afdc750543511328144f10`  
		Last Modified: Tue, 21 Apr 2026 17:29:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5f0081959d2d4563ac49e14f9c1f4336cb798a75e373114183548bb1856d0a`  
		Last Modified: Tue, 21 Apr 2026 17:29:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ac95ca11e48e551fb8ad109a01e43c278c773c0032a59c72ad3ed69ca54ca0`  
		Last Modified: Tue, 21 Apr 2026 17:29:11 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5063d93bdd9e020f2b332b73a98d8ddb8473312490e73c38aa9e230042a6888`  
		Last Modified: Tue, 21 Apr 2026 17:29:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0c005e45f1723303d05e5fa8e80cd0797f2f7fe5072fb7ad2467219fbf8e17e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62275505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53d5c8a15439946716a59b59c05dfa396f1ddc700c96448d6abc29682fc75ba`

```dockerfile
```

-	Layers:
	-	`sha256:52bcc498f153d576cf0ff6e75b73fa61a257f730ad8ff761f0d28739615bfcfc`  
		Last Modified: Tue, 21 Apr 2026 17:29:15 GMT  
		Size: 62.2 MB (62248650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410fd34ddcc23c044418f18536806999d5f34bfe563008640815591dffed54b4`  
		Last Modified: Tue, 21 Apr 2026 17:29:12 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:64ac2117b1ff8e501cf957bdac25f3f033db72e0bc01e52c0cb1c58e4875fc12
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
$ docker pull odoo@sha256:eb9a47a64f7dcd08957774124f135aac5378de425fce0c414ffaf7af4ed685ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.4 MB (684396522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2f9b4543860573b1e8196c2b886b519076c0664168d06ff5ddb1a8d67431e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:30 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:30 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:38 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:39 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:39 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Apr 2026 17:21:39 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:39 GMT
ARG ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
# Tue, 21 Apr 2026 17:22:31 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:32 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a2c1d53bcff5e02d3786ca6fd088d70400b8050d967b3b23ed7bee11fa6fd1`  
		Last Modified: Tue, 21 Apr 2026 17:24:19 GMT  
		Size: 254.6 MB (254569151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51529edcd55198c332cb9977fb3e6705bb027bb2c66be3df50cd30a3668a677`  
		Last Modified: Tue, 21 Apr 2026 17:24:10 GMT  
		Size: 14.4 MB (14359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75439a0797ae96daaaf54d35f49913a7b5d645582a3c44b05a152a8986587e91`  
		Last Modified: Tue, 21 Apr 2026 17:24:09 GMT  
		Size: 481.3 KB (481283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f041afb3f818336dae61719c3c742d12770b2641da20a28f68517d565b2d3c82`  
		Last Modified: Tue, 21 Apr 2026 17:24:21 GMT  
		Size: 385.3 MB (385250701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dcdf076d181637f247a0fdda02c85ee46654fe6df965260471fb0b299d913f`  
		Last Modified: Tue, 21 Apr 2026 17:24:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d31c53a929751a5ca644f1c2f83d03caa4c100794a77d152f535823c0d3de2`  
		Last Modified: Tue, 21 Apr 2026 17:24:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1369461b44a80175b1412e4f4644badf348963011b5420183bd6cf1430ee1df2`  
		Last Modified: Tue, 21 Apr 2026 17:24:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7130400d21d9596a8e3dc410dc5468453f03646af36c64084ea8aeef6118fe`  
		Last Modified: Tue, 21 Apr 2026 17:24:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ff37eca78bb2e22e67d9f7c5568bf88f906fe2729aadee37860d6a7ea42fa214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62267066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d542ff718c30ff2b88139264f55997738831a0aa5f0be59b7f0233a6c09525`

```dockerfile
```

-	Layers:
	-	`sha256:51e0920c5345c038d53854c1bdf066a4481af2f9d36715990f425ef0727332a3`  
		Last Modified: Tue, 21 Apr 2026 17:24:12 GMT  
		Size: 62.2 MB (62240267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1023b9760a6668fb8f481375cb8aaffca821ac79bf59f0d13109ae45c85ce6ad`  
		Last Modified: Tue, 21 Apr 2026 17:24:09 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:deb8312d6161d461367767ebe3e3d8287b5d4ddaa6056357332998cf8969b4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d50f1bef7b1ef23dcf31832b6ab4a147b2e749e979d51a98b04efb392b92b83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:57:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:57:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:57:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:57:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:57:18 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 20:58:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:58:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:58:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:58:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:58:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:58:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:58:27 GMT
USER odoo
# Mon, 04 May 2026 20:58:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:58:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06020f82bad6429dda80a5580e2edc922996244bfee4917f7d228f01d5005873`  
		Last Modified: Mon, 04 May 2026 21:00:46 GMT  
		Size: 252.0 MB (252027487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1375dc07ba914d2b5dd39fdf995ee7f4f36236976c8cba239eb754a86ce73`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 14.3 MB (14340777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f76573893a6df9475dd7328f8d5a2ec41556adbbf097a677679c3e396c6d0`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 483.8 KB (483781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da4bcf5509ea1436c286e21e10695d5c06263c11af710f78e4f1211e554814`  
		Last Modified: Mon, 04 May 2026 21:00:49 GMT  
		Size: 385.4 MB (385420382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ff6a3e6deda43a3e5e69e9896c2f20610ca5f49693049cfc4ed438eee76b4`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b2656f3617c78bc8a6f3fff8f99e51a281c6b9dbcd1702cb82881ffad60af`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8f2b7c0ca15824469119a7424b0e5e1fa450444b3b046b72a383eec35620f`  
		Last Modified: Mon, 04 May 2026 21:00:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f1100602f83d9866a405c8bfabfd366b8faf0cd25c2c560ca6caaa7f799b4b`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b9864d920f62cb996d47d41f9beda0ac6a42785ea99a59f0972ca3fa7e37b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8372b847d45130854effa92658e61c7edaf48ddbfd30bdd2b084f81f151952c3`

```dockerfile
```

-	Layers:
	-	`sha256:76ce18f183b90ed66db82ceded4f57c2be3d5b817adaceefa3e55cb25d4f77e7`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 62.3 MB (62254468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322109be1c7e63c7edb9fd92c67d90a20aadc34f947ac13e8e81d50c19c65b0`  
		Last Modified: Mon, 04 May 2026 21:00:31 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:9825ceb1c3205868cc05a7b0b8b91fd37a53d7661e6ba935b402ad7d66bba27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.6 MB (700590668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e7d0166cb24f4788ee4dd648d31f3d9d715dfbff05dfbd52629dfeb4156b3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260421
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
# Tue, 21 Apr 2026 17:24:05 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:24:07 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:24:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:24:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=c37092209c1e5ede571d5604a1c01b013e354a83
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:24:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:24:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:24:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:24:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:24:10 GMT
USER odoo
# Tue, 21 Apr 2026 17:24:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:24:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e589bc94427b982b2e114479ba676714b4da86fbaf472ee8d2a4780d881918`  
		Last Modified: Tue, 21 Apr 2026 17:29:20 GMT  
		Size: 385.8 MB (385788454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede50e1aba470ac784199f29882a4435c8b426c3f6afdc750543511328144f10`  
		Last Modified: Tue, 21 Apr 2026 17:29:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5f0081959d2d4563ac49e14f9c1f4336cb798a75e373114183548bb1856d0a`  
		Last Modified: Tue, 21 Apr 2026 17:29:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ac95ca11e48e551fb8ad109a01e43c278c773c0032a59c72ad3ed69ca54ca0`  
		Last Modified: Tue, 21 Apr 2026 17:29:11 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5063d93bdd9e020f2b332b73a98d8ddb8473312490e73c38aa9e230042a6888`  
		Last Modified: Tue, 21 Apr 2026 17:29:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0c005e45f1723303d05e5fa8e80cd0797f2f7fe5072fb7ad2467219fbf8e17e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62275505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53d5c8a15439946716a59b59c05dfa396f1ddc700c96448d6abc29682fc75ba`

```dockerfile
```

-	Layers:
	-	`sha256:52bcc498f153d576cf0ff6e75b73fa61a257f730ad8ff761f0d28739615bfcfc`  
		Last Modified: Tue, 21 Apr 2026 17:29:15 GMT  
		Size: 62.2 MB (62248650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410fd34ddcc23c044418f18536806999d5f34bfe563008640815591dffed54b4`  
		Last Modified: Tue, 21 Apr 2026 17:29:12 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260504`

```console
$ docker pull odoo@sha256:2b797d0c4af4d7eb018bdc30b02acf50cb51dd25b66990389d6f3a00728c471d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:18.0-20260504` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:deb8312d6161d461367767ebe3e3d8287b5d4ddaa6056357332998cf8969b4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d50f1bef7b1ef23dcf31832b6ab4a147b2e749e979d51a98b04efb392b92b83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:57:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:57:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:57:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:57:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:57:18 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 20:58:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:58:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:58:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:58:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:58:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:58:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:58:27 GMT
USER odoo
# Mon, 04 May 2026 20:58:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:58:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06020f82bad6429dda80a5580e2edc922996244bfee4917f7d228f01d5005873`  
		Last Modified: Mon, 04 May 2026 21:00:46 GMT  
		Size: 252.0 MB (252027487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1375dc07ba914d2b5dd39fdf995ee7f4f36236976c8cba239eb754a86ce73`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 14.3 MB (14340777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f76573893a6df9475dd7328f8d5a2ec41556adbbf097a677679c3e396c6d0`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 483.8 KB (483781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da4bcf5509ea1436c286e21e10695d5c06263c11af710f78e4f1211e554814`  
		Last Modified: Mon, 04 May 2026 21:00:49 GMT  
		Size: 385.4 MB (385420382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ff6a3e6deda43a3e5e69e9896c2f20610ca5f49693049cfc4ed438eee76b4`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b2656f3617c78bc8a6f3fff8f99e51a281c6b9dbcd1702cb82881ffad60af`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8f2b7c0ca15824469119a7424b0e5e1fa450444b3b046b72a383eec35620f`  
		Last Modified: Mon, 04 May 2026 21:00:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f1100602f83d9866a405c8bfabfd366b8faf0cd25c2c560ca6caaa7f799b4b`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:b9864d920f62cb996d47d41f9beda0ac6a42785ea99a59f0972ca3fa7e37b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8372b847d45130854effa92658e61c7edaf48ddbfd30bdd2b084f81f151952c3`

```dockerfile
```

-	Layers:
	-	`sha256:76ce18f183b90ed66db82ceded4f57c2be3d5b817adaceefa3e55cb25d4f77e7`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 62.3 MB (62254468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322109be1c7e63c7edb9fd92c67d90a20aadc34f947ac13e8e81d50c19c65b0`  
		Last Modified: Mon, 04 May 2026 21:00:31 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:6bcde1e043fa2958261e93d594d52e2c1e48a5c3792049db8fc1883260f4ee2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:52cf57ad834635dda524f54b83c4122d3e978078e43e0d2f4e75f65914017e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.7 MB (703666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609235d439be0af5d2525592bc349c049483bfc0899e487f18f4c3e2bfa1ca63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:33 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bed374753b7d34f37336fb7f07ced6765e3d83829604935205879f27e0ed7`  
		Last Modified: Tue, 21 Apr 2026 17:25:05 GMT  
		Size: 254.6 MB (254568497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1864809b7d4219e675d42d2f7130c9b0227420b724437d3beadddb8041358b58`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 14.4 MB (14360070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2205f275b3232be9b2fc0cbb5f57701ebce6485a2fae1dba8ee9343c4dfeb4`  
		Last Modified: Tue, 21 Apr 2026 17:24:56 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24f638d354288c212821ab5c7811b907019aa18a471c4c1189154b4589d179f`  
		Last Modified: Tue, 21 Apr 2026 17:25:10 GMT  
		Size: 404.5 MB (404521468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c87b03fd8e0de2c5b15193f281364be5b241e9822b7c1f7534b1c02759e27fd`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31902119af4bc1da9e2f910e02747689265fc3cf204abb608763fff3505a7005`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8113e92c8545c9101f7466df56f33aaa1ea20cd5cb69200786cfbd0a8a17fc`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaf672cf5f456330dbf337add3a0dc1a48b84d95c4b872f8c3453a37c79fd88`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcf127d541fb01a096cc6f3d7dc93ef21708941305975477489cecfe615269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70275145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f4a0b8e917a359011bfa7b251c589a8ab89ace0ece3e5fff3d11126f4ae60`

```dockerfile
```

-	Layers:
	-	`sha256:19ff740e6a2ceec4039e5c50cf643f1ad7d3f234e6ba84e642ff65e9d98f9e98`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 70.2 MB (70248052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d367f345ce6d068f39e8af1ba3b2dd60233c4a8d821e93226d04fd71bbcf49`  
		Last Modified: Tue, 21 Apr 2026 17:24:55 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:72af05da350386e0d42832379ee18481bdb750d94b6d2f2e7005e0defdcf8ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.9 MB (719857359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d532ab52bfa3ac1bbfeb2e3ac16d1136d0032676b02874015cc13570d773b2b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260421
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:24:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:24:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:24:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:24:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
USER odoo
# Tue, 21 Apr 2026 17:24:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:24:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddab69462fde54ff0c12c3ec9a466d95af5a4114d63852edd2d2f4d9ce6421b`  
		Last Modified: Tue, 21 Apr 2026 17:30:27 GMT  
		Size: 405.1 MB (405055149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eb53249213be84b13171cfb115879a0022c207b82404adf19de892075029b2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0223c562e510689150ffa76cbb7d8182813e27ccc655cc8ec63f9c5e62357`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4405878df9790bbd22d6d9cd1bd0c4685eec81aa5ce9c05bcfaf4d63f349c2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c63c374e6a1886c43433768ffb5ecc6206a3737ba25566d386fb08428a4e9d5`  
		Last Modified: Tue, 21 Apr 2026 17:30:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:75578d361f1e0c972c0a2b59bf14fe8713c2efa7e3307493193a28c9e0551fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70283596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877a8ba587ce7564b500e80193c0591a4fca8413200b32c94292027b9d7d4798`

```dockerfile
```

-	Layers:
	-	`sha256:1e025bdb1a77fdf791aaadd376128beb15c63231828bfa520dab96d896f9382a`  
		Last Modified: Tue, 21 Apr 2026 17:30:20 GMT  
		Size: 70.3 MB (70256441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ad3c96249ff64dda4c9ff470c726f532078ff2e47fd7b680f9385645d79dcc`  
		Last Modified: Tue, 21 Apr 2026 17:30:16 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:6bcde1e043fa2958261e93d594d52e2c1e48a5c3792049db8fc1883260f4ee2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:52cf57ad834635dda524f54b83c4122d3e978078e43e0d2f4e75f65914017e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.7 MB (703666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609235d439be0af5d2525592bc349c049483bfc0899e487f18f4c3e2bfa1ca63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:33 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bed374753b7d34f37336fb7f07ced6765e3d83829604935205879f27e0ed7`  
		Last Modified: Tue, 21 Apr 2026 17:25:05 GMT  
		Size: 254.6 MB (254568497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1864809b7d4219e675d42d2f7130c9b0227420b724437d3beadddb8041358b58`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 14.4 MB (14360070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2205f275b3232be9b2fc0cbb5f57701ebce6485a2fae1dba8ee9343c4dfeb4`  
		Last Modified: Tue, 21 Apr 2026 17:24:56 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24f638d354288c212821ab5c7811b907019aa18a471c4c1189154b4589d179f`  
		Last Modified: Tue, 21 Apr 2026 17:25:10 GMT  
		Size: 404.5 MB (404521468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c87b03fd8e0de2c5b15193f281364be5b241e9822b7c1f7534b1c02759e27fd`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31902119af4bc1da9e2f910e02747689265fc3cf204abb608763fff3505a7005`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8113e92c8545c9101f7466df56f33aaa1ea20cd5cb69200786cfbd0a8a17fc`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaf672cf5f456330dbf337add3a0dc1a48b84d95c4b872f8c3453a37c79fd88`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcf127d541fb01a096cc6f3d7dc93ef21708941305975477489cecfe615269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70275145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f4a0b8e917a359011bfa7b251c589a8ab89ace0ece3e5fff3d11126f4ae60`

```dockerfile
```

-	Layers:
	-	`sha256:19ff740e6a2ceec4039e5c50cf643f1ad7d3f234e6ba84e642ff65e9d98f9e98`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 70.2 MB (70248052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d367f345ce6d068f39e8af1ba3b2dd60233c4a8d821e93226d04fd71bbcf49`  
		Last Modified: Tue, 21 Apr 2026 17:24:55 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:72af05da350386e0d42832379ee18481bdb750d94b6d2f2e7005e0defdcf8ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.9 MB (719857359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d532ab52bfa3ac1bbfeb2e3ac16d1136d0032676b02874015cc13570d773b2b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260421
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:24:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:24:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:24:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:24:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
USER odoo
# Tue, 21 Apr 2026 17:24:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:24:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddab69462fde54ff0c12c3ec9a466d95af5a4114d63852edd2d2f4d9ce6421b`  
		Last Modified: Tue, 21 Apr 2026 17:30:27 GMT  
		Size: 405.1 MB (405055149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eb53249213be84b13171cfb115879a0022c207b82404adf19de892075029b2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0223c562e510689150ffa76cbb7d8182813e27ccc655cc8ec63f9c5e62357`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4405878df9790bbd22d6d9cd1bd0c4685eec81aa5ce9c05bcfaf4d63f349c2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c63c374e6a1886c43433768ffb5ecc6206a3737ba25566d386fb08428a4e9d5`  
		Last Modified: Tue, 21 Apr 2026 17:30:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:75578d361f1e0c972c0a2b59bf14fe8713c2efa7e3307493193a28c9e0551fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70283596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877a8ba587ce7564b500e80193c0591a4fca8413200b32c94292027b9d7d4798`

```dockerfile
```

-	Layers:
	-	`sha256:1e025bdb1a77fdf791aaadd376128beb15c63231828bfa520dab96d896f9382a`  
		Last Modified: Tue, 21 Apr 2026 17:30:20 GMT  
		Size: 70.3 MB (70256441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ad3c96249ff64dda4c9ff470c726f532078ff2e47fd7b680f9385645d79dcc`  
		Last Modified: Tue, 21 Apr 2026 17:30:16 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260504`

```console
$ docker pull odoo@sha256:22aa24157c65fff08c94e5e5421c8303bfe99ee8651ab6ea45889f7872a7c902
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:19.0-20260504` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:6bcde1e043fa2958261e93d594d52e2c1e48a5c3792049db8fc1883260f4ee2a
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
$ docker pull odoo@sha256:52cf57ad834635dda524f54b83c4122d3e978078e43e0d2f4e75f65914017e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.7 MB (703666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609235d439be0af5d2525592bc349c049483bfc0899e487f18f4c3e2bfa1ca63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:33 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bed374753b7d34f37336fb7f07ced6765e3d83829604935205879f27e0ed7`  
		Last Modified: Tue, 21 Apr 2026 17:25:05 GMT  
		Size: 254.6 MB (254568497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1864809b7d4219e675d42d2f7130c9b0227420b724437d3beadddb8041358b58`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 14.4 MB (14360070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2205f275b3232be9b2fc0cbb5f57701ebce6485a2fae1dba8ee9343c4dfeb4`  
		Last Modified: Tue, 21 Apr 2026 17:24:56 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24f638d354288c212821ab5c7811b907019aa18a471c4c1189154b4589d179f`  
		Last Modified: Tue, 21 Apr 2026 17:25:10 GMT  
		Size: 404.5 MB (404521468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c87b03fd8e0de2c5b15193f281364be5b241e9822b7c1f7534b1c02759e27fd`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31902119af4bc1da9e2f910e02747689265fc3cf204abb608763fff3505a7005`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8113e92c8545c9101f7466df56f33aaa1ea20cd5cb69200786cfbd0a8a17fc`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaf672cf5f456330dbf337add3a0dc1a48b84d95c4b872f8c3453a37c79fd88`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcf127d541fb01a096cc6f3d7dc93ef21708941305975477489cecfe615269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70275145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f4a0b8e917a359011bfa7b251c589a8ab89ace0ece3e5fff3d11126f4ae60`

```dockerfile
```

-	Layers:
	-	`sha256:19ff740e6a2ceec4039e5c50cf643f1ad7d3f234e6ba84e642ff65e9d98f9e98`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 70.2 MB (70248052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d367f345ce6d068f39e8af1ba3b2dd60233c4a8d821e93226d04fd71bbcf49`  
		Last Modified: Tue, 21 Apr 2026 17:24:55 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:72af05da350386e0d42832379ee18481bdb750d94b6d2f2e7005e0defdcf8ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.9 MB (719857359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d532ab52bfa3ac1bbfeb2e3ac16d1136d0032676b02874015cc13570d773b2b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260421
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:24:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:24:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:24:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:24:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
USER odoo
# Tue, 21 Apr 2026 17:24:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:24:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddab69462fde54ff0c12c3ec9a466d95af5a4114d63852edd2d2f4d9ce6421b`  
		Last Modified: Tue, 21 Apr 2026 17:30:27 GMT  
		Size: 405.1 MB (405055149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eb53249213be84b13171cfb115879a0022c207b82404adf19de892075029b2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0223c562e510689150ffa76cbb7d8182813e27ccc655cc8ec63f9c5e62357`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4405878df9790bbd22d6d9cd1bd0c4685eec81aa5ce9c05bcfaf4d63f349c2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c63c374e6a1886c43433768ffb5ecc6206a3737ba25566d386fb08428a4e9d5`  
		Last Modified: Tue, 21 Apr 2026 17:30:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:75578d361f1e0c972c0a2b59bf14fe8713c2efa7e3307493193a28c9e0551fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70283596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877a8ba587ce7564b500e80193c0591a4fca8413200b32c94292027b9d7d4798`

```dockerfile
```

-	Layers:
	-	`sha256:1e025bdb1a77fdf791aaadd376128beb15c63231828bfa520dab96d896f9382a`  
		Last Modified: Tue, 21 Apr 2026 17:30:20 GMT  
		Size: 70.3 MB (70256441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ad3c96249ff64dda4c9ff470c726f532078ff2e47fd7b680f9385645d79dcc`  
		Last Modified: Tue, 21 Apr 2026 17:30:16 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
