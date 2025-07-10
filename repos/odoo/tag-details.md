<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250710`](#odoo160-20250710)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250710`](#odoo170-20250710)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250710`](#odoo180-20250710)
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

## `odoo:16.0-20250710`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:17`

```console
$ docker pull odoo@sha256:d5050ece129fe3bd9cf9902ae273941e661aa0437954013c8d373bef7b52b777
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
$ docker pull odoo@sha256:38d449bfd532e2f049367e2f7eaaee395d5d83fab63718ae97f66f517eb8f718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (601024918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42896d69d38d6ea93fecfa87592e069fd397d2245af8801cb34a1a0a74ec74f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6be28e0623ce4048c941c0dc757d6d0175a7a88e59d48db0e6639a001666b6`  
		Last Modified: Wed, 02 Jul 2025 07:12:29 GMT  
		Size: 233.8 MB (233788730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4937b876813a364c138c349b87fdbb925b7736ebb96b37ee279f19416eeb1af`  
		Last Modified: Wed, 02 Jul 2025 05:34:47 GMT  
		Size: 2.5 MB (2522972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ce7f192e10ba62f367fd7e58d724dfab18a2aad8dce62af1a3f8a17caf5b3`  
		Last Modified: Wed, 02 Jul 2025 05:35:02 GMT  
		Size: 480.1 KB (480099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0c18ae065bbb9e1d40b6302484d3eab99bad7a4474f65c094686ba78b5182`  
		Last Modified: Wed, 02 Jul 2025 07:12:34 GMT  
		Size: 334.7 MB (334694994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62147dfa04c56f36f6d497fbc23d2b71f1d5f16894173e7d89e0c6cf1ac03f6d`  
		Last Modified: Wed, 02 Jul 2025 05:35:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814d5bae0f00e2c8beea969a88ec4edbcba1e1b0c79b31f9c220e097990293c`  
		Last Modified: Wed, 02 Jul 2025 05:35:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7283c7a05de2dce904aa4bc52a1227d8d936b066f173994f374862ec60ae1a32`  
		Last Modified: Wed, 02 Jul 2025 05:35:13 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6deb9576cc7cff0f403e9fdd42eac76d14ef284f9427005af686df125afee66e`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:6372b5f1f205036cb45712a295871a9c40823516722c6ca01436d1412a256f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40456795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9155c3d17afd9b1b889e0ba1cbcc64cc1333364e38a0a5afe31bbe73d2d8a90`

```dockerfile
```

-	Layers:
	-	`sha256:ea1ac38b9ff9f3fd7e656f83c64d40a4be03ccaae94daf75a42a01df10c0e81a`  
		Last Modified: Wed, 02 Jul 2025 07:12:26 GMT  
		Size: 40.4 MB (40429961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87fc2a8bc4fb4a7f48159165c675578d49a735356bf5b2e4f6b45ab12c8e4f23`  
		Last Modified: Wed, 02 Jul 2025 07:12:27 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a7a84dbaa7d572b8f5743716bfba35c787000936d88bbd55bc79779e329f5e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595807994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c257ff5807042d9a45cbed5466c01a222c30abdf92e4836c910565078edd3cf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c86124df46151281b12e28b4a56b43a15472ecf23c2fb3eccc7233bc3c847`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 231.2 MB (231155283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7ee5a1beb01cd4f56f69aed4ce84327c4e136c5c04f9531a526a7f9934cf9`  
		Last Modified: Wed, 02 Jul 2025 07:25:46 GMT  
		Size: 2.5 MB (2516262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2529d3bfb7f973f508e180afefaf73063a3c6655fbaeb45d744a1c8366ad6d77`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 480.1 KB (480091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314689f62bbe251a43c07b4ed464fd5e38b8445b30f5e6ee59b010e60716245f`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 334.3 MB (334294649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20714d6f9faba702a87f8635922d46fa78318b82ed697ce4af6b9408d7972054`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25164f12ac443f9a2af97106d243860a99587cbf6df70bd8a46bdb2e3f147ac`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1260ad8a8027341b0ce7bb9c98d2ba1fa7bf81909cd82f6e228a22c415fa0a`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0337061beff0ff71182e8cf23387fd833f78f1c9ef7b5ed37468c8dbca4687d`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:8809681750b3e980b07cb2aa638e8c89f5fa97e14a4620e251a39f90c46b0955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40463455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b55a2d9612d030d188e1b234b76a6c5a59a726ddc1391708aac2f2499c4e3e`

```dockerfile
```

-	Layers:
	-	`sha256:87478dcf6de60c9d5fdae37f459cf2e86be536b20b1e011834932d493eddd4f4`  
		Last Modified: Wed, 02 Jul 2025 10:12:56 GMT  
		Size: 40.4 MB (40436468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c0d402b37dd650b0050cca8959026ae49fe04abca3a1b5c47bc4e92fc9d4e8`  
		Last Modified: Wed, 02 Jul 2025 10:12:57 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:1d35450b35a85807fe5edb837894f96b6e4ddccde4c5af6d50310b0219efbff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617436188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7efe5e55516ca1b585e1738b32e1f841f591e8c63063fd074fb9d8ed767f5f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6ea6d5109d4d1b0a3362e810a1cd03a8680dcebb1b35dd00b36949d86c3e3`  
		Last Modified: Wed, 02 Jul 2025 14:49:08 GMT  
		Size: 243.3 MB (243261706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5064b7f25f4525a7d9e2d3d4505d2351d777fcd398b6d2b1acd03d9360cb25b`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 2.8 MB (2841522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4813f1ddec64145879a01ab0e281abf700bc8755c273d520e1bb54bfb92fc3c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc10ea94a3fe3bb85c21174020d10d3c3ae696130c97053de935696e8e0853b`  
		Last Modified: Wed, 02 Jul 2025 14:49:09 GMT  
		Size: 336.4 MB (336407793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309f0201e43c6f7651820cbc35a0d805a37b34b9eea7ac64ff87f59d96b2ee3`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588b7975b944ef790c69945f856978390ec723901b410dd5e33fcb262e6dc4c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518edefbe74cd2fc9419f3904d096b56deb01b7489ca79c251bc1be890077557`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26a27af91265cd5db5b1f19332a60a1487c0e55fbcf4d1f8a8858da065f8140`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:0cfc8c952430c8263bb11a1c745b5ad6cefc3eedfdc7ac602f5f96197d5e8785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40465459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0b81b3a787f0be3226c33bf36f0c0288b555066fd68669b1c2493a9cacd0ac`

```dockerfile
```

-	Layers:
	-	`sha256:4adcba5e71dbfa41a0073d1beb473856d9970708150ff39500998dad10716c3c`  
		Last Modified: Wed, 02 Jul 2025 07:13:45 GMT  
		Size: 40.4 MB (40438568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf30323e2b9f581d9fc4c01df76117646c8d4f580b68448786f7b16d20ed9a1`  
		Last Modified: Wed, 02 Jul 2025 07:13:46 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d5050ece129fe3bd9cf9902ae273941e661aa0437954013c8d373bef7b52b777
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
$ docker pull odoo@sha256:38d449bfd532e2f049367e2f7eaaee395d5d83fab63718ae97f66f517eb8f718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (601024918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42896d69d38d6ea93fecfa87592e069fd397d2245af8801cb34a1a0a74ec74f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6be28e0623ce4048c941c0dc757d6d0175a7a88e59d48db0e6639a001666b6`  
		Last Modified: Wed, 02 Jul 2025 07:12:29 GMT  
		Size: 233.8 MB (233788730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4937b876813a364c138c349b87fdbb925b7736ebb96b37ee279f19416eeb1af`  
		Last Modified: Wed, 02 Jul 2025 05:34:47 GMT  
		Size: 2.5 MB (2522972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ce7f192e10ba62f367fd7e58d724dfab18a2aad8dce62af1a3f8a17caf5b3`  
		Last Modified: Wed, 02 Jul 2025 05:35:02 GMT  
		Size: 480.1 KB (480099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0c18ae065bbb9e1d40b6302484d3eab99bad7a4474f65c094686ba78b5182`  
		Last Modified: Wed, 02 Jul 2025 07:12:34 GMT  
		Size: 334.7 MB (334694994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62147dfa04c56f36f6d497fbc23d2b71f1d5f16894173e7d89e0c6cf1ac03f6d`  
		Last Modified: Wed, 02 Jul 2025 05:35:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814d5bae0f00e2c8beea969a88ec4edbcba1e1b0c79b31f9c220e097990293c`  
		Last Modified: Wed, 02 Jul 2025 05:35:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7283c7a05de2dce904aa4bc52a1227d8d936b066f173994f374862ec60ae1a32`  
		Last Modified: Wed, 02 Jul 2025 05:35:13 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6deb9576cc7cff0f403e9fdd42eac76d14ef284f9427005af686df125afee66e`  
		Last Modified: Wed, 02 Jul 2025 05:35:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6372b5f1f205036cb45712a295871a9c40823516722c6ca01436d1412a256f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40456795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9155c3d17afd9b1b889e0ba1cbcc64cc1333364e38a0a5afe31bbe73d2d8a90`

```dockerfile
```

-	Layers:
	-	`sha256:ea1ac38b9ff9f3fd7e656f83c64d40a4be03ccaae94daf75a42a01df10c0e81a`  
		Last Modified: Wed, 02 Jul 2025 07:12:26 GMT  
		Size: 40.4 MB (40429961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87fc2a8bc4fb4a7f48159165c675578d49a735356bf5b2e4f6b45ab12c8e4f23`  
		Last Modified: Wed, 02 Jul 2025 07:12:27 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a7a84dbaa7d572b8f5743716bfba35c787000936d88bbd55bc79779e329f5e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595807994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c257ff5807042d9a45cbed5466c01a222c30abdf92e4836c910565078edd3cf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c86124df46151281b12e28b4a56b43a15472ecf23c2fb3eccc7233bc3c847`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 231.2 MB (231155283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7ee5a1beb01cd4f56f69aed4ce84327c4e136c5c04f9531a526a7f9934cf9`  
		Last Modified: Wed, 02 Jul 2025 07:25:46 GMT  
		Size: 2.5 MB (2516262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2529d3bfb7f973f508e180afefaf73063a3c6655fbaeb45d744a1c8366ad6d77`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 480.1 KB (480091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314689f62bbe251a43c07b4ed464fd5e38b8445b30f5e6ee59b010e60716245f`  
		Last Modified: Wed, 02 Jul 2025 10:15:36 GMT  
		Size: 334.3 MB (334294649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20714d6f9faba702a87f8635922d46fa78318b82ed697ce4af6b9408d7972054`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25164f12ac443f9a2af97106d243860a99587cbf6df70bd8a46bdb2e3f147ac`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1260ad8a8027341b0ce7bb9c98d2ba1fa7bf81909cd82f6e228a22c415fa0a`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0337061beff0ff71182e8cf23387fd833f78f1c9ef7b5ed37468c8dbca4687d`  
		Last Modified: Wed, 02 Jul 2025 06:14:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8809681750b3e980b07cb2aa638e8c89f5fa97e14a4620e251a39f90c46b0955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40463455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b55a2d9612d030d188e1b234b76a6c5a59a726ddc1391708aac2f2499c4e3e`

```dockerfile
```

-	Layers:
	-	`sha256:87478dcf6de60c9d5fdae37f459cf2e86be536b20b1e011834932d493eddd4f4`  
		Last Modified: Wed, 02 Jul 2025 10:12:56 GMT  
		Size: 40.4 MB (40436468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c0d402b37dd650b0050cca8959026ae49fe04abca3a1b5c47bc4e92fc9d4e8`  
		Last Modified: Wed, 02 Jul 2025 10:12:57 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1d35450b35a85807fe5edb837894f96b6e4ddccde4c5af6d50310b0219efbff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617436188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7efe5e55516ca1b585e1738b32e1f841f591e8c63063fd074fb9d8ed767f5f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6ea6d5109d4d1b0a3362e810a1cd03a8680dcebb1b35dd00b36949d86c3e3`  
		Last Modified: Wed, 02 Jul 2025 14:49:08 GMT  
		Size: 243.3 MB (243261706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5064b7f25f4525a7d9e2d3d4505d2351d777fcd398b6d2b1acd03d9360cb25b`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 2.8 MB (2841522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4813f1ddec64145879a01ab0e281abf700bc8755c273d520e1bb54bfb92fc3c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc10ea94a3fe3bb85c21174020d10d3c3ae696130c97053de935696e8e0853b`  
		Last Modified: Wed, 02 Jul 2025 14:49:09 GMT  
		Size: 336.4 MB (336407793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309f0201e43c6f7651820cbc35a0d805a37b34b9eea7ac64ff87f59d96b2ee3`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588b7975b944ef790c69945f856978390ec723901b410dd5e33fcb262e6dc4c`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518edefbe74cd2fc9419f3904d096b56deb01b7489ca79c251bc1be890077557`  
		Last Modified: Wed, 02 Jul 2025 04:23:09 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26a27af91265cd5db5b1f19332a60a1487c0e55fbcf4d1f8a8858da065f8140`  
		Last Modified: Wed, 02 Jul 2025 04:23:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0cfc8c952430c8263bb11a1c745b5ad6cefc3eedfdc7ac602f5f96197d5e8785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40465459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0b81b3a787f0be3226c33bf36f0c0288b555066fd68669b1c2493a9cacd0ac`

```dockerfile
```

-	Layers:
	-	`sha256:4adcba5e71dbfa41a0073d1beb473856d9970708150ff39500998dad10716c3c`  
		Last Modified: Wed, 02 Jul 2025 07:13:45 GMT  
		Size: 40.4 MB (40438568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf30323e2b9f581d9fc4c01df76117646c8d4f580b68448786f7b16d20ed9a1`  
		Last Modified: Wed, 02 Jul 2025 07:13:46 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250710`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:18`

```console
$ docker pull odoo@sha256:3f8bd1cfae97c6770830da17abda966fada9a1515961fa4eb636cf26cd685302
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
$ docker pull odoo@sha256:5cc8c420e9991f7c73d9bf5585ecd0f62e503218cb262c69e411edadf8305b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671974527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07380c9347bee149d19a626cb826650f1a17eeb80db90cef4aca4f4ed296802`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505ae1705c3fbee13d68d89efe5ee68807ece7ef97242d3404328e8884dca0f`  
		Last Modified: Wed, 02 Jul 2025 07:12:52 GMT  
		Size: 254.5 MB (254519039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff8f8953bb94fda9da4fca088bfc41b3542ccaed711e48b3a9b562b81aa0d6`  
		Last Modified: Wed, 02 Jul 2025 03:15:12 GMT  
		Size: 14.3 MB (14275544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da5abcd1121f4d67a267457dc8e7a3b189e8c8c8e8c10fa2d11c3046e2bf48a`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 479.9 KB (479899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ef76349e6b9fd321abefa3e3c6d2f84ed1431d452c7c5cce84be03993a4058`  
		Last Modified: Wed, 02 Jul 2025 07:13:01 GMT  
		Size: 373.0 MB (372979239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e08692a7bf8e0edd6fa87c2f4985212f63301754cfc27d4c811f46bc1ae73`  
		Last Modified: Wed, 02 Jul 2025 03:15:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb4c15c368458e13ff368a8b3276a6a672470265244f205291ec21378f29ab5`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3ab9a1ac400147c52aafaa76d3046cc7beb87c69f8b65016e10d8e765d4b0`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eba7df5719be0ea6a64a9c79e44f0ae91981da9a2e51d3e64dacf380513181`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:70b38a057c072d703b555e152b3d568d146b6aa77f9d9a71aa2d31b2cd27e3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e9e005fdceebc7e588f488274b3a173fd8c41a252b321dec0e5441b3b3842e`

```dockerfile
```

-	Layers:
	-	`sha256:0b91bfb147f1b3a8adc474899669cc30cdfeaad610b4f7ae51efa870c5b65819`  
		Last Modified: Wed, 02 Jul 2025 07:12:40 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aecc6c8988aa06318aa1e71f96d764b708900ebadeba40d8e49c764a46bf3ba`  
		Last Modified: Wed, 02 Jul 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:dc9592a16a6deff3c97eeb0a751ed4311b4e14bb9806e59271c1f7577bcf7547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668351873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b87f2b14619a1d5ad6a99383d339b592bf69fda4ad8b6c4e9e45991890f85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599923d3890d070101f674768dba0cc96125480fed5ab7562d29344219d38e1`  
		Last Modified: Wed, 02 Jul 2025 10:15:27 GMT  
		Size: 372.8 MB (372838682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2b66a652d1e4b3b32a2782c472ca3d3a8324f5334c40d1ca81e55cb5bb0ae`  
		Last Modified: Wed, 02 Jul 2025 07:13:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67748aa358e9c43f418b2f15314343a44df1c0e20a4e41d4a242089c6a5e5bec`  
		Last Modified: Wed, 02 Jul 2025 07:13:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e034dc509b560817e2739b6ed8fb8375e53a3f4ba3d84d7744d162b120e12d04`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099c2535c2ad00a73d70e886bf22b98dfb5d698ed1c025341502c9f1d3456b64`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:17412c8d264e2f1c08aa6f9a80a9f119c03bc1c864a6affc1a7e04991703898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b6750a308ff3684bc7b8499c20cb664877fe39024d2a13dda8fa6839c510d6`

```dockerfile
```

-	Layers:
	-	`sha256:2eb71e33ad446a2eaf333b07abc20a9f875054503b98715d6ffa6ab3645e586f`  
		Last Modified: Wed, 02 Jul 2025 10:13:44 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1063750fedcfd7195959c13131a685b2fa5708c594194bea23b4670a7ae6e089`  
		Last Modified: Wed, 02 Jul 2025 10:13:45 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:35bfdb6fbbc0706e955d08d757b6ca201a473aabf3c125487ddf12efc371c7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688187044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64176b42bf98d296525725398f7a92cef43ddd68da38d9880b95dfd50e97deb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b630f000bb741c56ceee013f0fa5295950e00d7db4db9cd2a77358a52e363e`  
		Last Modified: Wed, 02 Jul 2025 18:22:43 GMT  
		Size: 373.5 MB (373507290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97dbd706152799154425e73cc593cc350050e360e06c995f80621ecfdba07`  
		Last Modified: Wed, 02 Jul 2025 04:25:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb841bd213104808cad22caba8e076200444582c8b6766a14069e5b67f0b4076`  
		Last Modified: Wed, 02 Jul 2025 04:25:38 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2f3482e5edc25dea04e59f7d3f69c3a9bcb874ecd09ff7b76d09938b387316`  
		Last Modified: Wed, 02 Jul 2025 04:25:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95935b4f74e7325865844918ed4dc936bf6a7f5355be6a70c907e879756e3925`  
		Last Modified: Wed, 02 Jul 2025 04:25:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0b9b19efcc494b8caa9ccf52bcb03e0e7ddd213ac7ecf69b8dc03920083ee2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4584ac0e893b5bb6ab6ac40fb0055bcb4e2e8a460bed34d7f001302a4fba07a`

```dockerfile
```

-	Layers:
	-	`sha256:71826fd51a8a4a6f205b8879cda5575d12eb885004f2c0256e1e57fb103a96fa`  
		Last Modified: Wed, 02 Jul 2025 07:15:26 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af14adde1859cef369b47c64c3d6347187b3d11ea55a8b4e33b442e59dfdb33`  
		Last Modified: Wed, 02 Jul 2025 07:15:27 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:3f8bd1cfae97c6770830da17abda966fada9a1515961fa4eb636cf26cd685302
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
$ docker pull odoo@sha256:5cc8c420e9991f7c73d9bf5585ecd0f62e503218cb262c69e411edadf8305b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671974527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07380c9347bee149d19a626cb826650f1a17eeb80db90cef4aca4f4ed296802`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505ae1705c3fbee13d68d89efe5ee68807ece7ef97242d3404328e8884dca0f`  
		Last Modified: Wed, 02 Jul 2025 07:12:52 GMT  
		Size: 254.5 MB (254519039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff8f8953bb94fda9da4fca088bfc41b3542ccaed711e48b3a9b562b81aa0d6`  
		Last Modified: Wed, 02 Jul 2025 03:15:12 GMT  
		Size: 14.3 MB (14275544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da5abcd1121f4d67a267457dc8e7a3b189e8c8c8e8c10fa2d11c3046e2bf48a`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 479.9 KB (479899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ef76349e6b9fd321abefa3e3c6d2f84ed1431d452c7c5cce84be03993a4058`  
		Last Modified: Wed, 02 Jul 2025 07:13:01 GMT  
		Size: 373.0 MB (372979239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e08692a7bf8e0edd6fa87c2f4985212f63301754cfc27d4c811f46bc1ae73`  
		Last Modified: Wed, 02 Jul 2025 03:15:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb4c15c368458e13ff368a8b3276a6a672470265244f205291ec21378f29ab5`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3ab9a1ac400147c52aafaa76d3046cc7beb87c69f8b65016e10d8e765d4b0`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eba7df5719be0ea6a64a9c79e44f0ae91981da9a2e51d3e64dacf380513181`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:70b38a057c072d703b555e152b3d568d146b6aa77f9d9a71aa2d31b2cd27e3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e9e005fdceebc7e588f488274b3a173fd8c41a252b321dec0e5441b3b3842e`

```dockerfile
```

-	Layers:
	-	`sha256:0b91bfb147f1b3a8adc474899669cc30cdfeaad610b4f7ae51efa870c5b65819`  
		Last Modified: Wed, 02 Jul 2025 07:12:40 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aecc6c8988aa06318aa1e71f96d764b708900ebadeba40d8e49c764a46bf3ba`  
		Last Modified: Wed, 02 Jul 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:dc9592a16a6deff3c97eeb0a751ed4311b4e14bb9806e59271c1f7577bcf7547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668351873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b87f2b14619a1d5ad6a99383d339b592bf69fda4ad8b6c4e9e45991890f85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599923d3890d070101f674768dba0cc96125480fed5ab7562d29344219d38e1`  
		Last Modified: Wed, 02 Jul 2025 10:15:27 GMT  
		Size: 372.8 MB (372838682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2b66a652d1e4b3b32a2782c472ca3d3a8324f5334c40d1ca81e55cb5bb0ae`  
		Last Modified: Wed, 02 Jul 2025 07:13:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67748aa358e9c43f418b2f15314343a44df1c0e20a4e41d4a242089c6a5e5bec`  
		Last Modified: Wed, 02 Jul 2025 07:13:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e034dc509b560817e2739b6ed8fb8375e53a3f4ba3d84d7744d162b120e12d04`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099c2535c2ad00a73d70e886bf22b98dfb5d698ed1c025341502c9f1d3456b64`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:17412c8d264e2f1c08aa6f9a80a9f119c03bc1c864a6affc1a7e04991703898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b6750a308ff3684bc7b8499c20cb664877fe39024d2a13dda8fa6839c510d6`

```dockerfile
```

-	Layers:
	-	`sha256:2eb71e33ad446a2eaf333b07abc20a9f875054503b98715d6ffa6ab3645e586f`  
		Last Modified: Wed, 02 Jul 2025 10:13:44 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1063750fedcfd7195959c13131a685b2fa5708c594194bea23b4670a7ae6e089`  
		Last Modified: Wed, 02 Jul 2025 10:13:45 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:35bfdb6fbbc0706e955d08d757b6ca201a473aabf3c125487ddf12efc371c7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688187044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64176b42bf98d296525725398f7a92cef43ddd68da38d9880b95dfd50e97deb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b630f000bb741c56ceee013f0fa5295950e00d7db4db9cd2a77358a52e363e`  
		Last Modified: Wed, 02 Jul 2025 18:22:43 GMT  
		Size: 373.5 MB (373507290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97dbd706152799154425e73cc593cc350050e360e06c995f80621ecfdba07`  
		Last Modified: Wed, 02 Jul 2025 04:25:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb841bd213104808cad22caba8e076200444582c8b6766a14069e5b67f0b4076`  
		Last Modified: Wed, 02 Jul 2025 04:25:38 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2f3482e5edc25dea04e59f7d3f69c3a9bcb874ecd09ff7b76d09938b387316`  
		Last Modified: Wed, 02 Jul 2025 04:25:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95935b4f74e7325865844918ed4dc936bf6a7f5355be6a70c907e879756e3925`  
		Last Modified: Wed, 02 Jul 2025 04:25:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0b9b19efcc494b8caa9ccf52bcb03e0e7ddd213ac7ecf69b8dc03920083ee2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4584ac0e893b5bb6ab6ac40fb0055bcb4e2e8a460bed34d7f001302a4fba07a`

```dockerfile
```

-	Layers:
	-	`sha256:71826fd51a8a4a6f205b8879cda5575d12eb885004f2c0256e1e57fb103a96fa`  
		Last Modified: Wed, 02 Jul 2025 07:15:26 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af14adde1859cef369b47c64c3d6347187b3d11ea55a8b4e33b442e59dfdb33`  
		Last Modified: Wed, 02 Jul 2025 07:15:27 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250710`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:latest`

```console
$ docker pull odoo@sha256:3f8bd1cfae97c6770830da17abda966fada9a1515961fa4eb636cf26cd685302
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
$ docker pull odoo@sha256:5cc8c420e9991f7c73d9bf5585ecd0f62e503218cb262c69e411edadf8305b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 MB (671974527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07380c9347bee149d19a626cb826650f1a17eeb80db90cef4aca4f4ed296802`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e505ae1705c3fbee13d68d89efe5ee68807ece7ef97242d3404328e8884dca0f`  
		Last Modified: Wed, 02 Jul 2025 07:12:52 GMT  
		Size: 254.5 MB (254519039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff8f8953bb94fda9da4fca088bfc41b3542ccaed711e48b3a9b562b81aa0d6`  
		Last Modified: Wed, 02 Jul 2025 03:15:12 GMT  
		Size: 14.3 MB (14275544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da5abcd1121f4d67a267457dc8e7a3b189e8c8c8e8c10fa2d11c3046e2bf48a`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 479.9 KB (479899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ef76349e6b9fd321abefa3e3c6d2f84ed1431d452c7c5cce84be03993a4058`  
		Last Modified: Wed, 02 Jul 2025 07:13:01 GMT  
		Size: 373.0 MB (372979239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e08692a7bf8e0edd6fa87c2f4985212f63301754cfc27d4c811f46bc1ae73`  
		Last Modified: Wed, 02 Jul 2025 03:15:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb4c15c368458e13ff368a8b3276a6a672470265244f205291ec21378f29ab5`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3ab9a1ac400147c52aafaa76d3046cc7beb87c69f8b65016e10d8e765d4b0`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eba7df5719be0ea6a64a9c79e44f0ae91981da9a2e51d3e64dacf380513181`  
		Last Modified: Wed, 02 Jul 2025 03:15:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:70b38a057c072d703b555e152b3d568d146b6aa77f9d9a71aa2d31b2cd27e3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60220642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e9e005fdceebc7e588f488274b3a173fd8c41a252b321dec0e5441b3b3842e`

```dockerfile
```

-	Layers:
	-	`sha256:0b91bfb147f1b3a8adc474899669cc30cdfeaad610b4f7ae51efa870c5b65819`  
		Last Modified: Wed, 02 Jul 2025 07:12:40 GMT  
		Size: 60.2 MB (60193506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aecc6c8988aa06318aa1e71f96d764b708900ebadeba40d8e49c764a46bf3ba`  
		Last Modified: Wed, 02 Jul 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:dc9592a16a6deff3c97eeb0a751ed4311b4e14bb9806e59271c1f7577bcf7547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668351873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6b87f2b14619a1d5ad6a99383d339b592bf69fda4ad8b6c4e9e45991890f85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc1de84eced7ac5ac3be9fb82bf084138533f451c80fc50074430bd7eba7ff`  
		Last Modified: Wed, 02 Jul 2025 10:15:33 GMT  
		Size: 251.9 MB (251922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54c684cc197403c646d6fe146da92bf2a43322e200f6511a2449cf1c261f0e`  
		Last Modified: Wed, 02 Jul 2025 07:13:15 GMT  
		Size: 14.3 MB (14252759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ece915d45c456943d8e6a16ad51657b9008958c8e67faa8aa23329b15b9e0`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 479.8 KB (479839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599923d3890d070101f674768dba0cc96125480fed5ab7562d29344219d38e1`  
		Last Modified: Wed, 02 Jul 2025 10:15:27 GMT  
		Size: 372.8 MB (372838682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2b66a652d1e4b3b32a2782c472ca3d3a8324f5334c40d1ca81e55cb5bb0ae`  
		Last Modified: Wed, 02 Jul 2025 07:13:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67748aa358e9c43f418b2f15314343a44df1c0e20a4e41d4a242089c6a5e5bec`  
		Last Modified: Wed, 02 Jul 2025 07:13:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e034dc509b560817e2739b6ed8fb8375e53a3f4ba3d84d7744d162b120e12d04`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099c2535c2ad00a73d70e886bf22b98dfb5d698ed1c025341502c9f1d3456b64`  
		Last Modified: Wed, 02 Jul 2025 07:13:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:17412c8d264e2f1c08aa6f9a80a9f119c03bc1c864a6affc1a7e04991703898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60228093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b6750a308ff3684bc7b8499c20cb664877fe39024d2a13dda8fa6839c510d6`

```dockerfile
```

-	Layers:
	-	`sha256:2eb71e33ad446a2eaf333b07abc20a9f875054503b98715d6ffa6ab3645e586f`  
		Last Modified: Wed, 02 Jul 2025 10:13:44 GMT  
		Size: 60.2 MB (60200793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1063750fedcfd7195959c13131a685b2fa5708c594194bea23b4670a7ae6e089`  
		Last Modified: Wed, 02 Jul 2025 10:13:45 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:35bfdb6fbbc0706e955d08d757b6ca201a473aabf3c125487ddf12efc371c7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.2 MB (688187044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64176b42bf98d296525725398f7a92cef43ddd68da38d9880b95dfd50e97deb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 18 Jun 2025 14:35:54 GMT
ARG RELEASE
# Wed, 18 Jun 2025 14:35:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Jun 2025 14:35:54 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 18 Jun 2025 14:35:54 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 18 Jun 2025 14:35:54 GMT
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3184e637513d69556694435dc2fb3b3b37bf32ae06e0eab43d74580c85547`  
		Last Modified: Wed, 02 Jul 2025 18:22:58 GMT  
		Size: 265.1 MB (265077902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c3a6a2d0d072ebe783a7f85803c8853de229084f1c8d44195e53266668883`  
		Last Modified: Wed, 02 Jul 2025 05:13:35 GMT  
		Size: 14.8 MB (14798045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb1931a3349f14111e7890dff4722e4b8033a511e0f2c13fee1f6d50671541`  
		Last Modified: Wed, 02 Jul 2025 04:25:26 GMT  
		Size: 479.9 KB (479864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b630f000bb741c56ceee013f0fa5295950e00d7db4db9cd2a77358a52e363e`  
		Last Modified: Wed, 02 Jul 2025 18:22:43 GMT  
		Size: 373.5 MB (373507290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa97dbd706152799154425e73cc593cc350050e360e06c995f80621ecfdba07`  
		Last Modified: Wed, 02 Jul 2025 04:25:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb841bd213104808cad22caba8e076200444582c8b6766a14069e5b67f0b4076`  
		Last Modified: Wed, 02 Jul 2025 04:25:38 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2f3482e5edc25dea04e59f7d3f69c3a9bcb874ecd09ff7b76d09938b387316`  
		Last Modified: Wed, 02 Jul 2025 04:25:40 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95935b4f74e7325865844918ed4dc936bf6a7f5355be6a70c907e879756e3925`  
		Last Modified: Wed, 02 Jul 2025 04:25:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:0b9b19efcc494b8caa9ccf52bcb03e0e7ddd213ac7ecf69b8dc03920083ee2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60229093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4584ac0e893b5bb6ab6ac40fb0055bcb4e2e8a460bed34d7f001302a4fba07a`

```dockerfile
```

-	Layers:
	-	`sha256:71826fd51a8a4a6f205b8879cda5575d12eb885004f2c0256e1e57fb103a96fa`  
		Last Modified: Wed, 02 Jul 2025 07:15:26 GMT  
		Size: 60.2 MB (60201895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af14adde1859cef369b47c64c3d6347187b3d11ea55a8b4e33b442e59dfdb33`  
		Last Modified: Wed, 02 Jul 2025 07:15:27 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
