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
$ docker pull odoo@sha256:01416b44691e380a529bac37eb0d136b15a6f3e31b51f2418f62898a6f0445d7
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
$ docker pull odoo@sha256:fb2cb2f1dc837d0b4b747920c33f13eda507f540cc51cc0a0edffbe370294ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.2 MB (595200594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808e669ae26b8badf5ecbd888057a6f049e5f7c18fef0d10485022f5a18847aa`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb9a243ac74bdd6b55b6c4555c9ba5df3aa994c2afe7ec8d9a03cd1ccf39edd`  
		Last Modified: Wed, 09 Apr 2025 08:53:36 GMT  
		Size: 333.7 MB (333696747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c6787a45db59990af2c53f1f9b0fc0f5768b825a4707fa7128b797e1391059`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff6b4759ff8605916c950cdec0f31247df2e2d204821a4abacfcf62766f8f17`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca213b1d42f1f5e70b553a5a73009703669fc0e39355c9de5b2650d11d7b7309`  
		Last Modified: Wed, 09 Apr 2025 08:53:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b0b10c16724b66adaf1f67f871ad0eb98a62ef96ff6bd45f158d1a6161657a`  
		Last Modified: Wed, 09 Apr 2025 08:53:32 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:2e3ca727e632b3786519aea7c066b72aea508f32adb84783cb7c7835268b9bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5cd8fab8c7023ced7ab6d784f51d73209e13153db3fdc5293be63cd9ea1d1a`

```dockerfile
```

-	Layers:
	-	`sha256:53e413a887cfc32bbec1f1a7e026d7cf4a8370672819474343bde51e1d4b2c1e`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 39.8 MB (39768913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cea1550e10c51ee46ea0461e4bcba52d774b3d20e66c4b70c45a30384fe135`  
		Last Modified: Wed, 09 Apr 2025 08:53:29 GMT  
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
$ docker pull odoo@sha256:01416b44691e380a529bac37eb0d136b15a6f3e31b51f2418f62898a6f0445d7
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
$ docker pull odoo@sha256:fb2cb2f1dc837d0b4b747920c33f13eda507f540cc51cc0a0edffbe370294ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.2 MB (595200594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808e669ae26b8badf5ecbd888057a6f049e5f7c18fef0d10485022f5a18847aa`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb9a243ac74bdd6b55b6c4555c9ba5df3aa994c2afe7ec8d9a03cd1ccf39edd`  
		Last Modified: Wed, 09 Apr 2025 08:53:36 GMT  
		Size: 333.7 MB (333696747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c6787a45db59990af2c53f1f9b0fc0f5768b825a4707fa7128b797e1391059`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff6b4759ff8605916c950cdec0f31247df2e2d204821a4abacfcf62766f8f17`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca213b1d42f1f5e70b553a5a73009703669fc0e39355c9de5b2650d11d7b7309`  
		Last Modified: Wed, 09 Apr 2025 08:53:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b0b10c16724b66adaf1f67f871ad0eb98a62ef96ff6bd45f158d1a6161657a`  
		Last Modified: Wed, 09 Apr 2025 08:53:32 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2e3ca727e632b3786519aea7c066b72aea508f32adb84783cb7c7835268b9bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5cd8fab8c7023ced7ab6d784f51d73209e13153db3fdc5293be63cd9ea1d1a`

```dockerfile
```

-	Layers:
	-	`sha256:53e413a887cfc32bbec1f1a7e026d7cf4a8370672819474343bde51e1d4b2c1e`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 39.8 MB (39768913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cea1550e10c51ee46ea0461e4bcba52d774b3d20e66c4b70c45a30384fe135`  
		Last Modified: Wed, 09 Apr 2025 08:53:29 GMT  
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
$ docker pull odoo@sha256:01416b44691e380a529bac37eb0d136b15a6f3e31b51f2418f62898a6f0445d7
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
$ docker pull odoo@sha256:fb2cb2f1dc837d0b4b747920c33f13eda507f540cc51cc0a0edffbe370294ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.2 MB (595200594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808e669ae26b8badf5ecbd888057a6f049e5f7c18fef0d10485022f5a18847aa`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb9a243ac74bdd6b55b6c4555c9ba5df3aa994c2afe7ec8d9a03cd1ccf39edd`  
		Last Modified: Wed, 09 Apr 2025 08:53:36 GMT  
		Size: 333.7 MB (333696747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c6787a45db59990af2c53f1f9b0fc0f5768b825a4707fa7128b797e1391059`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff6b4759ff8605916c950cdec0f31247df2e2d204821a4abacfcf62766f8f17`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca213b1d42f1f5e70b553a5a73009703669fc0e39355c9de5b2650d11d7b7309`  
		Last Modified: Wed, 09 Apr 2025 08:53:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b0b10c16724b66adaf1f67f871ad0eb98a62ef96ff6bd45f158d1a6161657a`  
		Last Modified: Wed, 09 Apr 2025 08:53:32 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:2e3ca727e632b3786519aea7c066b72aea508f32adb84783cb7c7835268b9bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5cd8fab8c7023ced7ab6d784f51d73209e13153db3fdc5293be63cd9ea1d1a`

```dockerfile
```

-	Layers:
	-	`sha256:53e413a887cfc32bbec1f1a7e026d7cf4a8370672819474343bde51e1d4b2c1e`  
		Last Modified: Wed, 09 Apr 2025 08:53:31 GMT  
		Size: 39.8 MB (39768913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7cea1550e10c51ee46ea0461e4bcba52d774b3d20e66c4b70c45a30384fe135`  
		Last Modified: Wed, 09 Apr 2025 08:53:29 GMT  
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
$ docker pull odoo@sha256:b81189bac8724a55d9dc9a5f117550efb15781867eb7a72eff963c17f8c9106d
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
$ docker pull odoo@sha256:7b17817332c81e923fe2860d95a053bb50472eb3c083cfda522eb314893d22fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666463468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba293c91a5e85faad03a478504f053983b1c98e0e74c464f84145e812437f5ad`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f90952dae6165d5242078f746846abbc58c2cc44fa09ca8a4c18209d53df7`  
		Last Modified: Wed, 09 Apr 2025 08:47:49 GMT  
		Size: 370.9 MB (370944754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54d483244cbd765807b70d0bafd7756e9af64de5aee82021ae963e66d2d560f`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634f2b0e652687586098d43a8b441559d83049c570a62e6848356c2f9e87b79`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85214e0da48193405ded7ff55ab0832229216216bb2a178b6529509fc09c48fb`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bf860135472885237bac415f0f99cba7fa9ac124033f997bcde4496d281ff`  
		Last Modified: Wed, 09 Apr 2025 08:47:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:fa687cf5ebfc545647c8bfad64459a8dbe37a68d507ddc5a28aea6d1803aedf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59217817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761169e0a8fed7a87cbf509d301f87d3660bd84565bf0433dc1be31521b948d`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e2a4c474efcea7842985873ac83934241bc47bac5c354344d020d0b1084be`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 59.2 MB (59190519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77184d1ddd1a99829f78735c0f58ea57f539cb32caf5bc62598d3b9629e95dd0`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 27.3 KB (27298 bytes)  
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
$ docker pull odoo@sha256:b81189bac8724a55d9dc9a5f117550efb15781867eb7a72eff963c17f8c9106d
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
$ docker pull odoo@sha256:7b17817332c81e923fe2860d95a053bb50472eb3c083cfda522eb314893d22fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666463468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba293c91a5e85faad03a478504f053983b1c98e0e74c464f84145e812437f5ad`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f90952dae6165d5242078f746846abbc58c2cc44fa09ca8a4c18209d53df7`  
		Last Modified: Wed, 09 Apr 2025 08:47:49 GMT  
		Size: 370.9 MB (370944754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54d483244cbd765807b70d0bafd7756e9af64de5aee82021ae963e66d2d560f`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634f2b0e652687586098d43a8b441559d83049c570a62e6848356c2f9e87b79`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85214e0da48193405ded7ff55ab0832229216216bb2a178b6529509fc09c48fb`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bf860135472885237bac415f0f99cba7fa9ac124033f997bcde4496d281ff`  
		Last Modified: Wed, 09 Apr 2025 08:47:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fa687cf5ebfc545647c8bfad64459a8dbe37a68d507ddc5a28aea6d1803aedf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59217817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761169e0a8fed7a87cbf509d301f87d3660bd84565bf0433dc1be31521b948d`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e2a4c474efcea7842985873ac83934241bc47bac5c354344d020d0b1084be`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 59.2 MB (59190519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77184d1ddd1a99829f78735c0f58ea57f539cb32caf5bc62598d3b9629e95dd0`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 27.3 KB (27298 bytes)  
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
$ docker pull odoo@sha256:b81189bac8724a55d9dc9a5f117550efb15781867eb7a72eff963c17f8c9106d
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
$ docker pull odoo@sha256:7b17817332c81e923fe2860d95a053bb50472eb3c083cfda522eb314893d22fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666463468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba293c91a5e85faad03a478504f053983b1c98e0e74c464f84145e812437f5ad`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f90952dae6165d5242078f746846abbc58c2cc44fa09ca8a4c18209d53df7`  
		Last Modified: Wed, 09 Apr 2025 08:47:49 GMT  
		Size: 370.9 MB (370944754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54d483244cbd765807b70d0bafd7756e9af64de5aee82021ae963e66d2d560f`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634f2b0e652687586098d43a8b441559d83049c570a62e6848356c2f9e87b79`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85214e0da48193405ded7ff55ab0832229216216bb2a178b6529509fc09c48fb`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bf860135472885237bac415f0f99cba7fa9ac124033f997bcde4496d281ff`  
		Last Modified: Wed, 09 Apr 2025 08:47:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:fa687cf5ebfc545647c8bfad64459a8dbe37a68d507ddc5a28aea6d1803aedf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59217817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761169e0a8fed7a87cbf509d301f87d3660bd84565bf0433dc1be31521b948d`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e2a4c474efcea7842985873ac83934241bc47bac5c354344d020d0b1084be`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 59.2 MB (59190519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77184d1ddd1a99829f78735c0f58ea57f539cb32caf5bc62598d3b9629e95dd0`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 27.3 KB (27298 bytes)  
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
$ docker pull odoo@sha256:b81189bac8724a55d9dc9a5f117550efb15781867eb7a72eff963c17f8c9106d
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
$ docker pull odoo@sha256:7b17817332c81e923fe2860d95a053bb50472eb3c083cfda522eb314893d22fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.5 MB (666463468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba293c91a5e85faad03a478504f053983b1c98e0e74c464f84145e812437f5ad`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 01 Apr 2025 13:33:26 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f90952dae6165d5242078f746846abbc58c2cc44fa09ca8a4c18209d53df7`  
		Last Modified: Wed, 09 Apr 2025 08:47:49 GMT  
		Size: 370.9 MB (370944754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54d483244cbd765807b70d0bafd7756e9af64de5aee82021ae963e66d2d560f`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634f2b0e652687586098d43a8b441559d83049c570a62e6848356c2f9e87b79`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85214e0da48193405ded7ff55ab0832229216216bb2a178b6529509fc09c48fb`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bf860135472885237bac415f0f99cba7fa9ac124033f997bcde4496d281ff`  
		Last Modified: Wed, 09 Apr 2025 08:47:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fa687cf5ebfc545647c8bfad64459a8dbe37a68d507ddc5a28aea6d1803aedf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59217817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761169e0a8fed7a87cbf509d301f87d3660bd84565bf0433dc1be31521b948d`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e2a4c474efcea7842985873ac83934241bc47bac5c354344d020d0b1084be`  
		Last Modified: Wed, 09 Apr 2025 08:47:42 GMT  
		Size: 59.2 MB (59190519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77184d1ddd1a99829f78735c0f58ea57f539cb32caf5bc62598d3b9629e95dd0`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 27.3 KB (27298 bytes)  
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
