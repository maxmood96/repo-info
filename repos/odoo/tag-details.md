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
$ docker pull odoo@sha256:d0c41ecb8c1d6a8e9c0c3a54b922548501c0e8dd3e7711c39d1cd92c39d3097f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:8d387526d7b3bdb0a43841a3daffdc74f0cb705c1734fb5bc31851b055faeff6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564064085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1a3698c0024c78716a00dac618c3741bab401a3aa5bd9aed868cbf1d130754`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 13:02:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:02:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:02:38 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:02:38 GMT
ENV ODOO_VERSION=15.0
# Wed, 10 Apr 2024 13:02:38 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 13:02:38 GMT
ARG ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
# Wed, 10 Apr 2024 13:03:49 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 13:03:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 13:03:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 13:03:54 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 13:03:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 13:03:54 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 13:03:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 13:03:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 13:03:54 GMT
USER odoo
# Wed, 10 Apr 2024 13:03:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:03:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2045d8f0213447e0ed9c992443e5b28b28436258f31e1a7f0905c619febed4a`  
		Last Modified: Wed, 10 Apr 2024 13:05:24 GMT  
		Size: 220.3 MB (220292918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d284b698af5472e02d28e56879c21119101db7822e8d9da1cd0c8e56cfaa1`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 2.6 MB (2625949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6128ad9a05b37109de759a4d52717e2b12b67a316a0940e5722bc3062e8db6f`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 458.4 KB (458422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b445db085f290b02d8906d7dfc48b9635ecc1152e24096002518b622dd91a368`  
		Last Modified: Wed, 10 Apr 2024 13:05:33 GMT  
		Size: 309.3 MB (309256597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fe88281e93ba44881c665f96926a52ffe7feb7d2438eb05daf7fa54a60a840`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c9e604e9122af578a847f9f11b4052571e760a9adf0021d40d8002cebcad9`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddd787d49b9b05fcb214170aaf1c15f33435555911b86035de31fe3e0bb63f6`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ab60450c4d21eadfa20587cd8695202dedcc684b04148d9ad17531efd5eef`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:d0c41ecb8c1d6a8e9c0c3a54b922548501c0e8dd3e7711c39d1cd92c39d3097f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:8d387526d7b3bdb0a43841a3daffdc74f0cb705c1734fb5bc31851b055faeff6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564064085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1a3698c0024c78716a00dac618c3741bab401a3aa5bd9aed868cbf1d130754`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 13:02:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:02:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:02:38 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:02:38 GMT
ENV ODOO_VERSION=15.0
# Wed, 10 Apr 2024 13:02:38 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 13:02:38 GMT
ARG ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
# Wed, 10 Apr 2024 13:03:49 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 13:03:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 13:03:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 13:03:54 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 13:03:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 13:03:54 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 13:03:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 13:03:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 13:03:54 GMT
USER odoo
# Wed, 10 Apr 2024 13:03:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:03:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2045d8f0213447e0ed9c992443e5b28b28436258f31e1a7f0905c619febed4a`  
		Last Modified: Wed, 10 Apr 2024 13:05:24 GMT  
		Size: 220.3 MB (220292918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d284b698af5472e02d28e56879c21119101db7822e8d9da1cd0c8e56cfaa1`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 2.6 MB (2625949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6128ad9a05b37109de759a4d52717e2b12b67a316a0940e5722bc3062e8db6f`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 458.4 KB (458422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b445db085f290b02d8906d7dfc48b9635ecc1152e24096002518b622dd91a368`  
		Last Modified: Wed, 10 Apr 2024 13:05:33 GMT  
		Size: 309.3 MB (309256597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fe88281e93ba44881c665f96926a52ffe7feb7d2438eb05daf7fa54a60a840`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796c9e604e9122af578a847f9f11b4052571e760a9adf0021d40d8002cebcad9`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddd787d49b9b05fcb214170aaf1c15f33435555911b86035de31fe3e0bb63f6`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03ab60450c4d21eadfa20587cd8695202dedcc684b04148d9ad17531efd5eef`  
		Last Modified: Wed, 10 Apr 2024 13:04:58 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:cf82ec54966a737c870c59ed935659242588322c080e7e30dd13184b31043db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:12779b212405571c41b5a87dcf898730f4d26c4497e9b234efaf367cdb2a5dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.1 MB (583053407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991d6d7d8349768ca98291027fd45724fbbc71ff71759e95072c59a3956e21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:58:42 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:59:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:00:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:00:02 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:00:02 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 13:00:02 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 13:00:02 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 13:01:23 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 13:01:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 13:01:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 13:01:27 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 13:01:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 13:01:28 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 13:01:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 13:01:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 13:01:28 GMT
USER odoo
# Wed, 10 Apr 2024 13:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:01:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac79b7d43ed31e626ad7d7c9941d7c0a17c43c083711789fb83c11d9110dcfe`  
		Last Modified: Wed, 10 Apr 2024 13:04:36 GMT  
		Size: 219.6 MB (219603194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed26f48190afc427fd1165018baf6a3058a80e56d28e8e3d11097760605dbff`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 2.6 MB (2630065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308ec53827fb3d168639a63a8844a8db71a0d31b340ec755c0fd7b806e82e2f`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 458.4 KB (458435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55103c50d0671a0e74e25733bf563e1b1385308c2f5556417d7bd368bf7f0255`  
		Last Modified: Wed, 10 Apr 2024 13:04:49 GMT  
		Size: 328.9 MB (328931514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ce0132346425c9a36082e1c8d0e18d735a8db67a1e11659fb6f3eb260e5a85`  
		Last Modified: Wed, 10 Apr 2024 13:04:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f415ecaaf69ac8ff8cdcb7a49e86ef42b88c02f26aa3cd23130cd9b71802422`  
		Last Modified: Wed, 10 Apr 2024 13:04:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a959593167855c83078ab92593b745abd498070e040663d1d5ad5cd18acb5255`  
		Last Modified: Wed, 10 Apr 2024 13:04:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88136adb552f2475ba79d225d4c8b8028ed00a4585f9f48c039de7716d9a0db7`  
		Last Modified: Wed, 10 Apr 2024 13:04:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d25324e54f423555d398be28c22753c7f145dd72872033f85ec2b2c49b6fb70b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578656343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edb1eebdb62b7447cbab778e25400df04ffb2bc3b9acb366d95dae2f3a879d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 06:50:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 06:50:11 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:50:11 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 06:51:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 06:51:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:26 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 06:51:26 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 06:52:49 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 06:52:57 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 06:52:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 06:52:57 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 06:52:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 06:52:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 06:52:57 GMT
USER odoo
# Wed, 10 Apr 2024 06:52:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:52:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc553ed1e447dba5d7cd1531a7067a247647cf58771061d9030c71c8b6d14d`  
		Last Modified: Wed, 10 Apr 2024 06:53:31 GMT  
		Size: 216.9 MB (216903831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505728a268c4b89109c2cb3fd49cd9b1dcb63f30c015647bfc1823b0d6774451`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 2.6 MB (2635212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1bbf349d40bf14f17d8931d7c97e93408ecb08a25175182d63b2592b4c6eac`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a8e6a4767bc55af7ea7f4c72631e551d41cffa762efc5b73253398390b1d8`  
		Last Modified: Wed, 10 Apr 2024 06:53:42 GMT  
		Size: 328.6 MB (328580095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10420d0695cf8e799078b908497f64f76b477dba223add41e473ff0f111d500`  
		Last Modified: Wed, 10 Apr 2024 06:53:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac577dfe3513d6f531784319195b12c9d051aeeb1b1f4a38ae5b3d1166e8e98f`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d695a8a535ed74173ccf570325545b1e22d4819c7f7cf75da76d252b805d00`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a80f87e184f87ed1df1e8ac737ca7988f37e7389d3953e463fcfac6c7eab663`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:b000be7d56bb89a61e279293108dc3d25ebc3f1b1ae333649bcdfe39348771e3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b544ebb4a0072205ed70d0d5459c855d81e85f26e5edf838fb338d1e0687112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:11:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:11:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:11:35 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:11:36 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:15:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 12:16:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:16:14 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 12:16:15 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 12:16:16 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 12:16:17 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 12:18:59 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 12:19:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 12:19:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 12:19:15 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 12:19:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 12:19:17 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 12:19:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 12:19:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 12:19:18 GMT
USER odoo
# Wed, 10 Apr 2024 12:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 12:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e559728a938c6bae80d026fa29f2c38efa24baa26b769f31f8c84966d4e1df`  
		Last Modified: Wed, 10 Apr 2024 12:20:10 GMT  
		Size: 228.6 MB (228600553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203ec44cc6f31bfbafaf9862e879fbf8d13940d76cf12c60f413c3d4f7d2413`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 2.9 MB (2876015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe4e2bda71d3574d3ec461cc470d98dc69f9167871208766805ae0ec7e810f`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 458.4 KB (458444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bb59b6134dc895bace6ac001f367ef7df7681d8bb0e8675308b146b5f5fe0`  
		Last Modified: Wed, 10 Apr 2024 12:20:24 GMT  
		Size: 330.4 MB (330358150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9110cd77d7285e0fad9ff5e2b37e63a937f68ecd61c4aa9e602d19637a4e399`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc41657c316f5977709611ffae9798ea44ec41841054cecdfc9956512967de`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aa5a2c270579376228531eac51095da5ab0374e62d177cd7b9d06916b5e113`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2722d07f6e4f03f8bc5f976b559422fa1f74641856112a4306083f23a3784`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:cf82ec54966a737c870c59ed935659242588322c080e7e30dd13184b31043db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:12779b212405571c41b5a87dcf898730f4d26c4497e9b234efaf367cdb2a5dd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.1 MB (583053407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91991d6d7d8349768ca98291027fd45724fbbc71ff71759e95072c59a3956e21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:58:42 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:59:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:00:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:00:02 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:00:02 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 13:00:02 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 13:00:02 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 13:01:23 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 13:01:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 13:01:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 13:01:27 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 13:01:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 13:01:28 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 13:01:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 13:01:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 13:01:28 GMT
USER odoo
# Wed, 10 Apr 2024 13:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:01:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac79b7d43ed31e626ad7d7c9941d7c0a17c43c083711789fb83c11d9110dcfe`  
		Last Modified: Wed, 10 Apr 2024 13:04:36 GMT  
		Size: 219.6 MB (219603194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed26f48190afc427fd1165018baf6a3058a80e56d28e8e3d11097760605dbff`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 2.6 MB (2630065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308ec53827fb3d168639a63a8844a8db71a0d31b340ec755c0fd7b806e82e2f`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 458.4 KB (458435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55103c50d0671a0e74e25733bf563e1b1385308c2f5556417d7bd368bf7f0255`  
		Last Modified: Wed, 10 Apr 2024 13:04:49 GMT  
		Size: 328.9 MB (328931514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ce0132346425c9a36082e1c8d0e18d735a8db67a1e11659fb6f3eb260e5a85`  
		Last Modified: Wed, 10 Apr 2024 13:04:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f415ecaaf69ac8ff8cdcb7a49e86ef42b88c02f26aa3cd23130cd9b71802422`  
		Last Modified: Wed, 10 Apr 2024 13:04:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a959593167855c83078ab92593b745abd498070e040663d1d5ad5cd18acb5255`  
		Last Modified: Wed, 10 Apr 2024 13:04:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88136adb552f2475ba79d225d4c8b8028ed00a4585f9f48c039de7716d9a0db7`  
		Last Modified: Wed, 10 Apr 2024 13:04:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d25324e54f423555d398be28c22753c7f145dd72872033f85ec2b2c49b6fb70b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578656343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edb1eebdb62b7447cbab778e25400df04ffb2bc3b9acb366d95dae2f3a879d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 06:50:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 06:50:11 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:50:11 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 06:51:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 06:51:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:26 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 06:51:26 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 06:52:49 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 06:52:57 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 06:52:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 06:52:57 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 06:52:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 06:52:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 06:52:57 GMT
USER odoo
# Wed, 10 Apr 2024 06:52:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:52:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc553ed1e447dba5d7cd1531a7067a247647cf58771061d9030c71c8b6d14d`  
		Last Modified: Wed, 10 Apr 2024 06:53:31 GMT  
		Size: 216.9 MB (216903831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505728a268c4b89109c2cb3fd49cd9b1dcb63f30c015647bfc1823b0d6774451`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 2.6 MB (2635212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1bbf349d40bf14f17d8931d7c97e93408ecb08a25175182d63b2592b4c6eac`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a8e6a4767bc55af7ea7f4c72631e551d41cffa762efc5b73253398390b1d8`  
		Last Modified: Wed, 10 Apr 2024 06:53:42 GMT  
		Size: 328.6 MB (328580095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10420d0695cf8e799078b908497f64f76b477dba223add41e473ff0f111d500`  
		Last Modified: Wed, 10 Apr 2024 06:53:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac577dfe3513d6f531784319195b12c9d051aeeb1b1f4a38ae5b3d1166e8e98f`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d695a8a535ed74173ccf570325545b1e22d4819c7f7cf75da76d252b805d00`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a80f87e184f87ed1df1e8ac737ca7988f37e7389d3953e463fcfac6c7eab663`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b000be7d56bb89a61e279293108dc3d25ebc3f1b1ae333649bcdfe39348771e3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b544ebb4a0072205ed70d0d5459c855d81e85f26e5edf838fb338d1e0687112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:11:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:11:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:11:35 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:11:36 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:15:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 12:16:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:16:14 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 12:16:15 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 12:16:16 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 12:16:17 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 12:18:59 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 12:19:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 12:19:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 12:19:15 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 12:19:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 12:19:17 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 12:19:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 12:19:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 12:19:18 GMT
USER odoo
# Wed, 10 Apr 2024 12:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 12:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e559728a938c6bae80d026fa29f2c38efa24baa26b769f31f8c84966d4e1df`  
		Last Modified: Wed, 10 Apr 2024 12:20:10 GMT  
		Size: 228.6 MB (228600553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203ec44cc6f31bfbafaf9862e879fbf8d13940d76cf12c60f413c3d4f7d2413`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 2.9 MB (2876015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe4e2bda71d3574d3ec461cc470d98dc69f9167871208766805ae0ec7e810f`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 458.4 KB (458444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bb59b6134dc895bace6ac001f367ef7df7681d8bb0e8675308b146b5f5fe0`  
		Last Modified: Wed, 10 Apr 2024 12:20:24 GMT  
		Size: 330.4 MB (330358150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9110cd77d7285e0fad9ff5e2b37e63a937f68ecd61c4aa9e602d19637a4e399`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc41657c316f5977709611ffae9798ea44ec41841054cecdfc9956512967de`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aa5a2c270579376228531eac51095da5ab0374e62d177cd7b9d06916b5e113`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2722d07f6e4f03f8bc5f976b559422fa1f74641856112a4306083f23a3784`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:f4486384359584ee52dbcfb2731e884fe55757043995b52520bf3e78dcb3ad94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:88c13ebdf5d4d1a22980fd13d3e5a29fdbaad9f0c2f96cfecb377a68c6859914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 MB (601736486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664ffa2315571bfce9f651d3ab2160cb9fff44c797c15cbe4b1594f53542b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 21:04:04 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:04:09 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:04:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:04:09 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:04:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:04:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:04:09 GMT
USER odoo
# Fri, 05 Apr 2024 21:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:04:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03be2acc9355b0f6d9e76cc72d9f69f5ced32e7e2f086bfb9a12a4513d6cf4`  
		Last Modified: Fri, 05 Apr 2024 21:08:17 GMT  
		Size: 334.6 MB (334566422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64e1300180741927f64f634d3b915c421207c43f61407ad0f6f73af1ec78d0`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cefadd0ddd390bb291024573b6ee8b2f808df571becf6a3d9f38b548f343c8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b6346e17bf39dc387d1465d85fbc2dbc9014c612a0ee0729a0cb1ecdf208f8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8fd5127569c85d394e779e66669757a5493748b54ff27bc4810f0e85959b6`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7582c4c8cffc8d74265eb53be18d40725206ea460621bbbbc81c06e71cc34127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596704929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90470a5af1447796a35ed9c68f21f5f0c413cbfcf032d699582af72ea11fee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 03:34:12 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 03:34:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 03:36:14 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 03:36:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 03:36:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 03:36:22 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 03:36:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 03:36:22 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 03:36:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 03:36:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 03:36:22 GMT
USER odoo
# Tue, 16 Apr 2024 03:36:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:36:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c7944e8e2f0264d5eba3087fd5438d1f509ffa6665ca3787558fb8cd4d7408`  
		Last Modified: Tue, 16 Apr 2024 03:37:18 GMT  
		Size: 334.2 MB (334190519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d0a55b9f5e27226a951fa22947de31cdbdd4ee1e1a667314d738eb7aae6e76`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014bc2894e0986a50e8933a955904f24f0c30e6b4791fdb8f661f1fc485cd315`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452a72f5ae8853437450608dc3c9d65ee6316f59fa2ac47d7d0b09b9e3d7e2c4`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc803067bfdeb409956f21d7c4b8460e85b09cd06c32208a0ebc668860041989`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:b3242b265c88b2bcac7b7dc8568b12be7e5d5dfd2cffe0714f3efa22a4d9fb0a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618470261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dc0e91364c2d2f8197b1631e461a6291436820f54d2a217d81758a58951fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 02:27:44 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 02:27:45 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 02:32:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 02:33:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 02:33:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 02:33:21 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 02:33:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 02:33:23 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 02:33:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 02:33:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 02:33:30 GMT
USER odoo
# Tue, 16 Apr 2024 02:33:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 02:33:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac580667a28410cc8979c586c5faffe195d6894c3092f52cb35be46dd5c5c54`  
		Last Modified: Tue, 16 Apr 2024 02:34:44 GMT  
		Size: 336.3 MB (336314723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0871c91966eee2fc05bfe405aa20da9f2eaac7b331b38cae48480c5108ec1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b7e7abc278ed0cd27c5f8030fe2f1942d09b31970cc644d5a191e383b59d1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d04db108cd3503bc3080fe13bbef9199bd448fb19b952d57e8f2a39e57db10`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7a000910544187b0db486222014aa892301fda5291cc5468105a17cc23d155`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:f4486384359584ee52dbcfb2731e884fe55757043995b52520bf3e78dcb3ad94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:88c13ebdf5d4d1a22980fd13d3e5a29fdbaad9f0c2f96cfecb377a68c6859914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 MB (601736486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664ffa2315571bfce9f651d3ab2160cb9fff44c797c15cbe4b1594f53542b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 21:04:04 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:04:09 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:04:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:04:09 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:04:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:04:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:04:09 GMT
USER odoo
# Fri, 05 Apr 2024 21:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:04:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03be2acc9355b0f6d9e76cc72d9f69f5ced32e7e2f086bfb9a12a4513d6cf4`  
		Last Modified: Fri, 05 Apr 2024 21:08:17 GMT  
		Size: 334.6 MB (334566422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64e1300180741927f64f634d3b915c421207c43f61407ad0f6f73af1ec78d0`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cefadd0ddd390bb291024573b6ee8b2f808df571becf6a3d9f38b548f343c8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b6346e17bf39dc387d1465d85fbc2dbc9014c612a0ee0729a0cb1ecdf208f8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8fd5127569c85d394e779e66669757a5493748b54ff27bc4810f0e85959b6`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7582c4c8cffc8d74265eb53be18d40725206ea460621bbbbc81c06e71cc34127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596704929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90470a5af1447796a35ed9c68f21f5f0c413cbfcf032d699582af72ea11fee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 03:34:12 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 03:34:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 03:36:14 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 03:36:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 03:36:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 03:36:22 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 03:36:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 03:36:22 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 03:36:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 03:36:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 03:36:22 GMT
USER odoo
# Tue, 16 Apr 2024 03:36:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:36:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c7944e8e2f0264d5eba3087fd5438d1f509ffa6665ca3787558fb8cd4d7408`  
		Last Modified: Tue, 16 Apr 2024 03:37:18 GMT  
		Size: 334.2 MB (334190519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d0a55b9f5e27226a951fa22947de31cdbdd4ee1e1a667314d738eb7aae6e76`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014bc2894e0986a50e8933a955904f24f0c30e6b4791fdb8f661f1fc485cd315`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452a72f5ae8853437450608dc3c9d65ee6316f59fa2ac47d7d0b09b9e3d7e2c4`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc803067bfdeb409956f21d7c4b8460e85b09cd06c32208a0ebc668860041989`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b3242b265c88b2bcac7b7dc8568b12be7e5d5dfd2cffe0714f3efa22a4d9fb0a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618470261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dc0e91364c2d2f8197b1631e461a6291436820f54d2a217d81758a58951fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 02:27:44 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 02:27:45 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 02:32:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 02:33:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 02:33:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 02:33:21 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 02:33:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 02:33:23 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 02:33:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 02:33:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 02:33:30 GMT
USER odoo
# Tue, 16 Apr 2024 02:33:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 02:33:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac580667a28410cc8979c586c5faffe195d6894c3092f52cb35be46dd5c5c54`  
		Last Modified: Tue, 16 Apr 2024 02:34:44 GMT  
		Size: 336.3 MB (336314723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0871c91966eee2fc05bfe405aa20da9f2eaac7b331b38cae48480c5108ec1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b7e7abc278ed0cd27c5f8030fe2f1942d09b31970cc644d5a191e383b59d1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d04db108cd3503bc3080fe13bbef9199bd448fb19b952d57e8f2a39e57db10`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7a000910544187b0db486222014aa892301fda5291cc5468105a17cc23d155`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:f4486384359584ee52dbcfb2731e884fe55757043995b52520bf3e78dcb3ad94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:88c13ebdf5d4d1a22980fd13d3e5a29fdbaad9f0c2f96cfecb377a68c6859914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 MB (601736486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664ffa2315571bfce9f651d3ab2160cb9fff44c797c15cbe4b1594f53542b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 21:04:04 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:04:09 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:04:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:04:09 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:04:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:04:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:04:09 GMT
USER odoo
# Fri, 05 Apr 2024 21:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:04:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03be2acc9355b0f6d9e76cc72d9f69f5ced32e7e2f086bfb9a12a4513d6cf4`  
		Last Modified: Fri, 05 Apr 2024 21:08:17 GMT  
		Size: 334.6 MB (334566422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64e1300180741927f64f634d3b915c421207c43f61407ad0f6f73af1ec78d0`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cefadd0ddd390bb291024573b6ee8b2f808df571becf6a3d9f38b548f343c8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b6346e17bf39dc387d1465d85fbc2dbc9014c612a0ee0729a0cb1ecdf208f8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8fd5127569c85d394e779e66669757a5493748b54ff27bc4810f0e85959b6`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7582c4c8cffc8d74265eb53be18d40725206ea460621bbbbc81c06e71cc34127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596704929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90470a5af1447796a35ed9c68f21f5f0c413cbfcf032d699582af72ea11fee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 03:34:12 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 03:34:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 03:36:14 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 03:36:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 03:36:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 03:36:22 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 03:36:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 03:36:22 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 03:36:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 03:36:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 03:36:22 GMT
USER odoo
# Tue, 16 Apr 2024 03:36:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:36:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c7944e8e2f0264d5eba3087fd5438d1f509ffa6665ca3787558fb8cd4d7408`  
		Last Modified: Tue, 16 Apr 2024 03:37:18 GMT  
		Size: 334.2 MB (334190519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d0a55b9f5e27226a951fa22947de31cdbdd4ee1e1a667314d738eb7aae6e76`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014bc2894e0986a50e8933a955904f24f0c30e6b4791fdb8f661f1fc485cd315`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452a72f5ae8853437450608dc3c9d65ee6316f59fa2ac47d7d0b09b9e3d7e2c4`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc803067bfdeb409956f21d7c4b8460e85b09cd06c32208a0ebc668860041989`  
		Last Modified: Tue, 16 Apr 2024 03:36:47 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:b3242b265c88b2bcac7b7dc8568b12be7e5d5dfd2cffe0714f3efa22a4d9fb0a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618470261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dc0e91364c2d2f8197b1631e461a6291436820f54d2a217d81758a58951fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 02:27:44 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 02:27:45 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 02:32:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 02:33:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 02:33:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 02:33:21 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 02:33:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 02:33:23 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 02:33:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 02:33:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 02:33:30 GMT
USER odoo
# Tue, 16 Apr 2024 02:33:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 02:33:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac580667a28410cc8979c586c5faffe195d6894c3092f52cb35be46dd5c5c54`  
		Last Modified: Tue, 16 Apr 2024 02:34:44 GMT  
		Size: 336.3 MB (336314723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0871c91966eee2fc05bfe405aa20da9f2eaac7b331b38cae48480c5108ec1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b7e7abc278ed0cd27c5f8030fe2f1942d09b31970cc644d5a191e383b59d1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d04db108cd3503bc3080fe13bbef9199bd448fb19b952d57e8f2a39e57db10`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7a000910544187b0db486222014aa892301fda5291cc5468105a17cc23d155`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
