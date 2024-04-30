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
$ docker pull odoo@sha256:e808243941daee269d4dab6f8ef5175dc86a67c5eede9f1001fb1156c985225d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:10258878e203ce3bca818902c48260b9fd48424fe4067bec9599f97a121dc076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564171556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af716c61892a85d8d544b642dd36cee5a01a052fb4c48149476b8a996bd1d355`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:41:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:41:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:41:41 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:41:41 GMT
ENV ODOO_VERSION=15.0
# Mon, 29 Apr 2024 18:45:16 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:45:16 GMT
ARG ODOO_SHA=ded89a7635233e5bcd27869f777980bf5a637b24
# Mon, 29 Apr 2024 18:46:29 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ded89a7635233e5bcd27869f777980bf5a637b24
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:46:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:46:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:46:34 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ded89a7635233e5bcd27869f777980bf5a637b24
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:46:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:46:34 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:46:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:46:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:46:34 GMT
USER odoo
# Mon, 29 Apr 2024 18:46:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:46:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844298f77b5290c77d07c814122b04a5a0c27837cb2bdc442a97a023172f418`  
		Last Modified: Wed, 24 Apr 2024 13:44:26 GMT  
		Size: 220.3 MB (220294160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8352c49f618af1258a6a53a2b11a11831bdec468a8a9cfb443fe2064119b09`  
		Last Modified: Wed, 24 Apr 2024 13:44:02 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637b99e2b29aaa41f154e2a407ca74a4895714a3e8bcfd19aebecead0a2f61cb`  
		Last Modified: Wed, 24 Apr 2024 13:44:01 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3d311f5f2dab787b3ad611346fb19e3b504ecb17eb1d2f362d0742b99a9d96`  
		Last Modified: Mon, 29 Apr 2024 18:48:59 GMT  
		Size: 309.4 MB (309355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db047fc83718b3befc9b040853e7a1a9ab47b0d8755063b20cd2a5036b47fa82`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f65ce9088ec8b33ab5f497254b3c96bebfb2727637c42cfa0387b06b245882f`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990dd197852682edad58536e9099812d1221ef4584bffa2449d3d7c32833936`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4adb70ce9d8f58322a3215406383702f19d8c7e0e26fd641e903ad09d137f6`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:e808243941daee269d4dab6f8ef5175dc86a67c5eede9f1001fb1156c985225d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:10258878e203ce3bca818902c48260b9fd48424fe4067bec9599f97a121dc076
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564171556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af716c61892a85d8d544b642dd36cee5a01a052fb4c48149476b8a996bd1d355`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:41:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:41:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:41:41 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:41:41 GMT
ENV ODOO_VERSION=15.0
# Mon, 29 Apr 2024 18:45:16 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:45:16 GMT
ARG ODOO_SHA=ded89a7635233e5bcd27869f777980bf5a637b24
# Mon, 29 Apr 2024 18:46:29 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ded89a7635233e5bcd27869f777980bf5a637b24
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:46:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:46:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:46:34 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ded89a7635233e5bcd27869f777980bf5a637b24
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:46:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:46:34 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:46:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:46:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:46:34 GMT
USER odoo
# Mon, 29 Apr 2024 18:46:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:46:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844298f77b5290c77d07c814122b04a5a0c27837cb2bdc442a97a023172f418`  
		Last Modified: Wed, 24 Apr 2024 13:44:26 GMT  
		Size: 220.3 MB (220294160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8352c49f618af1258a6a53a2b11a11831bdec468a8a9cfb443fe2064119b09`  
		Last Modified: Wed, 24 Apr 2024 13:44:02 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637b99e2b29aaa41f154e2a407ca74a4895714a3e8bcfd19aebecead0a2f61cb`  
		Last Modified: Wed, 24 Apr 2024 13:44:01 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3d311f5f2dab787b3ad611346fb19e3b504ecb17eb1d2f362d0742b99a9d96`  
		Last Modified: Mon, 29 Apr 2024 18:48:59 GMT  
		Size: 309.4 MB (309355405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db047fc83718b3befc9b040853e7a1a9ab47b0d8755063b20cd2a5036b47fa82`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f65ce9088ec8b33ab5f497254b3c96bebfb2727637c42cfa0387b06b245882f`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990dd197852682edad58536e9099812d1221ef4584bffa2449d3d7c32833936`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4adb70ce9d8f58322a3215406383702f19d8c7e0e26fd641e903ad09d137f6`  
		Last Modified: Mon, 29 Apr 2024 18:48:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:b733d02b67a6a9b72edbbd409a1725e0d3113d4d432e202457368a966734079d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f8692f98fd0d1dac934f40bf708ffea37de1b7637ba3f2998161d6c8aa7d3446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583334610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139dc95d5964af991ee9d3258be7de0c3db5627388b68a5a5368e6f17d1dacf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:37:44 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 13:38:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:39:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:39:03 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:39:04 GMT
ENV ODOO_VERSION=16.0
# Mon, 29 Apr 2024 18:43:37 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:43:37 GMT
ARG ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
# Mon, 29 Apr 2024 18:45:00 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:45:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:45:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:45:05 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:45:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:45:05 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:45:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:45:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:45:05 GMT
USER odoo
# Mon, 29 Apr 2024 18:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:45:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b10b512b443a629773a6151d15753e241d9c89e695fc8769376c36816475426`  
		Last Modified: Wed, 24 Apr 2024 13:43:38 GMT  
		Size: 219.6 MB (219605091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f954fd7c585d0f341393980922d2e5b0e829b07f8a927c1ef49cb5b9a1e28`  
		Last Modified: Wed, 24 Apr 2024 13:43:13 GMT  
		Size: 2.6 MB (2631177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255380b0477fe6a4565c69b731391d7194a57d85be15c9c95945f92214994e2f`  
		Last Modified: Wed, 24 Apr 2024 13:43:12 GMT  
		Size: 458.4 KB (458387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a710f88e4d8c77ecc75108a088a9e57079a9941072ac12a0e7332b27d2a255ab`  
		Last Modified: Mon, 29 Apr 2024 18:48:15 GMT  
		Size: 329.2 MB (329203227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67f536a8172367ecd4e3b0a757038695e03e55dc9eb7503ed437c0d69b9500`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9952cd1006f5d5acca65e55cd48541a56eac5e570696999645d62c739c4824`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e0e44cf09508ef182179a3e8ed2c1e37e8ebac208702d5787abcdca504437`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e24953783156948dfdffbf5acacc2f398bbd25819e36c0472ff8485db90149e`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4cb8f8f5f4efaaf31d450fe23c2dbd53b651733e810ad164379886c051b32c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (578958575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd168e180743f24b2862ff4e80c360a8050e3e0e31ade770e5a850f8a13c9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Apr 2024 00:15:37 GMT
ARG ODOO_RELEASE=20240429
# Tue, 30 Apr 2024 00:15:37 GMT
ARG ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
# Tue, 30 Apr 2024 00:16:50 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Apr 2024 00:16:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 Apr 2024 00:16:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Apr 2024 00:16:59 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Apr 2024 00:16:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Apr 2024 00:16:59 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Apr 2024 00:16:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Apr 2024 00:16:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Apr 2024 00:16:59 GMT
USER odoo
# Tue, 30 Apr 2024 00:16:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 00:16:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07a071a6668b32806b488a8ac7e802ffd6a3f60bd6d634f3c10ca2f894c96e`  
		Last Modified: Tue, 30 Apr 2024 00:18:35 GMT  
		Size: 328.9 MB (328870944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134744acef690c38c30d8833ae0f51c33ab028ad42ba68a6750ff9183c82f2d6`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cb52d74238409d3694a77c4786b2b5763fc56e49758eb631cdf9b951c4f2f8`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb8751b1ef1cec318bcb0a44051c7843177bf4e3c7315d9f0d2b5fdda2d9a1b`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca3053940d473c813efdf64f83d17d0aa043aa2ff1ed8bea3cb97742bc9f4cb`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:213946e2a0ef8d8f9cc557dbcc864039e6a7bce5d405b9002df23d6b23f3377c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597891115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3bf3601047020af4549bd74e679f1d4b02aabebdcbc30e858912ac0239b024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 29 Apr 2024 18:06:54 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:06:55 GMT
ARG ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
# Mon, 29 Apr 2024 18:09:33 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:09:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:09:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:09:50 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:09:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:09:51 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:09:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:09:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:09:53 GMT
USER odoo
# Mon, 29 Apr 2024 18:09:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:09:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652145f7d82c8a71624671694f21905825351537dd8e342a16c79c0c2015dcaa`  
		Last Modified: Mon, 29 Apr 2024 18:12:08 GMT  
		Size: 330.6 MB (330639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce851d10cf7c7e6924847d487ada570b4cb8774114d0032b44be84f31e65c789`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57579ba1994b90961b0bb5a15fae3d11b2ae4e83e883aab6d8abfe48f40ef67`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d604e0e3078697cf59b8c5ffc3cf4cb5902d797cec56939b9ad96a54bf7c95`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2ddc8b0937aec9aeef42a814156f066ab6b9deba98ee169dcef8fea4e55c2`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:b733d02b67a6a9b72edbbd409a1725e0d3113d4d432e202457368a966734079d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f8692f98fd0d1dac934f40bf708ffea37de1b7637ba3f2998161d6c8aa7d3446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583334610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139dc95d5964af991ee9d3258be7de0c3db5627388b68a5a5368e6f17d1dacf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:37:44 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 13:38:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:39:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:39:03 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:39:04 GMT
ENV ODOO_VERSION=16.0
# Mon, 29 Apr 2024 18:43:37 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:43:37 GMT
ARG ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
# Mon, 29 Apr 2024 18:45:00 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:45:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:45:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:45:05 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:45:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:45:05 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:45:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:45:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:45:05 GMT
USER odoo
# Mon, 29 Apr 2024 18:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:45:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b10b512b443a629773a6151d15753e241d9c89e695fc8769376c36816475426`  
		Last Modified: Wed, 24 Apr 2024 13:43:38 GMT  
		Size: 219.6 MB (219605091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f954fd7c585d0f341393980922d2e5b0e829b07f8a927c1ef49cb5b9a1e28`  
		Last Modified: Wed, 24 Apr 2024 13:43:13 GMT  
		Size: 2.6 MB (2631177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255380b0477fe6a4565c69b731391d7194a57d85be15c9c95945f92214994e2f`  
		Last Modified: Wed, 24 Apr 2024 13:43:12 GMT  
		Size: 458.4 KB (458387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a710f88e4d8c77ecc75108a088a9e57079a9941072ac12a0e7332b27d2a255ab`  
		Last Modified: Mon, 29 Apr 2024 18:48:15 GMT  
		Size: 329.2 MB (329203227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67f536a8172367ecd4e3b0a757038695e03e55dc9eb7503ed437c0d69b9500`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9952cd1006f5d5acca65e55cd48541a56eac5e570696999645d62c739c4824`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e0e44cf09508ef182179a3e8ed2c1e37e8ebac208702d5787abcdca504437`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e24953783156948dfdffbf5acacc2f398bbd25819e36c0472ff8485db90149e`  
		Last Modified: Mon, 29 Apr 2024 18:47:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4cb8f8f5f4efaaf31d450fe23c2dbd53b651733e810ad164379886c051b32c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (578958575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd168e180743f24b2862ff4e80c360a8050e3e0e31ade770e5a850f8a13c9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Apr 2024 00:15:37 GMT
ARG ODOO_RELEASE=20240429
# Tue, 30 Apr 2024 00:15:37 GMT
ARG ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
# Tue, 30 Apr 2024 00:16:50 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Apr 2024 00:16:58 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 Apr 2024 00:16:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Apr 2024 00:16:59 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Apr 2024 00:16:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Apr 2024 00:16:59 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Apr 2024 00:16:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Apr 2024 00:16:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Apr 2024 00:16:59 GMT
USER odoo
# Tue, 30 Apr 2024 00:16:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 00:16:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c07a071a6668b32806b488a8ac7e802ffd6a3f60bd6d634f3c10ca2f894c96e`  
		Last Modified: Tue, 30 Apr 2024 00:18:35 GMT  
		Size: 328.9 MB (328870944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134744acef690c38c30d8833ae0f51c33ab028ad42ba68a6750ff9183c82f2d6`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cb52d74238409d3694a77c4786b2b5763fc56e49758eb631cdf9b951c4f2f8`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb8751b1ef1cec318bcb0a44051c7843177bf4e3c7315d9f0d2b5fdda2d9a1b`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca3053940d473c813efdf64f83d17d0aa043aa2ff1ed8bea3cb97742bc9f4cb`  
		Last Modified: Tue, 30 Apr 2024 00:18:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:213946e2a0ef8d8f9cc557dbcc864039e6a7bce5d405b9002df23d6b23f3377c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597891115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3bf3601047020af4549bd74e679f1d4b02aabebdcbc30e858912ac0239b024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 29 Apr 2024 18:06:54 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:06:55 GMT
ARG ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
# Mon, 29 Apr 2024 18:09:33 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:09:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:09:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:09:50 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=ab6ca8c472e544073731b645f37fe3ae6fe02aac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:09:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:09:51 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:09:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:09:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:09:53 GMT
USER odoo
# Mon, 29 Apr 2024 18:09:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:09:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652145f7d82c8a71624671694f21905825351537dd8e342a16c79c0c2015dcaa`  
		Last Modified: Mon, 29 Apr 2024 18:12:08 GMT  
		Size: 330.6 MB (330639407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce851d10cf7c7e6924847d487ada570b4cb8774114d0032b44be84f31e65c789`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57579ba1994b90961b0bb5a15fae3d11b2ae4e83e883aab6d8abfe48f40ef67`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d604e0e3078697cf59b8c5ffc3cf4cb5902d797cec56939b9ad96a54bf7c95`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2ddc8b0937aec9aeef42a814156f066ab6b9deba98ee169dcef8fea4e55c2`  
		Last Modified: Mon, 29 Apr 2024 18:11:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:2e87aabc56efd131dc45324d6534c2c184df98d5c52b6a556a20e226fb7b523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:df05145b9b12fd2d5a8ad0fff2d802c22eca27101111c39d76e51a3142daec88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602484926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934fff6843364f49042c58fa2a60a11aa212b70ac1c1d9f5192d66b4d4af2528`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:07:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 23:07:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 23:07:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 23:07:54 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 23:10:43 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 23:10:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:10:55 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 23:10:55 GMT
ENV ODOO_VERSION=17.0
# Mon, 29 Apr 2024 18:41:28 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:41:28 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Mon, 29 Apr 2024 18:43:27 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:43:31 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:43:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:43:32 GMT
USER odoo
# Mon, 29 Apr 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:43:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b5238fd169df40bd1f85f50944c0aa867267b18d599c3e2c98e2e863058d67`  
		Last Modified: Thu, 25 Apr 2024 23:14:02 GMT  
		Size: 233.7 MB (233722436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58730f4d7be038f1a6a3f32193c54664a29781460243f870e88d75a3bbcf0faf`  
		Last Modified: Thu, 25 Apr 2024 23:13:34 GMT  
		Size: 2.5 MB (2530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997d22c0450ed9a3e548e244da874760547decea70b2a2029c841e8eed5c70ff`  
		Last Modified: Thu, 25 Apr 2024 23:13:34 GMT  
		Size: 459.4 KB (459420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f44067b195a09cc9387a61618db29d137a6963a69912a08638621d2f9cc1d`  
		Last Modified: Mon, 29 Apr 2024 18:47:26 GMT  
		Size: 335.3 MB (335330339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a9ebc13b1e4c918d2d81c52db5d04c3e809758e62485328c60df2e47d41aad`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df2223219524f7ccc2a98acc0baeba4d227f1654246dd3cd9381fdfc52a2688`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f864156a6f2e0f050c0f16f8f4ebc8d1c90dc3a874721c24af9cb5eb4c52c1`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6813bd315402f0c5ad2f018d1afed310f036f27768c3b86e5ee35933cba7261`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:890a369fbeedb87fd850ec28eb0cd337ad85fa3869ce07423d033e1812332a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597448629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c326189ec166da5fbf723a8eea970a45120611fc36940efdc266fb568000`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:25:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:25:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:25:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:25:32 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:31:21 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:31:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:31:38 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:31:38 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Apr 2024 00:13:14 GMT
ARG ODOO_RELEASE=20240429
# Tue, 30 Apr 2024 00:13:14 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Tue, 30 Apr 2024 00:15:20 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Apr 2024 00:15:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 Apr 2024 00:15:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Apr 2024 00:15:29 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Apr 2024 00:15:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Apr 2024 00:15:29 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Apr 2024 00:15:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Apr 2024 00:15:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Apr 2024 00:15:29 GMT
USER odoo
# Tue, 30 Apr 2024 00:15:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 00:15:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187da141906722001c5c359161c4fe85507227149b57a2fbc0d342d6432cc5ea`  
		Last Modified: Thu, 25 Apr 2024 22:34:42 GMT  
		Size: 231.1 MB (231128133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569f8a9def1cf1035c2c0e5425ec4126c5b091a2450610fc976052c36d763d76`  
		Last Modified: Thu, 25 Apr 2024 22:34:23 GMT  
		Size: 2.5 MB (2523264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497241b34f7a0544bba89f995df2b40714055c5de05a0933ce8978b7b12923b2`  
		Last Modified: Thu, 25 Apr 2024 22:34:22 GMT  
		Size: 459.4 KB (459361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d11c305cc98e02d9eab1b0537e16bd9347aaf53bfb33e7962b84c092e103b64`  
		Last Modified: Tue, 30 Apr 2024 00:17:54 GMT  
		Size: 334.9 MB (334934398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235456a379eeae1a954d1cb230f0fed423c509a460316dd13e7c98b2c29e271c`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57895e32ee4978f7324ad7c253ff83ccde4e4d68c38f5f4fc4a91e48f0ad1aeb`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a06517e155c3b3125fc9d6e726a241b0cc90d70f416e2e8ffc168eec09766`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e7d06d6888ae88d6b1104956d8e9f6b6d88c0998870da32abb60ac886e3ee8`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:a313e1c8998cbde3b2616156f8f4abfefd6ab9ed7c24356be33653e60849cc33
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.2 MB (619231999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afafbcd8a9f52e256ab36b3dd0b5d3bce53ace843b9f6b53669b9729625cbeaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:09:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:09:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:09:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:09:04 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:19:56 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:20:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:20:28 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:20:30 GMT
ENV ODOO_VERSION=17.0
# Mon, 29 Apr 2024 18:03:29 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:03:29 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Mon, 29 Apr 2024 18:06:18 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:06:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:06:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:06:36 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:06:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:06:37 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:06:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:06:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:06:39 GMT
USER odoo
# Mon, 29 Apr 2024 18:06:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:06:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb89ed4f3fd92c20d209ee65962139d76e94701ca7dd1ecb0319b3fbfc79a2ea`  
		Last Modified: Thu, 25 Apr 2024 22:25:42 GMT  
		Size: 243.3 MB (243300752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0047e358abc545022c8cc2538c8b6f5acc0dc41dc0d7a2089da028723faf8c8`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 2.8 MB (2806239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab156d194b91801d0e0f992582594aabab33ed2f800afcee7c191f844958720`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 459.4 KB (459389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f379d6a847e39db32b43c629f59e26d981cc2a910402b786b04ff6c99e0513`  
		Last Modified: Mon, 29 Apr 2024 18:10:57 GMT  
		Size: 337.1 MB (337074847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7988b9c34ad91d1042bd8f12be2d8b4522aaf19969f2ef35371a5dc8040c430c`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b32bf0d52180971b1d4c2c8573edd33e1e17b25a4b6b75dec61d513fc6b8248`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c31c3813a18f5fb8da3086a82a887748641e9fb5b97c8b045d8370cc87103`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379f1ec29942b580ef2790c5519abe788d875aa4f85547ebdf9312dd89f5cbfc`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:2e87aabc56efd131dc45324d6534c2c184df98d5c52b6a556a20e226fb7b523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:df05145b9b12fd2d5a8ad0fff2d802c22eca27101111c39d76e51a3142daec88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602484926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934fff6843364f49042c58fa2a60a11aa212b70ac1c1d9f5192d66b4d4af2528`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:07:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 23:07:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 23:07:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 23:07:54 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 23:10:43 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 23:10:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:10:55 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 23:10:55 GMT
ENV ODOO_VERSION=17.0
# Mon, 29 Apr 2024 18:41:28 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:41:28 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Mon, 29 Apr 2024 18:43:27 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:43:31 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:43:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:43:32 GMT
USER odoo
# Mon, 29 Apr 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:43:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b5238fd169df40bd1f85f50944c0aa867267b18d599c3e2c98e2e863058d67`  
		Last Modified: Thu, 25 Apr 2024 23:14:02 GMT  
		Size: 233.7 MB (233722436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58730f4d7be038f1a6a3f32193c54664a29781460243f870e88d75a3bbcf0faf`  
		Last Modified: Thu, 25 Apr 2024 23:13:34 GMT  
		Size: 2.5 MB (2530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997d22c0450ed9a3e548e244da874760547decea70b2a2029c841e8eed5c70ff`  
		Last Modified: Thu, 25 Apr 2024 23:13:34 GMT  
		Size: 459.4 KB (459420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f44067b195a09cc9387a61618db29d137a6963a69912a08638621d2f9cc1d`  
		Last Modified: Mon, 29 Apr 2024 18:47:26 GMT  
		Size: 335.3 MB (335330339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a9ebc13b1e4c918d2d81c52db5d04c3e809758e62485328c60df2e47d41aad`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df2223219524f7ccc2a98acc0baeba4d227f1654246dd3cd9381fdfc52a2688`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f864156a6f2e0f050c0f16f8f4ebc8d1c90dc3a874721c24af9cb5eb4c52c1`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6813bd315402f0c5ad2f018d1afed310f036f27768c3b86e5ee35933cba7261`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:890a369fbeedb87fd850ec28eb0cd337ad85fa3869ce07423d033e1812332a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597448629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c326189ec166da5fbf723a8eea970a45120611fc36940efdc266fb568000`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:25:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:25:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:25:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:25:32 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:31:21 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:31:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:31:38 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:31:38 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Apr 2024 00:13:14 GMT
ARG ODOO_RELEASE=20240429
# Tue, 30 Apr 2024 00:13:14 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Tue, 30 Apr 2024 00:15:20 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Apr 2024 00:15:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 Apr 2024 00:15:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Apr 2024 00:15:29 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Apr 2024 00:15:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Apr 2024 00:15:29 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Apr 2024 00:15:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Apr 2024 00:15:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Apr 2024 00:15:29 GMT
USER odoo
# Tue, 30 Apr 2024 00:15:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 00:15:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187da141906722001c5c359161c4fe85507227149b57a2fbc0d342d6432cc5ea`  
		Last Modified: Thu, 25 Apr 2024 22:34:42 GMT  
		Size: 231.1 MB (231128133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569f8a9def1cf1035c2c0e5425ec4126c5b091a2450610fc976052c36d763d76`  
		Last Modified: Thu, 25 Apr 2024 22:34:23 GMT  
		Size: 2.5 MB (2523264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497241b34f7a0544bba89f995df2b40714055c5de05a0933ce8978b7b12923b2`  
		Last Modified: Thu, 25 Apr 2024 22:34:22 GMT  
		Size: 459.4 KB (459361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d11c305cc98e02d9eab1b0537e16bd9347aaf53bfb33e7962b84c092e103b64`  
		Last Modified: Tue, 30 Apr 2024 00:17:54 GMT  
		Size: 334.9 MB (334934398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235456a379eeae1a954d1cb230f0fed423c509a460316dd13e7c98b2c29e271c`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57895e32ee4978f7324ad7c253ff83ccde4e4d68c38f5f4fc4a91e48f0ad1aeb`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a06517e155c3b3125fc9d6e726a241b0cc90d70f416e2e8ffc168eec09766`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e7d06d6888ae88d6b1104956d8e9f6b6d88c0998870da32abb60ac886e3ee8`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a313e1c8998cbde3b2616156f8f4abfefd6ab9ed7c24356be33653e60849cc33
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.2 MB (619231999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afafbcd8a9f52e256ab36b3dd0b5d3bce53ace843b9f6b53669b9729625cbeaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:09:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:09:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:09:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:09:04 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:19:56 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:20:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:20:28 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:20:30 GMT
ENV ODOO_VERSION=17.0
# Mon, 29 Apr 2024 18:03:29 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:03:29 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Mon, 29 Apr 2024 18:06:18 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:06:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:06:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:06:36 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:06:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:06:37 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:06:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:06:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:06:39 GMT
USER odoo
# Mon, 29 Apr 2024 18:06:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:06:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb89ed4f3fd92c20d209ee65962139d76e94701ca7dd1ecb0319b3fbfc79a2ea`  
		Last Modified: Thu, 25 Apr 2024 22:25:42 GMT  
		Size: 243.3 MB (243300752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0047e358abc545022c8cc2538c8b6f5acc0dc41dc0d7a2089da028723faf8c8`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 2.8 MB (2806239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab156d194b91801d0e0f992582594aabab33ed2f800afcee7c191f844958720`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 459.4 KB (459389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f379d6a847e39db32b43c629f59e26d981cc2a910402b786b04ff6c99e0513`  
		Last Modified: Mon, 29 Apr 2024 18:10:57 GMT  
		Size: 337.1 MB (337074847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7988b9c34ad91d1042bd8f12be2d8b4522aaf19969f2ef35371a5dc8040c430c`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b32bf0d52180971b1d4c2c8573edd33e1e17b25a4b6b75dec61d513fc6b8248`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c31c3813a18f5fb8da3086a82a887748641e9fb5b97c8b045d8370cc87103`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379f1ec29942b580ef2790c5519abe788d875aa4f85547ebdf9312dd89f5cbfc`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:2e87aabc56efd131dc45324d6534c2c184df98d5c52b6a556a20e226fb7b523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:df05145b9b12fd2d5a8ad0fff2d802c22eca27101111c39d76e51a3142daec88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602484926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934fff6843364f49042c58fa2a60a11aa212b70ac1c1d9f5192d66b4d4af2528`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:07:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 23:07:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 23:07:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 23:07:54 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 23:10:43 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 23:10:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:10:55 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 23:10:55 GMT
ENV ODOO_VERSION=17.0
# Mon, 29 Apr 2024 18:41:28 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:41:28 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Mon, 29 Apr 2024 18:43:27 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:43:31 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:43:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:43:32 GMT
USER odoo
# Mon, 29 Apr 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:43:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b5238fd169df40bd1f85f50944c0aa867267b18d599c3e2c98e2e863058d67`  
		Last Modified: Thu, 25 Apr 2024 23:14:02 GMT  
		Size: 233.7 MB (233722436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58730f4d7be038f1a6a3f32193c54664a29781460243f870e88d75a3bbcf0faf`  
		Last Modified: Thu, 25 Apr 2024 23:13:34 GMT  
		Size: 2.5 MB (2530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997d22c0450ed9a3e548e244da874760547decea70b2a2029c841e8eed5c70ff`  
		Last Modified: Thu, 25 Apr 2024 23:13:34 GMT  
		Size: 459.4 KB (459420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f44067b195a09cc9387a61618db29d137a6963a69912a08638621d2f9cc1d`  
		Last Modified: Mon, 29 Apr 2024 18:47:26 GMT  
		Size: 335.3 MB (335330339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a9ebc13b1e4c918d2d81c52db5d04c3e809758e62485328c60df2e47d41aad`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df2223219524f7ccc2a98acc0baeba4d227f1654246dd3cd9381fdfc52a2688`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f864156a6f2e0f050c0f16f8f4ebc8d1c90dc3a874721c24af9cb5eb4c52c1`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6813bd315402f0c5ad2f018d1afed310f036f27768c3b86e5ee35933cba7261`  
		Last Modified: Mon, 29 Apr 2024 18:46:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:890a369fbeedb87fd850ec28eb0cd337ad85fa3869ce07423d033e1812332a15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597448629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c326189ec166da5fbf723a8eea970a45120611fc36940efdc266fb568000`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:25:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:25:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:25:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:25:32 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:31:21 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:31:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:31:38 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:31:38 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Apr 2024 00:13:14 GMT
ARG ODOO_RELEASE=20240429
# Tue, 30 Apr 2024 00:13:14 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Tue, 30 Apr 2024 00:15:20 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Apr 2024 00:15:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 30 Apr 2024 00:15:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Apr 2024 00:15:29 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Apr 2024 00:15:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Apr 2024 00:15:29 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Apr 2024 00:15:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Apr 2024 00:15:29 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Apr 2024 00:15:29 GMT
USER odoo
# Tue, 30 Apr 2024 00:15:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Apr 2024 00:15:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187da141906722001c5c359161c4fe85507227149b57a2fbc0d342d6432cc5ea`  
		Last Modified: Thu, 25 Apr 2024 22:34:42 GMT  
		Size: 231.1 MB (231128133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569f8a9def1cf1035c2c0e5425ec4126c5b091a2450610fc976052c36d763d76`  
		Last Modified: Thu, 25 Apr 2024 22:34:23 GMT  
		Size: 2.5 MB (2523264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497241b34f7a0544bba89f995df2b40714055c5de05a0933ce8978b7b12923b2`  
		Last Modified: Thu, 25 Apr 2024 22:34:22 GMT  
		Size: 459.4 KB (459361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d11c305cc98e02d9eab1b0537e16bd9347aaf53bfb33e7962b84c092e103b64`  
		Last Modified: Tue, 30 Apr 2024 00:17:54 GMT  
		Size: 334.9 MB (334934398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235456a379eeae1a954d1cb230f0fed423c509a460316dd13e7c98b2c29e271c`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57895e32ee4978f7324ad7c253ff83ccde4e4d68c38f5f4fc4a91e48f0ad1aeb`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a06517e155c3b3125fc9d6e726a241b0cc90d70f416e2e8ffc168eec09766`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e7d06d6888ae88d6b1104956d8e9f6b6d88c0998870da32abb60ac886e3ee8`  
		Last Modified: Tue, 30 Apr 2024 00:17:23 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a313e1c8998cbde3b2616156f8f4abfefd6ab9ed7c24356be33653e60849cc33
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.2 MB (619231999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afafbcd8a9f52e256ab36b3dd0b5d3bce53ace843b9f6b53669b9729625cbeaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:09:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:09:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:09:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:09:04 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:19:56 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:20:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:20:28 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:20:30 GMT
ENV ODOO_VERSION=17.0
# Mon, 29 Apr 2024 18:03:29 GMT
ARG ODOO_RELEASE=20240429
# Mon, 29 Apr 2024 18:03:29 GMT
ARG ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
# Mon, 29 Apr 2024 18:06:18 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Apr 2024 18:06:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 29 Apr 2024 18:06:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Apr 2024 18:06:36 GMT
# ARGS: ODOO_RELEASE=20240429 ODOO_SHA=12866ffdf469ce8e4639205bd74d59c211f37ed2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Apr 2024 18:06:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Apr 2024 18:06:37 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Apr 2024 18:06:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Apr 2024 18:06:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Apr 2024 18:06:39 GMT
USER odoo
# Mon, 29 Apr 2024 18:06:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Apr 2024 18:06:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb89ed4f3fd92c20d209ee65962139d76e94701ca7dd1ecb0319b3fbfc79a2ea`  
		Last Modified: Thu, 25 Apr 2024 22:25:42 GMT  
		Size: 243.3 MB (243300752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0047e358abc545022c8cc2538c8b6f5acc0dc41dc0d7a2089da028723faf8c8`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 2.8 MB (2806239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab156d194b91801d0e0f992582594aabab33ed2f800afcee7c191f844958720`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 459.4 KB (459389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f379d6a847e39db32b43c629f59e26d981cc2a910402b786b04ff6c99e0513`  
		Last Modified: Mon, 29 Apr 2024 18:10:57 GMT  
		Size: 337.1 MB (337074847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7988b9c34ad91d1042bd8f12be2d8b4522aaf19969f2ef35371a5dc8040c430c`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b32bf0d52180971b1d4c2c8573edd33e1e17b25a4b6b75dec61d513fc6b8248`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7c31c3813a18f5fb8da3086a82a887748641e9fb5b97c8b045d8370cc87103`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379f1ec29942b580ef2790c5519abe788d875aa4f85547ebdf9312dd89f5cbfc`  
		Last Modified: Mon, 29 Apr 2024 18:10:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
