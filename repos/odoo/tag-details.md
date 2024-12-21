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
$ docker pull odoo@sha256:ba007863b81519fd1637dec658781b73dca853baad23f84b0853728690b189c0
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
$ docker pull odoo@sha256:c89ab2babc3b62b5bfd5345ca3ccfd5ea7a94304a54326834b3f82559db2e39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.2 MB (579199918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2b828407421cbb87ea24a7a0060e4aa2fe3cbba5f4bf032e81d860f0ee45b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867e2cf663da3bb6518512f039899bf488edba93373554da5dfc29e3635e070`  
		Last Modified: Tue, 03 Dec 2024 06:38:15 GMT  
		Size: 216.9 MB (216921221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7f5c8836bd40090ae1e0762c3ff13bbca719cc7eafba1e4d62f9a44421ac4`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 2.6 MB (2583699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c271b056c038408296c949bbbf1934c1b2eeba44d7d751cfc8845f6ce025eb`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 484.1 KB (484106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ef8db0cdb7bedd9502d3ed3965fc4a1142091f5625f2a86325bdba1990291e`  
		Last Modified: Tue, 10 Dec 2024 00:42:20 GMT  
		Size: 330.5 MB (330463536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e136835b791363dfc29526946ed5055e2fc48544ee9cc4d5be6059cab3a1d`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c5ec9b8bd390d0466ace7d8131f8bc8963d7c3d824484ea79b1e847adc830`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658d46ff798c442f4c576b4de6c0ea783260005f7c65b9facd6f85a6830d96a`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9231fd11ef2b2f8784565e1f3db7d5078068dbacb34cab08df342f938a5ad`  
		Last Modified: Tue, 10 Dec 2024 00:42:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:4b5438444505f816c90308bffe178ee998f06fade2db8fbb6bbd578984854d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38906460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ffdf4595f753319a7d8dcfac1860ff01e64118eaceb8631379917c919c3a50`

```dockerfile
```

-	Layers:
	-	`sha256:c0378423225ab6687d7549a7c8982daaa94ee87bd57fca585f7edf528dc43659`  
		Last Modified: Tue, 10 Dec 2024 00:42:14 GMT  
		Size: 38.9 MB (38879591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a544cfc419510ae6c08ef00a80fe7f647f879afb1bea429b3d410028a78f1f9`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:ba007863b81519fd1637dec658781b73dca853baad23f84b0853728690b189c0
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
$ docker pull odoo@sha256:c89ab2babc3b62b5bfd5345ca3ccfd5ea7a94304a54326834b3f82559db2e39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.2 MB (579199918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2b828407421cbb87ea24a7a0060e4aa2fe3cbba5f4bf032e81d860f0ee45b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867e2cf663da3bb6518512f039899bf488edba93373554da5dfc29e3635e070`  
		Last Modified: Tue, 03 Dec 2024 06:38:15 GMT  
		Size: 216.9 MB (216921221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7f5c8836bd40090ae1e0762c3ff13bbca719cc7eafba1e4d62f9a44421ac4`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 2.6 MB (2583699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c271b056c038408296c949bbbf1934c1b2eeba44d7d751cfc8845f6ce025eb`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 484.1 KB (484106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ef8db0cdb7bedd9502d3ed3965fc4a1142091f5625f2a86325bdba1990291e`  
		Last Modified: Tue, 10 Dec 2024 00:42:20 GMT  
		Size: 330.5 MB (330463536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e136835b791363dfc29526946ed5055e2fc48544ee9cc4d5be6059cab3a1d`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3c5ec9b8bd390d0466ace7d8131f8bc8963d7c3d824484ea79b1e847adc830`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658d46ff798c442f4c576b4de6c0ea783260005f7c65b9facd6f85a6830d96a`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9231fd11ef2b2f8784565e1f3db7d5078068dbacb34cab08df342f938a5ad`  
		Last Modified: Tue, 10 Dec 2024 00:42:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4b5438444505f816c90308bffe178ee998f06fade2db8fbb6bbd578984854d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38906460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ffdf4595f753319a7d8dcfac1860ff01e64118eaceb8631379917c919c3a50`

```dockerfile
```

-	Layers:
	-	`sha256:c0378423225ab6687d7549a7c8982daaa94ee87bd57fca585f7edf528dc43659`  
		Last Modified: Tue, 10 Dec 2024 00:42:14 GMT  
		Size: 38.9 MB (38879591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a544cfc419510ae6c08ef00a80fe7f647f879afb1bea429b3d410028a78f1f9`  
		Last Modified: Tue, 10 Dec 2024 00:42:13 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241220`

```console
$ docker pull odoo@sha256:0a1f984a159d2fa0922fb3e084e5c15779ea65ed3060bd8d60664e8a81e4827d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `odoo:17`

```console
$ docker pull odoo@sha256:cd9aa9c10f3c8a0483d78e5694261c766ffe6cbfecc92e8497be07fa01c55162
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
$ docker pull odoo@sha256:339efb13b9b865cfa65fb3e7891be14aaf7c8ef7298e63ddd6fa6e520540b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593816588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f47ef0eb9264329ad8bdb2f56394519666a2517c31d73191d04a7bc82d216e2`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a7f3d060a5bf024bd57abc2f342cb13d31ea4333270f2cbc6bad56c37f9965`  
		Last Modified: Tue, 10 Dec 2024 00:39:23 GMT  
		Size: 332.3 MB (332346448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557f45c5e72f562c58f6a04ea0aaebba9685b13d0d31aa68968d44a59aa674ec`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6425793df87f3749808de310cbc23a32cee02f7f662d8fe14ea93c212df94c6d`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae7b5350f2ba9f9708f7bfc5b65a64a5395a402310f86bf7986cf794cce102b`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c3c007a16e23d409467a8aee069b8f8b814a07bece0fd37cbc0bd5438a3d7e`  
		Last Modified: Tue, 10 Dec 2024 00:39:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b08fc3a88b7aa890df376bb4be7e47269e1f16df91c6b5330a621edffc0274a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39689750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194b2348b7fccca3befdce28e4702e27dfbbe11e48c96c436bdd446e63cfd2a9`

```dockerfile
```

-	Layers:
	-	`sha256:59242a948e255e8cfebae1fb5ac12b570cd6600fe06f0c583eb8344f9dfa97d1`  
		Last Modified: Tue, 10 Dec 2024 00:39:17 GMT  
		Size: 39.7 MB (39662763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f971cf71c3b3846d6f8d64ecc78b905a53d4497df2d69d8a8d49b86c48b3a37`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ea280dccc1f80308752f64135a3e4afe77f31652fcb348ee7f8e943a5b995ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 MB (615484511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3ad633f47121247ddfba986ca423408ae6b4e05ba7d7e1ebf4a71752935200`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6497668f768c587276c268c6f71e055cb24f2360455d344f69d4a8e75dc29bf`  
		Last Modified: Mon, 09 Dec 2024 19:45:49 GMT  
		Size: 334.5 MB (334467899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b12dffad1f7790d376788e0ec2d86add55a2e85c0036ff7f0d7a0796035fd`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdd61f27b5789a42d38a5518d8c488c47a2f3eee10399b5b1fe6dd123e788`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed81c73a790c12c2e5c7d3c17e489689f339d19887aa1fb873e7ecfdb50597`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f2a1198f20279fe5e2be8d64e351602d498240e28cb402b54a73234745643c`  
		Last Modified: Mon, 09 Dec 2024 19:45:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:56cedb53a56eaa16cab20d10e4067aac47b1a51e932d9cf5013411db88ce20c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39691464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d4e034d9666b0ed70244002b9dd2a8a9089a133e20911891805cd50c75fbe`

```dockerfile
```

-	Layers:
	-	`sha256:02a27a42d7bf15381c77ee8ddb27e6eef2b60bea219ba97166e116dff98b5bea`  
		Last Modified: Mon, 09 Dec 2024 19:45:30 GMT  
		Size: 39.7 MB (39664573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7294ecb42656ca2cd9a1242e9ad2579db14d3ed71a347a374efa39522448a3`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cd9aa9c10f3c8a0483d78e5694261c766ffe6cbfecc92e8497be07fa01c55162
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
$ docker pull odoo@sha256:339efb13b9b865cfa65fb3e7891be14aaf7c8ef7298e63ddd6fa6e520540b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 MB (593816588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f47ef0eb9264329ad8bdb2f56394519666a2517c31d73191d04a7bc82d216e2`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a7f3d060a5bf024bd57abc2f342cb13d31ea4333270f2cbc6bad56c37f9965`  
		Last Modified: Tue, 10 Dec 2024 00:39:23 GMT  
		Size: 332.3 MB (332346448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557f45c5e72f562c58f6a04ea0aaebba9685b13d0d31aa68968d44a59aa674ec`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6425793df87f3749808de310cbc23a32cee02f7f662d8fe14ea93c212df94c6d`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae7b5350f2ba9f9708f7bfc5b65a64a5395a402310f86bf7986cf794cce102b`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c3c007a16e23d409467a8aee069b8f8b814a07bece0fd37cbc0bd5438a3d7e`  
		Last Modified: Tue, 10 Dec 2024 00:39:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b08fc3a88b7aa890df376bb4be7e47269e1f16df91c6b5330a621edffc0274a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39689750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194b2348b7fccca3befdce28e4702e27dfbbe11e48c96c436bdd446e63cfd2a9`

```dockerfile
```

-	Layers:
	-	`sha256:59242a948e255e8cfebae1fb5ac12b570cd6600fe06f0c583eb8344f9dfa97d1`  
		Last Modified: Tue, 10 Dec 2024 00:39:17 GMT  
		Size: 39.7 MB (39662763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f971cf71c3b3846d6f8d64ecc78b905a53d4497df2d69d8a8d49b86c48b3a37`  
		Last Modified: Tue, 10 Dec 2024 00:39:15 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ea280dccc1f80308752f64135a3e4afe77f31652fcb348ee7f8e943a5b995ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 MB (615484511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3ad633f47121247ddfba986ca423408ae6b4e05ba7d7e1ebf4a71752935200`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6497668f768c587276c268c6f71e055cb24f2360455d344f69d4a8e75dc29bf`  
		Last Modified: Mon, 09 Dec 2024 19:45:49 GMT  
		Size: 334.5 MB (334467899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b12dffad1f7790d376788e0ec2d86add55a2e85c0036ff7f0d7a0796035fd`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdd61f27b5789a42d38a5518d8c488c47a2f3eee10399b5b1fe6dd123e788`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed81c73a790c12c2e5c7d3c17e489689f339d19887aa1fb873e7ecfdb50597`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f2a1198f20279fe5e2be8d64e351602d498240e28cb402b54a73234745643c`  
		Last Modified: Mon, 09 Dec 2024 19:45:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:56cedb53a56eaa16cab20d10e4067aac47b1a51e932d9cf5013411db88ce20c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39691464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d4e034d9666b0ed70244002b9dd2a8a9089a133e20911891805cd50c75fbe`

```dockerfile
```

-	Layers:
	-	`sha256:02a27a42d7bf15381c77ee8ddb27e6eef2b60bea219ba97166e116dff98b5bea`  
		Last Modified: Mon, 09 Dec 2024 19:45:30 GMT  
		Size: 39.7 MB (39664573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7294ecb42656ca2cd9a1242e9ad2579db14d3ed71a347a374efa39522448a3`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241220`

```console
$ docker pull odoo@sha256:89029c3a7939309e619ffc2404409bffe5e1458f02fd9da9040cd12997411cc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `odoo:18`

```console
$ docker pull odoo@sha256:7168535457c1c610e3a4b280da5d18d29dce447f4724577ac892b18f9ad4ed75
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
$ docker pull odoo@sha256:2b2c743d28d167082cb6eecf2b2df2b734a306db9b8216375f86bf1a3d77ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.9 MB (658926368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a06786d527bd62ec376b7ccc743bbcbfa3a1216393461a40a332ed7bd18ba0e`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ecc3c41deba94deef9ef13230d21616fb856dd13b8ec0c592f3063a955318`  
		Last Modified: Tue, 03 Dec 2024 06:34:32 GMT  
		Size: 251.9 MB (251940434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730fbb6c4e05b09f822891bb1f189de5a363ff7032d6a5a5efec25322b27e42`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 14.2 MB (14204438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc74bc45ed2dfba386983367267b64df94f08164c3f10d6b199347554437c7`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5275c526cd5acb9cb27cfd5cb4dbda297a000fe1ab00e3258af2da1bdb20e9da`  
		Last Modified: Tue, 10 Dec 2024 00:35:20 GMT  
		Size: 363.4 MB (363401473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de11f687b0879ecc6ba735afc99f76c55b9882012caf3c033458f8b09acfb3`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabc91eab166031033ab6b0866ef7fc77e7dac970c70a4dfed015245474e4d48`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3099f781866843996e636081e569992f22d0f9e24b400d2ee0d0fb0c805a256`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecbc88ebb9d5f3a0ab100409136473945ff2f65ff684f5b846efeb308d262db`  
		Last Modified: Tue, 10 Dec 2024 00:35:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1fdc1f7020ec604c5d4c6980aea36262c31140d432f23dad691404098bbbebd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57758519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20a4e9aa1ae1b30e5cf56fceae5a49bd0b41f2b316c3bb746b56d0d3db023df`

```dockerfile
```

-	Layers:
	-	`sha256:928fc9f80af26ed5f4d27d77200111f4a9da2ab758aaf9928b2e701fabf61499`  
		Last Modified: Tue, 10 Dec 2024 00:35:15 GMT  
		Size: 57.7 MB (57731219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0619efda1d05c1d619535239ad389153c9a3918dbfe3681c0c538928aed23a1d`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:7168535457c1c610e3a4b280da5d18d29dce447f4724577ac892b18f9ad4ed75
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
$ docker pull odoo@sha256:2b2c743d28d167082cb6eecf2b2df2b734a306db9b8216375f86bf1a3d77ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.9 MB (658926368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a06786d527bd62ec376b7ccc743bbcbfa3a1216393461a40a332ed7bd18ba0e`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ecc3c41deba94deef9ef13230d21616fb856dd13b8ec0c592f3063a955318`  
		Last Modified: Tue, 03 Dec 2024 06:34:32 GMT  
		Size: 251.9 MB (251940434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730fbb6c4e05b09f822891bb1f189de5a363ff7032d6a5a5efec25322b27e42`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 14.2 MB (14204438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc74bc45ed2dfba386983367267b64df94f08164c3f10d6b199347554437c7`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5275c526cd5acb9cb27cfd5cb4dbda297a000fe1ab00e3258af2da1bdb20e9da`  
		Last Modified: Tue, 10 Dec 2024 00:35:20 GMT  
		Size: 363.4 MB (363401473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de11f687b0879ecc6ba735afc99f76c55b9882012caf3c033458f8b09acfb3`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabc91eab166031033ab6b0866ef7fc77e7dac970c70a4dfed015245474e4d48`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3099f781866843996e636081e569992f22d0f9e24b400d2ee0d0fb0c805a256`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecbc88ebb9d5f3a0ab100409136473945ff2f65ff684f5b846efeb308d262db`  
		Last Modified: Tue, 10 Dec 2024 00:35:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1fdc1f7020ec604c5d4c6980aea36262c31140d432f23dad691404098bbbebd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57758519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20a4e9aa1ae1b30e5cf56fceae5a49bd0b41f2b316c3bb746b56d0d3db023df`

```dockerfile
```

-	Layers:
	-	`sha256:928fc9f80af26ed5f4d27d77200111f4a9da2ab758aaf9928b2e701fabf61499`  
		Last Modified: Tue, 10 Dec 2024 00:35:15 GMT  
		Size: 57.7 MB (57731219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0619efda1d05c1d619535239ad389153c9a3918dbfe3681c0c538928aed23a1d`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241220`

```console
$ docker pull odoo@sha256:d41ad51466f339e12c05dc4094fdabe1ef0b3aa82380c7b989d40910681ff75b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `odoo:latest`

```console
$ docker pull odoo@sha256:7168535457c1c610e3a4b280da5d18d29dce447f4724577ac892b18f9ad4ed75
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
$ docker pull odoo@sha256:2b2c743d28d167082cb6eecf2b2df2b734a306db9b8216375f86bf1a3d77ef62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.9 MB (658926368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a06786d527bd62ec376b7ccc743bbcbfa3a1216393461a40a332ed7bd18ba0e`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=arm64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ecc3c41deba94deef9ef13230d21616fb856dd13b8ec0c592f3063a955318`  
		Last Modified: Tue, 03 Dec 2024 06:34:32 GMT  
		Size: 251.9 MB (251940434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730fbb6c4e05b09f822891bb1f189de5a363ff7032d6a5a5efec25322b27e42`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 14.2 MB (14204438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc74bc45ed2dfba386983367267b64df94f08164c3f10d6b199347554437c7`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5275c526cd5acb9cb27cfd5cb4dbda297a000fe1ab00e3258af2da1bdb20e9da`  
		Last Modified: Tue, 10 Dec 2024 00:35:20 GMT  
		Size: 363.4 MB (363401473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93de11f687b0879ecc6ba735afc99f76c55b9882012caf3c033458f8b09acfb3`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabc91eab166031033ab6b0866ef7fc77e7dac970c70a4dfed015245474e4d48`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3099f781866843996e636081e569992f22d0f9e24b400d2ee0d0fb0c805a256`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecbc88ebb9d5f3a0ab100409136473945ff2f65ff684f5b846efeb308d262db`  
		Last Modified: Tue, 10 Dec 2024 00:35:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1fdc1f7020ec604c5d4c6980aea36262c31140d432f23dad691404098bbbebd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57758519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20a4e9aa1ae1b30e5cf56fceae5a49bd0b41f2b316c3bb746b56d0d3db023df`

```dockerfile
```

-	Layers:
	-	`sha256:928fc9f80af26ed5f4d27d77200111f4a9da2ab758aaf9928b2e701fabf61499`  
		Last Modified: Tue, 10 Dec 2024 00:35:15 GMT  
		Size: 57.7 MB (57731219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0619efda1d05c1d619535239ad389153c9a3918dbfe3681c0c538928aed23a1d`  
		Last Modified: Tue, 10 Dec 2024 00:35:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
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
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json
