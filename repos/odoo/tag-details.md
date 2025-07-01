<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250618`](#odoo160-20250618)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250618`](#odoo170-20250618)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250618`](#odoo180-20250618)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:6b4864eacb5d3b84802a44197c73640f955dbc4e6e75d2af4eeb05869ee6998b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:4f4d44e170e5d043cff3bbcf284a5951a02681e94a9f6accf152273b7ebaff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (584975183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bec8caa86141b28e4b2a77d948f282b8397045428dc6475f51c2b643939c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a04a836703619c8909b27f54b193e6ba913b613cef69ba2252dac13bb9e0e5`  
		Last Modified: Tue, 01 Jul 2025 04:12:26 GMT  
		Size: 219.6 MB (219627619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb92d799a9492d494e265a43aeff2d2c728727be82bd15818b35f1d52575bd69`  
		Last Modified: Tue, 01 Jul 2025 02:32:34 GMT  
		Size: 2.6 MB (2627222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12702fe2bccd22112b60b21668f913e6abb712e821b5c8c5561b5ca59b846b74`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 479.0 KB (479042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a288b153da67364f5626c5fe17fc864ceab882c6f6b74cc95e085b6be75ef0`  
		Last Modified: Tue, 01 Jul 2025 04:12:34 GMT  
		Size: 332.0 MB (331982826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4b06b66489277d0f6d88e7c8529c1d8d0e5db1362343599026815bc50bb098`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23305ae50ad4dc0980ec5d230986a213f4c61ad35bb4f13bfbbaa9b74fe7a82`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ee37ad8f2bbcf421c52541e90cddad1100e577012716a5190eb3b2448154d`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5389ade6fd7e6053656a0f5c76590c07927a835a6d2e735b3d0530e1ba2808`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:ff7068c06032bd6a5616de3e9b1ac62deefe81cce8d9df0ce67882a0422b0389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39554647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e369457e7b603a111f04f373cd1b648309476b2fad61f1f26d222c9c4e80c5`

```dockerfile
```

-	Layers:
	-	`sha256:64281cd7a167bf05344fa7d477a8ff449fb89ccb154f35b87f122b786f23ead2`  
		Last Modified: Tue, 01 Jul 2025 04:12:21 GMT  
		Size: 39.5 MB (39527929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55a2d833ee6f892df9e5d90b482022ffc0ded3ca3f71284f78f98bde07c1cc6`  
		Last Modified: Tue, 01 Jul 2025 04:12:23 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ab297e2298c3195a7b271ceee214260643a8d368365461b9bbb50a2316d09024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580409873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42a916f1277b7b6d427fcf330172eae1bf0861f549afebced13856bbba79001`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079532b13293d18a64f0dd941d41a2bcd7990c1a72e8075fd97e515714ac6d8b`  
		Last Modified: Tue, 01 Jul 2025 10:16:33 GMT  
		Size: 216.9 MB (216919936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8ebd7487d1c2c36e39ec19cdd5f6c99f5d8e10dbbc95c341a4ba4678d40f3a`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 2.6 MB (2635460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4542ff2a6a1c0109a8d6b64c44add746499e5b5d65c8f045942f12e3b7bcfa7`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 479.1 KB (479068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826cd8748f8f7a18037b02851b31e6a1127ac1ea0c5784b47a9d79918ef9f10`  
		Last Modified: Tue, 01 Jul 2025 10:15:56 GMT  
		Size: 331.6 MB (331628837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622e8a59af11fc5f029ef50674fb1a034d5e1a833f3d3d7184cb6e67c33edd1`  
		Last Modified: Tue, 01 Jul 2025 07:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20266b889ee6409a6cb2a1649c96bf156167d439bc263177ebc6fa648580d972`  
		Last Modified: Tue, 01 Jul 2025 07:33:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f06c45c625c7ee39fd071786977ee928668c2dbe57fe81c00e326f6545610f5`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459cb9e156776565810c8fa0a87fc6b3579b19c21c13240e7db92bcc11fd1a5`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:dbe25c03ee93f0b0ec2c361d5c422e2ef2178b1089f738cc58a1f3891c58c0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39561265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c001dee951b1e5ed76fe1643f46fbbe8b894f0f7116ba09d3cb0fc9a1828f`

```dockerfile
```

-	Layers:
	-	`sha256:02c8ca39a7f78af64c5b21d55ba72ccb503c28c9e9290bbf08efc322da4c8680`  
		Last Modified: Tue, 01 Jul 2025 10:12:58 GMT  
		Size: 39.5 MB (39534395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8979e39f8cde5af3d1f0976181e954350fabac7aace2bbc281804ac12811e36f`  
		Last Modified: Tue, 01 Jul 2025 10:12:59 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:6b4864eacb5d3b84802a44197c73640f955dbc4e6e75d2af4eeb05869ee6998b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:4f4d44e170e5d043cff3bbcf284a5951a02681e94a9f6accf152273b7ebaff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (584975183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bec8caa86141b28e4b2a77d948f282b8397045428dc6475f51c2b643939c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a04a836703619c8909b27f54b193e6ba913b613cef69ba2252dac13bb9e0e5`  
		Last Modified: Tue, 01 Jul 2025 04:12:26 GMT  
		Size: 219.6 MB (219627619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb92d799a9492d494e265a43aeff2d2c728727be82bd15818b35f1d52575bd69`  
		Last Modified: Tue, 01 Jul 2025 02:32:34 GMT  
		Size: 2.6 MB (2627222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12702fe2bccd22112b60b21668f913e6abb712e821b5c8c5561b5ca59b846b74`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 479.0 KB (479042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a288b153da67364f5626c5fe17fc864ceab882c6f6b74cc95e085b6be75ef0`  
		Last Modified: Tue, 01 Jul 2025 04:12:34 GMT  
		Size: 332.0 MB (331982826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4b06b66489277d0f6d88e7c8529c1d8d0e5db1362343599026815bc50bb098`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23305ae50ad4dc0980ec5d230986a213f4c61ad35bb4f13bfbbaa9b74fe7a82`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ee37ad8f2bbcf421c52541e90cddad1100e577012716a5190eb3b2448154d`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5389ade6fd7e6053656a0f5c76590c07927a835a6d2e735b3d0530e1ba2808`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ff7068c06032bd6a5616de3e9b1ac62deefe81cce8d9df0ce67882a0422b0389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39554647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e369457e7b603a111f04f373cd1b648309476b2fad61f1f26d222c9c4e80c5`

```dockerfile
```

-	Layers:
	-	`sha256:64281cd7a167bf05344fa7d477a8ff449fb89ccb154f35b87f122b786f23ead2`  
		Last Modified: Tue, 01 Jul 2025 04:12:21 GMT  
		Size: 39.5 MB (39527929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55a2d833ee6f892df9e5d90b482022ffc0ded3ca3f71284f78f98bde07c1cc6`  
		Last Modified: Tue, 01 Jul 2025 04:12:23 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ab297e2298c3195a7b271ceee214260643a8d368365461b9bbb50a2316d09024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580409873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42a916f1277b7b6d427fcf330172eae1bf0861f549afebced13856bbba79001`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079532b13293d18a64f0dd941d41a2bcd7990c1a72e8075fd97e515714ac6d8b`  
		Last Modified: Tue, 01 Jul 2025 10:16:33 GMT  
		Size: 216.9 MB (216919936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8ebd7487d1c2c36e39ec19cdd5f6c99f5d8e10dbbc95c341a4ba4678d40f3a`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 2.6 MB (2635460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4542ff2a6a1c0109a8d6b64c44add746499e5b5d65c8f045942f12e3b7bcfa7`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 479.1 KB (479068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826cd8748f8f7a18037b02851b31e6a1127ac1ea0c5784b47a9d79918ef9f10`  
		Last Modified: Tue, 01 Jul 2025 10:15:56 GMT  
		Size: 331.6 MB (331628837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622e8a59af11fc5f029ef50674fb1a034d5e1a833f3d3d7184cb6e67c33edd1`  
		Last Modified: Tue, 01 Jul 2025 07:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20266b889ee6409a6cb2a1649c96bf156167d439bc263177ebc6fa648580d972`  
		Last Modified: Tue, 01 Jul 2025 07:33:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f06c45c625c7ee39fd071786977ee928668c2dbe57fe81c00e326f6545610f5`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459cb9e156776565810c8fa0a87fc6b3579b19c21c13240e7db92bcc11fd1a5`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:dbe25c03ee93f0b0ec2c361d5c422e2ef2178b1089f738cc58a1f3891c58c0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39561265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c001dee951b1e5ed76fe1643f46fbbe8b894f0f7116ba09d3cb0fc9a1828f`

```dockerfile
```

-	Layers:
	-	`sha256:02c8ca39a7f78af64c5b21d55ba72ccb503c28c9e9290bbf08efc322da4c8680`  
		Last Modified: Tue, 01 Jul 2025 10:12:58 GMT  
		Size: 39.5 MB (39534395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8979e39f8cde5af3d1f0976181e954350fabac7aace2bbc281804ac12811e36f`  
		Last Modified: Tue, 01 Jul 2025 10:12:59 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250618`

```console
$ docker pull odoo@sha256:6b4864eacb5d3b84802a44197c73640f955dbc4e6e75d2af4eeb05869ee6998b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250618` - linux; amd64

```console
$ docker pull odoo@sha256:4f4d44e170e5d043cff3bbcf284a5951a02681e94a9f6accf152273b7ebaff55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.0 MB (584975183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68bec8caa86141b28e4b2a77d948f282b8397045428dc6475f51c2b643939c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a04a836703619c8909b27f54b193e6ba913b613cef69ba2252dac13bb9e0e5`  
		Last Modified: Tue, 01 Jul 2025 04:12:26 GMT  
		Size: 219.6 MB (219627619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb92d799a9492d494e265a43aeff2d2c728727be82bd15818b35f1d52575bd69`  
		Last Modified: Tue, 01 Jul 2025 02:32:34 GMT  
		Size: 2.6 MB (2627222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12702fe2bccd22112b60b21668f913e6abb712e821b5c8c5561b5ca59b846b74`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 479.0 KB (479042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a288b153da67364f5626c5fe17fc864ceab882c6f6b74cc95e085b6be75ef0`  
		Last Modified: Tue, 01 Jul 2025 04:12:34 GMT  
		Size: 332.0 MB (331982826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4b06b66489277d0f6d88e7c8529c1d8d0e5db1362343599026815bc50bb098`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23305ae50ad4dc0980ec5d230986a213f4c61ad35bb4f13bfbbaa9b74fe7a82`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ee37ad8f2bbcf421c52541e90cddad1100e577012716a5190eb3b2448154d`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5389ade6fd7e6053656a0f5c76590c07927a835a6d2e735b3d0530e1ba2808`  
		Last Modified: Tue, 01 Jul 2025 02:32:33 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:ff7068c06032bd6a5616de3e9b1ac62deefe81cce8d9df0ce67882a0422b0389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39554647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e369457e7b603a111f04f373cd1b648309476b2fad61f1f26d222c9c4e80c5`

```dockerfile
```

-	Layers:
	-	`sha256:64281cd7a167bf05344fa7d477a8ff449fb89ccb154f35b87f122b786f23ead2`  
		Last Modified: Tue, 01 Jul 2025 04:12:21 GMT  
		Size: 39.5 MB (39527929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55a2d833ee6f892df9e5d90b482022ffc0ded3ca3f71284f78f98bde07c1cc6`  
		Last Modified: Tue, 01 Jul 2025 04:12:23 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250618` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ab297e2298c3195a7b271ceee214260643a8d368365461b9bbb50a2316d09024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580409873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42a916f1277b7b6d427fcf330172eae1bf0861f549afebced13856bbba79001`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=16.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=8ef8e9aee88108cf7c6f249381e8016752eefead
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079532b13293d18a64f0dd941d41a2bcd7990c1a72e8075fd97e515714ac6d8b`  
		Last Modified: Tue, 01 Jul 2025 10:16:33 GMT  
		Size: 216.9 MB (216919936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8ebd7487d1c2c36e39ec19cdd5f6c99f5d8e10dbbc95c341a4ba4678d40f3a`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 2.6 MB (2635460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4542ff2a6a1c0109a8d6b64c44add746499e5b5d65c8f045942f12e3b7bcfa7`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 479.1 KB (479068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826cd8748f8f7a18037b02851b31e6a1127ac1ea0c5784b47a9d79918ef9f10`  
		Last Modified: Tue, 01 Jul 2025 10:15:56 GMT  
		Size: 331.6 MB (331628837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622e8a59af11fc5f029ef50674fb1a034d5e1a833f3d3d7184cb6e67c33edd1`  
		Last Modified: Tue, 01 Jul 2025 07:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20266b889ee6409a6cb2a1649c96bf156167d439bc263177ebc6fa648580d972`  
		Last Modified: Tue, 01 Jul 2025 07:33:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f06c45c625c7ee39fd071786977ee928668c2dbe57fe81c00e326f6545610f5`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459cb9e156776565810c8fa0a87fc6b3579b19c21c13240e7db92bcc11fd1a5`  
		Last Modified: Tue, 01 Jul 2025 07:33:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:dbe25c03ee93f0b0ec2c361d5c422e2ef2178b1089f738cc58a1f3891c58c0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39561265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c001dee951b1e5ed76fe1643f46fbbe8b894f0f7116ba09d3cb0fc9a1828f`

```dockerfile
```

-	Layers:
	-	`sha256:02c8ca39a7f78af64c5b21d55ba72ccb503c28c9e9290bbf08efc322da4c8680`  
		Last Modified: Tue, 01 Jul 2025 10:12:58 GMT  
		Size: 39.5 MB (39534395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8979e39f8cde5af3d1f0976181e954350fabac7aace2bbc281804ac12811e36f`  
		Last Modified: Tue, 01 Jul 2025 10:12:59 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:5ca8599e1b48bc2b21a25f255539e711eabbedbee3aed7c9b89351f83ea1accc
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
$ docker pull odoo@sha256:8fa614b2d0087688e61312e2087dacfa21650047c7f9aa07c6b6fd584b07b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (601019393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f350f0d98144c39f285220b402158418dc5315c67ef92ed74c0223bfa857f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9756d4f5d03259789163906b292cf4e571ad18d028597b45daec7c8ea53351ff`  
		Last Modified: Wed, 18 Jun 2025 19:13:28 GMT  
		Size: 233.8 MB (233787328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e58c294ecf17f62b4fb9b0a53806192e1f53397b0636dfa24f6027279f72b4`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 2.5 MB (2523052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fb39b46fd43ecaff52a2b94c14b45f42fbb06f4a73d47cc80fec229859792b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0206baaea5e9950028ff734746f018d2e4d0a345a0a80892347790ff4606a921`  
		Last Modified: Wed, 18 Jun 2025 19:13:12 GMT  
		Size: 334.7 MB (334693451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8626b4b7090c4097f891ad8cba29720a6a3619026ce5187f5a345dbf33d3db3`  
		Last Modified: Wed, 18 Jun 2025 16:45:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c401e1f91e9603fd8ca573986d0093b0e942dd1cbf3ed878a4fcf580ae53239b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e876e29b9458c8b8d50126b29e1ff18660923bc1763c7b866648311f84e1b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ca70622080cfbcfc20c742cf5c71197ce3a5a2b3933462ac814490668647f`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:6d4acc539e4348c6a72e28a7e450c6d459dfea1a934d03be5510e81b6a489d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40456796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbff25acfe8b5db4455612a2a19f43798d07fac84b59ea7d628f3ed99df997d`

```dockerfile
```

-	Layers:
	-	`sha256:7b62ff22d8b71c915615f3ec07cea4f214b308f2cd9f58198877a6583384f333`  
		Last Modified: Wed, 18 Jun 2025 19:12:41 GMT  
		Size: 40.4 MB (40429961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11645f0a1e3a2edabe1015dfefc97ba2ee2e479a61b44fc88ec90fb898ba0dad`  
		Last Modified: Wed, 18 Jun 2025 19:12:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:13e4de34af41d7e8235de872d7620c828e71429b076d39c2c23ead6eeaa016e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595803186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeb07aa5ff07bdba769079339ca752ab5d08d03266f32dd8a17644db8247452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7941e49a83a04ceea10c033d4c236e2f85303a5dbf77970e9653cba1ebe426d`  
		Last Modified: Wed, 18 Jun 2025 19:17:04 GMT  
		Size: 231.2 MB (231155625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc7d38ad6bc697e2d0171cd7e256286b0e624974fc7790d66b1f1e2fc7d473`  
		Last Modified: Wed, 18 Jun 2025 17:51:00 GMT  
		Size: 2.5 MB (2516377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d589e010a0b9df0173256737ed710097bc7a89ce7ea0b9e8b07bd26153911a6`  
		Last Modified: Wed, 18 Jun 2025 17:50:59 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc1e09e4c3c444120f93631b9f3742f9dd68510c99d1da8f29c7861e6347d12`  
		Last Modified: Wed, 18 Jun 2025 19:17:08 GMT  
		Size: 334.3 MB (334293081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92379b5afacb7dc79c55e61846bd50969708c81683f13859a1229ffed1434b2`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6582c56a777b40d297b43944c1e7049d5e7a8643f5d3f389a2d89e1e71e490`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08c821dbb1a9f34d8e5b035e138ce43ac1b0ad13a6f491da1afa66b4847a1b`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f54dab77f9cb0b4e01abc7d44deb602605fc990a7ba29e25e70ab2095ece0c`  
		Last Modified: Wed, 18 Jun 2025 17:50:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:ce467fb7815179f51c46fc3d2634d862975d6eb5794a987b3b62b456579d3436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40463454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec98789a1794c27be7d1c31b4f6a436ed707fd3cb024020a5a094352652a95f0`

```dockerfile
```

-	Layers:
	-	`sha256:52fd1431f7ffedaed76f954ea332791dfd82609dd5b6488582db417ee4130e83`  
		Last Modified: Wed, 18 Jun 2025 19:13:23 GMT  
		Size: 40.4 MB (40436468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a66bee4305bb79dceb89e4365f29895718b9750c955d5c25e0bb68674a8c5c`  
		Last Modified: Wed, 18 Jun 2025 19:13:24 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:828600a487aa65cd18e3a0e32d3e3ae8d9bddb65176195ab13199fb4a6154c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617433712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311c834147999bc07490009ca2d8a6888993ba8f9ad56dd877962586350a1c13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68660bffd25d551102e7f13bcdc5312dd1ae000e4b5c647addfea1a4826fae01`  
		Last Modified: Wed, 18 Jun 2025 19:21:13 GMT  
		Size: 243.3 MB (243259365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683ebc559b801d5c18185644bb0477356010cc230c801d41fc892a10ab74bad`  
		Last Modified: Wed, 18 Jun 2025 19:19:28 GMT  
		Size: 2.8 MB (2841434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d60a9166edfac0e3a9265ebcdb8803a36089702dadf139d93e2f25831393f7`  
		Last Modified: Wed, 18 Jun 2025 19:19:28 GMT  
		Size: 480.1 KB (480098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8633f758acf290b02aa371ad930fd9b5015684db66f311256c54e41fcd8f3502`  
		Last Modified: Wed, 18 Jun 2025 19:20:09 GMT  
		Size: 336.4 MB (336410017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b36e3c09d3e2fac782ac45242fb035b2ebc843bdb1ec6b37633e7b5444b21e`  
		Last Modified: Wed, 18 Jun 2025 19:19:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec35e3c804db54f6fe3fcc35e0861c0c665b8d3e17c40b50030ca76a654e33`  
		Last Modified: Wed, 18 Jun 2025 19:19:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989ab4a4fdf36e7079dd3d7b704da8ae59d6654f1eedc8a5d087623601a2c24`  
		Last Modified: Wed, 18 Jun 2025 19:19:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed44666da283f182779ce91067be97e3865619d5a199d2f71025374180a5522`  
		Last Modified: Wed, 18 Jun 2025 19:19:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:5742309eb25856844e4362928c05ba6e01856a08cc5ece7ba86618bbee13c3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40465459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4c864a850fc98af4f3ab06b9ed8088de702a85b25c04f55fbfb4435767ba5`

```dockerfile
```

-	Layers:
	-	`sha256:34ee307c288ecdddfc94454f1b02c1aaa553998ef7add5e38f7c291e2637826d`  
		Last Modified: Wed, 18 Jun 2025 19:14:02 GMT  
		Size: 40.4 MB (40438568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e26bc8ef47c2332ddd7be0e05cecd17282d51f72d64a7adc47fea7c048fb53d`  
		Last Modified: Wed, 18 Jun 2025 19:14:03 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:5ca8599e1b48bc2b21a25f255539e711eabbedbee3aed7c9b89351f83ea1accc
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
$ docker pull odoo@sha256:8fa614b2d0087688e61312e2087dacfa21650047c7f9aa07c6b6fd584b07b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (601019393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f350f0d98144c39f285220b402158418dc5315c67ef92ed74c0223bfa857f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9756d4f5d03259789163906b292cf4e571ad18d028597b45daec7c8ea53351ff`  
		Last Modified: Wed, 18 Jun 2025 19:13:28 GMT  
		Size: 233.8 MB (233787328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e58c294ecf17f62b4fb9b0a53806192e1f53397b0636dfa24f6027279f72b4`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 2.5 MB (2523052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fb39b46fd43ecaff52a2b94c14b45f42fbb06f4a73d47cc80fec229859792b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0206baaea5e9950028ff734746f018d2e4d0a345a0a80892347790ff4606a921`  
		Last Modified: Wed, 18 Jun 2025 19:13:12 GMT  
		Size: 334.7 MB (334693451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8626b4b7090c4097f891ad8cba29720a6a3619026ce5187f5a345dbf33d3db3`  
		Last Modified: Wed, 18 Jun 2025 16:45:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c401e1f91e9603fd8ca573986d0093b0e942dd1cbf3ed878a4fcf580ae53239b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e876e29b9458c8b8d50126b29e1ff18660923bc1763c7b866648311f84e1b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ca70622080cfbcfc20c742cf5c71197ce3a5a2b3933462ac814490668647f`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6d4acc539e4348c6a72e28a7e450c6d459dfea1a934d03be5510e81b6a489d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40456796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbff25acfe8b5db4455612a2a19f43798d07fac84b59ea7d628f3ed99df997d`

```dockerfile
```

-	Layers:
	-	`sha256:7b62ff22d8b71c915615f3ec07cea4f214b308f2cd9f58198877a6583384f333`  
		Last Modified: Wed, 18 Jun 2025 19:12:41 GMT  
		Size: 40.4 MB (40429961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11645f0a1e3a2edabe1015dfefc97ba2ee2e479a61b44fc88ec90fb898ba0dad`  
		Last Modified: Wed, 18 Jun 2025 19:12:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:13e4de34af41d7e8235de872d7620c828e71429b076d39c2c23ead6eeaa016e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595803186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeb07aa5ff07bdba769079339ca752ab5d08d03266f32dd8a17644db8247452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7941e49a83a04ceea10c033d4c236e2f85303a5dbf77970e9653cba1ebe426d`  
		Last Modified: Wed, 18 Jun 2025 19:17:04 GMT  
		Size: 231.2 MB (231155625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc7d38ad6bc697e2d0171cd7e256286b0e624974fc7790d66b1f1e2fc7d473`  
		Last Modified: Wed, 18 Jun 2025 17:51:00 GMT  
		Size: 2.5 MB (2516377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d589e010a0b9df0173256737ed710097bc7a89ce7ea0b9e8b07bd26153911a6`  
		Last Modified: Wed, 18 Jun 2025 17:50:59 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc1e09e4c3c444120f93631b9f3742f9dd68510c99d1da8f29c7861e6347d12`  
		Last Modified: Wed, 18 Jun 2025 19:17:08 GMT  
		Size: 334.3 MB (334293081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92379b5afacb7dc79c55e61846bd50969708c81683f13859a1229ffed1434b2`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6582c56a777b40d297b43944c1e7049d5e7a8643f5d3f389a2d89e1e71e490`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08c821dbb1a9f34d8e5b035e138ce43ac1b0ad13a6f491da1afa66b4847a1b`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f54dab77f9cb0b4e01abc7d44deb602605fc990a7ba29e25e70ab2095ece0c`  
		Last Modified: Wed, 18 Jun 2025 17:50:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ce467fb7815179f51c46fc3d2634d862975d6eb5794a987b3b62b456579d3436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40463454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec98789a1794c27be7d1c31b4f6a436ed707fd3cb024020a5a094352652a95f0`

```dockerfile
```

-	Layers:
	-	`sha256:52fd1431f7ffedaed76f954ea332791dfd82609dd5b6488582db417ee4130e83`  
		Last Modified: Wed, 18 Jun 2025 19:13:23 GMT  
		Size: 40.4 MB (40436468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a66bee4305bb79dceb89e4365f29895718b9750c955d5c25e0bb68674a8c5c`  
		Last Modified: Wed, 18 Jun 2025 19:13:24 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:828600a487aa65cd18e3a0e32d3e3ae8d9bddb65176195ab13199fb4a6154c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617433712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311c834147999bc07490009ca2d8a6888993ba8f9ad56dd877962586350a1c13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68660bffd25d551102e7f13bcdc5312dd1ae000e4b5c647addfea1a4826fae01`  
		Last Modified: Wed, 18 Jun 2025 19:21:13 GMT  
		Size: 243.3 MB (243259365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683ebc559b801d5c18185644bb0477356010cc230c801d41fc892a10ab74bad`  
		Last Modified: Wed, 18 Jun 2025 19:19:28 GMT  
		Size: 2.8 MB (2841434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d60a9166edfac0e3a9265ebcdb8803a36089702dadf139d93e2f25831393f7`  
		Last Modified: Wed, 18 Jun 2025 19:19:28 GMT  
		Size: 480.1 KB (480098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8633f758acf290b02aa371ad930fd9b5015684db66f311256c54e41fcd8f3502`  
		Last Modified: Wed, 18 Jun 2025 19:20:09 GMT  
		Size: 336.4 MB (336410017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b36e3c09d3e2fac782ac45242fb035b2ebc843bdb1ec6b37633e7b5444b21e`  
		Last Modified: Wed, 18 Jun 2025 19:19:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec35e3c804db54f6fe3fcc35e0861c0c665b8d3e17c40b50030ca76a654e33`  
		Last Modified: Wed, 18 Jun 2025 19:19:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989ab4a4fdf36e7079dd3d7b704da8ae59d6654f1eedc8a5d087623601a2c24`  
		Last Modified: Wed, 18 Jun 2025 19:19:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed44666da283f182779ce91067be97e3865619d5a199d2f71025374180a5522`  
		Last Modified: Wed, 18 Jun 2025 19:19:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5742309eb25856844e4362928c05ba6e01856a08cc5ece7ba86618bbee13c3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40465459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4c864a850fc98af4f3ab06b9ed8088de702a85b25c04f55fbfb4435767ba5`

```dockerfile
```

-	Layers:
	-	`sha256:34ee307c288ecdddfc94454f1b02c1aaa553998ef7add5e38f7c291e2637826d`  
		Last Modified: Wed, 18 Jun 2025 19:14:02 GMT  
		Size: 40.4 MB (40438568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e26bc8ef47c2332ddd7be0e05cecd17282d51f72d64a7adc47fea7c048fb53d`  
		Last Modified: Wed, 18 Jun 2025 19:14:03 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250618`

```console
$ docker pull odoo@sha256:5ca8599e1b48bc2b21a25f255539e711eabbedbee3aed7c9b89351f83ea1accc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250618` - linux; amd64

```console
$ docker pull odoo@sha256:8fa614b2d0087688e61312e2087dacfa21650047c7f9aa07c6b6fd584b07b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (601019393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091f350f0d98144c39f285220b402158418dc5315c67ef92ed74c0223bfa857f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9756d4f5d03259789163906b292cf4e571ad18d028597b45daec7c8ea53351ff`  
		Last Modified: Wed, 18 Jun 2025 19:13:28 GMT  
		Size: 233.8 MB (233787328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e58c294ecf17f62b4fb9b0a53806192e1f53397b0636dfa24f6027279f72b4`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 2.5 MB (2523052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fb39b46fd43ecaff52a2b94c14b45f42fbb06f4a73d47cc80fec229859792b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0206baaea5e9950028ff734746f018d2e4d0a345a0a80892347790ff4606a921`  
		Last Modified: Wed, 18 Jun 2025 19:13:12 GMT  
		Size: 334.7 MB (334693451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8626b4b7090c4097f891ad8cba29720a6a3619026ce5187f5a345dbf33d3db3`  
		Last Modified: Wed, 18 Jun 2025 16:45:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c401e1f91e9603fd8ca573986d0093b0e942dd1cbf3ed878a4fcf580ae53239b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e876e29b9458c8b8d50126b29e1ff18660923bc1763c7b866648311f84e1b`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ca70622080cfbcfc20c742cf5c71197ce3a5a2b3933462ac814490668647f`  
		Last Modified: Wed, 18 Jun 2025 16:45:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:6d4acc539e4348c6a72e28a7e450c6d459dfea1a934d03be5510e81b6a489d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40456796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbff25acfe8b5db4455612a2a19f43798d07fac84b59ea7d628f3ed99df997d`

```dockerfile
```

-	Layers:
	-	`sha256:7b62ff22d8b71c915615f3ec07cea4f214b308f2cd9f58198877a6583384f333`  
		Last Modified: Wed, 18 Jun 2025 19:12:41 GMT  
		Size: 40.4 MB (40429961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11645f0a1e3a2edabe1015dfefc97ba2ee2e479a61b44fc88ec90fb898ba0dad`  
		Last Modified: Wed, 18 Jun 2025 19:12:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250618` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:13e4de34af41d7e8235de872d7620c828e71429b076d39c2c23ead6eeaa016e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595803186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeb07aa5ff07bdba769079339ca752ab5d08d03266f32dd8a17644db8247452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7941e49a83a04ceea10c033d4c236e2f85303a5dbf77970e9653cba1ebe426d`  
		Last Modified: Wed, 18 Jun 2025 19:17:04 GMT  
		Size: 231.2 MB (231155625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cc7d38ad6bc697e2d0171cd7e256286b0e624974fc7790d66b1f1e2fc7d473`  
		Last Modified: Wed, 18 Jun 2025 17:51:00 GMT  
		Size: 2.5 MB (2516377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d589e010a0b9df0173256737ed710097bc7a89ce7ea0b9e8b07bd26153911a6`  
		Last Modified: Wed, 18 Jun 2025 17:50:59 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc1e09e4c3c444120f93631b9f3742f9dd68510c99d1da8f29c7861e6347d12`  
		Last Modified: Wed, 18 Jun 2025 19:17:08 GMT  
		Size: 334.3 MB (334293081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92379b5afacb7dc79c55e61846bd50969708c81683f13859a1229ffed1434b2`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6582c56a777b40d297b43944c1e7049d5e7a8643f5d3f389a2d89e1e71e490`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08c821dbb1a9f34d8e5b035e138ce43ac1b0ad13a6f491da1afa66b4847a1b`  
		Last Modified: Wed, 18 Jun 2025 17:50:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f54dab77f9cb0b4e01abc7d44deb602605fc990a7ba29e25e70ab2095ece0c`  
		Last Modified: Wed, 18 Jun 2025 17:50:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:ce467fb7815179f51c46fc3d2634d862975d6eb5794a987b3b62b456579d3436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40463454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec98789a1794c27be7d1c31b4f6a436ed707fd3cb024020a5a094352652a95f0`

```dockerfile
```

-	Layers:
	-	`sha256:52fd1431f7ffedaed76f954ea332791dfd82609dd5b6488582db417ee4130e83`  
		Last Modified: Wed, 18 Jun 2025 19:13:23 GMT  
		Size: 40.4 MB (40436468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a66bee4305bb79dceb89e4365f29895718b9750c955d5c25e0bb68674a8c5c`  
		Last Modified: Wed, 18 Jun 2025 19:13:24 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250618` - linux; ppc64le

```console
$ docker pull odoo@sha256:828600a487aa65cd18e3a0e32d3e3ae8d9bddb65176195ab13199fb4a6154c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617433712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311c834147999bc07490009ca2d8a6888993ba8f9ad56dd877962586350a1c13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=17.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=38091d03d1680a2ce10ecb90a6868ce6ee7ba808
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68660bffd25d551102e7f13bcdc5312dd1ae000e4b5c647addfea1a4826fae01`  
		Last Modified: Wed, 18 Jun 2025 19:21:13 GMT  
		Size: 243.3 MB (243259365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683ebc559b801d5c18185644bb0477356010cc230c801d41fc892a10ab74bad`  
		Last Modified: Wed, 18 Jun 2025 19:19:28 GMT  
		Size: 2.8 MB (2841434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d60a9166edfac0e3a9265ebcdb8803a36089702dadf139d93e2f25831393f7`  
		Last Modified: Wed, 18 Jun 2025 19:19:28 GMT  
		Size: 480.1 KB (480098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8633f758acf290b02aa371ad930fd9b5015684db66f311256c54e41fcd8f3502`  
		Last Modified: Wed, 18 Jun 2025 19:20:09 GMT  
		Size: 336.4 MB (336410017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b36e3c09d3e2fac782ac45242fb035b2ebc843bdb1ec6b37633e7b5444b21e`  
		Last Modified: Wed, 18 Jun 2025 19:19:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec35e3c804db54f6fe3fcc35e0861c0c665b8d3e17c40b50030ca76a654e33`  
		Last Modified: Wed, 18 Jun 2025 19:19:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989ab4a4fdf36e7079dd3d7b704da8ae59d6654f1eedc8a5d087623601a2c24`  
		Last Modified: Wed, 18 Jun 2025 19:19:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed44666da283f182779ce91067be97e3865619d5a199d2f71025374180a5522`  
		Last Modified: Wed, 18 Jun 2025 19:19:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:5742309eb25856844e4362928c05ba6e01856a08cc5ece7ba86618bbee13c3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40465459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4c864a850fc98af4f3ab06b9ed8088de702a85b25c04f55fbfb4435767ba5`

```dockerfile
```

-	Layers:
	-	`sha256:34ee307c288ecdddfc94454f1b02c1aaa553998ef7add5e38f7c291e2637826d`  
		Last Modified: Wed, 18 Jun 2025 19:14:02 GMT  
		Size: 40.4 MB (40438568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e26bc8ef47c2332ddd7be0e05cecd17282d51f72d64a7adc47fea7c048fb53d`  
		Last Modified: Wed, 18 Jun 2025 19:14:03 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:6dc919e23f5dbed19f92caa427728a367acf1a02403fadeee8bd1fd2e7aec8ba
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
$ docker pull odoo@sha256:c0a250101a5e0121e92990cbf504ba0605fe6e82a99041b856b79c05cee673d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671969855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2b3a32e5f2b8e6f454236291f2ec917392be65b2b6946b33d2b245799b85ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4234501345d307bd9f65c766e8db33bd9c378fd03c463a9cb1acabe5318fb5`  
		Last Modified: Wed, 18 Jun 2025 19:13:02 GMT  
		Size: 254.5 MB (254518234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7cc80f51b46b254a0418ae8b65327421c1c4eac89566bc8c473cd8ce2a1a46`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 14.3 MB (14275218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb58e27e9792354432bde0711e32cc963f834c3648b55edd42288da1527457d`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 479.9 KB (479903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6a5412666a189baff0daeabdbcfbd0e8bc16e2d2fbe99c9446c5f04a10c7fc`  
		Last Modified: Wed, 18 Jun 2025 19:13:10 GMT  
		Size: 373.0 MB (372978731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77134505c950e6f9d6e266f0c891cbeb80a0c1f13170f38eb1e60bafa90435e`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82dc038c3c2ae8d6a08b7d90b56dff8854c3fbdf1b04c63d806103d6d9973e`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea9fffbdac2772812c887e3ffd6f0ba12f7b18584109cea57d4e971cd113fc`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1fc3ac85198c0c5f694cd3132e22e8a6984a794ef866508c495f49b8da749`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:875d8852a780ff9805fd317796d51da51d52a9c9bf38cd032a5dce0ef90b549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f57a35dccf57bdb803441e4d8c1e18099b723094a1adb40b2db712be8948ee`

```dockerfile
```

-	Layers:
	-	`sha256:416c053ddc57b1003c54d7b0658fa509fa0644ed09bb126714552163f55472ae`  
		Last Modified: Wed, 18 Jun 2025 19:12:56 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734c5b3d67aab672dd853e7e603c6f7987c969cc3ae2f6366a7fc3f3f3c7863`  
		Last Modified: Wed, 18 Jun 2025 19:12:58 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a036c1eb19a806ac9f940ac0b741cadd69d11e329ab0bd576644e96a8e8e818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668366951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bd4d437c2b43962128df31ea289ce4943915c2ffb72c025d347981f003ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ad9ec42e0c72203fc4e741e810810c5bc3959b3a74c7427a29043c27e0fa1f`  
		Last Modified: Wed, 18 Jun 2025 19:16:14 GMT  
		Size: 251.9 MB (251940522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5396d56cba65bdf2ac1646bb6b21175f78ac62bc81e647514e04de537db6622`  
		Last Modified: Wed, 18 Jun 2025 19:15:16 GMT  
		Size: 14.3 MB (14252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bca9551cf98da899128969736fdada648f6d2b9328a2d25f3a253b15b009a7`  
		Last Modified: Wed, 18 Jun 2025 19:15:14 GMT  
		Size: 479.9 KB (479860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a472b9def55f3cf0a5fa36895abb76a9e986b4bd8c182eab30cc69c656c6631`  
		Last Modified: Wed, 18 Jun 2025 19:15:27 GMT  
		Size: 372.8 MB (372839322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be68f87b0cf8e3931f1e879f4c614549b27b9b72998ced76551b2b90eab7063a`  
		Last Modified: Wed, 18 Jun 2025 19:15:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155f6167ca45714328aab1f7bac236a7c7dd85310be370d869916d01390f32c`  
		Last Modified: Wed, 18 Jun 2025 19:15:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf062f9a313fb1f5889a6dd5aec40edb63d3d7661bb36abc8e2dcef028cd198`  
		Last Modified: Wed, 18 Jun 2025 19:15:21 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d773f39697e191467d1ee974fce35978f0967055ffcde25348d9d9ea3153b43`  
		Last Modified: Wed, 18 Jun 2025 19:15:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c95b613d1ae1cdd255e0086816b2d6a9235330a45af9e2f74cd4f3ed4b228d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac3bd5d8a868eb3e08bcdc0ba986be6162910735d452f9a1e2fc170951de40`

```dockerfile
```

-	Layers:
	-	`sha256:3ac3b4225ece7f61986f0f22c98ae80bf8af16fc1fd748e65ed8fa738429bc45`  
		Last Modified: Wed, 18 Jun 2025 19:14:20 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6fde6a38d3657c58812a4cadc83e829c9da984d45b49ae0609476ffb3214be`  
		Last Modified: Wed, 18 Jun 2025 19:14:21 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:17b24255af93209d335d01b936d4f26c8da949dfe031652d468dc4e67b80d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688206935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e39066c85063a2a5ff5ee0823c62eca8705b34c26f7acda74bfa8500cbbf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fc2d4ee74b1b2c592dca638818da1ee6352c960e55cfdb70e5d02c28fa890`  
		Last Modified: Wed, 18 Jun 2025 19:17:12 GMT  
		Size: 265.1 MB (265078378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831033ba3dff76bea04d0aa434d577aaf114978bb0a3e8a844cc8d742f40fc`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 14.8 MB (14798069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216651f85201562423a21a2da979d28618fc3f7e298d4009e5c3ebef39b0389`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 479.9 KB (479915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a38073a067ec12e8b66e4a3020e80694e59110ee9150313438d6cfad6d3db6`  
		Last Modified: Wed, 18 Jun 2025 19:17:30 GMT  
		Size: 373.5 MB (373522922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da69e4a6943a3a17a8b26a3feed656aca650ed3ef87931e3a4dc456fffe71e3`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6f2f246a7fc6db355098991a8a84f0b7781f7321e4653de81d9229fa1b399`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6e6a238a979b9ec6a160c193d6ca5920d6d5a1990806adf804378096b8435a`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1e3b320ec59b534149a31259963aae69f90f327e97937ce1d56c8e7282a22`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:75be06765bdeabce1983980683cbd9579b81c47ed1a1cbd4becdd05baecbb281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34db7a4fe6086b31d9b958d2c7f9275571e738183ed399b1178b28cf41ec748c`

```dockerfile
```

-	Layers:
	-	`sha256:efc486fcdb370e403f960b944ce24e9404d5de87ff9918a23bde0670dcc77666`  
		Last Modified: Wed, 18 Jun 2025 19:15:33 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4d777bfe234811876a84a3d305f4ef26bf51a67816d925c8369fe9a1af2182`  
		Last Modified: Wed, 18 Jun 2025 19:15:35 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:6dc919e23f5dbed19f92caa427728a367acf1a02403fadeee8bd1fd2e7aec8ba
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
$ docker pull odoo@sha256:c0a250101a5e0121e92990cbf504ba0605fe6e82a99041b856b79c05cee673d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671969855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2b3a32e5f2b8e6f454236291f2ec917392be65b2b6946b33d2b245799b85ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4234501345d307bd9f65c766e8db33bd9c378fd03c463a9cb1acabe5318fb5`  
		Last Modified: Wed, 18 Jun 2025 19:13:02 GMT  
		Size: 254.5 MB (254518234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7cc80f51b46b254a0418ae8b65327421c1c4eac89566bc8c473cd8ce2a1a46`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 14.3 MB (14275218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb58e27e9792354432bde0711e32cc963f834c3648b55edd42288da1527457d`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 479.9 KB (479903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6a5412666a189baff0daeabdbcfbd0e8bc16e2d2fbe99c9446c5f04a10c7fc`  
		Last Modified: Wed, 18 Jun 2025 19:13:10 GMT  
		Size: 373.0 MB (372978731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77134505c950e6f9d6e266f0c891cbeb80a0c1f13170f38eb1e60bafa90435e`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82dc038c3c2ae8d6a08b7d90b56dff8854c3fbdf1b04c63d806103d6d9973e`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea9fffbdac2772812c887e3ffd6f0ba12f7b18584109cea57d4e971cd113fc`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1fc3ac85198c0c5f694cd3132e22e8a6984a794ef866508c495f49b8da749`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:875d8852a780ff9805fd317796d51da51d52a9c9bf38cd032a5dce0ef90b549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f57a35dccf57bdb803441e4d8c1e18099b723094a1adb40b2db712be8948ee`

```dockerfile
```

-	Layers:
	-	`sha256:416c053ddc57b1003c54d7b0658fa509fa0644ed09bb126714552163f55472ae`  
		Last Modified: Wed, 18 Jun 2025 19:12:56 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734c5b3d67aab672dd853e7e603c6f7987c969cc3ae2f6366a7fc3f3f3c7863`  
		Last Modified: Wed, 18 Jun 2025 19:12:58 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a036c1eb19a806ac9f940ac0b741cadd69d11e329ab0bd576644e96a8e8e818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668366951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bd4d437c2b43962128df31ea289ce4943915c2ffb72c025d347981f003ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ad9ec42e0c72203fc4e741e810810c5bc3959b3a74c7427a29043c27e0fa1f`  
		Last Modified: Wed, 18 Jun 2025 19:16:14 GMT  
		Size: 251.9 MB (251940522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5396d56cba65bdf2ac1646bb6b21175f78ac62bc81e647514e04de537db6622`  
		Last Modified: Wed, 18 Jun 2025 19:15:16 GMT  
		Size: 14.3 MB (14252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bca9551cf98da899128969736fdada648f6d2b9328a2d25f3a253b15b009a7`  
		Last Modified: Wed, 18 Jun 2025 19:15:14 GMT  
		Size: 479.9 KB (479860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a472b9def55f3cf0a5fa36895abb76a9e986b4bd8c182eab30cc69c656c6631`  
		Last Modified: Wed, 18 Jun 2025 19:15:27 GMT  
		Size: 372.8 MB (372839322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be68f87b0cf8e3931f1e879f4c614549b27b9b72998ced76551b2b90eab7063a`  
		Last Modified: Wed, 18 Jun 2025 19:15:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155f6167ca45714328aab1f7bac236a7c7dd85310be370d869916d01390f32c`  
		Last Modified: Wed, 18 Jun 2025 19:15:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf062f9a313fb1f5889a6dd5aec40edb63d3d7661bb36abc8e2dcef028cd198`  
		Last Modified: Wed, 18 Jun 2025 19:15:21 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d773f39697e191467d1ee974fce35978f0967055ffcde25348d9d9ea3153b43`  
		Last Modified: Wed, 18 Jun 2025 19:15:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c95b613d1ae1cdd255e0086816b2d6a9235330a45af9e2f74cd4f3ed4b228d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac3bd5d8a868eb3e08bcdc0ba986be6162910735d452f9a1e2fc170951de40`

```dockerfile
```

-	Layers:
	-	`sha256:3ac3b4225ece7f61986f0f22c98ae80bf8af16fc1fd748e65ed8fa738429bc45`  
		Last Modified: Wed, 18 Jun 2025 19:14:20 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6fde6a38d3657c58812a4cadc83e829c9da984d45b49ae0609476ffb3214be`  
		Last Modified: Wed, 18 Jun 2025 19:14:21 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:17b24255af93209d335d01b936d4f26c8da949dfe031652d468dc4e67b80d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688206935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e39066c85063a2a5ff5ee0823c62eca8705b34c26f7acda74bfa8500cbbf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fc2d4ee74b1b2c592dca638818da1ee6352c960e55cfdb70e5d02c28fa890`  
		Last Modified: Wed, 18 Jun 2025 19:17:12 GMT  
		Size: 265.1 MB (265078378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831033ba3dff76bea04d0aa434d577aaf114978bb0a3e8a844cc8d742f40fc`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 14.8 MB (14798069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216651f85201562423a21a2da979d28618fc3f7e298d4009e5c3ebef39b0389`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 479.9 KB (479915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a38073a067ec12e8b66e4a3020e80694e59110ee9150313438d6cfad6d3db6`  
		Last Modified: Wed, 18 Jun 2025 19:17:30 GMT  
		Size: 373.5 MB (373522922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da69e4a6943a3a17a8b26a3feed656aca650ed3ef87931e3a4dc456fffe71e3`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6f2f246a7fc6db355098991a8a84f0b7781f7321e4653de81d9229fa1b399`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6e6a238a979b9ec6a160c193d6ca5920d6d5a1990806adf804378096b8435a`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1e3b320ec59b534149a31259963aae69f90f327e97937ce1d56c8e7282a22`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:75be06765bdeabce1983980683cbd9579b81c47ed1a1cbd4becdd05baecbb281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34db7a4fe6086b31d9b958d2c7f9275571e738183ed399b1178b28cf41ec748c`

```dockerfile
```

-	Layers:
	-	`sha256:efc486fcdb370e403f960b944ce24e9404d5de87ff9918a23bde0670dcc77666`  
		Last Modified: Wed, 18 Jun 2025 19:15:33 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4d777bfe234811876a84a3d305f4ef26bf51a67816d925c8369fe9a1af2182`  
		Last Modified: Wed, 18 Jun 2025 19:15:35 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250618`

```console
$ docker pull odoo@sha256:6dc919e23f5dbed19f92caa427728a367acf1a02403fadeee8bd1fd2e7aec8ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250618` - linux; amd64

```console
$ docker pull odoo@sha256:c0a250101a5e0121e92990cbf504ba0605fe6e82a99041b856b79c05cee673d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671969855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2b3a32e5f2b8e6f454236291f2ec917392be65b2b6946b33d2b245799b85ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4234501345d307bd9f65c766e8db33bd9c378fd03c463a9cb1acabe5318fb5`  
		Last Modified: Wed, 18 Jun 2025 19:13:02 GMT  
		Size: 254.5 MB (254518234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7cc80f51b46b254a0418ae8b65327421c1c4eac89566bc8c473cd8ce2a1a46`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 14.3 MB (14275218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb58e27e9792354432bde0711e32cc963f834c3648b55edd42288da1527457d`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 479.9 KB (479903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6a5412666a189baff0daeabdbcfbd0e8bc16e2d2fbe99c9446c5f04a10c7fc`  
		Last Modified: Wed, 18 Jun 2025 19:13:10 GMT  
		Size: 373.0 MB (372978731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77134505c950e6f9d6e266f0c891cbeb80a0c1f13170f38eb1e60bafa90435e`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82dc038c3c2ae8d6a08b7d90b56dff8854c3fbdf1b04c63d806103d6d9973e`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea9fffbdac2772812c887e3ffd6f0ba12f7b18584109cea57d4e971cd113fc`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1fc3ac85198c0c5f694cd3132e22e8a6984a794ef866508c495f49b8da749`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:875d8852a780ff9805fd317796d51da51d52a9c9bf38cd032a5dce0ef90b549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f57a35dccf57bdb803441e4d8c1e18099b723094a1adb40b2db712be8948ee`

```dockerfile
```

-	Layers:
	-	`sha256:416c053ddc57b1003c54d7b0658fa509fa0644ed09bb126714552163f55472ae`  
		Last Modified: Wed, 18 Jun 2025 19:12:56 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734c5b3d67aab672dd853e7e603c6f7987c969cc3ae2f6366a7fc3f3f3c7863`  
		Last Modified: Wed, 18 Jun 2025 19:12:58 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250618` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a036c1eb19a806ac9f940ac0b741cadd69d11e329ab0bd576644e96a8e8e818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668366951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bd4d437c2b43962128df31ea289ce4943915c2ffb72c025d347981f003ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ad9ec42e0c72203fc4e741e810810c5bc3959b3a74c7427a29043c27e0fa1f`  
		Last Modified: Wed, 18 Jun 2025 19:16:14 GMT  
		Size: 251.9 MB (251940522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5396d56cba65bdf2ac1646bb6b21175f78ac62bc81e647514e04de537db6622`  
		Last Modified: Wed, 18 Jun 2025 19:15:16 GMT  
		Size: 14.3 MB (14252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bca9551cf98da899128969736fdada648f6d2b9328a2d25f3a253b15b009a7`  
		Last Modified: Wed, 18 Jun 2025 19:15:14 GMT  
		Size: 479.9 KB (479860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a472b9def55f3cf0a5fa36895abb76a9e986b4bd8c182eab30cc69c656c6631`  
		Last Modified: Wed, 18 Jun 2025 19:15:27 GMT  
		Size: 372.8 MB (372839322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be68f87b0cf8e3931f1e879f4c614549b27b9b72998ced76551b2b90eab7063a`  
		Last Modified: Wed, 18 Jun 2025 19:15:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155f6167ca45714328aab1f7bac236a7c7dd85310be370d869916d01390f32c`  
		Last Modified: Wed, 18 Jun 2025 19:15:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf062f9a313fb1f5889a6dd5aec40edb63d3d7661bb36abc8e2dcef028cd198`  
		Last Modified: Wed, 18 Jun 2025 19:15:21 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d773f39697e191467d1ee974fce35978f0967055ffcde25348d9d9ea3153b43`  
		Last Modified: Wed, 18 Jun 2025 19:15:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:c95b613d1ae1cdd255e0086816b2d6a9235330a45af9e2f74cd4f3ed4b228d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac3bd5d8a868eb3e08bcdc0ba986be6162910735d452f9a1e2fc170951de40`

```dockerfile
```

-	Layers:
	-	`sha256:3ac3b4225ece7f61986f0f22c98ae80bf8af16fc1fd748e65ed8fa738429bc45`  
		Last Modified: Wed, 18 Jun 2025 19:14:20 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6fde6a38d3657c58812a4cadc83e829c9da984d45b49ae0609476ffb3214be`  
		Last Modified: Wed, 18 Jun 2025 19:14:21 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250618` - linux; ppc64le

```console
$ docker pull odoo@sha256:17b24255af93209d335d01b936d4f26c8da949dfe031652d468dc4e67b80d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688206935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e39066c85063a2a5ff5ee0823c62eca8705b34c26f7acda74bfa8500cbbf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fc2d4ee74b1b2c592dca638818da1ee6352c960e55cfdb70e5d02c28fa890`  
		Last Modified: Wed, 18 Jun 2025 19:17:12 GMT  
		Size: 265.1 MB (265078378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831033ba3dff76bea04d0aa434d577aaf114978bb0a3e8a844cc8d742f40fc`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 14.8 MB (14798069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216651f85201562423a21a2da979d28618fc3f7e298d4009e5c3ebef39b0389`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 479.9 KB (479915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a38073a067ec12e8b66e4a3020e80694e59110ee9150313438d6cfad6d3db6`  
		Last Modified: Wed, 18 Jun 2025 19:17:30 GMT  
		Size: 373.5 MB (373522922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da69e4a6943a3a17a8b26a3feed656aca650ed3ef87931e3a4dc456fffe71e3`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6f2f246a7fc6db355098991a8a84f0b7781f7321e4653de81d9229fa1b399`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6e6a238a979b9ec6a160c193d6ca5920d6d5a1990806adf804378096b8435a`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1e3b320ec59b534149a31259963aae69f90f327e97937ce1d56c8e7282a22`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250618` - unknown; unknown

```console
$ docker pull odoo@sha256:75be06765bdeabce1983980683cbd9579b81c47ed1a1cbd4becdd05baecbb281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34db7a4fe6086b31d9b958d2c7f9275571e738183ed399b1178b28cf41ec748c`

```dockerfile
```

-	Layers:
	-	`sha256:efc486fcdb370e403f960b944ce24e9404d5de87ff9918a23bde0670dcc77666`  
		Last Modified: Wed, 18 Jun 2025 19:15:33 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4d777bfe234811876a84a3d305f4ef26bf51a67816d925c8369fe9a1af2182`  
		Last Modified: Wed, 18 Jun 2025 19:15:35 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:6dc919e23f5dbed19f92caa427728a367acf1a02403fadeee8bd1fd2e7aec8ba
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
$ docker pull odoo@sha256:c0a250101a5e0121e92990cbf504ba0605fe6e82a99041b856b79c05cee673d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671969855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2b3a32e5f2b8e6f454236291f2ec917392be65b2b6946b33d2b245799b85ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=amd64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4234501345d307bd9f65c766e8db33bd9c378fd03c463a9cb1acabe5318fb5`  
		Last Modified: Wed, 18 Jun 2025 19:13:02 GMT  
		Size: 254.5 MB (254518234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7cc80f51b46b254a0418ae8b65327421c1c4eac89566bc8c473cd8ce2a1a46`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 14.3 MB (14275218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb58e27e9792354432bde0711e32cc963f834c3648b55edd42288da1527457d`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 479.9 KB (479903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6a5412666a189baff0daeabdbcfbd0e8bc16e2d2fbe99c9446c5f04a10c7fc`  
		Last Modified: Wed, 18 Jun 2025 19:13:10 GMT  
		Size: 373.0 MB (372978731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77134505c950e6f9d6e266f0c891cbeb80a0c1f13170f38eb1e60bafa90435e`  
		Last Modified: Wed, 18 Jun 2025 16:47:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e82dc038c3c2ae8d6a08b7d90b56dff8854c3fbdf1b04c63d806103d6d9973e`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea9fffbdac2772812c887e3ffd6f0ba12f7b18584109cea57d4e971cd113fc`  
		Last Modified: Wed, 18 Jun 2025 16:47:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a1fc3ac85198c0c5f694cd3132e22e8a6984a794ef866508c495f49b8da749`  
		Last Modified: Wed, 18 Jun 2025 16:47:18 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:875d8852a780ff9805fd317796d51da51d52a9c9bf38cd032a5dce0ef90b549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f57a35dccf57bdb803441e4d8c1e18099b723094a1adb40b2db712be8948ee`

```dockerfile
```

-	Layers:
	-	`sha256:416c053ddc57b1003c54d7b0658fa509fa0644ed09bb126714552163f55472ae`  
		Last Modified: Wed, 18 Jun 2025 19:12:56 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734c5b3d67aab672dd853e7e603c6f7987c969cc3ae2f6366a7fc3f3f3c7863`  
		Last Modified: Wed, 18 Jun 2025 19:12:58 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a036c1eb19a806ac9f940ac0b741cadd69d11e329ab0bd576644e96a8e8e818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668366951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bd4d437c2b43962128df31ea289ce4943915c2ffb72c025d347981f003ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=arm64
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ad9ec42e0c72203fc4e741e810810c5bc3959b3a74c7427a29043c27e0fa1f`  
		Last Modified: Wed, 18 Jun 2025 19:16:14 GMT  
		Size: 251.9 MB (251940522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5396d56cba65bdf2ac1646bb6b21175f78ac62bc81e647514e04de537db6622`  
		Last Modified: Wed, 18 Jun 2025 19:15:16 GMT  
		Size: 14.3 MB (14252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bca9551cf98da899128969736fdada648f6d2b9328a2d25f3a253b15b009a7`  
		Last Modified: Wed, 18 Jun 2025 19:15:14 GMT  
		Size: 479.9 KB (479860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a472b9def55f3cf0a5fa36895abb76a9e986b4bd8c182eab30cc69c656c6631`  
		Last Modified: Wed, 18 Jun 2025 19:15:27 GMT  
		Size: 372.8 MB (372839322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be68f87b0cf8e3931f1e879f4c614549b27b9b72998ced76551b2b90eab7063a`  
		Last Modified: Wed, 18 Jun 2025 19:15:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a155f6167ca45714328aab1f7bac236a7c7dd85310be370d869916d01390f32c`  
		Last Modified: Wed, 18 Jun 2025 19:15:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf062f9a313fb1f5889a6dd5aec40edb63d3d7661bb36abc8e2dcef028cd198`  
		Last Modified: Wed, 18 Jun 2025 19:15:21 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d773f39697e191467d1ee974fce35978f0967055ffcde25348d9d9ea3153b43`  
		Last Modified: Wed, 18 Jun 2025 19:15:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c95b613d1ae1cdd255e0086816b2d6a9235330a45af9e2f74cd4f3ed4b228d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ac3bd5d8a868eb3e08bcdc0ba986be6162910735d452f9a1e2fc170951de40`

```dockerfile
```

-	Layers:
	-	`sha256:3ac3b4225ece7f61986f0f22c98ae80bf8af16fc1fd748e65ed8fa738429bc45`  
		Last Modified: Wed, 18 Jun 2025 19:14:20 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6fde6a38d3657c58812a4cadc83e829c9da984d45b49ae0609476ffb3214be`  
		Last Modified: Wed, 18 Jun 2025 19:14:21 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:17b24255af93209d335d01b936d4f26c8da949dfe031652d468dc4e67b80d77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688206935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e39066c85063a2a5ff5ee0823c62eca8705b34c26f7acda74bfa8500cbbf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Wed, 18 Jun 2025 14:35:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 18 Jun 2025 14:35:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Jun 2025 14:35:54 GMT
ARG TARGETARCH=ppc64le
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_VERSION=18.0
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_RELEASE=20250618
# Wed, 18 Jun 2025 14:35:54 GMT
ARG ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250618 ODOO_SHA=890716bb151cf5e9abb4ae4f33e94705ae83db1b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 18 Jun 2025 14:35:54 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 18 Jun 2025 14:35:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 18 Jun 2025 14:35:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 18 Jun 2025 14:35:54 GMT
USER odoo
# Wed, 18 Jun 2025 14:35:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Jun 2025 14:35:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fc2d4ee74b1b2c592dca638818da1ee6352c960e55cfdb70e5d02c28fa890`  
		Last Modified: Wed, 18 Jun 2025 19:17:12 GMT  
		Size: 265.1 MB (265078378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831033ba3dff76bea04d0aa434d577aaf114978bb0a3e8a844cc8d742f40fc`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 14.8 MB (14798069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5216651f85201562423a21a2da979d28618fc3f7e298d4009e5c3ebef39b0389`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 479.9 KB (479915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a38073a067ec12e8b66e4a3020e80694e59110ee9150313438d6cfad6d3db6`  
		Last Modified: Wed, 18 Jun 2025 19:17:30 GMT  
		Size: 373.5 MB (373522922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da69e4a6943a3a17a8b26a3feed656aca650ed3ef87931e3a4dc456fffe71e3`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6f2f246a7fc6db355098991a8a84f0b7781f7321e4653de81d9229fa1b399`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6e6a238a979b9ec6a160c193d6ca5920d6d5a1990806adf804378096b8435a`  
		Last Modified: Wed, 18 Jun 2025 17:37:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1e3b320ec59b534149a31259963aae69f90f327e97937ce1d56c8e7282a22`  
		Last Modified: Wed, 18 Jun 2025 17:37:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:75be06765bdeabce1983980683cbd9579b81c47ed1a1cbd4becdd05baecbb281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34db7a4fe6086b31d9b958d2c7f9275571e738183ed399b1178b28cf41ec748c`

```dockerfile
```

-	Layers:
	-	`sha256:efc486fcdb370e403f960b944ce24e9404d5de87ff9918a23bde0670dcc77666`  
		Last Modified: Wed, 18 Jun 2025 19:15:33 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4d777bfe234811876a84a3d305f4ef26bf51a67816d925c8369fe9a1af2182`  
		Last Modified: Wed, 18 Jun 2025 19:15:35 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json
