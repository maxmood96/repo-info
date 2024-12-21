<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241220`](#odoo160-20241220)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241220`](#odoo170-20241220)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241220`](#odoo180-20241220)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:78bf478012be2073cdcb59ae7f932a4707ebcb8923164fcdaa6f13a348bd17e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f7425890d59f31a119f442922825ea8a1d0d9f1e8ccdfcab1f4a3d0c98cbdeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.8 MB (583783603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f95873d5774abced2a29fe8f0db828154a3ba6273f98d23862e6455a9c62154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=C.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=16.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1b993667a3496d65b1f0f325028c0d34469692507d31b06b562ca81fd447a7`  
		Last Modified: Fri, 20 Dec 2024 21:38:43 GMT  
		Size: 219.6 MB (219629117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d8b12b5f461fe35d0fa76b1c3e8acc00b567a19c9f757f567f2f15611283b`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 2.6 MB (2575933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39101b6ecb419b736d34613ef73089ef487508fd342ba3037e39aa4d3bc67985`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 484.1 KB (484108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd43d5bf5ad9585071e0cd6ca86a2407573c959b10e178e32e7716c1088dcbc`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 330.8 MB (330839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14bdb4a8a7cd19494848a20081c3ea5be20c1cf272bb6a08c538b61b4a5a424`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7809c342d15e4425533f9d20597612bc29d215f9b119c068ff8670558c38a104`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f11e314e4990ab33252f71baa7343439c7291a0adb0c2da38eaefef1648bb`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b12df68ac86b69f4678ce2aba599bd141bbfddad7fe37c5d9bcef7a15776ff`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:2baa56f8aaa41293879f3d451a7137b024462ff3e06f55343de502589216c57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38843492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a734b59e539595352f5d8f90b03cc3b4509286f7b4e8afe171e9bb70bddc7dd`

```dockerfile
```

-	Layers:
	-	`sha256:53f874778ad6d21ef19c071d8050320ea37ef02177f09084d9944dcb04909488`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 38.8 MB (38816775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea4370198e071869872bb9ef0848edf74351c72e796a1192f06894425663fd6`  
		Last Modified: Fri, 20 Dec 2024 21:38:40 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3789370df95f3a2b4833a1a3a2623470bf74bad87f62f08c93b3876b4f1289ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.2 MB (579237667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da44cec7eef6b1fbad53816d727f860ed517607a93c145397d3889dd81d685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=C.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=16.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f99f42778b27d577648ab73543149f99f5e4b36cd96ab468bde6f0a3cee6289`  
		Last Modified: Sat, 21 Dec 2024 01:00:36 GMT  
		Size: 216.9 MB (216921814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8e2a21909b4eb01678ce13bb6cea408546cb19a8db2018d456f138db785b70`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 2.6 MB (2583744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4399fafa35bd9a05da829ecdc1feca0f9d5ac356e0d52a963f0581da0108b3a9`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 484.1 KB (484115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fca720cd0711112814e585c27418ba8f3b5ad05e0056e33f1b5477819165c4`  
		Last Modified: Sat, 21 Dec 2024 01:00:38 GMT  
		Size: 330.5 MB (330500636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907cfcc89a77bec86993f50b0beb8da64b7bf0fda735c844b7dca61e0b976c2`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca8037abdfcfd0eafb3256132ed8f47f00db59880802e614abd62d21b5c0860`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547ca5d7a4cdd88cc388f8bec8659e77e84c857b1adbc707ccafb882b7ff29da`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb8ce422d69dce8151c5f27a62e7d71b181e906a1510364c73716293dfb7da`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:85af75ede22b64dc1eec1376bf8573249150a31b8ecbe1f53a52bfd416fb2f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38850115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca0aa8841984e44635fba248ac3eef82cfbf36d252277318e6a0a1f6cb64f70`

```dockerfile
```

-	Layers:
	-	`sha256:52df1ba2fb55dbb40942ab899f8f170015d500fde4e1113e43e7c125ddeec713`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 38.8 MB (38823245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b716b16020f2ca429b0a7fbf5fa28ebcb6a8d55823e83767e6d91c3945ef62c`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:78bf478012be2073cdcb59ae7f932a4707ebcb8923164fcdaa6f13a348bd17e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f7425890d59f31a119f442922825ea8a1d0d9f1e8ccdfcab1f4a3d0c98cbdeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.8 MB (583783603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f95873d5774abced2a29fe8f0db828154a3ba6273f98d23862e6455a9c62154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=C.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=16.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1b993667a3496d65b1f0f325028c0d34469692507d31b06b562ca81fd447a7`  
		Last Modified: Fri, 20 Dec 2024 21:38:43 GMT  
		Size: 219.6 MB (219629117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d8b12b5f461fe35d0fa76b1c3e8acc00b567a19c9f757f567f2f15611283b`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 2.6 MB (2575933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39101b6ecb419b736d34613ef73089ef487508fd342ba3037e39aa4d3bc67985`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 484.1 KB (484108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd43d5bf5ad9585071e0cd6ca86a2407573c959b10e178e32e7716c1088dcbc`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 330.8 MB (330839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14bdb4a8a7cd19494848a20081c3ea5be20c1cf272bb6a08c538b61b4a5a424`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7809c342d15e4425533f9d20597612bc29d215f9b119c068ff8670558c38a104`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f11e314e4990ab33252f71baa7343439c7291a0adb0c2da38eaefef1648bb`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b12df68ac86b69f4678ce2aba599bd141bbfddad7fe37c5d9bcef7a15776ff`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2baa56f8aaa41293879f3d451a7137b024462ff3e06f55343de502589216c57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38843492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a734b59e539595352f5d8f90b03cc3b4509286f7b4e8afe171e9bb70bddc7dd`

```dockerfile
```

-	Layers:
	-	`sha256:53f874778ad6d21ef19c071d8050320ea37ef02177f09084d9944dcb04909488`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 38.8 MB (38816775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea4370198e071869872bb9ef0848edf74351c72e796a1192f06894425663fd6`  
		Last Modified: Fri, 20 Dec 2024 21:38:40 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3789370df95f3a2b4833a1a3a2623470bf74bad87f62f08c93b3876b4f1289ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.2 MB (579237667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da44cec7eef6b1fbad53816d727f860ed517607a93c145397d3889dd81d685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=C.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=16.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f99f42778b27d577648ab73543149f99f5e4b36cd96ab468bde6f0a3cee6289`  
		Last Modified: Sat, 21 Dec 2024 01:00:36 GMT  
		Size: 216.9 MB (216921814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8e2a21909b4eb01678ce13bb6cea408546cb19a8db2018d456f138db785b70`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 2.6 MB (2583744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4399fafa35bd9a05da829ecdc1feca0f9d5ac356e0d52a963f0581da0108b3a9`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 484.1 KB (484115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fca720cd0711112814e585c27418ba8f3b5ad05e0056e33f1b5477819165c4`  
		Last Modified: Sat, 21 Dec 2024 01:00:38 GMT  
		Size: 330.5 MB (330500636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907cfcc89a77bec86993f50b0beb8da64b7bf0fda735c844b7dca61e0b976c2`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca8037abdfcfd0eafb3256132ed8f47f00db59880802e614abd62d21b5c0860`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547ca5d7a4cdd88cc388f8bec8659e77e84c857b1adbc707ccafb882b7ff29da`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb8ce422d69dce8151c5f27a62e7d71b181e906a1510364c73716293dfb7da`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:85af75ede22b64dc1eec1376bf8573249150a31b8ecbe1f53a52bfd416fb2f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38850115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca0aa8841984e44635fba248ac3eef82cfbf36d252277318e6a0a1f6cb64f70`

```dockerfile
```

-	Layers:
	-	`sha256:52df1ba2fb55dbb40942ab899f8f170015d500fde4e1113e43e7c125ddeec713`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 38.8 MB (38823245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b716b16020f2ca429b0a7fbf5fa28ebcb6a8d55823e83767e6d91c3945ef62c`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241220`

```console
$ docker pull odoo@sha256:78bf478012be2073cdcb59ae7f932a4707ebcb8923164fcdaa6f13a348bd17e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241220` - linux; amd64

```console
$ docker pull odoo@sha256:f7425890d59f31a119f442922825ea8a1d0d9f1e8ccdfcab1f4a3d0c98cbdeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.8 MB (583783603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f95873d5774abced2a29fe8f0db828154a3ba6273f98d23862e6455a9c62154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=C.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=16.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1b993667a3496d65b1f0f325028c0d34469692507d31b06b562ca81fd447a7`  
		Last Modified: Fri, 20 Dec 2024 21:38:43 GMT  
		Size: 219.6 MB (219629117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43d8b12b5f461fe35d0fa76b1c3e8acc00b567a19c9f757f567f2f15611283b`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 2.6 MB (2575933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39101b6ecb419b736d34613ef73089ef487508fd342ba3037e39aa4d3bc67985`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 484.1 KB (484108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd43d5bf5ad9585071e0cd6ca86a2407573c959b10e178e32e7716c1088dcbc`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 330.8 MB (330839366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14bdb4a8a7cd19494848a20081c3ea5be20c1cf272bb6a08c538b61b4a5a424`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7809c342d15e4425533f9d20597612bc29d215f9b119c068ff8670558c38a104`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f11e314e4990ab33252f71baa7343439c7291a0adb0c2da38eaefef1648bb`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b12df68ac86b69f4678ce2aba599bd141bbfddad7fe37c5d9bcef7a15776ff`  
		Last Modified: Fri, 20 Dec 2024 21:38:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:2baa56f8aaa41293879f3d451a7137b024462ff3e06f55343de502589216c57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38843492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a734b59e539595352f5d8f90b03cc3b4509286f7b4e8afe171e9bb70bddc7dd`

```dockerfile
```

-	Layers:
	-	`sha256:53f874778ad6d21ef19c071d8050320ea37ef02177f09084d9944dcb04909488`  
		Last Modified: Fri, 20 Dec 2024 21:38:41 GMT  
		Size: 38.8 MB (38816775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea4370198e071869872bb9ef0848edf74351c72e796a1192f06894425663fd6`  
		Last Modified: Fri, 20 Dec 2024 21:38:40 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241220` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3789370df95f3a2b4833a1a3a2623470bf74bad87f62f08c93b3876b4f1289ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.2 MB (579237667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da44cec7eef6b1fbad53816d727f860ed517607a93c145397d3889dd81d685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=C.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=16.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=6312a02426f8b8c8b7578947cd8733e8f042de54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f99f42778b27d577648ab73543149f99f5e4b36cd96ab468bde6f0a3cee6289`  
		Last Modified: Sat, 21 Dec 2024 01:00:36 GMT  
		Size: 216.9 MB (216921814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8e2a21909b4eb01678ce13bb6cea408546cb19a8db2018d456f138db785b70`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 2.6 MB (2583744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4399fafa35bd9a05da829ecdc1feca0f9d5ac356e0d52a963f0581da0108b3a9`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 484.1 KB (484115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fca720cd0711112814e585c27418ba8f3b5ad05e0056e33f1b5477819165c4`  
		Last Modified: Sat, 21 Dec 2024 01:00:38 GMT  
		Size: 330.5 MB (330500636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a907cfcc89a77bec86993f50b0beb8da64b7bf0fda735c844b7dca61e0b976c2`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca8037abdfcfd0eafb3256132ed8f47f00db59880802e614abd62d21b5c0860`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547ca5d7a4cdd88cc388f8bec8659e77e84c857b1adbc707ccafb882b7ff29da`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb8ce422d69dce8151c5f27a62e7d71b181e906a1510364c73716293dfb7da`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:85af75ede22b64dc1eec1376bf8573249150a31b8ecbe1f53a52bfd416fb2f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38850115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca0aa8841984e44635fba248ac3eef82cfbf36d252277318e6a0a1f6cb64f70`

```dockerfile
```

-	Layers:
	-	`sha256:52df1ba2fb55dbb40942ab899f8f170015d500fde4e1113e43e7c125ddeec713`  
		Last Modified: Sat, 21 Dec 2024 01:00:32 GMT  
		Size: 38.8 MB (38823245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b716b16020f2ca429b0a7fbf5fa28ebcb6a8d55823e83767e6d91c3945ef62c`  
		Last Modified: Sat, 21 Dec 2024 01:00:31 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:7366cf959e187480fea19608644edd5ed558d8dafe1d4fa45b28d97545757627
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:8b0d971060f5925fff066af01214d2921f4b5d7d5d00051eba89bef815b889c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 MB (599132670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ffdde288e4ae47b0b02476350814801da7dac67a35a9ba6d4153bd47483894`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2feca412f9e81f41bdbe24ccba304e86d042476a4c38870fbd810f4cd175a`  
		Last Modified: Fri, 20 Dec 2024 21:38:49 GMT  
		Size: 233.8 MB (233785209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ef6548fa597ae3ca87c59062b4c4022b4471bb4931575dda13dda090b64aa`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 2.5 MB (2493420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77ae0631101ec7763345816c22aabecdf3f5354cfe70db8d3f12c2aa08d08b`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 485.2 KB (485163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17565d98d1e3e344b607884b5d1a86485558bef2b05183d28991fdbc9a931c8`  
		Last Modified: Fri, 20 Dec 2024 21:38:50 GMT  
		Size: 332.8 MB (332830748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe09c3047e18bf57cc01c6a33a466ebd26d174db033fded438ebbc54d906ca7`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a748c2ebb60efba2c359ee0078a2592a3f30d0e384b937491dafae811165388`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db63efae760a3ff0f2170c8f3c3036b72d6a16c14d8bba6f386ded225cc6563`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680932bdedf9d22d9d2a8c9b6540ac036369cf307827d6421da88871b75b5171`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:453540e0c1abeb24766f8d8787846cd6ea450d89185d1bcc8c18b23512457ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb3c5a5bf9c7659ce698ed14102b5ce9ff1fb7ea0c375751e869e426b3891b`

```dockerfile
```

-	Layers:
	-	`sha256:57c5cbb9d431254ef0983659941d7bd795ec985c596d90cedf5fb37e702b83a3`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 39.6 MB (39617184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dd49539169300adad47e61bbfaab1e0c2b26a7c920d03ce41744eaddcf8448`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5a73fdf75552f93e12d4ecb945645856ea4a61f13f60c85ec3bec195ec8465b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593928475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29760ede423140587522d4fe462ea00ec514774e8dd2eb829616081e5d6e4dfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374a9e4340a77adfaf37aa8b690de88b5b846cae4816f974c9ff8e3cd7ebd65`  
		Last Modified: Sat, 21 Dec 2024 00:56:45 GMT  
		Size: 231.1 MB (231145582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557bfac97d6ff8b53664087c3e0ced110117eabf311c976a476f5e290dce367c`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 2.5 MB (2485678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf1bc126f1793146545bb0a035c4a500662e18a1f26923cb78730c94e665e2`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 485.1 KB (485131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a385d3cf06c1c981973db9d60c681b3a452636ba43e08e2757113bd486917`  
		Last Modified: Sat, 21 Dec 2024 00:56:51 GMT  
		Size: 332.5 MB (332451313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e05d5b1db3a7e4283f1e1d3f217c8b2649ff9a123ef9eca6cbcd8bbd3df13fb`  
		Last Modified: Sat, 21 Dec 2024 00:56:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697984b16ce4bc6096446aee218d6f8c8f0664704c25831c9b63fc4ff690e59b`  
		Last Modified: Sat, 21 Dec 2024 00:56:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889241a6784662fcc2e366c12ba2f79ce73b0fe8d98c01069aac659e9c297cbf`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af033263648b6f0d051731881123c3546ff9c6a0fa205e778a1d2a736a35b80`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:42f3d77419bb8b4b2973cbc447f98f8b90f81a636b661ae34be81636dd85a2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39650682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f952867f9299d804094bfc1e259b668a6da9e25d45d088c9cc81f5c260f07f`

```dockerfile
```

-	Layers:
	-	`sha256:ee8a755ae4b266e815073419692b04fd6aacab680d21c32a0954444c2d070b36`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 39.6 MB (39623695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3d816409bbe7ffe906428064586ac2abad27702e2fcdd4001a23f56bf4b66b`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:52c5010d8bbebdd6b2c00cd255eceb8e2ab7e84b65610bd906a492843be6084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.6 MB (615594703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68479cec03dfb83ddcea9157175df6241cc389b07451cd03dbdc94df0d15eb19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3511aa35f3f82e9098acbae99da7769e9540c98b1506e84f28888273bb464a73`  
		Last Modified: Sat, 21 Dec 2024 00:03:38 GMT  
		Size: 485.2 KB (485159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d16076f2a6ce44f015c77d1f7ecd1f4e5ea1b4a8b140079a6bb31e2979c0c`  
		Last Modified: Sat, 21 Dec 2024 00:04:12 GMT  
		Size: 334.6 MB (334558523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b769a50dde2a48019c460189bc6239e6531c03bb2767d3a2ab2bb9811e64e5`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759806d39e97546058d221996ed33d826df50938b396eca3affd80408491f86a`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e4453bb777f3fabe90e82716585d65ce5e9585abcd0e60bef9848ef9c4c9d`  
		Last Modified: Sat, 21 Dec 2024 00:03:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221ce28e997a59bb47afca477ed004071d463cc887b30dbb026c34ac68472120`  
		Last Modified: Sat, 21 Dec 2024 00:03:41 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:81ceab4cda7404b8f3b58929cba35255c4eea3eb9990eb73453ef325b53ab6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39652402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc810a72f24ca1730c110fb8ec6f683c6c58c931aa79850dcfece089a35710`

```dockerfile
```

-	Layers:
	-	`sha256:b22b99b324fe85b8ce626f865afbb0cc44741e1db757f67723c99ba2ed8e93ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 39.6 MB (39625511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb38925b08ff01896ba09ff597b12651bff40bf8584ee1e105b765ccbdfbb5a4`  
		Last Modified: Sat, 21 Dec 2024 00:03:38 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7366cf959e187480fea19608644edd5ed558d8dafe1d4fa45b28d97545757627
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:8b0d971060f5925fff066af01214d2921f4b5d7d5d00051eba89bef815b889c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 MB (599132670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ffdde288e4ae47b0b02476350814801da7dac67a35a9ba6d4153bd47483894`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2feca412f9e81f41bdbe24ccba304e86d042476a4c38870fbd810f4cd175a`  
		Last Modified: Fri, 20 Dec 2024 21:38:49 GMT  
		Size: 233.8 MB (233785209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ef6548fa597ae3ca87c59062b4c4022b4471bb4931575dda13dda090b64aa`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 2.5 MB (2493420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77ae0631101ec7763345816c22aabecdf3f5354cfe70db8d3f12c2aa08d08b`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 485.2 KB (485163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17565d98d1e3e344b607884b5d1a86485558bef2b05183d28991fdbc9a931c8`  
		Last Modified: Fri, 20 Dec 2024 21:38:50 GMT  
		Size: 332.8 MB (332830748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe09c3047e18bf57cc01c6a33a466ebd26d174db033fded438ebbc54d906ca7`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a748c2ebb60efba2c359ee0078a2592a3f30d0e384b937491dafae811165388`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db63efae760a3ff0f2170c8f3c3036b72d6a16c14d8bba6f386ded225cc6563`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680932bdedf9d22d9d2a8c9b6540ac036369cf307827d6421da88871b75b5171`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:453540e0c1abeb24766f8d8787846cd6ea450d89185d1bcc8c18b23512457ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb3c5a5bf9c7659ce698ed14102b5ce9ff1fb7ea0c375751e869e426b3891b`

```dockerfile
```

-	Layers:
	-	`sha256:57c5cbb9d431254ef0983659941d7bd795ec985c596d90cedf5fb37e702b83a3`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 39.6 MB (39617184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dd49539169300adad47e61bbfaab1e0c2b26a7c920d03ce41744eaddcf8448`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5a73fdf75552f93e12d4ecb945645856ea4a61f13f60c85ec3bec195ec8465b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593928475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29760ede423140587522d4fe462ea00ec514774e8dd2eb829616081e5d6e4dfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374a9e4340a77adfaf37aa8b690de88b5b846cae4816f974c9ff8e3cd7ebd65`  
		Last Modified: Sat, 21 Dec 2024 00:56:45 GMT  
		Size: 231.1 MB (231145582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557bfac97d6ff8b53664087c3e0ced110117eabf311c976a476f5e290dce367c`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 2.5 MB (2485678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf1bc126f1793146545bb0a035c4a500662e18a1f26923cb78730c94e665e2`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 485.1 KB (485131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a385d3cf06c1c981973db9d60c681b3a452636ba43e08e2757113bd486917`  
		Last Modified: Sat, 21 Dec 2024 00:56:51 GMT  
		Size: 332.5 MB (332451313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e05d5b1db3a7e4283f1e1d3f217c8b2649ff9a123ef9eca6cbcd8bbd3df13fb`  
		Last Modified: Sat, 21 Dec 2024 00:56:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697984b16ce4bc6096446aee218d6f8c8f0664704c25831c9b63fc4ff690e59b`  
		Last Modified: Sat, 21 Dec 2024 00:56:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889241a6784662fcc2e366c12ba2f79ce73b0fe8d98c01069aac659e9c297cbf`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af033263648b6f0d051731881123c3546ff9c6a0fa205e778a1d2a736a35b80`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:42f3d77419bb8b4b2973cbc447f98f8b90f81a636b661ae34be81636dd85a2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39650682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f952867f9299d804094bfc1e259b668a6da9e25d45d088c9cc81f5c260f07f`

```dockerfile
```

-	Layers:
	-	`sha256:ee8a755ae4b266e815073419692b04fd6aacab680d21c32a0954444c2d070b36`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 39.6 MB (39623695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3d816409bbe7ffe906428064586ac2abad27702e2fcdd4001a23f56bf4b66b`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:52c5010d8bbebdd6b2c00cd255eceb8e2ab7e84b65610bd906a492843be6084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.6 MB (615594703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68479cec03dfb83ddcea9157175df6241cc389b07451cd03dbdc94df0d15eb19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3511aa35f3f82e9098acbae99da7769e9540c98b1506e84f28888273bb464a73`  
		Last Modified: Sat, 21 Dec 2024 00:03:38 GMT  
		Size: 485.2 KB (485159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d16076f2a6ce44f015c77d1f7ecd1f4e5ea1b4a8b140079a6bb31e2979c0c`  
		Last Modified: Sat, 21 Dec 2024 00:04:12 GMT  
		Size: 334.6 MB (334558523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b769a50dde2a48019c460189bc6239e6531c03bb2767d3a2ab2bb9811e64e5`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759806d39e97546058d221996ed33d826df50938b396eca3affd80408491f86a`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e4453bb777f3fabe90e82716585d65ce5e9585abcd0e60bef9848ef9c4c9d`  
		Last Modified: Sat, 21 Dec 2024 00:03:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221ce28e997a59bb47afca477ed004071d463cc887b30dbb026c34ac68472120`  
		Last Modified: Sat, 21 Dec 2024 00:03:41 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:81ceab4cda7404b8f3b58929cba35255c4eea3eb9990eb73453ef325b53ab6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39652402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc810a72f24ca1730c110fb8ec6f683c6c58c931aa79850dcfece089a35710`

```dockerfile
```

-	Layers:
	-	`sha256:b22b99b324fe85b8ce626f865afbb0cc44741e1db757f67723c99ba2ed8e93ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 39.6 MB (39625511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb38925b08ff01896ba09ff597b12651bff40bf8584ee1e105b765ccbdfbb5a4`  
		Last Modified: Sat, 21 Dec 2024 00:03:38 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241220`

```console
$ docker pull odoo@sha256:7366cf959e187480fea19608644edd5ed558d8dafe1d4fa45b28d97545757627
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241220` - linux; amd64

```console
$ docker pull odoo@sha256:8b0d971060f5925fff066af01214d2921f4b5d7d5d00051eba89bef815b889c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 MB (599132670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ffdde288e4ae47b0b02476350814801da7dac67a35a9ba6d4153bd47483894`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb2feca412f9e81f41bdbe24ccba304e86d042476a4c38870fbd810f4cd175a`  
		Last Modified: Fri, 20 Dec 2024 21:38:49 GMT  
		Size: 233.8 MB (233785209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ef6548fa597ae3ca87c59062b4c4022b4471bb4931575dda13dda090b64aa`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 2.5 MB (2493420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77ae0631101ec7763345816c22aabecdf3f5354cfe70db8d3f12c2aa08d08b`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 485.2 KB (485163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17565d98d1e3e344b607884b5d1a86485558bef2b05183d28991fdbc9a931c8`  
		Last Modified: Fri, 20 Dec 2024 21:38:50 GMT  
		Size: 332.8 MB (332830748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe09c3047e18bf57cc01c6a33a466ebd26d174db033fded438ebbc54d906ca7`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a748c2ebb60efba2c359ee0078a2592a3f30d0e384b937491dafae811165388`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db63efae760a3ff0f2170c8f3c3036b72d6a16c14d8bba6f386ded225cc6563`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680932bdedf9d22d9d2a8c9b6540ac036369cf307827d6421da88871b75b5171`  
		Last Modified: Fri, 20 Dec 2024 21:38:47 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:453540e0c1abeb24766f8d8787846cd6ea450d89185d1bcc8c18b23512457ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39644019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbb3c5a5bf9c7659ce698ed14102b5ce9ff1fb7ea0c375751e869e426b3891b`

```dockerfile
```

-	Layers:
	-	`sha256:57c5cbb9d431254ef0983659941d7bd795ec985c596d90cedf5fb37e702b83a3`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 39.6 MB (39617184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dd49539169300adad47e61bbfaab1e0c2b26a7c920d03ce41744eaddcf8448`  
		Last Modified: Fri, 20 Dec 2024 21:38:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241220` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5a73fdf75552f93e12d4ecb945645856ea4a61f13f60c85ec3bec195ec8465b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593928475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29760ede423140587522d4fe462ea00ec514774e8dd2eb829616081e5d6e4dfb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374a9e4340a77adfaf37aa8b690de88b5b846cae4816f974c9ff8e3cd7ebd65`  
		Last Modified: Sat, 21 Dec 2024 00:56:45 GMT  
		Size: 231.1 MB (231145582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557bfac97d6ff8b53664087c3e0ced110117eabf311c976a476f5e290dce367c`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 2.5 MB (2485678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf1bc126f1793146545bb0a035c4a500662e18a1f26923cb78730c94e665e2`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 485.1 KB (485131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a385d3cf06c1c981973db9d60c681b3a452636ba43e08e2757113bd486917`  
		Last Modified: Sat, 21 Dec 2024 00:56:51 GMT  
		Size: 332.5 MB (332451313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e05d5b1db3a7e4283f1e1d3f217c8b2649ff9a123ef9eca6cbcd8bbd3df13fb`  
		Last Modified: Sat, 21 Dec 2024 00:56:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697984b16ce4bc6096446aee218d6f8c8f0664704c25831c9b63fc4ff690e59b`  
		Last Modified: Sat, 21 Dec 2024 00:56:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889241a6784662fcc2e366c12ba2f79ce73b0fe8d98c01069aac659e9c297cbf`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af033263648b6f0d051731881123c3546ff9c6a0fa205e778a1d2a736a35b80`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:42f3d77419bb8b4b2973cbc447f98f8b90f81a636b661ae34be81636dd85a2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39650682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f952867f9299d804094bfc1e259b668a6da9e25d45d088c9cc81f5c260f07f`

```dockerfile
```

-	Layers:
	-	`sha256:ee8a755ae4b266e815073419692b04fd6aacab680d21c32a0954444c2d070b36`  
		Last Modified: Sat, 21 Dec 2024 00:56:42 GMT  
		Size: 39.6 MB (39623695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3d816409bbe7ffe906428064586ac2abad27702e2fcdd4001a23f56bf4b66b`  
		Last Modified: Sat, 21 Dec 2024 00:56:40 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241220` - linux; ppc64le

```console
$ docker pull odoo@sha256:52c5010d8bbebdd6b2c00cd255eceb8e2ab7e84b65610bd906a492843be6084e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.6 MB (615594703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68479cec03dfb83ddcea9157175df6241cc389b07451cd03dbdc94df0d15eb19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=17.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=db83c23c2c4a4b5c7881cde0c4d8868c7b9adf10
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3511aa35f3f82e9098acbae99da7769e9540c98b1506e84f28888273bb464a73`  
		Last Modified: Sat, 21 Dec 2024 00:03:38 GMT  
		Size: 485.2 KB (485159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d16076f2a6ce44f015c77d1f7ecd1f4e5ea1b4a8b140079a6bb31e2979c0c`  
		Last Modified: Sat, 21 Dec 2024 00:04:12 GMT  
		Size: 334.6 MB (334558523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b769a50dde2a48019c460189bc6239e6531c03bb2767d3a2ab2bb9811e64e5`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759806d39e97546058d221996ed33d826df50938b396eca3affd80408491f86a`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e4453bb777f3fabe90e82716585d65ce5e9585abcd0e60bef9848ef9c4c9d`  
		Last Modified: Sat, 21 Dec 2024 00:03:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221ce28e997a59bb47afca477ed004071d463cc887b30dbb026c34ac68472120`  
		Last Modified: Sat, 21 Dec 2024 00:03:41 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:81ceab4cda7404b8f3b58929cba35255c4eea3eb9990eb73453ef325b53ab6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39652402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc810a72f24ca1730c110fb8ec6f683c6c58c931aa79850dcfece089a35710`

```dockerfile
```

-	Layers:
	-	`sha256:b22b99b324fe85b8ce626f865afbb0cc44741e1db757f67723c99ba2ed8e93ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:40 GMT  
		Size: 39.6 MB (39625511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb38925b08ff01896ba09ff597b12651bff40bf8584ee1e105b765ccbdfbb5a4`  
		Last Modified: Sat, 21 Dec 2024 00:03:38 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:45359e55db45d18c5910565737a9248bbd8f703f5cfc6727c11e98dde73b72e3
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
$ docker pull odoo@sha256:7210e03d9cf342d483f2364d788e5c9f6caa8d21d45bfa02f027a00f90d2872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.0 MB (664987839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f19506852fd496c1ebd05a70eef134f2766cacea30ed18d85ed5c442f1512e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bfa426956f0d3dee8d467c9cd9fb7dc96944ac5d0043a991f2faf5d776d38`  
		Last Modified: Fri, 20 Dec 2024 21:39:31 GMT  
		Size: 254.5 MB (254517159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beef98c531274f7a65d4291a50cddbff406a305d24cc7f38b379adf8835c046`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 14.2 MB (14231152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a24ab1b689402cd934d251a9807614884ca3c70e5182f449c37997f3331d39`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 484.9 KB (484922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30284ee22cbc96ded71ce8824072c85b59832e9a4fb7202be6cc5a025d19d1`  
		Last Modified: Fri, 20 Dec 2024 21:39:32 GMT  
		Size: 366.0 MB (366000198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb3acb89fe659129b497747dcbdf2e2541e832a9ea8b310103532d8a8f965b9`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc4802ba8f92f149cb5339f35d87829ed8bd95fe7f353585d39625050af4e9d`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408c8d7b0910bff34277d496b992263a791d03370d0e05da546e5916cf99eb0`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f64275041427f94de352287f2a1a005b4dd5b1f0974e6ea4ad8f7671fe9b8`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:67c6a6c8df5b3f10f10b6dd1f7bb0105aa3422011da9b88b10ff2609ccefb785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71132c5faab4ac39bd02cb632c1f1894614eac80ab67c06953d8a45a0e2b1d2`

```dockerfile
```

-	Layers:
	-	`sha256:51a36a76d69fac45ab33579637fcb365457974962797ffed5aac07e7ab91e170`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 58.2 MB (58171271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e306f6b60b73072fa78c1ffdd840ddcbecba1164ecf99c208ecc996ffa8195`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fd818ed4405c1f6e1d114ab9b3e1e00efcdd4ea27c5b15ccf745c79c1a0b2afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.4 MB (661381203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae53dc12a0851afce9cf4ce74b6c1851de89964b7aa7ed917d90e8f83eb8f660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d565ed86e62ed5d5676c9727f5b1a3633ee3969c042d236ac1fba49d667c49c`  
		Last Modified: Sat, 21 Dec 2024 00:50:36 GMT  
		Size: 251.9 MB (251942487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc4a9b6e811923fcc8654b16fbe78b05100b28f0b1f7105f09898bf1bcd42b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 14.2 MB (14204415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b59dc1c63a4356c8a42497e257f940b2c3eab334ecfe5269e8b0d460ca6a1b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 485.0 KB (485011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d94b4db5328e42514c5e9e2b17572618290407965e5af8bb19f3de2a38d787`  
		Last Modified: Sat, 21 Dec 2024 00:50:39 GMT  
		Size: 365.9 MB (365854177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280e70df6a5798c89ff351ee7a8910c89505d590b8b46e26dda7c0460193f467`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db36efb65b60792f80cbc6f9705afc30d0e573cd0ebd9d9ea9705c7caf30d7`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798dc2bcd0476b455d4099407e3dd8a69d2ebc23bdd853dbae9652d82a1ddb5`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9be0be4f2dc32f1ec549f347dd5fdfc08a59a6c5925430f3bd6f09b4ed60cd`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:36ddfe054901074ec59bbcf9dbbd518f1c34eff487dd8bc0e7ac4fa41f95d6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58205861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a251c066c97bff288a5774aeb8485fa42996df00dd3fe97bcfad06b260ff4`

```dockerfile
```

-	Layers:
	-	`sha256:7ee68fd52b224977303ea982458d308d0d8e32e321da5ea107b7f8bc2b1e4c4f`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 58.2 MB (58178562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89feb69451c921a778b3b1db306faa7ddda36fb862d67df5927e0f875e42b5a`  
		Last Modified: Sat, 21 Dec 2024 00:50:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:a43b6e7a5c0239e2dc8f44358966966e924bc8d9c66396206590b8d8f0f05424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 MB (681302860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45071ee7de16f5ebdb8a6a0a5852d5e13f7234698a4150f1d5a3bca966f770b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ffb8de052783553ede75de3dcf047207b1020f389a00dc7c9a47f559006ed`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e4dc279df9bf9857c7a56847be434dc833fe138067b3b7c516c529465fe2`  
		Last Modified: Fri, 20 Dec 2024 23:53:51 GMT  
		Size: 366.6 MB (366560974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a73ab9ec049f7dbe1a13c760320a30e96a77542468b8c4c438ab1a368d5ad77`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdfee60ef90ac7d45c362bf64de028e581bd04626ba0214c735cdf58b951b5`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0ab8fd43d73f1afe89256e0cca811401a095e96c593e2c42d12393ebc7092`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4276f31639907cf9dfbc6cade9bdcbadd750c6180c36e70c745da874d025107`  
		Last Modified: Fri, 20 Dec 2024 23:53:42 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:dab238c2e6d8c020f3b6dc4d1556d7d01ea2ab6a8e4713e59069e64381a777b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58206632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ae390907047a429718eb91f0cd9774fe4d9c835c81bda86973d4d393c3986f`

```dockerfile
```

-	Layers:
	-	`sha256:e6a26a877e33bfca133bfe577c58d8487b46f42c0086f6c84bff728d49f21496`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 58.2 MB (58179434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7d715bdbc52c13dd96ef89af61a8f32550437ff71a7493d7f6769a2df6d3f`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:45359e55db45d18c5910565737a9248bbd8f703f5cfc6727c11e98dde73b72e3
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
$ docker pull odoo@sha256:7210e03d9cf342d483f2364d788e5c9f6caa8d21d45bfa02f027a00f90d2872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.0 MB (664987839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f19506852fd496c1ebd05a70eef134f2766cacea30ed18d85ed5c442f1512e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bfa426956f0d3dee8d467c9cd9fb7dc96944ac5d0043a991f2faf5d776d38`  
		Last Modified: Fri, 20 Dec 2024 21:39:31 GMT  
		Size: 254.5 MB (254517159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beef98c531274f7a65d4291a50cddbff406a305d24cc7f38b379adf8835c046`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 14.2 MB (14231152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a24ab1b689402cd934d251a9807614884ca3c70e5182f449c37997f3331d39`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 484.9 KB (484922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30284ee22cbc96ded71ce8824072c85b59832e9a4fb7202be6cc5a025d19d1`  
		Last Modified: Fri, 20 Dec 2024 21:39:32 GMT  
		Size: 366.0 MB (366000198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb3acb89fe659129b497747dcbdf2e2541e832a9ea8b310103532d8a8f965b9`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc4802ba8f92f149cb5339f35d87829ed8bd95fe7f353585d39625050af4e9d`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408c8d7b0910bff34277d496b992263a791d03370d0e05da546e5916cf99eb0`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f64275041427f94de352287f2a1a005b4dd5b1f0974e6ea4ad8f7671fe9b8`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:67c6a6c8df5b3f10f10b6dd1f7bb0105aa3422011da9b88b10ff2609ccefb785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71132c5faab4ac39bd02cb632c1f1894614eac80ab67c06953d8a45a0e2b1d2`

```dockerfile
```

-	Layers:
	-	`sha256:51a36a76d69fac45ab33579637fcb365457974962797ffed5aac07e7ab91e170`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 58.2 MB (58171271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e306f6b60b73072fa78c1ffdd840ddcbecba1164ecf99c208ecc996ffa8195`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fd818ed4405c1f6e1d114ab9b3e1e00efcdd4ea27c5b15ccf745c79c1a0b2afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.4 MB (661381203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae53dc12a0851afce9cf4ce74b6c1851de89964b7aa7ed917d90e8f83eb8f660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d565ed86e62ed5d5676c9727f5b1a3633ee3969c042d236ac1fba49d667c49c`  
		Last Modified: Sat, 21 Dec 2024 00:50:36 GMT  
		Size: 251.9 MB (251942487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc4a9b6e811923fcc8654b16fbe78b05100b28f0b1f7105f09898bf1bcd42b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 14.2 MB (14204415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b59dc1c63a4356c8a42497e257f940b2c3eab334ecfe5269e8b0d460ca6a1b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 485.0 KB (485011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d94b4db5328e42514c5e9e2b17572618290407965e5af8bb19f3de2a38d787`  
		Last Modified: Sat, 21 Dec 2024 00:50:39 GMT  
		Size: 365.9 MB (365854177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280e70df6a5798c89ff351ee7a8910c89505d590b8b46e26dda7c0460193f467`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db36efb65b60792f80cbc6f9705afc30d0e573cd0ebd9d9ea9705c7caf30d7`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798dc2bcd0476b455d4099407e3dd8a69d2ebc23bdd853dbae9652d82a1ddb5`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9be0be4f2dc32f1ec549f347dd5fdfc08a59a6c5925430f3bd6f09b4ed60cd`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:36ddfe054901074ec59bbcf9dbbd518f1c34eff487dd8bc0e7ac4fa41f95d6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58205861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a251c066c97bff288a5774aeb8485fa42996df00dd3fe97bcfad06b260ff4`

```dockerfile
```

-	Layers:
	-	`sha256:7ee68fd52b224977303ea982458d308d0d8e32e321da5ea107b7f8bc2b1e4c4f`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 58.2 MB (58178562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89feb69451c921a778b3b1db306faa7ddda36fb862d67df5927e0f875e42b5a`  
		Last Modified: Sat, 21 Dec 2024 00:50:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a43b6e7a5c0239e2dc8f44358966966e924bc8d9c66396206590b8d8f0f05424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 MB (681302860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45071ee7de16f5ebdb8a6a0a5852d5e13f7234698a4150f1d5a3bca966f770b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ffb8de052783553ede75de3dcf047207b1020f389a00dc7c9a47f559006ed`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e4dc279df9bf9857c7a56847be434dc833fe138067b3b7c516c529465fe2`  
		Last Modified: Fri, 20 Dec 2024 23:53:51 GMT  
		Size: 366.6 MB (366560974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a73ab9ec049f7dbe1a13c760320a30e96a77542468b8c4c438ab1a368d5ad77`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdfee60ef90ac7d45c362bf64de028e581bd04626ba0214c735cdf58b951b5`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0ab8fd43d73f1afe89256e0cca811401a095e96c593e2c42d12393ebc7092`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4276f31639907cf9dfbc6cade9bdcbadd750c6180c36e70c745da874d025107`  
		Last Modified: Fri, 20 Dec 2024 23:53:42 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:dab238c2e6d8c020f3b6dc4d1556d7d01ea2ab6a8e4713e59069e64381a777b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58206632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ae390907047a429718eb91f0cd9774fe4d9c835c81bda86973d4d393c3986f`

```dockerfile
```

-	Layers:
	-	`sha256:e6a26a877e33bfca133bfe577c58d8487b46f42c0086f6c84bff728d49f21496`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 58.2 MB (58179434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7d715bdbc52c13dd96ef89af61a8f32550437ff71a7493d7f6769a2df6d3f`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241220`

```console
$ docker pull odoo@sha256:45359e55db45d18c5910565737a9248bbd8f703f5cfc6727c11e98dde73b72e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241220` - linux; amd64

```console
$ docker pull odoo@sha256:7210e03d9cf342d483f2364d788e5c9f6caa8d21d45bfa02f027a00f90d2872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.0 MB (664987839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f19506852fd496c1ebd05a70eef134f2766cacea30ed18d85ed5c442f1512e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bfa426956f0d3dee8d467c9cd9fb7dc96944ac5d0043a991f2faf5d776d38`  
		Last Modified: Fri, 20 Dec 2024 21:39:31 GMT  
		Size: 254.5 MB (254517159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beef98c531274f7a65d4291a50cddbff406a305d24cc7f38b379adf8835c046`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 14.2 MB (14231152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a24ab1b689402cd934d251a9807614884ca3c70e5182f449c37997f3331d39`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 484.9 KB (484922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30284ee22cbc96ded71ce8824072c85b59832e9a4fb7202be6cc5a025d19d1`  
		Last Modified: Fri, 20 Dec 2024 21:39:32 GMT  
		Size: 366.0 MB (366000198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb3acb89fe659129b497747dcbdf2e2541e832a9ea8b310103532d8a8f965b9`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc4802ba8f92f149cb5339f35d87829ed8bd95fe7f353585d39625050af4e9d`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408c8d7b0910bff34277d496b992263a791d03370d0e05da546e5916cf99eb0`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f64275041427f94de352287f2a1a005b4dd5b1f0974e6ea4ad8f7671fe9b8`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:67c6a6c8df5b3f10f10b6dd1f7bb0105aa3422011da9b88b10ff2609ccefb785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71132c5faab4ac39bd02cb632c1f1894614eac80ab67c06953d8a45a0e2b1d2`

```dockerfile
```

-	Layers:
	-	`sha256:51a36a76d69fac45ab33579637fcb365457974962797ffed5aac07e7ab91e170`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 58.2 MB (58171271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e306f6b60b73072fa78c1ffdd840ddcbecba1164ecf99c208ecc996ffa8195`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241220` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fd818ed4405c1f6e1d114ab9b3e1e00efcdd4ea27c5b15ccf745c79c1a0b2afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.4 MB (661381203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae53dc12a0851afce9cf4ce74b6c1851de89964b7aa7ed917d90e8f83eb8f660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d565ed86e62ed5d5676c9727f5b1a3633ee3969c042d236ac1fba49d667c49c`  
		Last Modified: Sat, 21 Dec 2024 00:50:36 GMT  
		Size: 251.9 MB (251942487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc4a9b6e811923fcc8654b16fbe78b05100b28f0b1f7105f09898bf1bcd42b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 14.2 MB (14204415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b59dc1c63a4356c8a42497e257f940b2c3eab334ecfe5269e8b0d460ca6a1b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 485.0 KB (485011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d94b4db5328e42514c5e9e2b17572618290407965e5af8bb19f3de2a38d787`  
		Last Modified: Sat, 21 Dec 2024 00:50:39 GMT  
		Size: 365.9 MB (365854177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280e70df6a5798c89ff351ee7a8910c89505d590b8b46e26dda7c0460193f467`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db36efb65b60792f80cbc6f9705afc30d0e573cd0ebd9d9ea9705c7caf30d7`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798dc2bcd0476b455d4099407e3dd8a69d2ebc23bdd853dbae9652d82a1ddb5`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9be0be4f2dc32f1ec549f347dd5fdfc08a59a6c5925430f3bd6f09b4ed60cd`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:36ddfe054901074ec59bbcf9dbbd518f1c34eff487dd8bc0e7ac4fa41f95d6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58205861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a251c066c97bff288a5774aeb8485fa42996df00dd3fe97bcfad06b260ff4`

```dockerfile
```

-	Layers:
	-	`sha256:7ee68fd52b224977303ea982458d308d0d8e32e321da5ea107b7f8bc2b1e4c4f`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 58.2 MB (58178562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89feb69451c921a778b3b1db306faa7ddda36fb862d67df5927e0f875e42b5a`  
		Last Modified: Sat, 21 Dec 2024 00:50:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241220` - linux; ppc64le

```console
$ docker pull odoo@sha256:a43b6e7a5c0239e2dc8f44358966966e924bc8d9c66396206590b8d8f0f05424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 MB (681302860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45071ee7de16f5ebdb8a6a0a5852d5e13f7234698a4150f1d5a3bca966f770b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ffb8de052783553ede75de3dcf047207b1020f389a00dc7c9a47f559006ed`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e4dc279df9bf9857c7a56847be434dc833fe138067b3b7c516c529465fe2`  
		Last Modified: Fri, 20 Dec 2024 23:53:51 GMT  
		Size: 366.6 MB (366560974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a73ab9ec049f7dbe1a13c760320a30e96a77542468b8c4c438ab1a368d5ad77`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdfee60ef90ac7d45c362bf64de028e581bd04626ba0214c735cdf58b951b5`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0ab8fd43d73f1afe89256e0cca811401a095e96c593e2c42d12393ebc7092`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4276f31639907cf9dfbc6cade9bdcbadd750c6180c36e70c745da874d025107`  
		Last Modified: Fri, 20 Dec 2024 23:53:42 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241220` - unknown; unknown

```console
$ docker pull odoo@sha256:dab238c2e6d8c020f3b6dc4d1556d7d01ea2ab6a8e4713e59069e64381a777b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58206632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ae390907047a429718eb91f0cd9774fe4d9c835c81bda86973d4d393c3986f`

```dockerfile
```

-	Layers:
	-	`sha256:e6a26a877e33bfca133bfe577c58d8487b46f42c0086f6c84bff728d49f21496`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 58.2 MB (58179434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7d715bdbc52c13dd96ef89af61a8f32550437ff71a7493d7f6769a2df6d3f`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:45359e55db45d18c5910565737a9248bbd8f703f5cfc6727c11e98dde73b72e3
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
$ docker pull odoo@sha256:7210e03d9cf342d483f2364d788e5c9f6caa8d21d45bfa02f027a00f90d2872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.0 MB (664987839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f19506852fd496c1ebd05a70eef134f2766cacea30ed18d85ed5c442f1512e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=amd64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bfa426956f0d3dee8d467c9cd9fb7dc96944ac5d0043a991f2faf5d776d38`  
		Last Modified: Fri, 20 Dec 2024 21:39:31 GMT  
		Size: 254.5 MB (254517159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beef98c531274f7a65d4291a50cddbff406a305d24cc7f38b379adf8835c046`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 14.2 MB (14231152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a24ab1b689402cd934d251a9807614884ca3c70e5182f449c37997f3331d39`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 484.9 KB (484922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc30284ee22cbc96ded71ce8824072c85b59832e9a4fb7202be6cc5a025d19d1`  
		Last Modified: Fri, 20 Dec 2024 21:39:32 GMT  
		Size: 366.0 MB (366000198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb3acb89fe659129b497747dcbdf2e2541e832a9ea8b310103532d8a8f965b9`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc4802ba8f92f149cb5339f35d87829ed8bd95fe7f353585d39625050af4e9d`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408c8d7b0910bff34277d496b992263a791d03370d0e05da546e5916cf99eb0`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f64275041427f94de352287f2a1a005b4dd5b1f0974e6ea4ad8f7671fe9b8`  
		Last Modified: Fri, 20 Dec 2024 21:39:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:67c6a6c8df5b3f10f10b6dd1f7bb0105aa3422011da9b88b10ff2609ccefb785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58198407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71132c5faab4ac39bd02cb632c1f1894614eac80ab67c06953d8a45a0e2b1d2`

```dockerfile
```

-	Layers:
	-	`sha256:51a36a76d69fac45ab33579637fcb365457974962797ffed5aac07e7ab91e170`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 58.2 MB (58171271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e306f6b60b73072fa78c1ffdd840ddcbecba1164ecf99c208ecc996ffa8195`  
		Last Modified: Fri, 20 Dec 2024 21:39:28 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fd818ed4405c1f6e1d114ab9b3e1e00efcdd4ea27c5b15ccf745c79c1a0b2afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.4 MB (661381203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae53dc12a0851afce9cf4ce74b6c1851de89964b7aa7ed917d90e8f83eb8f660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=arm64
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d565ed86e62ed5d5676c9727f5b1a3633ee3969c042d236ac1fba49d667c49c`  
		Last Modified: Sat, 21 Dec 2024 00:50:36 GMT  
		Size: 251.9 MB (251942487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc4a9b6e811923fcc8654b16fbe78b05100b28f0b1f7105f09898bf1bcd42b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 14.2 MB (14204415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b59dc1c63a4356c8a42497e257f940b2c3eab334ecfe5269e8b0d460ca6a1b`  
		Last Modified: Sat, 21 Dec 2024 00:50:31 GMT  
		Size: 485.0 KB (485011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d94b4db5328e42514c5e9e2b17572618290407965e5af8bb19f3de2a38d787`  
		Last Modified: Sat, 21 Dec 2024 00:50:39 GMT  
		Size: 365.9 MB (365854177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280e70df6a5798c89ff351ee7a8910c89505d590b8b46e26dda7c0460193f467`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db36efb65b60792f80cbc6f9705afc30d0e573cd0ebd9d9ea9705c7caf30d7`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798dc2bcd0476b455d4099407e3dd8a69d2ebc23bdd853dbae9652d82a1ddb5`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9be0be4f2dc32f1ec549f347dd5fdfc08a59a6c5925430f3bd6f09b4ed60cd`  
		Last Modified: Sat, 21 Dec 2024 00:50:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:36ddfe054901074ec59bbcf9dbbd518f1c34eff487dd8bc0e7ac4fa41f95d6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58205861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048a251c066c97bff288a5774aeb8485fa42996df00dd3fe97bcfad06b260ff4`

```dockerfile
```

-	Layers:
	-	`sha256:7ee68fd52b224977303ea982458d308d0d8e32e321da5ea107b7f8bc2b1e4c4f`  
		Last Modified: Sat, 21 Dec 2024 00:50:32 GMT  
		Size: 58.2 MB (58178562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89feb69451c921a778b3b1db306faa7ddda36fb862d67df5927e0f875e42b5a`  
		Last Modified: Sat, 21 Dec 2024 00:50:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a43b6e7a5c0239e2dc8f44358966966e924bc8d9c66396206590b8d8f0f05424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.3 MB (681302860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45071ee7de16f5ebdb8a6a0a5852d5e13f7234698a4150f1d5a3bca966f770b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 14:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 20 Dec 2024 14:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2024 14:50:55 GMT
ARG TARGETARCH=ppc64le
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_VERSION=18.0
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_RELEASE=20241220
# Fri, 20 Dec 2024 14:50:55 GMT
ARG ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241220 ODOO_SHA=449cd495882dc0f35bc11632414fcdc585ed350e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 20 Dec 2024 14:50:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 20 Dec 2024 14:50:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 20 Dec 2024 14:50:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 20 Dec 2024 14:50:55 GMT
USER odoo
# Fri, 20 Dec 2024 14:50:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Dec 2024 14:50:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ffb8de052783553ede75de3dcf047207b1020f389a00dc7c9a47f559006ed`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e4dc279df9bf9857c7a56847be434dc833fe138067b3b7c516c529465fe2`  
		Last Modified: Fri, 20 Dec 2024 23:53:51 GMT  
		Size: 366.6 MB (366560974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a73ab9ec049f7dbe1a13c760320a30e96a77542468b8c4c438ab1a368d5ad77`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fdfee60ef90ac7d45c362bf64de028e581bd04626ba0214c735cdf58b951b5`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf0ab8fd43d73f1afe89256e0cca811401a095e96c593e2c42d12393ebc7092`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4276f31639907cf9dfbc6cade9bdcbadd750c6180c36e70c745da874d025107`  
		Last Modified: Fri, 20 Dec 2024 23:53:42 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:dab238c2e6d8c020f3b6dc4d1556d7d01ea2ab6a8e4713e59069e64381a777b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58206632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ae390907047a429718eb91f0cd9774fe4d9c835c81bda86973d4d393c3986f`

```dockerfile
```

-	Layers:
	-	`sha256:e6a26a877e33bfca133bfe577c58d8487b46f42c0086f6c84bff728d49f21496`  
		Last Modified: Fri, 20 Dec 2024 23:53:41 GMT  
		Size: 58.2 MB (58179434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7d715bdbc52c13dd96ef89af61a8f32550437ff71a7493d7f6769a2df6d3f`  
		Last Modified: Fri, 20 Dec 2024 23:53:39 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
