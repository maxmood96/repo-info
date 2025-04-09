<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250401`](#odoo160-20250401)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250401`](#odoo170-20250401)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250401`](#odoo180-20250401)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:b15777c3fbfab60c89772e7ec232e6f023f5daa20f7653278136e0133ec8baa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:ab64166456f725698342bde123d41db18a44ddc5175a4754168ae73b71f89753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584601434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe5132729480b3cd90e7400d03b35fe548ace51f75194812e7c1250ce316cb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77efbe21c55698efe60bf6e806e71ecd48fcb100da94c8ac1f538a70ec204e46`  
		Last Modified: Tue, 08 Apr 2025 01:39:43 GMT  
		Size: 219.6 MB (219625682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a88e42e1ae01faecc29ab081c04b35ddc8436b7623a9950c1fd5a7f64563a3`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 2.6 MB (2623334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ad070d3ca4c80cd584e4afe563d52e0ce5005db6608278e811d526c050e82`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaadb07ed1523aa3b67fc253307013f5d4152459e9551ed92692549b37a6f81`  
		Last Modified: Tue, 08 Apr 2025 01:39:44 GMT  
		Size: 331.6 MB (331614779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d3d248f77813f66d044f05f0a9a4492c82f30968c2b4fdcf4020011f2271e`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710a0761438dc000b0ffc6b4c53bd9019b08d450baf455b6bea5ad1fe4a5e745`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a52000065c4297be89c247c83764540c1fc92c47520c77ff8d5cfd397816d5`  
		Last Modified: Tue, 08 Apr 2025 01:39:41 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851728c4b8431dec809337ea3f2ce4aa9f9e91ebc46a3eef0edfc76355520a`  
		Last Modified: Tue, 08 Apr 2025 01:39:41 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:693a9a5c1ec0d678e945c2f1e7a2912fe47c18bdbf9d185c9f94be1f3c877e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26789bc3954188cdadecd287cdb1c59cd4f3bc9b98fe116bdc9b494a1e64abf`

```dockerfile
```

-	Layers:
	-	`sha256:4375f979d86285d4e284d3210c79a631db6ac45c0f243b3878cea7eba573fce1`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 38.9 MB (38866996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea5437ee9d648d9dba73b73852f840c9a182dc8974808b45da66ae6b02c7539`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3e9b83dad809e9654e865090f0ddea80735202c606baf31ec612ed9353bb96f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580056697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1acdc60ffeafd24614ef1c94c03932b402c4e4a285648ac8092b947112d03c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2029413564da7113c0389fe7b7ba9fce4699f2c9503f670cbaa7e3c8f17cce`  
		Last Modified: Tue, 08 Apr 2025 06:47:35 GMT  
		Size: 216.9 MB (216914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f551443d8e3d3bd6c829c7639100568296a8bc200a4791e7d97abcf7b39b352`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 2.6 MB (2631471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46db77d709e3e33cd4c4ca341461bbd62394b2bf9d4fc13565823bc0b669c8c1`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a13d3eaea52d6ff7ea8723d1922f7695a7051d11f019c580801c7de0407fc`  
		Last Modified: Tue, 08 Apr 2025 06:47:37 GMT  
		Size: 331.3 MB (331280984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cce5decf684916b8f18628b56c41e06ae948a9f344130de25947a7ee5bebde`  
		Last Modified: Tue, 08 Apr 2025 06:47:31 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f273f21361e067695831b6259990879359bd86ffd39a3e66c212c3fb91f8851`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52d062c39b7d4ce3547175b8ed0d0c12c8b93a6f1cdc1760aca1451dc9bead`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd45e8a94c6ad2d14811cb11fc104193eee86a44d9f27258da27301f21401322`  
		Last Modified: Tue, 08 Apr 2025 06:47:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:27b14404e7b2c26fc2e53de587be651af5355c3c010bbb63f787a9408a0d93ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38900332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4477f13661985ecb0ba6c583085179f51ed76b62c3b96708ae85f9d47fb199ab`

```dockerfile
```

-	Layers:
	-	`sha256:548fca1346571ec396a5e9de36af5046b0b38bce753955c88950c80b2fc6c442`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 38.9 MB (38873462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68407f08d7a14d70f27d9011485668534d60832fdc75531113254141069e993`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:b15777c3fbfab60c89772e7ec232e6f023f5daa20f7653278136e0133ec8baa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:ab64166456f725698342bde123d41db18a44ddc5175a4754168ae73b71f89753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584601434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe5132729480b3cd90e7400d03b35fe548ace51f75194812e7c1250ce316cb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77efbe21c55698efe60bf6e806e71ecd48fcb100da94c8ac1f538a70ec204e46`  
		Last Modified: Tue, 08 Apr 2025 01:39:43 GMT  
		Size: 219.6 MB (219625682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a88e42e1ae01faecc29ab081c04b35ddc8436b7623a9950c1fd5a7f64563a3`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 2.6 MB (2623334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ad070d3ca4c80cd584e4afe563d52e0ce5005db6608278e811d526c050e82`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaadb07ed1523aa3b67fc253307013f5d4152459e9551ed92692549b37a6f81`  
		Last Modified: Tue, 08 Apr 2025 01:39:44 GMT  
		Size: 331.6 MB (331614779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d3d248f77813f66d044f05f0a9a4492c82f30968c2b4fdcf4020011f2271e`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710a0761438dc000b0ffc6b4c53bd9019b08d450baf455b6bea5ad1fe4a5e745`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a52000065c4297be89c247c83764540c1fc92c47520c77ff8d5cfd397816d5`  
		Last Modified: Tue, 08 Apr 2025 01:39:41 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851728c4b8431dec809337ea3f2ce4aa9f9e91ebc46a3eef0edfc76355520a`  
		Last Modified: Tue, 08 Apr 2025 01:39:41 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:693a9a5c1ec0d678e945c2f1e7a2912fe47c18bdbf9d185c9f94be1f3c877e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26789bc3954188cdadecd287cdb1c59cd4f3bc9b98fe116bdc9b494a1e64abf`

```dockerfile
```

-	Layers:
	-	`sha256:4375f979d86285d4e284d3210c79a631db6ac45c0f243b3878cea7eba573fce1`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 38.9 MB (38866996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea5437ee9d648d9dba73b73852f840c9a182dc8974808b45da66ae6b02c7539`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3e9b83dad809e9654e865090f0ddea80735202c606baf31ec612ed9353bb96f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580056697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1acdc60ffeafd24614ef1c94c03932b402c4e4a285648ac8092b947112d03c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2029413564da7113c0389fe7b7ba9fce4699f2c9503f670cbaa7e3c8f17cce`  
		Last Modified: Tue, 08 Apr 2025 06:47:35 GMT  
		Size: 216.9 MB (216914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f551443d8e3d3bd6c829c7639100568296a8bc200a4791e7d97abcf7b39b352`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 2.6 MB (2631471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46db77d709e3e33cd4c4ca341461bbd62394b2bf9d4fc13565823bc0b669c8c1`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a13d3eaea52d6ff7ea8723d1922f7695a7051d11f019c580801c7de0407fc`  
		Last Modified: Tue, 08 Apr 2025 06:47:37 GMT  
		Size: 331.3 MB (331280984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cce5decf684916b8f18628b56c41e06ae948a9f344130de25947a7ee5bebde`  
		Last Modified: Tue, 08 Apr 2025 06:47:31 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f273f21361e067695831b6259990879359bd86ffd39a3e66c212c3fb91f8851`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52d062c39b7d4ce3547175b8ed0d0c12c8b93a6f1cdc1760aca1451dc9bead`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd45e8a94c6ad2d14811cb11fc104193eee86a44d9f27258da27301f21401322`  
		Last Modified: Tue, 08 Apr 2025 06:47:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:27b14404e7b2c26fc2e53de587be651af5355c3c010bbb63f787a9408a0d93ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38900332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4477f13661985ecb0ba6c583085179f51ed76b62c3b96708ae85f9d47fb199ab`

```dockerfile
```

-	Layers:
	-	`sha256:548fca1346571ec396a5e9de36af5046b0b38bce753955c88950c80b2fc6c442`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 38.9 MB (38873462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68407f08d7a14d70f27d9011485668534d60832fdc75531113254141069e993`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250401`

```console
$ docker pull odoo@sha256:b15777c3fbfab60c89772e7ec232e6f023f5daa20f7653278136e0133ec8baa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250401` - linux; amd64

```console
$ docker pull odoo@sha256:ab64166456f725698342bde123d41db18a44ddc5175a4754168ae73b71f89753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584601434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe5132729480b3cd90e7400d03b35fe548ace51f75194812e7c1250ce316cb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77efbe21c55698efe60bf6e806e71ecd48fcb100da94c8ac1f538a70ec204e46`  
		Last Modified: Tue, 08 Apr 2025 01:39:43 GMT  
		Size: 219.6 MB (219625682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a88e42e1ae01faecc29ab081c04b35ddc8436b7623a9950c1fd5a7f64563a3`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 2.6 MB (2623334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779ad070d3ca4c80cd584e4afe563d52e0ce5005db6608278e811d526c050e82`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaadb07ed1523aa3b67fc253307013f5d4152459e9551ed92692549b37a6f81`  
		Last Modified: Tue, 08 Apr 2025 01:39:44 GMT  
		Size: 331.6 MB (331614779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d3d248f77813f66d044f05f0a9a4492c82f30968c2b4fdcf4020011f2271e`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710a0761438dc000b0ffc6b4c53bd9019b08d450baf455b6bea5ad1fe4a5e745`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a52000065c4297be89c247c83764540c1fc92c47520c77ff8d5cfd397816d5`  
		Last Modified: Tue, 08 Apr 2025 01:39:41 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20851728c4b8431dec809337ea3f2ce4aa9f9e91ebc46a3eef0edfc76355520a`  
		Last Modified: Tue, 08 Apr 2025 01:39:41 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:693a9a5c1ec0d678e945c2f1e7a2912fe47c18bdbf9d185c9f94be1f3c877e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26789bc3954188cdadecd287cdb1c59cd4f3bc9b98fe116bdc9b494a1e64abf`

```dockerfile
```

-	Layers:
	-	`sha256:4375f979d86285d4e284d3210c79a631db6ac45c0f243b3878cea7eba573fce1`  
		Last Modified: Tue, 08 Apr 2025 01:39:40 GMT  
		Size: 38.9 MB (38866996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea5437ee9d648d9dba73b73852f840c9a182dc8974808b45da66ae6b02c7539`  
		Last Modified: Tue, 08 Apr 2025 01:39:39 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250401` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3e9b83dad809e9654e865090f0ddea80735202c606baf31ec612ed9353bb96f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580056697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1acdc60ffeafd24614ef1c94c03932b402c4e4a285648ac8092b947112d03c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=C.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=b2964a946a8daebf40453dc30f97bfa093471b0b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2029413564da7113c0389fe7b7ba9fce4699f2c9503f670cbaa7e3c8f17cce`  
		Last Modified: Tue, 08 Apr 2025 06:47:35 GMT  
		Size: 216.9 MB (216914521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f551443d8e3d3bd6c829c7639100568296a8bc200a4791e7d97abcf7b39b352`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 2.6 MB (2631471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46db77d709e3e33cd4c4ca341461bbd62394b2bf9d4fc13565823bc0b669c8c1`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a13d3eaea52d6ff7ea8723d1922f7695a7051d11f019c580801c7de0407fc`  
		Last Modified: Tue, 08 Apr 2025 06:47:37 GMT  
		Size: 331.3 MB (331280984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cce5decf684916b8f18628b56c41e06ae948a9f344130de25947a7ee5bebde`  
		Last Modified: Tue, 08 Apr 2025 06:47:31 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f273f21361e067695831b6259990879359bd86ffd39a3e66c212c3fb91f8851`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd52d062c39b7d4ce3547175b8ed0d0c12c8b93a6f1cdc1760aca1451dc9bead`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd45e8a94c6ad2d14811cb11fc104193eee86a44d9f27258da27301f21401322`  
		Last Modified: Tue, 08 Apr 2025 06:47:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:27b14404e7b2c26fc2e53de587be651af5355c3c010bbb63f787a9408a0d93ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38900332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4477f13661985ecb0ba6c583085179f51ed76b62c3b96708ae85f9d47fb199ab`

```dockerfile
```

-	Layers:
	-	`sha256:548fca1346571ec396a5e9de36af5046b0b38bce753955c88950c80b2fc6c442`  
		Last Modified: Tue, 08 Apr 2025 06:47:32 GMT  
		Size: 38.9 MB (38873462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68407f08d7a14d70f27d9011485668534d60832fdc75531113254141069e993`  
		Last Modified: Tue, 08 Apr 2025 06:47:30 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:d13d9ae34fb8bff25fc42e42d9ae671e0d585af3cf338b1beaf99994b4d0602c
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
$ docker pull odoo@sha256:f5dfcfe661289993f826b58bff4438bb3310675c47dde3fdb815e8151c06b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.4 MB (600414373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01b0693beb06509e7d91d3582290add5026b7c6ba97c06fc387dcb9a8a33e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5e09ddb6593f24d61e0c59c41553de8c00536a48419a368d3e59c3490c0dd`  
		Last Modified: Wed, 09 Apr 2025 01:21:54 GMT  
		Size: 233.8 MB (233779235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e21cd45ea948cac8cf68ced919f562486e9004686648dd46f88600fdda898`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 2.5 MB (2520289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54980fa8d0236e72d51f3b477f9679c603ce1f8b0a93d043af39cca9fbe6bab1`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 478.9 KB (478886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463a4899c00d17de3d8d9f327d59c5c9787d1f6fe9ceecfdce986c3da0cf5d03`  
		Last Modified: Wed, 09 Apr 2025 01:21:56 GMT  
		Size: 334.1 MB (334101160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93755250e37a2f849e4e91ccff6ae4dde8f2de48e907be74c25226675721c99`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51119626abe8108567efc452c64a55331f66655a4f005bba0ba6ceda979d12e`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6103745ec075f8a8d27a8318d8e1803994a7d0cdef30fd4eeb1ff25b754dd7f8`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9701cdfea2fe5cb4af53ddf2dabaff02ecd77ec9c0a1554a44449e1383333`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:30a1e6604d9aaa457d447310e072211f3bff5e96679791c3b6f3d10034a8946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39789241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4bbd6ac3352d5ff2b6d643da68ac36285de4f59d71cc35c413247bac3296b0`

```dockerfile
```

-	Layers:
	-	`sha256:7723b0e41fb49f9424565e4c30631d68c575abf1cc6a421dfa4d1d2a03937fb5`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 39.8 MB (39762406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c92de5de16248dbc853b506c7e6674e735824f94f45aaa05d6cacacad4b117a`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:24b90812a4f34c91963886931e55ff1bee211f4a4ffb1989073b1d186bf45493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597295825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78144ac6f5e592cd7752e52794cf4997d8677ff0fe7596096d6631fa232866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230a28bce0670b2fee0bccd57d3c8d2703957ed9c6af3fa34e690a259b96ae7`  
		Last Modified: Thu, 20 Mar 2025 17:25:45 GMT  
		Size: 233.2 MB (233249821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d2a85358db3763d633bff05933ceea9a6ce2120cc671008bee262e654beb5`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 2.5 MB (2511571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8185b8d5c44edf9913d06d5f7e9bd8ef0955eb501aed26b66d19ba7fdbb12f6c`  
		Last Modified: Thu, 20 Mar 2025 17:25:39 GMT  
		Size: 478.8 KB (478820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8771ef990f4341fec043adb1b7230d08c64b882b8e659356cb5fec6896de6f0`  
		Last Modified: Tue, 01 Apr 2025 21:50:31 GMT  
		Size: 333.7 MB (333694992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f15f909724d1a0b3552f8d52048582d6e2192f46050a0665669fbd6d64214`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f6e59653173392440e62b1133b8369e85ffd19821b972173741d9a4ea26c6`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e20f8d745099ebc02283495a6287514b9d8248e0954c05f96d98574aebf026`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf57f01e15fe3e208bf93a07c2500a4eff63e1b59b770970391d7269c51b549`  
		Last Modified: Tue, 01 Apr 2025 21:50:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1ee0d22f01d006e5c025def243815b897eae8ca761a74e2cfaa80ddc480b511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39793368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278800e1324134907de05cf7ce16af26c5ee14d44e997a735510fbb3e4dffb63`

```dockerfile
```

-	Layers:
	-	`sha256:c356663e1b07fe5a9dc6adbf6bcdd79db550f28f4ff326d71fc0fffb762d4695`  
		Last Modified: Tue, 01 Apr 2025 21:50:24 GMT  
		Size: 39.8 MB (39766381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81191e52d405316246a3205d5c4aef7b02dd3aaaaa7fc6d0695e17b7d6fb24a0`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:75a0b8fda19d6f68ce29417c54e9f9800fa554476dd4bccf4ee25bf587351c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.8 MB (616839894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff3537cdba435d3b4d5b032e8546b80030fe95ba0d43eeab4b2b3597e28cfdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c12a4a7b53b19919cbd7364940269365a1f4a84390b440902873cc204be1dba`  
		Last Modified: Wed, 09 Apr 2025 06:18:10 GMT  
		Size: 335.8 MB (335808857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f594820bfa7c44d8bbb3ac05f6d8ddb645eb74dc590029985ba1693601555783`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4a4304c573512db44f18ac885caa0d98f72353322a72286d620ca452bb9f7`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0da97541582d04890ddcc0ee38d5e8e82e9f79e6fd6fd7677def0e6ff09b25`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a42d3bb65d3b0d81d1b7dd5aaf1248ee6421b7e04edf83f18b50cf8fd3388`  
		Last Modified: Wed, 09 Apr 2025 06:17:49 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:10b80964df3afdc0ddd10a3ecb02d81ff32964fb881da7986042f672fb8d3ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39797603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17820ecd1c022112c21c1b8d9e60953aaddc43b4339ba7dce24c17dd29be277f`

```dockerfile
```

-	Layers:
	-	`sha256:f5f9b9bfa2cf6aa34495389636ba378921f0a9fd4c02ba7716b5d876e644ea52`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 39.8 MB (39770713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076ef39429e025770344bcfe78e8deda1068e40f5d661b82a18fe8acde855e33`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d13d9ae34fb8bff25fc42e42d9ae671e0d585af3cf338b1beaf99994b4d0602c
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
$ docker pull odoo@sha256:f5dfcfe661289993f826b58bff4438bb3310675c47dde3fdb815e8151c06b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.4 MB (600414373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01b0693beb06509e7d91d3582290add5026b7c6ba97c06fc387dcb9a8a33e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5e09ddb6593f24d61e0c59c41553de8c00536a48419a368d3e59c3490c0dd`  
		Last Modified: Wed, 09 Apr 2025 01:21:54 GMT  
		Size: 233.8 MB (233779235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e21cd45ea948cac8cf68ced919f562486e9004686648dd46f88600fdda898`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 2.5 MB (2520289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54980fa8d0236e72d51f3b477f9679c603ce1f8b0a93d043af39cca9fbe6bab1`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 478.9 KB (478886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463a4899c00d17de3d8d9f327d59c5c9787d1f6fe9ceecfdce986c3da0cf5d03`  
		Last Modified: Wed, 09 Apr 2025 01:21:56 GMT  
		Size: 334.1 MB (334101160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93755250e37a2f849e4e91ccff6ae4dde8f2de48e907be74c25226675721c99`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51119626abe8108567efc452c64a55331f66655a4f005bba0ba6ceda979d12e`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6103745ec075f8a8d27a8318d8e1803994a7d0cdef30fd4eeb1ff25b754dd7f8`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9701cdfea2fe5cb4af53ddf2dabaff02ecd77ec9c0a1554a44449e1383333`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:30a1e6604d9aaa457d447310e072211f3bff5e96679791c3b6f3d10034a8946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39789241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4bbd6ac3352d5ff2b6d643da68ac36285de4f59d71cc35c413247bac3296b0`

```dockerfile
```

-	Layers:
	-	`sha256:7723b0e41fb49f9424565e4c30631d68c575abf1cc6a421dfa4d1d2a03937fb5`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 39.8 MB (39762406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c92de5de16248dbc853b506c7e6674e735824f94f45aaa05d6cacacad4b117a`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:24b90812a4f34c91963886931e55ff1bee211f4a4ffb1989073b1d186bf45493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597295825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78144ac6f5e592cd7752e52794cf4997d8677ff0fe7596096d6631fa232866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230a28bce0670b2fee0bccd57d3c8d2703957ed9c6af3fa34e690a259b96ae7`  
		Last Modified: Thu, 20 Mar 2025 17:25:45 GMT  
		Size: 233.2 MB (233249821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d2a85358db3763d633bff05933ceea9a6ce2120cc671008bee262e654beb5`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 2.5 MB (2511571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8185b8d5c44edf9913d06d5f7e9bd8ef0955eb501aed26b66d19ba7fdbb12f6c`  
		Last Modified: Thu, 20 Mar 2025 17:25:39 GMT  
		Size: 478.8 KB (478820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8771ef990f4341fec043adb1b7230d08c64b882b8e659356cb5fec6896de6f0`  
		Last Modified: Tue, 01 Apr 2025 21:50:31 GMT  
		Size: 333.7 MB (333694992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f15f909724d1a0b3552f8d52048582d6e2192f46050a0665669fbd6d64214`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f6e59653173392440e62b1133b8369e85ffd19821b972173741d9a4ea26c6`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e20f8d745099ebc02283495a6287514b9d8248e0954c05f96d98574aebf026`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf57f01e15fe3e208bf93a07c2500a4eff63e1b59b770970391d7269c51b549`  
		Last Modified: Tue, 01 Apr 2025 21:50:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1ee0d22f01d006e5c025def243815b897eae8ca761a74e2cfaa80ddc480b511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39793368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278800e1324134907de05cf7ce16af26c5ee14d44e997a735510fbb3e4dffb63`

```dockerfile
```

-	Layers:
	-	`sha256:c356663e1b07fe5a9dc6adbf6bcdd79db550f28f4ff326d71fc0fffb762d4695`  
		Last Modified: Tue, 01 Apr 2025 21:50:24 GMT  
		Size: 39.8 MB (39766381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81191e52d405316246a3205d5c4aef7b02dd3aaaaa7fc6d0695e17b7d6fb24a0`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:75a0b8fda19d6f68ce29417c54e9f9800fa554476dd4bccf4ee25bf587351c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.8 MB (616839894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff3537cdba435d3b4d5b032e8546b80030fe95ba0d43eeab4b2b3597e28cfdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c12a4a7b53b19919cbd7364940269365a1f4a84390b440902873cc204be1dba`  
		Last Modified: Wed, 09 Apr 2025 06:18:10 GMT  
		Size: 335.8 MB (335808857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f594820bfa7c44d8bbb3ac05f6d8ddb645eb74dc590029985ba1693601555783`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4a4304c573512db44f18ac885caa0d98f72353322a72286d620ca452bb9f7`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0da97541582d04890ddcc0ee38d5e8e82e9f79e6fd6fd7677def0e6ff09b25`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a42d3bb65d3b0d81d1b7dd5aaf1248ee6421b7e04edf83f18b50cf8fd3388`  
		Last Modified: Wed, 09 Apr 2025 06:17:49 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:10b80964df3afdc0ddd10a3ecb02d81ff32964fb881da7986042f672fb8d3ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39797603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17820ecd1c022112c21c1b8d9e60953aaddc43b4339ba7dce24c17dd29be277f`

```dockerfile
```

-	Layers:
	-	`sha256:f5f9b9bfa2cf6aa34495389636ba378921f0a9fd4c02ba7716b5d876e644ea52`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 39.8 MB (39770713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076ef39429e025770344bcfe78e8deda1068e40f5d661b82a18fe8acde855e33`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250401`

```console
$ docker pull odoo@sha256:d13d9ae34fb8bff25fc42e42d9ae671e0d585af3cf338b1beaf99994b4d0602c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250401` - linux; amd64

```console
$ docker pull odoo@sha256:f5dfcfe661289993f826b58bff4438bb3310675c47dde3fdb815e8151c06b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.4 MB (600414373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d01b0693beb06509e7d91d3582290add5026b7c6ba97c06fc387dcb9a8a33e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5e09ddb6593f24d61e0c59c41553de8c00536a48419a368d3e59c3490c0dd`  
		Last Modified: Wed, 09 Apr 2025 01:21:54 GMT  
		Size: 233.8 MB (233779235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e21cd45ea948cac8cf68ced919f562486e9004686648dd46f88600fdda898`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 2.5 MB (2520289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54980fa8d0236e72d51f3b477f9679c603ce1f8b0a93d043af39cca9fbe6bab1`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 478.9 KB (478886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463a4899c00d17de3d8d9f327d59c5c9787d1f6fe9ceecfdce986c3da0cf5d03`  
		Last Modified: Wed, 09 Apr 2025 01:21:56 GMT  
		Size: 334.1 MB (334101160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93755250e37a2f849e4e91ccff6ae4dde8f2de48e907be74c25226675721c99`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51119626abe8108567efc452c64a55331f66655a4f005bba0ba6ceda979d12e`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6103745ec075f8a8d27a8318d8e1803994a7d0cdef30fd4eeb1ff25b754dd7f8`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9701cdfea2fe5cb4af53ddf2dabaff02ecd77ec9c0a1554a44449e1383333`  
		Last Modified: Wed, 09 Apr 2025 01:21:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:30a1e6604d9aaa457d447310e072211f3bff5e96679791c3b6f3d10034a8946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39789241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4bbd6ac3352d5ff2b6d643da68ac36285de4f59d71cc35c413247bac3296b0`

```dockerfile
```

-	Layers:
	-	`sha256:7723b0e41fb49f9424565e4c30631d68c575abf1cc6a421dfa4d1d2a03937fb5`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 39.8 MB (39762406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c92de5de16248dbc853b506c7e6674e735824f94f45aaa05d6cacacad4b117a`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250401` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:24b90812a4f34c91963886931e55ff1bee211f4a4ffb1989073b1d186bf45493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597295825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78144ac6f5e592cd7752e52794cf4997d8677ff0fe7596096d6631fa232866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230a28bce0670b2fee0bccd57d3c8d2703957ed9c6af3fa34e690a259b96ae7`  
		Last Modified: Thu, 20 Mar 2025 17:25:45 GMT  
		Size: 233.2 MB (233249821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d2a85358db3763d633bff05933ceea9a6ce2120cc671008bee262e654beb5`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 2.5 MB (2511571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8185b8d5c44edf9913d06d5f7e9bd8ef0955eb501aed26b66d19ba7fdbb12f6c`  
		Last Modified: Thu, 20 Mar 2025 17:25:39 GMT  
		Size: 478.8 KB (478820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8771ef990f4341fec043adb1b7230d08c64b882b8e659356cb5fec6896de6f0`  
		Last Modified: Tue, 01 Apr 2025 21:50:31 GMT  
		Size: 333.7 MB (333694992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32f15f909724d1a0b3552f8d52048582d6e2192f46050a0665669fbd6d64214`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f6e59653173392440e62b1133b8369e85ffd19821b972173741d9a4ea26c6`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e20f8d745099ebc02283495a6287514b9d8248e0954c05f96d98574aebf026`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf57f01e15fe3e208bf93a07c2500a4eff63e1b59b770970391d7269c51b549`  
		Last Modified: Tue, 01 Apr 2025 21:50:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:1ee0d22f01d006e5c025def243815b897eae8ca761a74e2cfaa80ddc480b511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39793368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278800e1324134907de05cf7ce16af26c5ee14d44e997a735510fbb3e4dffb63`

```dockerfile
```

-	Layers:
	-	`sha256:c356663e1b07fe5a9dc6adbf6bcdd79db550f28f4ff326d71fc0fffb762d4695`  
		Last Modified: Tue, 01 Apr 2025 21:50:24 GMT  
		Size: 39.8 MB (39766381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81191e52d405316246a3205d5c4aef7b02dd3aaaaa7fc6d0695e17b7d6fb24a0`  
		Last Modified: Tue, 01 Apr 2025 21:50:22 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250401` - linux; ppc64le

```console
$ docker pull odoo@sha256:75a0b8fda19d6f68ce29417c54e9f9800fa554476dd4bccf4ee25bf587351c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.8 MB (616839894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff3537cdba435d3b4d5b032e8546b80030fe95ba0d43eeab4b2b3597e28cfdc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=7c4814eb00f0eb50ef5a16c31f241d6e69a05bb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c12a4a7b53b19919cbd7364940269365a1f4a84390b440902873cc204be1dba`  
		Last Modified: Wed, 09 Apr 2025 06:18:10 GMT  
		Size: 335.8 MB (335808857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f594820bfa7c44d8bbb3ac05f6d8ddb645eb74dc590029985ba1693601555783`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4a4304c573512db44f18ac885caa0d98f72353322a72286d620ca452bb9f7`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0da97541582d04890ddcc0ee38d5e8e82e9f79e6fd6fd7677def0e6ff09b25`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13a42d3bb65d3b0d81d1b7dd5aaf1248ee6421b7e04edf83f18b50cf8fd3388`  
		Last Modified: Wed, 09 Apr 2025 06:17:49 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:10b80964df3afdc0ddd10a3ecb02d81ff32964fb881da7986042f672fb8d3ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39797603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17820ecd1c022112c21c1b8d9e60953aaddc43b4339ba7dce24c17dd29be277f`

```dockerfile
```

-	Layers:
	-	`sha256:f5f9b9bfa2cf6aa34495389636ba378921f0a9fd4c02ba7716b5d876e644ea52`  
		Last Modified: Wed, 09 Apr 2025 06:17:48 GMT  
		Size: 39.8 MB (39770713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076ef39429e025770344bcfe78e8deda1068e40f5d661b82a18fe8acde855e33`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:b942266f95a7c2893bd55082c0248e1f412932b0c893a46a7028d923b6982880
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
$ docker pull odoo@sha256:17c06d4f8e76796fa0917b428130af1f142122ceb27c42de1ac4a4903eca371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670100905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ac087466901f2fa4fd9378e7de9dea86c934f1fc34e1076494574d353da59d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3af6b1de5f47f8225ab322291ea7d85acf9898f9dbebc03e75351a36f14c7`  
		Last Modified: Wed, 09 Apr 2025 01:23:01 GMT  
		Size: 254.5 MB (254517420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7970f506e51c8c88021d8660b506f6bedf5f56dc15ccd29041507a5e718119c6`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 14.3 MB (14267275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e80ed59d8d401dcb12c1f49d2ff7b123001473f136ed9396438a21722ecd4c7`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 478.6 KB (478628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e41ebd955975138efc55b3b25dccae3044dfa91a78d8cf0e6640d2944cd1f7`  
		Last Modified: Wed, 09 Apr 2025 01:23:03 GMT  
		Size: 371.1 MB (371117491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd480b60a655628623ae5ceb1b200442a921ac421d4eb5b6330af0099ba4ec16`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c37fde890b687a4c38e0b8cdb275d04dd5c9e9abdb6b898db721c0c9730a215`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da556ab199ba00182102eec955678ab634a774b71866575028f72239ded601e7`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb767771b066740336919596a5edf70f9bb2789a221aca26c1f498c789d95628`  
		Last Modified: Wed, 09 Apr 2025 01:22:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:12525dd46951a2406c9a025fad256f358daee6a2d1874e8fbe4e8f1aa25ca486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59210368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d04663129d7f76cc4c7bf2d36b46d2b86841c653f023dea7c1c51e2baa4d5`

```dockerfile
```

-	Layers:
	-	`sha256:a6f7363e801646f99d3872e7a3759ddc7e7b37d5f3deda2ea6102a26f5bf9bb9`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 59.2 MB (59183232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f571c639a18eac865f6d2165fe9fb935fcfef4abf4d93628bb5e35b5681a736f`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:16bc2e19f1f569c56c2b30a53f7b4f5bc1af27173a4385e02ef732160105da96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.1 MB (671096696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e10e623130c4c431f4252d76952c598a081e7582e4d341e3c363accad8002b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730f827b8b7817a0d4aa80fe57257039cd9098da1ac96e7c7eae75dcfc14d15`  
		Last Modified: Thu, 20 Mar 2025 17:19:11 GMT  
		Size: 254.2 MB (254156179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3cf7384512c28559c37404199f0662a7ae17ceb5ff872ae06a04b0b03f3cbc`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 16.6 MB (16621658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab85031777875a4a365d33aab4dc2c17d243e324e097d6f0e4f9d9bada5fad`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 478.6 KB (478605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de27d976ec8bc7073577a9fa768b8797514ef49d5d1b8a2c6a1ab362706eb8b`  
		Last Modified: Tue, 01 Apr 2025 21:46:42 GMT  
		Size: 370.9 MB (370944216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e780cf9eb8b6f78085a806c67051371e987af7614ca14d7c0597c4f95bec039`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9012450fd07a580f20cd7cb6fe419e62dc571dc38ee6cd7779fd4673822b35d3`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af85c0d6aa5ba890ad51982d8b2ed8a3a1effeef4f2fa1cca69e5e9de6a36d`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662381813250f71d5249c0310289d3234b8cf61749ca3f7a6968c45a86f1dc5c`  
		Last Modified: Tue, 01 Apr 2025 21:46:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d11734d3963af70d2c62b0702b928de34d9f3091b24b788799e03ef1ba0c1e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59219442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9470896373f23c0b4187cf1bff9d4fd066d7f00331fcdbaa3dce09a97893a5a4`

```dockerfile
```

-	Layers:
	-	`sha256:e986c8bfb1e0c7a08a4b3cc368d5df071234b8ecbb5dfb73e8ab0aff5ffc1c4b`  
		Last Modified: Tue, 01 Apr 2025 21:46:35 GMT  
		Size: 59.2 MB (59192142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a93d51ad9c3cd71e6add4ea152aaba95f77d7092a0898641253098156c9149`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:64eac330d2af6892de7ee2e0268d4113a6b859aff1ee500ad28bc54ca1d16663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686340776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6922dfeb45325fff81e8eb85fc512f042d64cd3b27013bf979b64fa2b89c10cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1260cb7cecc16808565f8bd1fc8b5427ae287ef25f7f7c428156be634992cc`  
		Last Modified: Wed, 09 Apr 2025 06:08:52 GMT  
		Size: 371.6 MB (371640454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8a66e7f18b62b52d20ab06db18a87113fe1ba0d4fab321536c9b8b27de7c32`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdab8b965447fcad18089ad1e8e13c3042d245f4ec49aae0a3f866acafd5cd5`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c1b651699e8a159f2162382b10f1f64a14e3d3f7c0492c4a51416a269ae411`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86352da3d7b6968cde55b71fe9ec0cb5170f02ac97355f22f8384ddf3e8cc83`  
		Last Modified: Wed, 09 Apr 2025 06:08:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0ceb0f832fb296de99e25b9e2e93064ee722cff83bc28db088934ed39e704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59218573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb37236b53d2cee56cb7fc2c84ae90f41734c2afeff5bce2ec8ff1243a6dd83`

```dockerfile
```

-	Layers:
	-	`sha256:8ccf19a95d487a9db155ae6e3e78a8edd4aac37ca56bdd3d8735fe9e4d3a802d`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 59.2 MB (59191375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501a183cb97183b24e2e2a79baca72a8b3218b863b080689121559c9e1f425`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:b942266f95a7c2893bd55082c0248e1f412932b0c893a46a7028d923b6982880
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
$ docker pull odoo@sha256:17c06d4f8e76796fa0917b428130af1f142122ceb27c42de1ac4a4903eca371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670100905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ac087466901f2fa4fd9378e7de9dea86c934f1fc34e1076494574d353da59d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3af6b1de5f47f8225ab322291ea7d85acf9898f9dbebc03e75351a36f14c7`  
		Last Modified: Wed, 09 Apr 2025 01:23:01 GMT  
		Size: 254.5 MB (254517420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7970f506e51c8c88021d8660b506f6bedf5f56dc15ccd29041507a5e718119c6`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 14.3 MB (14267275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e80ed59d8d401dcb12c1f49d2ff7b123001473f136ed9396438a21722ecd4c7`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 478.6 KB (478628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e41ebd955975138efc55b3b25dccae3044dfa91a78d8cf0e6640d2944cd1f7`  
		Last Modified: Wed, 09 Apr 2025 01:23:03 GMT  
		Size: 371.1 MB (371117491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd480b60a655628623ae5ceb1b200442a921ac421d4eb5b6330af0099ba4ec16`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c37fde890b687a4c38e0b8cdb275d04dd5c9e9abdb6b898db721c0c9730a215`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da556ab199ba00182102eec955678ab634a774b71866575028f72239ded601e7`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb767771b066740336919596a5edf70f9bb2789a221aca26c1f498c789d95628`  
		Last Modified: Wed, 09 Apr 2025 01:22:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:12525dd46951a2406c9a025fad256f358daee6a2d1874e8fbe4e8f1aa25ca486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59210368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d04663129d7f76cc4c7bf2d36b46d2b86841c653f023dea7c1c51e2baa4d5`

```dockerfile
```

-	Layers:
	-	`sha256:a6f7363e801646f99d3872e7a3759ddc7e7b37d5f3deda2ea6102a26f5bf9bb9`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 59.2 MB (59183232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f571c639a18eac865f6d2165fe9fb935fcfef4abf4d93628bb5e35b5681a736f`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:16bc2e19f1f569c56c2b30a53f7b4f5bc1af27173a4385e02ef732160105da96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.1 MB (671096696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e10e623130c4c431f4252d76952c598a081e7582e4d341e3c363accad8002b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730f827b8b7817a0d4aa80fe57257039cd9098da1ac96e7c7eae75dcfc14d15`  
		Last Modified: Thu, 20 Mar 2025 17:19:11 GMT  
		Size: 254.2 MB (254156179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3cf7384512c28559c37404199f0662a7ae17ceb5ff872ae06a04b0b03f3cbc`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 16.6 MB (16621658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab85031777875a4a365d33aab4dc2c17d243e324e097d6f0e4f9d9bada5fad`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 478.6 KB (478605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de27d976ec8bc7073577a9fa768b8797514ef49d5d1b8a2c6a1ab362706eb8b`  
		Last Modified: Tue, 01 Apr 2025 21:46:42 GMT  
		Size: 370.9 MB (370944216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e780cf9eb8b6f78085a806c67051371e987af7614ca14d7c0597c4f95bec039`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9012450fd07a580f20cd7cb6fe419e62dc571dc38ee6cd7779fd4673822b35d3`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af85c0d6aa5ba890ad51982d8b2ed8a3a1effeef4f2fa1cca69e5e9de6a36d`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662381813250f71d5249c0310289d3234b8cf61749ca3f7a6968c45a86f1dc5c`  
		Last Modified: Tue, 01 Apr 2025 21:46:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d11734d3963af70d2c62b0702b928de34d9f3091b24b788799e03ef1ba0c1e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59219442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9470896373f23c0b4187cf1bff9d4fd066d7f00331fcdbaa3dce09a97893a5a4`

```dockerfile
```

-	Layers:
	-	`sha256:e986c8bfb1e0c7a08a4b3cc368d5df071234b8ecbb5dfb73e8ab0aff5ffc1c4b`  
		Last Modified: Tue, 01 Apr 2025 21:46:35 GMT  
		Size: 59.2 MB (59192142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a93d51ad9c3cd71e6add4ea152aaba95f77d7092a0898641253098156c9149`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:64eac330d2af6892de7ee2e0268d4113a6b859aff1ee500ad28bc54ca1d16663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686340776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6922dfeb45325fff81e8eb85fc512f042d64cd3b27013bf979b64fa2b89c10cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1260cb7cecc16808565f8bd1fc8b5427ae287ef25f7f7c428156be634992cc`  
		Last Modified: Wed, 09 Apr 2025 06:08:52 GMT  
		Size: 371.6 MB (371640454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8a66e7f18b62b52d20ab06db18a87113fe1ba0d4fab321536c9b8b27de7c32`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdab8b965447fcad18089ad1e8e13c3042d245f4ec49aae0a3f866acafd5cd5`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c1b651699e8a159f2162382b10f1f64a14e3d3f7c0492c4a51416a269ae411`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86352da3d7b6968cde55b71fe9ec0cb5170f02ac97355f22f8384ddf3e8cc83`  
		Last Modified: Wed, 09 Apr 2025 06:08:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0ceb0f832fb296de99e25b9e2e93064ee722cff83bc28db088934ed39e704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59218573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb37236b53d2cee56cb7fc2c84ae90f41734c2afeff5bce2ec8ff1243a6dd83`

```dockerfile
```

-	Layers:
	-	`sha256:8ccf19a95d487a9db155ae6e3e78a8edd4aac37ca56bdd3d8735fe9e4d3a802d`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 59.2 MB (59191375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501a183cb97183b24e2e2a79baca72a8b3218b863b080689121559c9e1f425`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250401`

```console
$ docker pull odoo@sha256:b942266f95a7c2893bd55082c0248e1f412932b0c893a46a7028d923b6982880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250401` - linux; amd64

```console
$ docker pull odoo@sha256:17c06d4f8e76796fa0917b428130af1f142122ceb27c42de1ac4a4903eca371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670100905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ac087466901f2fa4fd9378e7de9dea86c934f1fc34e1076494574d353da59d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3af6b1de5f47f8225ab322291ea7d85acf9898f9dbebc03e75351a36f14c7`  
		Last Modified: Wed, 09 Apr 2025 01:23:01 GMT  
		Size: 254.5 MB (254517420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7970f506e51c8c88021d8660b506f6bedf5f56dc15ccd29041507a5e718119c6`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 14.3 MB (14267275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e80ed59d8d401dcb12c1f49d2ff7b123001473f136ed9396438a21722ecd4c7`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 478.6 KB (478628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e41ebd955975138efc55b3b25dccae3044dfa91a78d8cf0e6640d2944cd1f7`  
		Last Modified: Wed, 09 Apr 2025 01:23:03 GMT  
		Size: 371.1 MB (371117491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd480b60a655628623ae5ceb1b200442a921ac421d4eb5b6330af0099ba4ec16`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c37fde890b687a4c38e0b8cdb275d04dd5c9e9abdb6b898db721c0c9730a215`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da556ab199ba00182102eec955678ab634a774b71866575028f72239ded601e7`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb767771b066740336919596a5edf70f9bb2789a221aca26c1f498c789d95628`  
		Last Modified: Wed, 09 Apr 2025 01:22:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:12525dd46951a2406c9a025fad256f358daee6a2d1874e8fbe4e8f1aa25ca486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59210368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d04663129d7f76cc4c7bf2d36b46d2b86841c653f023dea7c1c51e2baa4d5`

```dockerfile
```

-	Layers:
	-	`sha256:a6f7363e801646f99d3872e7a3759ddc7e7b37d5f3deda2ea6102a26f5bf9bb9`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 59.2 MB (59183232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f571c639a18eac865f6d2165fe9fb935fcfef4abf4d93628bb5e35b5681a736f`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250401` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:16bc2e19f1f569c56c2b30a53f7b4f5bc1af27173a4385e02ef732160105da96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.1 MB (671096696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e10e623130c4c431f4252d76952c598a081e7582e4d341e3c363accad8002b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730f827b8b7817a0d4aa80fe57257039cd9098da1ac96e7c7eae75dcfc14d15`  
		Last Modified: Thu, 20 Mar 2025 17:19:11 GMT  
		Size: 254.2 MB (254156179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3cf7384512c28559c37404199f0662a7ae17ceb5ff872ae06a04b0b03f3cbc`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 16.6 MB (16621658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab85031777875a4a365d33aab4dc2c17d243e324e097d6f0e4f9d9bada5fad`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 478.6 KB (478605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de27d976ec8bc7073577a9fa768b8797514ef49d5d1b8a2c6a1ab362706eb8b`  
		Last Modified: Tue, 01 Apr 2025 21:46:42 GMT  
		Size: 370.9 MB (370944216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e780cf9eb8b6f78085a806c67051371e987af7614ca14d7c0597c4f95bec039`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9012450fd07a580f20cd7cb6fe419e62dc571dc38ee6cd7779fd4673822b35d3`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af85c0d6aa5ba890ad51982d8b2ed8a3a1effeef4f2fa1cca69e5e9de6a36d`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662381813250f71d5249c0310289d3234b8cf61749ca3f7a6968c45a86f1dc5c`  
		Last Modified: Tue, 01 Apr 2025 21:46:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:d11734d3963af70d2c62b0702b928de34d9f3091b24b788799e03ef1ba0c1e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59219442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9470896373f23c0b4187cf1bff9d4fd066d7f00331fcdbaa3dce09a97893a5a4`

```dockerfile
```

-	Layers:
	-	`sha256:e986c8bfb1e0c7a08a4b3cc368d5df071234b8ecbb5dfb73e8ab0aff5ffc1c4b`  
		Last Modified: Tue, 01 Apr 2025 21:46:35 GMT  
		Size: 59.2 MB (59192142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a93d51ad9c3cd71e6add4ea152aaba95f77d7092a0898641253098156c9149`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250401` - linux; ppc64le

```console
$ docker pull odoo@sha256:64eac330d2af6892de7ee2e0268d4113a6b859aff1ee500ad28bc54ca1d16663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686340776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6922dfeb45325fff81e8eb85fc512f042d64cd3b27013bf979b64fa2b89c10cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1260cb7cecc16808565f8bd1fc8b5427ae287ef25f7f7c428156be634992cc`  
		Last Modified: Wed, 09 Apr 2025 06:08:52 GMT  
		Size: 371.6 MB (371640454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8a66e7f18b62b52d20ab06db18a87113fe1ba0d4fab321536c9b8b27de7c32`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdab8b965447fcad18089ad1e8e13c3042d245f4ec49aae0a3f866acafd5cd5`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c1b651699e8a159f2162382b10f1f64a14e3d3f7c0492c4a51416a269ae411`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86352da3d7b6968cde55b71fe9ec0cb5170f02ac97355f22f8384ddf3e8cc83`  
		Last Modified: Wed, 09 Apr 2025 06:08:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0ceb0f832fb296de99e25b9e2e93064ee722cff83bc28db088934ed39e704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59218573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb37236b53d2cee56cb7fc2c84ae90f41734c2afeff5bce2ec8ff1243a6dd83`

```dockerfile
```

-	Layers:
	-	`sha256:8ccf19a95d487a9db155ae6e3e78a8edd4aac37ca56bdd3d8735fe9e4d3a802d`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 59.2 MB (59191375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501a183cb97183b24e2e2a79baca72a8b3218b863b080689121559c9e1f425`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:b942266f95a7c2893bd55082c0248e1f412932b0c893a46a7028d923b6982880
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
$ docker pull odoo@sha256:17c06d4f8e76796fa0917b428130af1f142122ceb27c42de1ac4a4903eca371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670100905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ac087466901f2fa4fd9378e7de9dea86c934f1fc34e1076494574d353da59d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3af6b1de5f47f8225ab322291ea7d85acf9898f9dbebc03e75351a36f14c7`  
		Last Modified: Wed, 09 Apr 2025 01:23:01 GMT  
		Size: 254.5 MB (254517420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7970f506e51c8c88021d8660b506f6bedf5f56dc15ccd29041507a5e718119c6`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 14.3 MB (14267275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e80ed59d8d401dcb12c1f49d2ff7b123001473f136ed9396438a21722ecd4c7`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 478.6 KB (478628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e41ebd955975138efc55b3b25dccae3044dfa91a78d8cf0e6640d2944cd1f7`  
		Last Modified: Wed, 09 Apr 2025 01:23:03 GMT  
		Size: 371.1 MB (371117491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd480b60a655628623ae5ceb1b200442a921ac421d4eb5b6330af0099ba4ec16`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c37fde890b687a4c38e0b8cdb275d04dd5c9e9abdb6b898db721c0c9730a215`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da556ab199ba00182102eec955678ab634a774b71866575028f72239ded601e7`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb767771b066740336919596a5edf70f9bb2789a221aca26c1f498c789d95628`  
		Last Modified: Wed, 09 Apr 2025 01:22:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:12525dd46951a2406c9a025fad256f358daee6a2d1874e8fbe4e8f1aa25ca486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59210368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71d04663129d7f76cc4c7bf2d36b46d2b86841c653f023dea7c1c51e2baa4d5`

```dockerfile
```

-	Layers:
	-	`sha256:a6f7363e801646f99d3872e7a3759ddc7e7b37d5f3deda2ea6102a26f5bf9bb9`  
		Last Modified: Wed, 09 Apr 2025 01:22:58 GMT  
		Size: 59.2 MB (59183232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f571c639a18eac865f6d2165fe9fb935fcfef4abf4d93628bb5e35b5681a736f`  
		Last Modified: Wed, 09 Apr 2025 01:22:57 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:16bc2e19f1f569c56c2b30a53f7b4f5bc1af27173a4385e02ef732160105da96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.1 MB (671096696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e10e623130c4c431f4252d76952c598a081e7582e4d341e3c363accad8002b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=arm64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730f827b8b7817a0d4aa80fe57257039cd9098da1ac96e7c7eae75dcfc14d15`  
		Last Modified: Thu, 20 Mar 2025 17:19:11 GMT  
		Size: 254.2 MB (254156179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3cf7384512c28559c37404199f0662a7ae17ceb5ff872ae06a04b0b03f3cbc`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 16.6 MB (16621658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab85031777875a4a365d33aab4dc2c17d243e324e097d6f0e4f9d9bada5fad`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 478.6 KB (478605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de27d976ec8bc7073577a9fa768b8797514ef49d5d1b8a2c6a1ab362706eb8b`  
		Last Modified: Tue, 01 Apr 2025 21:46:42 GMT  
		Size: 370.9 MB (370944216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e780cf9eb8b6f78085a806c67051371e987af7614ca14d7c0597c4f95bec039`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9012450fd07a580f20cd7cb6fe419e62dc571dc38ee6cd7779fd4673822b35d3`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44af85c0d6aa5ba890ad51982d8b2ed8a3a1effeef4f2fa1cca69e5e9de6a36d`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662381813250f71d5249c0310289d3234b8cf61749ca3f7a6968c45a86f1dc5c`  
		Last Modified: Tue, 01 Apr 2025 21:46:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d11734d3963af70d2c62b0702b928de34d9f3091b24b788799e03ef1ba0c1e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59219442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9470896373f23c0b4187cf1bff9d4fd066d7f00331fcdbaa3dce09a97893a5a4`

```dockerfile
```

-	Layers:
	-	`sha256:e986c8bfb1e0c7a08a4b3cc368d5df071234b8ecbb5dfb73e8ab0aff5ffc1c4b`  
		Last Modified: Tue, 01 Apr 2025 21:46:35 GMT  
		Size: 59.2 MB (59192142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a93d51ad9c3cd71e6add4ea152aaba95f77d7092a0898641253098156c9149`  
		Last Modified: Tue, 01 Apr 2025 21:46:33 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:64eac330d2af6892de7ee2e0268d4113a6b859aff1ee500ad28bc54ca1d16663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686340776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6922dfeb45325fff81e8eb85fc512f042d64cd3b27013bf979b64fa2b89c10cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Apr 2025 13:33:26 GMT
ARG RELEASE
# Tue, 01 Apr 2025 13:33:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 13:33:26 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 13:33:26 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1260cb7cecc16808565f8bd1fc8b5427ae287ef25f7f7c428156be634992cc`  
		Last Modified: Wed, 09 Apr 2025 06:08:52 GMT  
		Size: 371.6 MB (371640454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8a66e7f18b62b52d20ab06db18a87113fe1ba0d4fab321536c9b8b27de7c32`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdab8b965447fcad18089ad1e8e13c3042d245f4ec49aae0a3f866acafd5cd5`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c1b651699e8a159f2162382b10f1f64a14e3d3f7c0492c4a51416a269ae411`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86352da3d7b6968cde55b71fe9ec0cb5170f02ac97355f22f8384ddf3e8cc83`  
		Last Modified: Wed, 09 Apr 2025 06:08:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0ceb0f832fb296de99e25b9e2e93064ee722cff83bc28db088934ed39e704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59218573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb37236b53d2cee56cb7fc2c84ae90f41734c2afeff5bce2ec8ff1243a6dd83`

```dockerfile
```

-	Layers:
	-	`sha256:8ccf19a95d487a9db155ae6e3e78a8edd4aac37ca56bdd3d8735fe9e4d3a802d`  
		Last Modified: Wed, 09 Apr 2025 06:08:30 GMT  
		Size: 59.2 MB (59191375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7501a183cb97183b24e2e2a79baca72a8b3218b863b080689121559c9e1f425`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
