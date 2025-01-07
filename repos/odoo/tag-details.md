<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250106`](#odoo160-20250106)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250106`](#odoo170-20250106)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250106`](#odoo180-20250106)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:a2a1918c4ecd45b0228d100fcdc85e018f59646e0afd5467f3b59be028b6fb46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:17cf98e60380fafd354cfbbb3b343023a94cb16815f4c598d40a9991e426bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583871875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44caa5295f588f9102c06932c3fb2b9e886070cd492341597dc59d2001d8da59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5bec3479e173968b46757261ab8c520f2b8e93a5750ce42a6fbbdccb6c99ab`  
		Last Modified: Tue, 07 Jan 2025 02:31:32 GMT  
		Size: 219.6 MB (219629318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c74f28d1e171691743824cfa673b6919cb04667d0df9a077d62d026235e06`  
		Size: 2.6 MB (2575918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9352d5d7ec50156ee7d8feb6f33f61d6698bb0f27382a725557a3d4f542959d`  
		Last Modified: Tue, 07 Jan 2025 02:31:28 GMT  
		Size: 484.2 KB (484164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0cb79fadce27b7215008e5eafe7d6286fbec0e255bf1c921dc5b8ede1cf221`  
		Last Modified: Tue, 07 Jan 2025 02:31:33 GMT  
		Size: 330.9 MB (330927398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c49f3ceb9cff2ce5100ceb437239bb35f75c9b9fbc640923d27e07ed6ac9019`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633e1d0b5452b880749243e8be81fd3b402fe640e54e445f7c72f43f5db101a`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41a00b934e9a376600ec63e9f5148b5aac5032b7ed9df38e31ef842e148788`  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f642f31ba3f860cf737bc7d66c2af12baec4377c002744908efe9fcec9db6`  
		Last Modified: Tue, 07 Jan 2025 02:31:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:988d78574e5a90c6348e796c6dca527f8b98b8ad1172c5a0759aaa3f158a3264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38844193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c00cb05a9ea27a016c4470670d9bcfefb31f0d6325d6646142e6131880d1e8b`

```dockerfile
```

-	Layers:
	-	`sha256:267d3867ceeef4f86c4007c41a869a0fbc0ef6d7cd9103a3cdda0d55ae1d56b0`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 38.8 MB (38817477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a20e810718ddcd4f1b967f3c8af17a40320efddaf8ab68c6df0ada15635c34`  
		Size: 26.7 KB (26716 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:502354d424ea761b24040e8abf39c7f9fc55d02b1ef4a3d0b8326d9236df669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 MB (579320808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e790a626f4faff7db5de4e587962d2bde609c32eb4daeebf072cd91ce0b59dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4a31873b89a71b18b125e5c32d01fe2accbf9750e4bec3f2f78b0b985c27c`  
		Last Modified: Wed, 25 Dec 2024 02:32:24 GMT  
		Size: 216.9 MB (216922259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6a02c38ade9317909bb846aa32ef1fe4f2af806c739d9b93511a6181206058`  
		Last Modified: Wed, 25 Dec 2024 02:32:19 GMT  
		Size: 2.6 MB (2583734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b14da727db1359300dd09999c415ca2194cd27df9ccf8ff9b23f31c14fd61c`  
		Last Modified: Wed, 25 Dec 2024 02:32:19 GMT  
		Size: 484.1 KB (484122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb882572bf524442ebe160c1eecdfc45cd9f76c22c0ec3384238342b615a6a`  
		Last Modified: Tue, 07 Jan 2025 03:14:47 GMT  
		Size: 330.6 MB (330583412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c819c4c5b309d1ddc5ef0c4a3d2f418bbaaf94819d5f95ec29985e365cf0531`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbc75337729ddf604574163506f3a7f9913cd81a263d6dff668624adbeda9b`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a0b1c8a7b5abdeeddbe90bc57bb49693a88fa4aa273dbf98c7e754e04b50cb`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a06851f901deb70a2432ee6ba7c3f0da1f53c78e403a3d2f11a7950b6a4965`  
		Last Modified: Tue, 07 Jan 2025 03:14:41 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:52f00fa2cdbed1cb01cbd705db8acd93badf6100a850f628aefa1581ec6b0c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38850816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cdcb95e1669761d60b34135385b06d713ba18fb352d98636331cbcad32bc5e`

```dockerfile
```

-	Layers:
	-	`sha256:af2f353519a49ff7425898f5f4c997c4be903277e8aeb1fff4b778bf67c74c5a`  
		Last Modified: Tue, 07 Jan 2025 03:14:42 GMT  
		Size: 38.8 MB (38823947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52479dd15156c54d9c05a4e03a2602542c69115823fa8e0a1efac46cde97aaa6`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:a2a1918c4ecd45b0228d100fcdc85e018f59646e0afd5467f3b59be028b6fb46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:17cf98e60380fafd354cfbbb3b343023a94cb16815f4c598d40a9991e426bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583871875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44caa5295f588f9102c06932c3fb2b9e886070cd492341597dc59d2001d8da59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5bec3479e173968b46757261ab8c520f2b8e93a5750ce42a6fbbdccb6c99ab`  
		Last Modified: Tue, 07 Jan 2025 02:31:32 GMT  
		Size: 219.6 MB (219629318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c74f28d1e171691743824cfa673b6919cb04667d0df9a077d62d026235e06`  
		Size: 2.6 MB (2575918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9352d5d7ec50156ee7d8feb6f33f61d6698bb0f27382a725557a3d4f542959d`  
		Last Modified: Tue, 07 Jan 2025 02:31:28 GMT  
		Size: 484.2 KB (484164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0cb79fadce27b7215008e5eafe7d6286fbec0e255bf1c921dc5b8ede1cf221`  
		Last Modified: Tue, 07 Jan 2025 02:31:33 GMT  
		Size: 330.9 MB (330927398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c49f3ceb9cff2ce5100ceb437239bb35f75c9b9fbc640923d27e07ed6ac9019`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633e1d0b5452b880749243e8be81fd3b402fe640e54e445f7c72f43f5db101a`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41a00b934e9a376600ec63e9f5148b5aac5032b7ed9df38e31ef842e148788`  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f642f31ba3f860cf737bc7d66c2af12baec4377c002744908efe9fcec9db6`  
		Last Modified: Tue, 07 Jan 2025 02:31:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:988d78574e5a90c6348e796c6dca527f8b98b8ad1172c5a0759aaa3f158a3264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38844193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c00cb05a9ea27a016c4470670d9bcfefb31f0d6325d6646142e6131880d1e8b`

```dockerfile
```

-	Layers:
	-	`sha256:267d3867ceeef4f86c4007c41a869a0fbc0ef6d7cd9103a3cdda0d55ae1d56b0`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 38.8 MB (38817477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a20e810718ddcd4f1b967f3c8af17a40320efddaf8ab68c6df0ada15635c34`  
		Size: 26.7 KB (26716 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:502354d424ea761b24040e8abf39c7f9fc55d02b1ef4a3d0b8326d9236df669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 MB (579320808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e790a626f4faff7db5de4e587962d2bde609c32eb4daeebf072cd91ce0b59dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4a31873b89a71b18b125e5c32d01fe2accbf9750e4bec3f2f78b0b985c27c`  
		Last Modified: Wed, 25 Dec 2024 02:32:24 GMT  
		Size: 216.9 MB (216922259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6a02c38ade9317909bb846aa32ef1fe4f2af806c739d9b93511a6181206058`  
		Last Modified: Wed, 25 Dec 2024 02:32:19 GMT  
		Size: 2.6 MB (2583734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b14da727db1359300dd09999c415ca2194cd27df9ccf8ff9b23f31c14fd61c`  
		Last Modified: Wed, 25 Dec 2024 02:32:19 GMT  
		Size: 484.1 KB (484122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb882572bf524442ebe160c1eecdfc45cd9f76c22c0ec3384238342b615a6a`  
		Last Modified: Tue, 07 Jan 2025 03:14:47 GMT  
		Size: 330.6 MB (330583412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c819c4c5b309d1ddc5ef0c4a3d2f418bbaaf94819d5f95ec29985e365cf0531`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbc75337729ddf604574163506f3a7f9913cd81a263d6dff668624adbeda9b`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a0b1c8a7b5abdeeddbe90bc57bb49693a88fa4aa273dbf98c7e754e04b50cb`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a06851f901deb70a2432ee6ba7c3f0da1f53c78e403a3d2f11a7950b6a4965`  
		Last Modified: Tue, 07 Jan 2025 03:14:41 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:52f00fa2cdbed1cb01cbd705db8acd93badf6100a850f628aefa1581ec6b0c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38850816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cdcb95e1669761d60b34135385b06d713ba18fb352d98636331cbcad32bc5e`

```dockerfile
```

-	Layers:
	-	`sha256:af2f353519a49ff7425898f5f4c997c4be903277e8aeb1fff4b778bf67c74c5a`  
		Last Modified: Tue, 07 Jan 2025 03:14:42 GMT  
		Size: 38.8 MB (38823947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52479dd15156c54d9c05a4e03a2602542c69115823fa8e0a1efac46cde97aaa6`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250106`

```console
$ docker pull odoo@sha256:a2a1918c4ecd45b0228d100fcdc85e018f59646e0afd5467f3b59be028b6fb46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250106` - linux; amd64

```console
$ docker pull odoo@sha256:17cf98e60380fafd354cfbbb3b343023a94cb16815f4c598d40a9991e426bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583871875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44caa5295f588f9102c06932c3fb2b9e886070cd492341597dc59d2001d8da59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5bec3479e173968b46757261ab8c520f2b8e93a5750ce42a6fbbdccb6c99ab`  
		Last Modified: Tue, 07 Jan 2025 02:31:32 GMT  
		Size: 219.6 MB (219629318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c74f28d1e171691743824cfa673b6919cb04667d0df9a077d62d026235e06`  
		Size: 2.6 MB (2575918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9352d5d7ec50156ee7d8feb6f33f61d6698bb0f27382a725557a3d4f542959d`  
		Last Modified: Tue, 07 Jan 2025 02:31:28 GMT  
		Size: 484.2 KB (484164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0cb79fadce27b7215008e5eafe7d6286fbec0e255bf1c921dc5b8ede1cf221`  
		Last Modified: Tue, 07 Jan 2025 02:31:33 GMT  
		Size: 330.9 MB (330927398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c49f3ceb9cff2ce5100ceb437239bb35f75c9b9fbc640923d27e07ed6ac9019`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c633e1d0b5452b880749243e8be81fd3b402fe640e54e445f7c72f43f5db101a`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41a00b934e9a376600ec63e9f5148b5aac5032b7ed9df38e31ef842e148788`  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39f642f31ba3f860cf737bc7d66c2af12baec4377c002744908efe9fcec9db6`  
		Last Modified: Tue, 07 Jan 2025 02:31:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:988d78574e5a90c6348e796c6dca527f8b98b8ad1172c5a0759aaa3f158a3264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38844193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c00cb05a9ea27a016c4470670d9bcfefb31f0d6325d6646142e6131880d1e8b`

```dockerfile
```

-	Layers:
	-	`sha256:267d3867ceeef4f86c4007c41a869a0fbc0ef6d7cd9103a3cdda0d55ae1d56b0`  
		Last Modified: Tue, 07 Jan 2025 02:31:29 GMT  
		Size: 38.8 MB (38817477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a20e810718ddcd4f1b967f3c8af17a40320efddaf8ab68c6df0ada15635c34`  
		Size: 26.7 KB (26716 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250106` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:502354d424ea761b24040e8abf39c7f9fc55d02b1ef4a3d0b8326d9236df669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 MB (579320808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e790a626f4faff7db5de4e587962d2bde609c32eb4daeebf072cd91ce0b59dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=C.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=333d25fa5ce0e5c43149800d50a7870f3b2c90ec
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4a31873b89a71b18b125e5c32d01fe2accbf9750e4bec3f2f78b0b985c27c`  
		Last Modified: Wed, 25 Dec 2024 02:32:24 GMT  
		Size: 216.9 MB (216922259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6a02c38ade9317909bb846aa32ef1fe4f2af806c739d9b93511a6181206058`  
		Last Modified: Wed, 25 Dec 2024 02:32:19 GMT  
		Size: 2.6 MB (2583734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b14da727db1359300dd09999c415ca2194cd27df9ccf8ff9b23f31c14fd61c`  
		Last Modified: Wed, 25 Dec 2024 02:32:19 GMT  
		Size: 484.1 KB (484122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb882572bf524442ebe160c1eecdfc45cd9f76c22c0ec3384238342b615a6a`  
		Last Modified: Tue, 07 Jan 2025 03:14:47 GMT  
		Size: 330.6 MB (330583412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c819c4c5b309d1ddc5ef0c4a3d2f418bbaaf94819d5f95ec29985e365cf0531`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbc75337729ddf604574163506f3a7f9913cd81a263d6dff668624adbeda9b`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a0b1c8a7b5abdeeddbe90bc57bb49693a88fa4aa273dbf98c7e754e04b50cb`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a06851f901deb70a2432ee6ba7c3f0da1f53c78e403a3d2f11a7950b6a4965`  
		Last Modified: Tue, 07 Jan 2025 03:14:41 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:52f00fa2cdbed1cb01cbd705db8acd93badf6100a850f628aefa1581ec6b0c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38850816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cdcb95e1669761d60b34135385b06d713ba18fb352d98636331cbcad32bc5e`

```dockerfile
```

-	Layers:
	-	`sha256:af2f353519a49ff7425898f5f4c997c4be903277e8aeb1fff4b778bf67c74c5a`  
		Last Modified: Tue, 07 Jan 2025 03:14:42 GMT  
		Size: 38.8 MB (38823947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52479dd15156c54d9c05a4e03a2602542c69115823fa8e0a1efac46cde97aaa6`  
		Last Modified: Tue, 07 Jan 2025 03:14:40 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:63bc0927cefaba46d0b225850cea8cc4d15d5220ead743538b1adf1f82b76b5b
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
$ docker pull odoo@sha256:4322dc0dd371c438e1d469a8d27c110bfd4ea19661d4149867ecc6d24d45db0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 MB (599228889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c9cdb5859493e4c1221e02797ae8b19fb4550f69bb46aea40e5d17c4f186be`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd20077cf98b423e48fba4bd69702c598d11ef14265b5cc652773ce2e6abd49`  
		Last Modified: Tue, 07 Jan 2025 02:31:41 GMT  
		Size: 233.8 MB (233784220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b809babc59c9a4ada4713f6bc6a19b64f6278e7badaf673292e07a602797e6`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 2.5 MB (2493393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c3db1c096e40a7d02212292663b5f00c926cd5e9b70961359ddd65a14add48`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 485.1 KB (485137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58447963dc7adc343c38da5e3220eeccc9fca48452cb40ac994c2b66b65318b3`  
		Size: 332.9 MB (332928010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d85a753f3cdfb8b2abdfea200b5450a23116e129673ced8e0834c378fada513`  
		Last Modified: Tue, 07 Jan 2025 02:31:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ae3d1cb6ff5771580aa0778c4674ad29fbd8fa00ea01bf85386f1d91f0f331`  
		Last Modified: Tue, 07 Jan 2025 02:31:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c767fa3292cc6d539948e442f215d715020c3c3e34bd8ceb50a9c19fbeb530`  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19cbf41e877e4fe5ebdda3da8c412c80a50dcad8e71edb5256cbf50861dcf7`  
		Last Modified: Tue, 07 Jan 2025 02:31:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:efec5c044840319e37895d5b230b60ae9fa5f37b82a283f4d71267594df7b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39669534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f37cc6a8f8e97b8be578b8df279e90e217870ebf19478e37c716c5e0994e2d`

```dockerfile
```

-	Layers:
	-	`sha256:0a09b6cad67e9d6d8378d4e49652607550adb097f7cdb8848d6b108a3e17697e`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 39.6 MB (39642700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1962c219512c402f66c11f47ebfb2413f72b03c109f794941c7ba7bd1cb7e049`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c11df7717a92727bd6ad0429bd132ab63fd879b09a2d6cc3f27bbe8315ea478c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594018811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fd0a1865c64d6b7f40bca08064d639b8844ba6a980a1b15000cff47e1616b4`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:f31bfbbb9550325e01db1542742d31e087257be6b8415e0514902fc390e55f31`  
		Last Modified: Tue, 07 Jan 2025 03:11:54 GMT  
		Size: 332.5 MB (332541651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7ecb77b07a520a09ef5f1d144be66971714a16e57308c7b66827b6f09f2fed`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067af3dd2929e9a6ce31563e21a7d5a258ba7c0e0ba19f2bd13fdbd23d81a966`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f685f224fb14e06ea475054fdb44e229e2b770626f3a524bd886401576fb87b`  
		Last Modified: Tue, 07 Jan 2025 03:11:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf0d0ed79ff3586e77975402fa6186807ec33e523af9e6ca55d997fab414942`  
		Last Modified: Tue, 07 Jan 2025 03:11:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f850bbd7daea4bf8ae81fdaa42e8ca9fe5bef36de1605044a6edd1b6ef3f0cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39676198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6c0f452571dff45e760c8faac27218f136b0c614461e59bd3d822ea7fd5c3f`

```dockerfile
```

-	Layers:
	-	`sha256:ea8fbbf1f740a02130dab9aa85010a55ba4163506e5f71632ecbb42cf308e284`  
		Last Modified: Tue, 07 Jan 2025 03:11:49 GMT  
		Size: 39.6 MB (39649211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214274062702083af849d457f9736774c09fb70f7787858b3c76933f45c3c7e8`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:93b003eaf779129a55bb8c38bb67c308906b250898378e09ef7bf4192d0de66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.7 MB (615689612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ee8c543cb29429f0dc6f1a8f6d0ca855355a626ca5a3deaf4d6e7229c36fea`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:cc1d82811df3ab5dd49ecdd58c28075c2bf3f8528814441a800e7d1111cc9b70`  
		Last Modified: Tue, 07 Jan 2025 02:47:37 GMT  
		Size: 334.7 MB (334653433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f46a8897ea171cb508ba9af13f07f1c319a66289f624d1af98474a9787f84d3`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e789af1a3aff8da608c0ff13cf80e0d7c23d8550e90251f7bf6d48b6a9d5bab`  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a0ed4fceabfa98681aab7a4fabe05e74c0f8be0d852dcd431b1522f9b3ae8`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525c5ea95eda1c157ddfe21166d65748da3e3a6dc01e8ce985761d204fb234ad`  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:7daf4f34a3d607d06501114141e149e30423a2baffb15ffa537c42e85a3eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39677918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c10c4219d40730e4ec9204ef75f099c1a52e2fce91e315e26731fddf99962e`

```dockerfile
```

-	Layers:
	-	`sha256:2aa4c9d22a3ebe1aa495ed082f440083b47f6fd53ee365b10440d7097286b9db`  
		Last Modified: Tue, 07 Jan 2025 02:47:18 GMT  
		Size: 39.7 MB (39651027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab78e5c5fccdf702262e511233c60480f4f99e44310c18114d19fcc57947d4d`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:63bc0927cefaba46d0b225850cea8cc4d15d5220ead743538b1adf1f82b76b5b
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
$ docker pull odoo@sha256:4322dc0dd371c438e1d469a8d27c110bfd4ea19661d4149867ecc6d24d45db0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 MB (599228889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c9cdb5859493e4c1221e02797ae8b19fb4550f69bb46aea40e5d17c4f186be`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd20077cf98b423e48fba4bd69702c598d11ef14265b5cc652773ce2e6abd49`  
		Last Modified: Tue, 07 Jan 2025 02:31:41 GMT  
		Size: 233.8 MB (233784220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b809babc59c9a4ada4713f6bc6a19b64f6278e7badaf673292e07a602797e6`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 2.5 MB (2493393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c3db1c096e40a7d02212292663b5f00c926cd5e9b70961359ddd65a14add48`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 485.1 KB (485137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58447963dc7adc343c38da5e3220eeccc9fca48452cb40ac994c2b66b65318b3`  
		Size: 332.9 MB (332928010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d85a753f3cdfb8b2abdfea200b5450a23116e129673ced8e0834c378fada513`  
		Last Modified: Tue, 07 Jan 2025 02:31:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ae3d1cb6ff5771580aa0778c4674ad29fbd8fa00ea01bf85386f1d91f0f331`  
		Last Modified: Tue, 07 Jan 2025 02:31:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c767fa3292cc6d539948e442f215d715020c3c3e34bd8ceb50a9c19fbeb530`  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19cbf41e877e4fe5ebdda3da8c412c80a50dcad8e71edb5256cbf50861dcf7`  
		Last Modified: Tue, 07 Jan 2025 02:31:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:efec5c044840319e37895d5b230b60ae9fa5f37b82a283f4d71267594df7b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39669534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f37cc6a8f8e97b8be578b8df279e90e217870ebf19478e37c716c5e0994e2d`

```dockerfile
```

-	Layers:
	-	`sha256:0a09b6cad67e9d6d8378d4e49652607550adb097f7cdb8848d6b108a3e17697e`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 39.6 MB (39642700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1962c219512c402f66c11f47ebfb2413f72b03c109f794941c7ba7bd1cb7e049`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c11df7717a92727bd6ad0429bd132ab63fd879b09a2d6cc3f27bbe8315ea478c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594018811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fd0a1865c64d6b7f40bca08064d639b8844ba6a980a1b15000cff47e1616b4`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:f31bfbbb9550325e01db1542742d31e087257be6b8415e0514902fc390e55f31`  
		Last Modified: Tue, 07 Jan 2025 03:11:54 GMT  
		Size: 332.5 MB (332541651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7ecb77b07a520a09ef5f1d144be66971714a16e57308c7b66827b6f09f2fed`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067af3dd2929e9a6ce31563e21a7d5a258ba7c0e0ba19f2bd13fdbd23d81a966`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f685f224fb14e06ea475054fdb44e229e2b770626f3a524bd886401576fb87b`  
		Last Modified: Tue, 07 Jan 2025 03:11:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf0d0ed79ff3586e77975402fa6186807ec33e523af9e6ca55d997fab414942`  
		Last Modified: Tue, 07 Jan 2025 03:11:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f850bbd7daea4bf8ae81fdaa42e8ca9fe5bef36de1605044a6edd1b6ef3f0cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39676198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6c0f452571dff45e760c8faac27218f136b0c614461e59bd3d822ea7fd5c3f`

```dockerfile
```

-	Layers:
	-	`sha256:ea8fbbf1f740a02130dab9aa85010a55ba4163506e5f71632ecbb42cf308e284`  
		Last Modified: Tue, 07 Jan 2025 03:11:49 GMT  
		Size: 39.6 MB (39649211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214274062702083af849d457f9736774c09fb70f7787858b3c76933f45c3c7e8`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:93b003eaf779129a55bb8c38bb67c308906b250898378e09ef7bf4192d0de66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.7 MB (615689612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ee8c543cb29429f0dc6f1a8f6d0ca855355a626ca5a3deaf4d6e7229c36fea`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:cc1d82811df3ab5dd49ecdd58c28075c2bf3f8528814441a800e7d1111cc9b70`  
		Last Modified: Tue, 07 Jan 2025 02:47:37 GMT  
		Size: 334.7 MB (334653433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f46a8897ea171cb508ba9af13f07f1c319a66289f624d1af98474a9787f84d3`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e789af1a3aff8da608c0ff13cf80e0d7c23d8550e90251f7bf6d48b6a9d5bab`  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a0ed4fceabfa98681aab7a4fabe05e74c0f8be0d852dcd431b1522f9b3ae8`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525c5ea95eda1c157ddfe21166d65748da3e3a6dc01e8ce985761d204fb234ad`  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7daf4f34a3d607d06501114141e149e30423a2baffb15ffa537c42e85a3eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39677918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c10c4219d40730e4ec9204ef75f099c1a52e2fce91e315e26731fddf99962e`

```dockerfile
```

-	Layers:
	-	`sha256:2aa4c9d22a3ebe1aa495ed082f440083b47f6fd53ee365b10440d7097286b9db`  
		Last Modified: Tue, 07 Jan 2025 02:47:18 GMT  
		Size: 39.7 MB (39651027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab78e5c5fccdf702262e511233c60480f4f99e44310c18114d19fcc57947d4d`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250106`

```console
$ docker pull odoo@sha256:63bc0927cefaba46d0b225850cea8cc4d15d5220ead743538b1adf1f82b76b5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250106` - linux; amd64

```console
$ docker pull odoo@sha256:4322dc0dd371c438e1d469a8d27c110bfd4ea19661d4149867ecc6d24d45db0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 MB (599228889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c9cdb5859493e4c1221e02797ae8b19fb4550f69bb46aea40e5d17c4f186be`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd20077cf98b423e48fba4bd69702c598d11ef14265b5cc652773ce2e6abd49`  
		Last Modified: Tue, 07 Jan 2025 02:31:41 GMT  
		Size: 233.8 MB (233784220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b809babc59c9a4ada4713f6bc6a19b64f6278e7badaf673292e07a602797e6`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 2.5 MB (2493393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c3db1c096e40a7d02212292663b5f00c926cd5e9b70961359ddd65a14add48`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 485.1 KB (485137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58447963dc7adc343c38da5e3220eeccc9fca48452cb40ac994c2b66b65318b3`  
		Size: 332.9 MB (332928010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d85a753f3cdfb8b2abdfea200b5450a23116e129673ced8e0834c378fada513`  
		Last Modified: Tue, 07 Jan 2025 02:31:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ae3d1cb6ff5771580aa0778c4674ad29fbd8fa00ea01bf85386f1d91f0f331`  
		Last Modified: Tue, 07 Jan 2025 02:31:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c767fa3292cc6d539948e442f215d715020c3c3e34bd8ceb50a9c19fbeb530`  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19cbf41e877e4fe5ebdda3da8c412c80a50dcad8e71edb5256cbf50861dcf7`  
		Last Modified: Tue, 07 Jan 2025 02:31:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:efec5c044840319e37895d5b230b60ae9fa5f37b82a283f4d71267594df7b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39669534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f37cc6a8f8e97b8be578b8df279e90e217870ebf19478e37c716c5e0994e2d`

```dockerfile
```

-	Layers:
	-	`sha256:0a09b6cad67e9d6d8378d4e49652607550adb097f7cdb8848d6b108a3e17697e`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 39.6 MB (39642700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1962c219512c402f66c11f47ebfb2413f72b03c109f794941c7ba7bd1cb7e049`  
		Last Modified: Tue, 07 Jan 2025 02:31:37 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250106` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c11df7717a92727bd6ad0429bd132ab63fd879b09a2d6cc3f27bbe8315ea478c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594018811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fd0a1865c64d6b7f40bca08064d639b8844ba6a980a1b15000cff47e1616b4`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:f31bfbbb9550325e01db1542742d31e087257be6b8415e0514902fc390e55f31`  
		Last Modified: Tue, 07 Jan 2025 03:11:54 GMT  
		Size: 332.5 MB (332541651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7ecb77b07a520a09ef5f1d144be66971714a16e57308c7b66827b6f09f2fed`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067af3dd2929e9a6ce31563e21a7d5a258ba7c0e0ba19f2bd13fdbd23d81a966`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f685f224fb14e06ea475054fdb44e229e2b770626f3a524bd886401576fb87b`  
		Last Modified: Tue, 07 Jan 2025 03:11:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf0d0ed79ff3586e77975402fa6186807ec33e523af9e6ca55d997fab414942`  
		Last Modified: Tue, 07 Jan 2025 03:11:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:f850bbd7daea4bf8ae81fdaa42e8ca9fe5bef36de1605044a6edd1b6ef3f0cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39676198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6c0f452571dff45e760c8faac27218f136b0c614461e59bd3d822ea7fd5c3f`

```dockerfile
```

-	Layers:
	-	`sha256:ea8fbbf1f740a02130dab9aa85010a55ba4163506e5f71632ecbb42cf308e284`  
		Last Modified: Tue, 07 Jan 2025 03:11:49 GMT  
		Size: 39.6 MB (39649211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214274062702083af849d457f9736774c09fb70f7787858b3c76933f45c3c7e8`  
		Last Modified: Tue, 07 Jan 2025 03:11:47 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250106` - linux; ppc64le

```console
$ docker pull odoo@sha256:93b003eaf779129a55bb8c38bb67c308906b250898378e09ef7bf4192d0de66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.7 MB (615689612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ee8c543cb29429f0dc6f1a8f6d0ca855355a626ca5a3deaf4d6e7229c36fea`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=17.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=992ed03cd110444dadd906fff010e3becd275148
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:cc1d82811df3ab5dd49ecdd58c28075c2bf3f8528814441a800e7d1111cc9b70`  
		Last Modified: Tue, 07 Jan 2025 02:47:37 GMT  
		Size: 334.7 MB (334653433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f46a8897ea171cb508ba9af13f07f1c319a66289f624d1af98474a9787f84d3`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e789af1a3aff8da608c0ff13cf80e0d7c23d8550e90251f7bf6d48b6a9d5bab`  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a0ed4fceabfa98681aab7a4fabe05e74c0f8be0d852dcd431b1522f9b3ae8`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525c5ea95eda1c157ddfe21166d65748da3e3a6dc01e8ce985761d204fb234ad`  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:7daf4f34a3d607d06501114141e149e30423a2baffb15ffa537c42e85a3eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39677918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c10c4219d40730e4ec9204ef75f099c1a52e2fce91e315e26731fddf99962e`

```dockerfile
```

-	Layers:
	-	`sha256:2aa4c9d22a3ebe1aa495ed082f440083b47f6fd53ee365b10440d7097286b9db`  
		Last Modified: Tue, 07 Jan 2025 02:47:18 GMT  
		Size: 39.7 MB (39651027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab78e5c5fccdf702262e511233c60480f4f99e44310c18114d19fcc57947d4d`  
		Last Modified: Tue, 07 Jan 2025 02:47:16 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:543477de90679293a85df149702b36f495669635efe12d1720ae1bc13f686e2c
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
$ docker pull odoo@sha256:a498cae86713a72149e35a1c11d1cf87dbeb62430af14567cf1407d3db8a7784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.4 MB (665427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b6544e1db91a142d2c520f79b9a47616b5943d650980964dde2089d622105`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45887c5bf36402135d3e8159888d8ff9b09ab897d3a90f477e330ef32b7ae686`  
		Last Modified: Tue, 07 Jan 2025 02:32:21 GMT  
		Size: 254.5 MB (254516340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59a74fe4514c470984758b86d9f4346217337f639f879106cba18ff0d0434d`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 14.2 MB (14230118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779ba51ba9acb9f403e7edde3fcdba2d6e41c4f57234338771b72c88737fa16`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485b916b73cef04bcacbf17ab015401c49254ad71a4c042aed754b899d438337`  
		Last Modified: Tue, 07 Jan 2025 02:32:22 GMT  
		Size: 366.4 MB (366442093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c3af110c11e78703a052f7868f1e44d199a26581b7932b0cade9fad97f3880`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ebf5753311702190b3351f562a8b8dfb1fc0f21c70c26b07cd8085ffec6143`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d84072118698624ab758a78d90820d1a3fd02c4c5ecc77edb3e7610f390e5`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd84a8f05c331526c12eaf53c1e4af3c2e4ca5807bf362a7392f552177642d`  
		Last Modified: Tue, 07 Jan 2025 02:32:19 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:64d1c65e58cad0864196065e5b240fa319fb5a3679db41b8293fda4d76f18db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58364432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aecabbe8d04e417c58799658bc5a16954242bd67ba3c43941587f276756a38`

```dockerfile
```

-	Layers:
	-	`sha256:eff02ed18115b0801edae6c8f6973fc48e581a85389736e9b75b255684a7e2d0`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 58.3 MB (58337296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc62a67d30aa95c392dcc712100c54b7a5f722c7da486ee96e0b89444130346`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b580ded05326157c2298f89b77037f123d36032f286c660a944e6e3f51f81c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661820054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99376e4e9b2067b5a1db4a820e2bba6526b5e815299c842fff0f9a43373a5f07`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:9bfdab3d8df1faefb7de77c3510c909b0d99bcc1178d007b57aa9fa14fb7708e`  
		Last Modified: Tue, 07 Jan 2025 03:08:06 GMT  
		Size: 366.3 MB (366293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2acfe7737e2bc45549f931b08c66b4a369dc9bb65f6cbe0cd87429c3dd953d`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26168a6ee953389d3643543cdcf15bb5a1528243bf1c24211be96e4cabd0b73`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10bb73bc2141fdbe9fff870d974984a6d7957459ca3c281a740af23d7e61b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07ee242d4ef58b8ea6cc8982985575954ca6467b7fb00a01b48aae31aeb054`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:660d0fa1249a6d89acd57d3a74a4e400a769e52a38da6f93f7782f5d1d518be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c050e05a959ebbc656f5ec34b21cb22cef19c4570a37f688ebd0062ed178002`

```dockerfile
```

-	Layers:
	-	`sha256:1e581cee7af1c587bef0d3f8380b79a872b62ab3270490c2295cf05758f760e8`  
		Last Modified: Tue, 07 Jan 2025 03:08:00 GMT  
		Size: 58.3 MB (58344587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a028aad2cee0766059b838aa806f374cc72ae58d95ad5bb62c39fc2dc7034b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:b697b0ddf3ad2d4af5898bdc66da21586229734cb6c13e853887b80fa6f53d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681736287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83741869a79d9a0715568c8ae3ccecd75b5acc24b807a1b78a78f07ca2589251`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396dc4cb926aa2a8ffba5bbc0efd80eb54163b1ab9ce89ceda59c1a92b994590`  
		Last Modified: Tue, 07 Jan 2025 02:41:14 GMT  
		Size: 367.0 MB (366994400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c2c0160ebfb3debc4fcdd3f9a207bdb108367f7c369b0b38d72de794b773ef`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e4a21b179f843fa4d6aeaf5fdc92317d8184aa3111ee93cd33a675a3dbc9b`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798846e905b54fa491b50be015bf621884d34e4d62319a80cb5253e583e418ac`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6925157dec2af072810af50593a5b824f8865e952c4f77c1a0ee5af7069a8cd`  
		Last Modified: Tue, 07 Jan 2025 02:41:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:f68f3f61505e82340d0c463c04d18ba420cbd560551f5a6a504769699cc3d367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58372657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d42833478f3b62b0785d4227c4d0f177fe9a4b41944a23f9f65ca4adfae0b`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b48bd1b3ac530a7b3347d18c723b6ce76cbf64171c402de6ed292ea031d10`  
		Last Modified: Tue, 07 Jan 2025 02:41:07 GMT  
		Size: 58.3 MB (58345459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb70fd5251e0f584e7d9cd98c270a9e70778d88f3d38285ed979f1f089075a79`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:543477de90679293a85df149702b36f495669635efe12d1720ae1bc13f686e2c
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
$ docker pull odoo@sha256:a498cae86713a72149e35a1c11d1cf87dbeb62430af14567cf1407d3db8a7784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.4 MB (665427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b6544e1db91a142d2c520f79b9a47616b5943d650980964dde2089d622105`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45887c5bf36402135d3e8159888d8ff9b09ab897d3a90f477e330ef32b7ae686`  
		Last Modified: Tue, 07 Jan 2025 02:32:21 GMT  
		Size: 254.5 MB (254516340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59a74fe4514c470984758b86d9f4346217337f639f879106cba18ff0d0434d`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 14.2 MB (14230118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779ba51ba9acb9f403e7edde3fcdba2d6e41c4f57234338771b72c88737fa16`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485b916b73cef04bcacbf17ab015401c49254ad71a4c042aed754b899d438337`  
		Last Modified: Tue, 07 Jan 2025 02:32:22 GMT  
		Size: 366.4 MB (366442093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c3af110c11e78703a052f7868f1e44d199a26581b7932b0cade9fad97f3880`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ebf5753311702190b3351f562a8b8dfb1fc0f21c70c26b07cd8085ffec6143`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d84072118698624ab758a78d90820d1a3fd02c4c5ecc77edb3e7610f390e5`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd84a8f05c331526c12eaf53c1e4af3c2e4ca5807bf362a7392f552177642d`  
		Last Modified: Tue, 07 Jan 2025 02:32:19 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:64d1c65e58cad0864196065e5b240fa319fb5a3679db41b8293fda4d76f18db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58364432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aecabbe8d04e417c58799658bc5a16954242bd67ba3c43941587f276756a38`

```dockerfile
```

-	Layers:
	-	`sha256:eff02ed18115b0801edae6c8f6973fc48e581a85389736e9b75b255684a7e2d0`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 58.3 MB (58337296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc62a67d30aa95c392dcc712100c54b7a5f722c7da486ee96e0b89444130346`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b580ded05326157c2298f89b77037f123d36032f286c660a944e6e3f51f81c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661820054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99376e4e9b2067b5a1db4a820e2bba6526b5e815299c842fff0f9a43373a5f07`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:9bfdab3d8df1faefb7de77c3510c909b0d99bcc1178d007b57aa9fa14fb7708e`  
		Last Modified: Tue, 07 Jan 2025 03:08:06 GMT  
		Size: 366.3 MB (366293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2acfe7737e2bc45549f931b08c66b4a369dc9bb65f6cbe0cd87429c3dd953d`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26168a6ee953389d3643543cdcf15bb5a1528243bf1c24211be96e4cabd0b73`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10bb73bc2141fdbe9fff870d974984a6d7957459ca3c281a740af23d7e61b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07ee242d4ef58b8ea6cc8982985575954ca6467b7fb00a01b48aae31aeb054`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:660d0fa1249a6d89acd57d3a74a4e400a769e52a38da6f93f7782f5d1d518be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c050e05a959ebbc656f5ec34b21cb22cef19c4570a37f688ebd0062ed178002`

```dockerfile
```

-	Layers:
	-	`sha256:1e581cee7af1c587bef0d3f8380b79a872b62ab3270490c2295cf05758f760e8`  
		Last Modified: Tue, 07 Jan 2025 03:08:00 GMT  
		Size: 58.3 MB (58344587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a028aad2cee0766059b838aa806f374cc72ae58d95ad5bb62c39fc2dc7034b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b697b0ddf3ad2d4af5898bdc66da21586229734cb6c13e853887b80fa6f53d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681736287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83741869a79d9a0715568c8ae3ccecd75b5acc24b807a1b78a78f07ca2589251`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396dc4cb926aa2a8ffba5bbc0efd80eb54163b1ab9ce89ceda59c1a92b994590`  
		Last Modified: Tue, 07 Jan 2025 02:41:14 GMT  
		Size: 367.0 MB (366994400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c2c0160ebfb3debc4fcdd3f9a207bdb108367f7c369b0b38d72de794b773ef`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e4a21b179f843fa4d6aeaf5fdc92317d8184aa3111ee93cd33a675a3dbc9b`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798846e905b54fa491b50be015bf621884d34e4d62319a80cb5253e583e418ac`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6925157dec2af072810af50593a5b824f8865e952c4f77c1a0ee5af7069a8cd`  
		Last Modified: Tue, 07 Jan 2025 02:41:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f68f3f61505e82340d0c463c04d18ba420cbd560551f5a6a504769699cc3d367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58372657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d42833478f3b62b0785d4227c4d0f177fe9a4b41944a23f9f65ca4adfae0b`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b48bd1b3ac530a7b3347d18c723b6ce76cbf64171c402de6ed292ea031d10`  
		Last Modified: Tue, 07 Jan 2025 02:41:07 GMT  
		Size: 58.3 MB (58345459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb70fd5251e0f584e7d9cd98c270a9e70778d88f3d38285ed979f1f089075a79`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250106`

```console
$ docker pull odoo@sha256:543477de90679293a85df149702b36f495669635efe12d1720ae1bc13f686e2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250106` - linux; amd64

```console
$ docker pull odoo@sha256:a498cae86713a72149e35a1c11d1cf87dbeb62430af14567cf1407d3db8a7784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.4 MB (665427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b6544e1db91a142d2c520f79b9a47616b5943d650980964dde2089d622105`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45887c5bf36402135d3e8159888d8ff9b09ab897d3a90f477e330ef32b7ae686`  
		Last Modified: Tue, 07 Jan 2025 02:32:21 GMT  
		Size: 254.5 MB (254516340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59a74fe4514c470984758b86d9f4346217337f639f879106cba18ff0d0434d`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 14.2 MB (14230118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779ba51ba9acb9f403e7edde3fcdba2d6e41c4f57234338771b72c88737fa16`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485b916b73cef04bcacbf17ab015401c49254ad71a4c042aed754b899d438337`  
		Last Modified: Tue, 07 Jan 2025 02:32:22 GMT  
		Size: 366.4 MB (366442093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c3af110c11e78703a052f7868f1e44d199a26581b7932b0cade9fad97f3880`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ebf5753311702190b3351f562a8b8dfb1fc0f21c70c26b07cd8085ffec6143`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d84072118698624ab758a78d90820d1a3fd02c4c5ecc77edb3e7610f390e5`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd84a8f05c331526c12eaf53c1e4af3c2e4ca5807bf362a7392f552177642d`  
		Last Modified: Tue, 07 Jan 2025 02:32:19 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:64d1c65e58cad0864196065e5b240fa319fb5a3679db41b8293fda4d76f18db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58364432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aecabbe8d04e417c58799658bc5a16954242bd67ba3c43941587f276756a38`

```dockerfile
```

-	Layers:
	-	`sha256:eff02ed18115b0801edae6c8f6973fc48e581a85389736e9b75b255684a7e2d0`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 58.3 MB (58337296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc62a67d30aa95c392dcc712100c54b7a5f722c7da486ee96e0b89444130346`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250106` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b580ded05326157c2298f89b77037f123d36032f286c660a944e6e3f51f81c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661820054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99376e4e9b2067b5a1db4a820e2bba6526b5e815299c842fff0f9a43373a5f07`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:9bfdab3d8df1faefb7de77c3510c909b0d99bcc1178d007b57aa9fa14fb7708e`  
		Last Modified: Tue, 07 Jan 2025 03:08:06 GMT  
		Size: 366.3 MB (366293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2acfe7737e2bc45549f931b08c66b4a369dc9bb65f6cbe0cd87429c3dd953d`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26168a6ee953389d3643543cdcf15bb5a1528243bf1c24211be96e4cabd0b73`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10bb73bc2141fdbe9fff870d974984a6d7957459ca3c281a740af23d7e61b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07ee242d4ef58b8ea6cc8982985575954ca6467b7fb00a01b48aae31aeb054`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:660d0fa1249a6d89acd57d3a74a4e400a769e52a38da6f93f7782f5d1d518be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c050e05a959ebbc656f5ec34b21cb22cef19c4570a37f688ebd0062ed178002`

```dockerfile
```

-	Layers:
	-	`sha256:1e581cee7af1c587bef0d3f8380b79a872b62ab3270490c2295cf05758f760e8`  
		Last Modified: Tue, 07 Jan 2025 03:08:00 GMT  
		Size: 58.3 MB (58344587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a028aad2cee0766059b838aa806f374cc72ae58d95ad5bb62c39fc2dc7034b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250106` - linux; ppc64le

```console
$ docker pull odoo@sha256:b697b0ddf3ad2d4af5898bdc66da21586229734cb6c13e853887b80fa6f53d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681736287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83741869a79d9a0715568c8ae3ccecd75b5acc24b807a1b78a78f07ca2589251`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396dc4cb926aa2a8ffba5bbc0efd80eb54163b1ab9ce89ceda59c1a92b994590`  
		Last Modified: Tue, 07 Jan 2025 02:41:14 GMT  
		Size: 367.0 MB (366994400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c2c0160ebfb3debc4fcdd3f9a207bdb108367f7c369b0b38d72de794b773ef`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e4a21b179f843fa4d6aeaf5fdc92317d8184aa3111ee93cd33a675a3dbc9b`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798846e905b54fa491b50be015bf621884d34e4d62319a80cb5253e583e418ac`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6925157dec2af072810af50593a5b824f8865e952c4f77c1a0ee5af7069a8cd`  
		Last Modified: Tue, 07 Jan 2025 02:41:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250106` - unknown; unknown

```console
$ docker pull odoo@sha256:f68f3f61505e82340d0c463c04d18ba420cbd560551f5a6a504769699cc3d367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58372657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d42833478f3b62b0785d4227c4d0f177fe9a4b41944a23f9f65ca4adfae0b`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b48bd1b3ac530a7b3347d18c723b6ce76cbf64171c402de6ed292ea031d10`  
		Last Modified: Tue, 07 Jan 2025 02:41:07 GMT  
		Size: 58.3 MB (58345459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb70fd5251e0f584e7d9cd98c270a9e70778d88f3d38285ed979f1f089075a79`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:543477de90679293a85df149702b36f495669635efe12d1720ae1bc13f686e2c
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
$ docker pull odoo@sha256:a498cae86713a72149e35a1c11d1cf87dbeb62430af14567cf1407d3db8a7784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.4 MB (665427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b6544e1db91a142d2c520f79b9a47616b5943d650980964dde2089d622105`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45887c5bf36402135d3e8159888d8ff9b09ab897d3a90f477e330ef32b7ae686`  
		Last Modified: Tue, 07 Jan 2025 02:32:21 GMT  
		Size: 254.5 MB (254516340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59a74fe4514c470984758b86d9f4346217337f639f879106cba18ff0d0434d`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 14.2 MB (14230118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779ba51ba9acb9f403e7edde3fcdba2d6e41c4f57234338771b72c88737fa16`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485b916b73cef04bcacbf17ab015401c49254ad71a4c042aed754b899d438337`  
		Last Modified: Tue, 07 Jan 2025 02:32:22 GMT  
		Size: 366.4 MB (366442093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c3af110c11e78703a052f7868f1e44d199a26581b7932b0cade9fad97f3880`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ebf5753311702190b3351f562a8b8dfb1fc0f21c70c26b07cd8085ffec6143`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d84072118698624ab758a78d90820d1a3fd02c4c5ecc77edb3e7610f390e5`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd84a8f05c331526c12eaf53c1e4af3c2e4ca5807bf362a7392f552177642d`  
		Last Modified: Tue, 07 Jan 2025 02:32:19 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:64d1c65e58cad0864196065e5b240fa319fb5a3679db41b8293fda4d76f18db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58364432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aecabbe8d04e417c58799658bc5a16954242bd67ba3c43941587f276756a38`

```dockerfile
```

-	Layers:
	-	`sha256:eff02ed18115b0801edae6c8f6973fc48e581a85389736e9b75b255684a7e2d0`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 58.3 MB (58337296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc62a67d30aa95c392dcc712100c54b7a5f722c7da486ee96e0b89444130346`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b580ded05326157c2298f89b77037f123d36032f286c660a944e6e3f51f81c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661820054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99376e4e9b2067b5a1db4a820e2bba6526b5e815299c842fff0f9a43373a5f07`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
	-	`sha256:9bfdab3d8df1faefb7de77c3510c909b0d99bcc1178d007b57aa9fa14fb7708e`  
		Last Modified: Tue, 07 Jan 2025 03:08:06 GMT  
		Size: 366.3 MB (366293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2acfe7737e2bc45549f931b08c66b4a369dc9bb65f6cbe0cd87429c3dd953d`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26168a6ee953389d3643543cdcf15bb5a1528243bf1c24211be96e4cabd0b73`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10bb73bc2141fdbe9fff870d974984a6d7957459ca3c281a740af23d7e61b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07ee242d4ef58b8ea6cc8982985575954ca6467b7fb00a01b48aae31aeb054`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:660d0fa1249a6d89acd57d3a74a4e400a769e52a38da6f93f7782f5d1d518be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c050e05a959ebbc656f5ec34b21cb22cef19c4570a37f688ebd0062ed178002`

```dockerfile
```

-	Layers:
	-	`sha256:1e581cee7af1c587bef0d3f8380b79a872b62ab3270490c2295cf05758f760e8`  
		Last Modified: Tue, 07 Jan 2025 03:08:00 GMT  
		Size: 58.3 MB (58344587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a028aad2cee0766059b838aa806f374cc72ae58d95ad5bb62c39fc2dc7034b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:b697b0ddf3ad2d4af5898bdc66da21586229734cb6c13e853887b80fa6f53d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681736287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83741869a79d9a0715568c8ae3ccecd75b5acc24b807a1b78a78f07ca2589251`
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
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
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
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396dc4cb926aa2a8ffba5bbc0efd80eb54163b1ab9ce89ceda59c1a92b994590`  
		Last Modified: Tue, 07 Jan 2025 02:41:14 GMT  
		Size: 367.0 MB (366994400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c2c0160ebfb3debc4fcdd3f9a207bdb108367f7c369b0b38d72de794b773ef`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e4a21b179f843fa4d6aeaf5fdc92317d8184aa3111ee93cd33a675a3dbc9b`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798846e905b54fa491b50be015bf621884d34e4d62319a80cb5253e583e418ac`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6925157dec2af072810af50593a5b824f8865e952c4f77c1a0ee5af7069a8cd`  
		Last Modified: Tue, 07 Jan 2025 02:41:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f68f3f61505e82340d0c463c04d18ba420cbd560551f5a6a504769699cc3d367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58372657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d42833478f3b62b0785d4227c4d0f177fe9a4b41944a23f9f65ca4adfae0b`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b48bd1b3ac530a7b3347d18c723b6ce76cbf64171c402de6ed292ea031d10`  
		Last Modified: Tue, 07 Jan 2025 02:41:07 GMT  
		Size: 58.3 MB (58345459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb70fd5251e0f584e7d9cd98c270a9e70778d88f3d38285ed979f1f089075a79`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
