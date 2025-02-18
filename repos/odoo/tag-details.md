<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250218`](#odoo160-20250218)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250218`](#odoo170-20250218)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250218`](#odoo180-20250218)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:f46b9a17ef457d38a51e438ddfa110970222750dec0f9885fd47bd1830b49078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:164d5973d30303a0bd899c9ee6a5b22e30239a7098734a3a0ec6120cce6ada95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (583966957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deed2fc80bb8c60aff6b7a3f75803182da1dfda84c8b0a3a25a3cc397f008ce2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=16.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db842141c7407114900322c44fe2af339d0ea91b76ad0ac7f4501463a90ea414`  
		Last Modified: Mon, 10 Feb 2025 20:16:14 GMT  
		Size: 219.6 MB (219628843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc94f357778b0eb5bf74b9ffa3041491037775bb8bfa7eeb481847f4bd61655`  
		Last Modified: Mon, 10 Feb 2025 20:12:37 GMT  
		Size: 2.6 MB (2575962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3af0f52fff3dc819d6379bf97345c64116350d4696ab8979cbf8981485379d7`  
		Last Modified: Mon, 10 Feb 2025 20:12:21 GMT  
		Size: 484.9 KB (484909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd97df4d7e35ecf84145a9f896f9a8cc762b740500b2b823977bdf287316b4c`  
		Last Modified: Mon, 10 Feb 2025 20:12:34 GMT  
		Size: 331.0 MB (331022223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ec4d87c58703d4fa49b418394d24f764fbbaaa66ed5c31dcb0e878ebdf310`  
		Last Modified: Mon, 10 Feb 2025 20:12:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e0d9bed2a9b7eddd49da93eec3a7916005f31d314ed495518f37757ef2a44e`  
		Last Modified: Mon, 10 Feb 2025 20:12:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c33d40fae475593cb888a03455d981f2b64fb835cc55f60dc1aa261fc5cc974`  
		Last Modified: Mon, 10 Feb 2025 20:12:54 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0069cac309b97f5c78856b81c1c571b50f326b0fcd943bbdc5b8a40be87538`  
		Last Modified: Mon, 10 Feb 2025 20:12:54 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:26c9f235e979a32a4ed3173ee8bacf22b0d0f61ecf59b633c6e9c16868b47428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38863600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100c8bbb3a2742f47440f474dd5338d3ae3b1c6c61b5d6c8d247b85947720f24`

```dockerfile
```

-	Layers:
	-	`sha256:5620ab7bc33c58009077b99863e54b44feb142c6fe9152dd5fd1cbe9ea80f2a8`  
		Last Modified: Mon, 10 Feb 2025 19:31:15 GMT  
		Size: 38.8 MB (38836882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0836e59076582be68229eac269291104a0338b73bdb27d015eeb4c42af2b79f`  
		Last Modified: Mon, 10 Feb 2025 19:31:14 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0138baba96c2b5833ea752b0db1a438837b8b8ae1b114cdb0d6ea5e84191680a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579440779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49da6c59d7a1a3f0be0fd2aed14e2c42e6a6992e6cc0a27aed54496a819bab9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=16.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff4be9ddc2ce9c0973f24556b70e5def80b93b12dde61c1dc183b17f401de`  
		Last Modified: Mon, 10 Feb 2025 21:39:01 GMT  
		Size: 216.9 MB (216922101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec6fc362eeeaba34f96d497d74afe7ab7fffac2131628c585688aa2d07a663`  
		Last Modified: Mon, 10 Feb 2025 22:13:01 GMT  
		Size: 2.6 MB (2583894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe5dc7a8dce9250c384cb8e94b1ca2c03d4d916985761a4acc90f52b20f640`  
		Last Modified: Mon, 10 Feb 2025 20:22:24 GMT  
		Size: 485.0 KB (484976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518c5880c6b2ea0f4188caeb01c1afd98658b5a866c746a75ac6ebd9ffe9b518`  
		Last Modified: Mon, 10 Feb 2025 20:12:37 GMT  
		Size: 330.7 MB (330702566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336155ad7f3af288e4191456e6dd3f51931471cfa2f7ee9c5dcdb846994361e6`  
		Last Modified: Mon, 10 Feb 2025 21:38:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7dc65db5321d49e2432e9a9130ff2b10a01a547ac4dc0cb26de7bb0ff47586`  
		Last Modified: Mon, 10 Feb 2025 21:01:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8802a63aaf5286ac14f207e084f1334063a63680d9fb737f47a80ed10a9080e7`  
		Last Modified: Mon, 10 Feb 2025 20:22:27 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba55d53e6b836c6b123c5f93f552b5553b3e8ef068cea64dac8a21b4bfed16`  
		Last Modified: Mon, 10 Feb 2025 20:12:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d6c5a441243ca22464215cfdbad3c9597513fdd193839b8a563fb19b4ee28726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38870222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be59eb0b29004fc713d489f6eef4f65caeb523ac3ba4ef1c29968ae73ee0666f`

```dockerfile
```

-	Layers:
	-	`sha256:fec0a987967ad78245c34ca242ef8a94ad551c591a27f72f177bb0de65c5b992`  
		Last Modified: Mon, 10 Feb 2025 19:59:04 GMT  
		Size: 38.8 MB (38843352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e8bb1d03d9ee9a6d2bd32b47cf19e9c9ad1f19ef0ddf40120a2f83ba625f6b`  
		Last Modified: Mon, 10 Feb 2025 19:59:02 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:f46b9a17ef457d38a51e438ddfa110970222750dec0f9885fd47bd1830b49078
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:164d5973d30303a0bd899c9ee6a5b22e30239a7098734a3a0ec6120cce6ada95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (583966957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deed2fc80bb8c60aff6b7a3f75803182da1dfda84c8b0a3a25a3cc397f008ce2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=16.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db842141c7407114900322c44fe2af339d0ea91b76ad0ac7f4501463a90ea414`  
		Last Modified: Mon, 10 Feb 2025 20:16:14 GMT  
		Size: 219.6 MB (219628843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc94f357778b0eb5bf74b9ffa3041491037775bb8bfa7eeb481847f4bd61655`  
		Last Modified: Mon, 10 Feb 2025 20:12:37 GMT  
		Size: 2.6 MB (2575962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3af0f52fff3dc819d6379bf97345c64116350d4696ab8979cbf8981485379d7`  
		Last Modified: Mon, 10 Feb 2025 20:12:21 GMT  
		Size: 484.9 KB (484909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd97df4d7e35ecf84145a9f896f9a8cc762b740500b2b823977bdf287316b4c`  
		Last Modified: Mon, 10 Feb 2025 20:12:34 GMT  
		Size: 331.0 MB (331022223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3ec4d87c58703d4fa49b418394d24f764fbbaaa66ed5c31dcb0e878ebdf310`  
		Last Modified: Mon, 10 Feb 2025 20:12:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e0d9bed2a9b7eddd49da93eec3a7916005f31d314ed495518f37757ef2a44e`  
		Last Modified: Mon, 10 Feb 2025 20:12:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c33d40fae475593cb888a03455d981f2b64fb835cc55f60dc1aa261fc5cc974`  
		Last Modified: Mon, 10 Feb 2025 20:12:54 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0069cac309b97f5c78856b81c1c571b50f326b0fcd943bbdc5b8a40be87538`  
		Last Modified: Mon, 10 Feb 2025 20:12:54 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:26c9f235e979a32a4ed3173ee8bacf22b0d0f61ecf59b633c6e9c16868b47428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38863600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100c8bbb3a2742f47440f474dd5338d3ae3b1c6c61b5d6c8d247b85947720f24`

```dockerfile
```

-	Layers:
	-	`sha256:5620ab7bc33c58009077b99863e54b44feb142c6fe9152dd5fd1cbe9ea80f2a8`  
		Last Modified: Mon, 10 Feb 2025 19:31:15 GMT  
		Size: 38.8 MB (38836882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0836e59076582be68229eac269291104a0338b73bdb27d015eeb4c42af2b79f`  
		Last Modified: Mon, 10 Feb 2025 19:31:14 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0138baba96c2b5833ea752b0db1a438837b8b8ae1b114cdb0d6ea5e84191680a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579440779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49da6c59d7a1a3f0be0fd2aed14e2c42e6a6992e6cc0a27aed54496a819bab9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=16.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5ccf115b98cc27f86bdc30d1220cbcf7b4276f6c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff4be9ddc2ce9c0973f24556b70e5def80b93b12dde61c1dc183b17f401de`  
		Last Modified: Mon, 10 Feb 2025 21:39:01 GMT  
		Size: 216.9 MB (216922101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec6fc362eeeaba34f96d497d74afe7ab7fffac2131628c585688aa2d07a663`  
		Last Modified: Mon, 10 Feb 2025 22:13:01 GMT  
		Size: 2.6 MB (2583894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe5dc7a8dce9250c384cb8e94b1ca2c03d4d916985761a4acc90f52b20f640`  
		Last Modified: Mon, 10 Feb 2025 20:22:24 GMT  
		Size: 485.0 KB (484976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518c5880c6b2ea0f4188caeb01c1afd98658b5a866c746a75ac6ebd9ffe9b518`  
		Last Modified: Mon, 10 Feb 2025 20:12:37 GMT  
		Size: 330.7 MB (330702566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336155ad7f3af288e4191456e6dd3f51931471cfa2f7ee9c5dcdb846994361e6`  
		Last Modified: Mon, 10 Feb 2025 21:38:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7dc65db5321d49e2432e9a9130ff2b10a01a547ac4dc0cb26de7bb0ff47586`  
		Last Modified: Mon, 10 Feb 2025 21:01:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8802a63aaf5286ac14f207e084f1334063a63680d9fb737f47a80ed10a9080e7`  
		Last Modified: Mon, 10 Feb 2025 20:22:27 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba55d53e6b836c6b123c5f93f552b5553b3e8ef068cea64dac8a21b4bfed16`  
		Last Modified: Mon, 10 Feb 2025 20:12:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d6c5a441243ca22464215cfdbad3c9597513fdd193839b8a563fb19b4ee28726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38870222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be59eb0b29004fc713d489f6eef4f65caeb523ac3ba4ef1c29968ae73ee0666f`

```dockerfile
```

-	Layers:
	-	`sha256:fec0a987967ad78245c34ca242ef8a94ad551c591a27f72f177bb0de65c5b992`  
		Last Modified: Mon, 10 Feb 2025 19:59:04 GMT  
		Size: 38.8 MB (38843352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e8bb1d03d9ee9a6d2bd32b47cf19e9c9ad1f19ef0ddf40120a2f83ba625f6b`  
		Last Modified: Mon, 10 Feb 2025 19:59:02 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250218`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:17`

```console
$ docker pull odoo@sha256:b26422ce3290e7df6dc952c17c4f937792dd5159ca7a9aab7b57983af8cd48db
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
$ docker pull odoo@sha256:26c09e3cc0642471f910b7732bfa0ee42d747213476df7f9a1ad838edd40b893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599474976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b67000cebb7d80822fe8cd29cdb5191abf707ec144ede47ed3761c5c31c1d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=17.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e9b9b75b78a7152821b935008d888ca8e575e631f68308a6e55a6247aaad5b`  
		Last Modified: Mon, 10 Feb 2025 20:12:43 GMT  
		Size: 233.8 MB (233764601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ee55e19891ccb7eac361106a0c0db72393b63ceb987c741ffa1ec7894515c`  
		Last Modified: Mon, 10 Feb 2025 20:12:47 GMT  
		Size: 2.5 MB (2493812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c6614ccc7cbc07d0e614b5b6ab415b5258f31dad61222a1c38bd3b2b4b9fb6`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 485.9 KB (485942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9009e54d6efe8a60057805950f7dbba330cec41c118caa4c5f5fc5fa558f8`  
		Last Modified: Mon, 10 Feb 2025 20:13:55 GMT  
		Size: 333.2 MB (333192243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a02c62c359d99d7749234c7dbc7ea7ba86e12d9234f7413a0af21333ee0d5d`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3983ce9cc33aca3275b8b30325c28b1c0b5284451c1867ca5cf524d550d7fe2a`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872a6e36dbcacbd1016371d8e7defaeca3821585bc816b9a4056199d4625543`  
		Last Modified: Mon, 10 Feb 2025 20:12:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56c3d8929b1c39987f543fe0587b1b8a5ebecdd89f43ba2a1fa610fa0da0923`  
		Last Modified: Mon, 10 Feb 2025 20:12:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:6c618c09f021ccfb0060ceb47f0c02ed2c069442e30bf6c3404fe0b244df58ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69740c3b6a06aab6f3eab849a9ce011091bffeba33cf0c37712c0bedea7307e8`

```dockerfile
```

-	Layers:
	-	`sha256:eb0d8a1fec1afe6b1883876dea4d204a29cc852f16ae54768d031350ab05e513`  
		Last Modified: Mon, 10 Feb 2025 19:30:55 GMT  
		Size: 39.7 MB (39702158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61559928dbc814265c13947ea8f6c70ea11c5e062ea90b9d4ec32d5af3667b52`  
		Last Modified: Mon, 10 Feb 2025 19:30:55 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6cfe3df894ab01b372059fbe8660ee648cacd5d86f6d3cc748b884a4fd0a3b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594296439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33af0c2c573036c9ba3664e75684f1f7f360235be4ed57a44fffe1f50b9f8e4`
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
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=17.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd174319b3d49c009bb49f3781216969dfe5c7ac9bd0424821c5aba3c12c68`  
		Last Modified: Mon, 10 Feb 2025 20:13:13 GMT  
		Size: 231.2 MB (231161373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac50e3a0dfc9c3070305e2bc94d63f87bcb756c74e69f2821d9afa07c8b5a9`  
		Last Modified: Mon, 10 Feb 2025 20:12:56 GMT  
		Size: 2.5 MB (2485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2861d19b53d55b76e3e17c50520c494841f59ad3653dc49bf4c1576074de3aa3`  
		Last Modified: Mon, 10 Feb 2025 20:20:14 GMT  
		Size: 486.0 KB (485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50ec3eb57589b344b047aa84c9a174266d66aa7df0cb8b9fe9bf367d3787439`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 332.8 MB (332802543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60b49ffc28d93e483a7c147253e0c153aaa183d45f82db65102f4e56551a86`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85f11355f38deb08bab326fd83de66d52c4a053794fef70828b4ab07531980`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d449c409cd44084e833f585b7418e4a0a3bc3cbc9bb3c2aaa25b819b9c49936b`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e0f8f26ac41a6aa9e185ed4e8659ec86040484c02013231cbb1157413ce34f`  
		Last Modified: Mon, 10 Feb 2025 20:12:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:16736a38acec093b793de1a7358b528e81ced1a30971a064107eb8df5e66fffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39735656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4993ad20c12c7c900a9e71ae420ce098c0dbbe2de537f13d245d9f30c9ea549`

```dockerfile
```

-	Layers:
	-	`sha256:d0d364f19a16da912553d04fa4b7797fb0a726eac7d3cdb1073f86a89d762f82`  
		Last Modified: Mon, 10 Feb 2025 19:55:19 GMT  
		Size: 39.7 MB (39708669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1309541422c41bc14275a8ae368310f93139f2ddeaa65f4b8997f6c268bcb394`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:01d58e0ada5e6359003d70146a17efdfd43f89ab1b9adfa81b9d12d36d0eecf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615936131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c2e562c30a915b3dd1c69f60829f12212ab18ba07bae9052511df9753dc45c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=ppc64le
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=17.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Tue, 04 Feb 2025 07:01:41 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be366a421bba9a2f2eb85712d06dd803611984eece2cffdeea7c9f4baa2f2d`  
		Last Modified: Mon, 10 Feb 2025 19:44:54 GMT  
		Size: 243.3 MB (243286771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea167816e99f042c18eaece41b176b2d95c32a2ef59146837650dc36cbb54b`  
		Last Modified: Mon, 10 Feb 2025 20:35:22 GMT  
		Size: 2.8 MB (2798267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b96a634db7dbb5e96d74e32260d7d4351a29e086452ffbefc92a1e99abac5a3`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 486.0 KB (485991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9501b18665de676e1e84cd20fdeb73048dac67b92118c37fd73e65c9b9d481f`  
		Last Modified: Mon, 10 Feb 2025 19:44:43 GMT  
		Size: 334.9 MB (334914727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97d58dc250802e3afee529e6799742390e8413060632fb9b80d3b46cee9e4cf`  
		Last Modified: Tue, 11 Feb 2025 04:31:24 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456179d7ad82746463bd063f6ff4e8ea859d15af6de2619c97f6540bd17a830f`  
		Last Modified: Tue, 11 Feb 2025 04:31:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623cfdfcafed26891498c2a7a7d105e42cabec0a9600bcadf0a9b4d050ad10b7`  
		Last Modified: Mon, 10 Feb 2025 19:44:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1949cbb3b5e3762900f09d298da8a3135929b185b822b92c4ea9002552ff9`  
		Last Modified: Mon, 10 Feb 2025 19:44:32 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c29e29c8809461929494184a5eec3d58ff81a55a03f7b1c15b7c53c1bf2fa3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39737376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f447b23b00bba4fc621c2027f1f5eac7226ae6c4411715a46f4c64b57155948`

```dockerfile
```

-	Layers:
	-	`sha256:549cc497e20379e464ea61e0cdadcdd9cbdb975e0fae24817d4781ae712cb780`  
		Last Modified: Mon, 10 Feb 2025 19:44:32 GMT  
		Size: 39.7 MB (39710485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a274dc5337ccf8826d97c9607ead98844e76f3f4c8730c79e7a7c18cf00774`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:b26422ce3290e7df6dc952c17c4f937792dd5159ca7a9aab7b57983af8cd48db
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
$ docker pull odoo@sha256:26c09e3cc0642471f910b7732bfa0ee42d747213476df7f9a1ad838edd40b893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599474976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b67000cebb7d80822fe8cd29cdb5191abf707ec144ede47ed3761c5c31c1d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=17.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e9b9b75b78a7152821b935008d888ca8e575e631f68308a6e55a6247aaad5b`  
		Last Modified: Mon, 10 Feb 2025 20:12:43 GMT  
		Size: 233.8 MB (233764601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ee55e19891ccb7eac361106a0c0db72393b63ceb987c741ffa1ec7894515c`  
		Last Modified: Mon, 10 Feb 2025 20:12:47 GMT  
		Size: 2.5 MB (2493812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c6614ccc7cbc07d0e614b5b6ab415b5258f31dad61222a1c38bd3b2b4b9fb6`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 485.9 KB (485942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9009e54d6efe8a60057805950f7dbba330cec41c118caa4c5f5fc5fa558f8`  
		Last Modified: Mon, 10 Feb 2025 20:13:55 GMT  
		Size: 333.2 MB (333192243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a02c62c359d99d7749234c7dbc7ea7ba86e12d9234f7413a0af21333ee0d5d`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3983ce9cc33aca3275b8b30325c28b1c0b5284451c1867ca5cf524d550d7fe2a`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872a6e36dbcacbd1016371d8e7defaeca3821585bc816b9a4056199d4625543`  
		Last Modified: Mon, 10 Feb 2025 20:12:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56c3d8929b1c39987f543fe0587b1b8a5ebecdd89f43ba2a1fa610fa0da0923`  
		Last Modified: Mon, 10 Feb 2025 20:12:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6c618c09f021ccfb0060ceb47f0c02ed2c069442e30bf6c3404fe0b244df58ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69740c3b6a06aab6f3eab849a9ce011091bffeba33cf0c37712c0bedea7307e8`

```dockerfile
```

-	Layers:
	-	`sha256:eb0d8a1fec1afe6b1883876dea4d204a29cc852f16ae54768d031350ab05e513`  
		Last Modified: Mon, 10 Feb 2025 19:30:55 GMT  
		Size: 39.7 MB (39702158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61559928dbc814265c13947ea8f6c70ea11c5e062ea90b9d4ec32d5af3667b52`  
		Last Modified: Mon, 10 Feb 2025 19:30:55 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6cfe3df894ab01b372059fbe8660ee648cacd5d86f6d3cc748b884a4fd0a3b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594296439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33af0c2c573036c9ba3664e75684f1f7f360235be4ed57a44fffe1f50b9f8e4`
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
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=17.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd174319b3d49c009bb49f3781216969dfe5c7ac9bd0424821c5aba3c12c68`  
		Last Modified: Mon, 10 Feb 2025 20:13:13 GMT  
		Size: 231.2 MB (231161373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac50e3a0dfc9c3070305e2bc94d63f87bcb756c74e69f2821d9afa07c8b5a9`  
		Last Modified: Mon, 10 Feb 2025 20:12:56 GMT  
		Size: 2.5 MB (2485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2861d19b53d55b76e3e17c50520c494841f59ad3653dc49bf4c1576074de3aa3`  
		Last Modified: Mon, 10 Feb 2025 20:20:14 GMT  
		Size: 486.0 KB (485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50ec3eb57589b344b047aa84c9a174266d66aa7df0cb8b9fe9bf367d3787439`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 332.8 MB (332802543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60b49ffc28d93e483a7c147253e0c153aaa183d45f82db65102f4e56551a86`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85f11355f38deb08bab326fd83de66d52c4a053794fef70828b4ab07531980`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d449c409cd44084e833f585b7418e4a0a3bc3cbc9bb3c2aaa25b819b9c49936b`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e0f8f26ac41a6aa9e185ed4e8659ec86040484c02013231cbb1157413ce34f`  
		Last Modified: Mon, 10 Feb 2025 20:12:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:16736a38acec093b793de1a7358b528e81ced1a30971a064107eb8df5e66fffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39735656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4993ad20c12c7c900a9e71ae420ce098c0dbbe2de537f13d245d9f30c9ea549`

```dockerfile
```

-	Layers:
	-	`sha256:d0d364f19a16da912553d04fa4b7797fb0a726eac7d3cdb1073f86a89d762f82`  
		Last Modified: Mon, 10 Feb 2025 19:55:19 GMT  
		Size: 39.7 MB (39708669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1309541422c41bc14275a8ae368310f93139f2ddeaa65f4b8997f6c268bcb394`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:01d58e0ada5e6359003d70146a17efdfd43f89ab1b9adfa81b9d12d36d0eecf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615936131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c2e562c30a915b3dd1c69f60829f12212ab18ba07bae9052511df9753dc45c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=ppc64le
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=17.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=99e6b16a8062831a8458a1d60f85bc637ed03bbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Tue, 04 Feb 2025 07:01:41 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be366a421bba9a2f2eb85712d06dd803611984eece2cffdeea7c9f4baa2f2d`  
		Last Modified: Mon, 10 Feb 2025 19:44:54 GMT  
		Size: 243.3 MB (243286771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea167816e99f042c18eaece41b176b2d95c32a2ef59146837650dc36cbb54b`  
		Last Modified: Mon, 10 Feb 2025 20:35:22 GMT  
		Size: 2.8 MB (2798267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b96a634db7dbb5e96d74e32260d7d4351a29e086452ffbefc92a1e99abac5a3`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 486.0 KB (485991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9501b18665de676e1e84cd20fdeb73048dac67b92118c37fd73e65c9b9d481f`  
		Last Modified: Mon, 10 Feb 2025 19:44:43 GMT  
		Size: 334.9 MB (334914727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97d58dc250802e3afee529e6799742390e8413060632fb9b80d3b46cee9e4cf`  
		Last Modified: Tue, 11 Feb 2025 04:31:24 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456179d7ad82746463bd063f6ff4e8ea859d15af6de2619c97f6540bd17a830f`  
		Last Modified: Tue, 11 Feb 2025 04:31:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623cfdfcafed26891498c2a7a7d105e42cabec0a9600bcadf0a9b4d050ad10b7`  
		Last Modified: Mon, 10 Feb 2025 19:44:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1949cbb3b5e3762900f09d298da8a3135929b185b822b92c4ea9002552ff9`  
		Last Modified: Mon, 10 Feb 2025 19:44:32 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c29e29c8809461929494184a5eec3d58ff81a55a03f7b1c15b7c53c1bf2fa3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39737376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f447b23b00bba4fc621c2027f1f5eac7226ae6c4411715a46f4c64b57155948`

```dockerfile
```

-	Layers:
	-	`sha256:549cc497e20379e464ea61e0cdadcdd9cbdb975e0fae24817d4781ae712cb780`  
		Last Modified: Mon, 10 Feb 2025 19:44:32 GMT  
		Size: 39.7 MB (39710485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a274dc5337ccf8826d97c9607ead98844e76f3f4c8730c79e7a7c18cf00774`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250218`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:18`

```console
$ docker pull odoo@sha256:e984296ff633ad1c41d5b2ce099e9c75727a330a2fcda60cb4724d3dfe00587e
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
$ docker pull odoo@sha256:ed3e0573d8dc50a7f0d8a874b9e0dcdb42510f2f491f783cb3a9c7fc3d85f0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.8 MB (668821858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549291bfd3cb5580386caf6e6cbecbfe6e75147fb39a08b857f776ba870ce60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93c8457230a63c5fefa8a18a55154a4d9e66501ea9798169b1c202be5870e64`  
		Last Modified: Mon, 10 Feb 2025 20:13:11 GMT  
		Size: 254.5 MB (254514665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d65c04e02a60a679132af7431d0de40543254188f4388470d5a270764bff527`  
		Last Modified: Mon, 10 Feb 2025 20:12:51 GMT  
		Size: 16.6 MB (16634870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e32a3c71a37305f330e98d26d05f4813c2c3db9e6491f1de9e2c08853e931`  
		Last Modified: Mon, 10 Feb 2025 20:12:55 GMT  
		Size: 485.7 KB (485725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ffdf7ada3d25bc89191e5ab5ed201fc562e0357359cb5a57e71042a35faa99`  
		Last Modified: Mon, 10 Feb 2025 20:13:08 GMT  
		Size: 367.4 MB (367429874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a02c62c359d99d7749234c7dbc7ea7ba86e12d9234f7413a0af21333ee0d5d`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2fb41ec4dfebf94ae4caeb265eebe9141bce36c484ca20f2c8ffe94a298d1e`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec91224c0307bdc867bbd18a3867c214e7ac92aff1b326e10520c817997e9a4`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b87f359ce03e621bd093d9c62c2c21bc913f9f78dd786abb6cd76aa2c14e9`  
		Last Modified: Mon, 10 Feb 2025 20:12:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d6dea5db3797508ad116f48e44d8db4a86507e00ddba7b55343ec2e69a792227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58502815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4ae0831eae72c2bb41b56ffe25e7e7b22ef73e148a9581b0dd95449ccd287d`

```dockerfile
```

-	Layers:
	-	`sha256:2c72ce9fa2d675776ea4f1d90eeb1a6d55e6ac52cf6f53f6b311d1734f34db4c`  
		Last Modified: Tue, 11 Feb 2025 10:02:47 GMT  
		Size: 58.5 MB (58475679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769c881a6e94e403056206373113ed66c5cf22e0c6a6a7e902620745b4997963`  
		Last Modified: Tue, 11 Feb 2025 10:02:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a62bd3145fc5c753e4fcd2d8c30eec4afa4cbfbdcea6a2e2257b6f00c9d080c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 MB (665205895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81af33182b1229b54babc7d46ac4a8db7b86c8f3eb2678d1ff52d31e285e8e0`
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
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 20:19:59 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 20:19:48 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 20:56:29 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c170fc6f3a93f27a45563edadd842fccfa276908110f763a5c925fda6ec1ca4c`  
		Last Modified: Mon, 10 Feb 2025 20:19:58 GMT  
		Size: 367.3 MB (367299757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfae44fbb129501505113d1e98aa82cc0012c80cbba4e9480b5f5ede8d9f5178`  
		Last Modified: Mon, 10 Feb 2025 20:19:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36565f0b254fe5085e6637cf18b71ecdff18aceccb4f701a38a81420c228d79`  
		Last Modified: Mon, 10 Feb 2025 20:19:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0d7729a69ffae57421fc62aabba7b44213db3a99dfc556d4459b98068e329`  
		Last Modified: Mon, 10 Feb 2025 20:19:51 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35be8019f78f6aeeed2353b8b526f1dd15df9939de788076eef3c70a08e6b1d1`  
		Last Modified: Mon, 10 Feb 2025 20:25:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:59ccc0584a4a870b931ab3ec2af0fe87bb92e165ada2a52e62054d615da7c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58510270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71051e33e0a726f5b2b6981e7042ac5504d75c8e9f0e8939043e8c1151d127d`

```dockerfile
```

-	Layers:
	-	`sha256:f575e9c1a9ac1b41123a687b20ad6d8cd3b5aa009b0ab3595ef98d6d4828fb2d`  
		Last Modified: Mon, 17 Feb 2025 08:12:36 GMT  
		Size: 58.5 MB (58482970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd59be01d2a10a58f34db4d5f1ff9ee63bd876e295ac01bc9ee47d9a89d609b`  
		Last Modified: Tue, 11 Feb 2025 10:03:49 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:d5a9b7740facb0f73384c72fe37478836d7d6f3be8dff8ee07b8c7f6bd44b516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.2 MB (685228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ce4e1a930429c3a87189a3c10030f98850d5f109952c5cc8fa3489a9e8db82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=ppc64le
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Tue, 11 Feb 2025 10:04:05 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Tue, 11 Feb 2025 10:05:22 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Tue, 11 Feb 2025 10:03:56 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ebdfd5cae90e665bc71c3b7d9d9c22c23f9250b65886700ff84958ca60188`  
		Last Modified: Tue, 11 Feb 2025 10:04:09 GMT  
		Size: 368.0 MB (367970253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db94ad5e4581072bac30b1f283b3bc048bce683f7ca053367d9d120d991ecc4`  
		Last Modified: Tue, 11 Feb 2025 06:06:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a28c04c6e61973e5fec7cca066fa13d7307f4ced12163423b98e9d253bcb6`  
		Last Modified: Tue, 11 Feb 2025 10:03:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38722995d30c6e2d4be74ac5fc9b2aa8b4e9150f0a02354d5bd256145c7d3133`  
		Last Modified: Thu, 13 Feb 2025 18:23:50 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372cd5fbdde7a18b51116b89d043b2ca11d9156e29347b9b7397625aa89c13d`  
		Last Modified: Tue, 11 Feb 2025 06:06:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c653f00151186ce57500a66373bbf59853f49b78c0baf99f098f56110748b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58511040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646e1861ab8ab4e07f770835468c074727dd94e048aee7697ba88ad5be79852f`

```dockerfile
```

-	Layers:
	-	`sha256:2907c1ff3ac8deeedf25cd92fe2c9f6e92274fad98df7dab14597bcdea953fa8`  
		Last Modified: Tue, 11 Feb 2025 10:05:35 GMT  
		Size: 58.5 MB (58483842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c31ecbd9f32c3486ef587e4763db0650fbe21afee1a24bb28c561f837cdd0ca`  
		Last Modified: Tue, 11 Feb 2025 10:05:31 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:e984296ff633ad1c41d5b2ce099e9c75727a330a2fcda60cb4724d3dfe00587e
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
$ docker pull odoo@sha256:ed3e0573d8dc50a7f0d8a874b9e0dcdb42510f2f491f783cb3a9c7fc3d85f0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.8 MB (668821858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549291bfd3cb5580386caf6e6cbecbfe6e75147fb39a08b857f776ba870ce60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93c8457230a63c5fefa8a18a55154a4d9e66501ea9798169b1c202be5870e64`  
		Last Modified: Mon, 10 Feb 2025 20:13:11 GMT  
		Size: 254.5 MB (254514665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d65c04e02a60a679132af7431d0de40543254188f4388470d5a270764bff527`  
		Last Modified: Mon, 10 Feb 2025 20:12:51 GMT  
		Size: 16.6 MB (16634870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e32a3c71a37305f330e98d26d05f4813c2c3db9e6491f1de9e2c08853e931`  
		Last Modified: Mon, 10 Feb 2025 20:12:55 GMT  
		Size: 485.7 KB (485725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ffdf7ada3d25bc89191e5ab5ed201fc562e0357359cb5a57e71042a35faa99`  
		Last Modified: Mon, 10 Feb 2025 20:13:08 GMT  
		Size: 367.4 MB (367429874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a02c62c359d99d7749234c7dbc7ea7ba86e12d9234f7413a0af21333ee0d5d`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2fb41ec4dfebf94ae4caeb265eebe9141bce36c484ca20f2c8ffe94a298d1e`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec91224c0307bdc867bbd18a3867c214e7ac92aff1b326e10520c817997e9a4`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b87f359ce03e621bd093d9c62c2c21bc913f9f78dd786abb6cd76aa2c14e9`  
		Last Modified: Mon, 10 Feb 2025 20:12:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d6dea5db3797508ad116f48e44d8db4a86507e00ddba7b55343ec2e69a792227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58502815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4ae0831eae72c2bb41b56ffe25e7e7b22ef73e148a9581b0dd95449ccd287d`

```dockerfile
```

-	Layers:
	-	`sha256:2c72ce9fa2d675776ea4f1d90eeb1a6d55e6ac52cf6f53f6b311d1734f34db4c`  
		Last Modified: Tue, 11 Feb 2025 10:02:47 GMT  
		Size: 58.5 MB (58475679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769c881a6e94e403056206373113ed66c5cf22e0c6a6a7e902620745b4997963`  
		Last Modified: Tue, 11 Feb 2025 10:02:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a62bd3145fc5c753e4fcd2d8c30eec4afa4cbfbdcea6a2e2257b6f00c9d080c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 MB (665205895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81af33182b1229b54babc7d46ac4a8db7b86c8f3eb2678d1ff52d31e285e8e0`
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
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 20:19:59 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 20:19:48 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 20:56:29 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c170fc6f3a93f27a45563edadd842fccfa276908110f763a5c925fda6ec1ca4c`  
		Last Modified: Mon, 10 Feb 2025 20:19:58 GMT  
		Size: 367.3 MB (367299757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfae44fbb129501505113d1e98aa82cc0012c80cbba4e9480b5f5ede8d9f5178`  
		Last Modified: Mon, 10 Feb 2025 20:19:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36565f0b254fe5085e6637cf18b71ecdff18aceccb4f701a38a81420c228d79`  
		Last Modified: Mon, 10 Feb 2025 20:19:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0d7729a69ffae57421fc62aabba7b44213db3a99dfc556d4459b98068e329`  
		Last Modified: Mon, 10 Feb 2025 20:19:51 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35be8019f78f6aeeed2353b8b526f1dd15df9939de788076eef3c70a08e6b1d1`  
		Last Modified: Mon, 10 Feb 2025 20:25:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:59ccc0584a4a870b931ab3ec2af0fe87bb92e165ada2a52e62054d615da7c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58510270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71051e33e0a726f5b2b6981e7042ac5504d75c8e9f0e8939043e8c1151d127d`

```dockerfile
```

-	Layers:
	-	`sha256:f575e9c1a9ac1b41123a687b20ad6d8cd3b5aa009b0ab3595ef98d6d4828fb2d`  
		Last Modified: Mon, 17 Feb 2025 08:12:36 GMT  
		Size: 58.5 MB (58482970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd59be01d2a10a58f34db4d5f1ff9ee63bd876e295ac01bc9ee47d9a89d609b`  
		Last Modified: Tue, 11 Feb 2025 10:03:49 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:d5a9b7740facb0f73384c72fe37478836d7d6f3be8dff8ee07b8c7f6bd44b516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.2 MB (685228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ce4e1a930429c3a87189a3c10030f98850d5f109952c5cc8fa3489a9e8db82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=ppc64le
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Tue, 11 Feb 2025 10:04:05 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Tue, 11 Feb 2025 10:05:22 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Tue, 11 Feb 2025 10:03:56 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ebdfd5cae90e665bc71c3b7d9d9c22c23f9250b65886700ff84958ca60188`  
		Last Modified: Tue, 11 Feb 2025 10:04:09 GMT  
		Size: 368.0 MB (367970253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db94ad5e4581072bac30b1f283b3bc048bce683f7ca053367d9d120d991ecc4`  
		Last Modified: Tue, 11 Feb 2025 06:06:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a28c04c6e61973e5fec7cca066fa13d7307f4ced12163423b98e9d253bcb6`  
		Last Modified: Tue, 11 Feb 2025 10:03:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38722995d30c6e2d4be74ac5fc9b2aa8b4e9150f0a02354d5bd256145c7d3133`  
		Last Modified: Thu, 13 Feb 2025 18:23:50 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372cd5fbdde7a18b51116b89d043b2ca11d9156e29347b9b7397625aa89c13d`  
		Last Modified: Tue, 11 Feb 2025 06:06:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c653f00151186ce57500a66373bbf59853f49b78c0baf99f098f56110748b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58511040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646e1861ab8ab4e07f770835468c074727dd94e048aee7697ba88ad5be79852f`

```dockerfile
```

-	Layers:
	-	`sha256:2907c1ff3ac8deeedf25cd92fe2c9f6e92274fad98df7dab14597bcdea953fa8`  
		Last Modified: Tue, 11 Feb 2025 10:05:35 GMT  
		Size: 58.5 MB (58483842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c31ecbd9f32c3486ef587e4763db0650fbe21afee1a24bb28c561f837cdd0ca`  
		Last Modified: Tue, 11 Feb 2025 10:05:31 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250218`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:latest`

```console
$ docker pull odoo@sha256:e984296ff633ad1c41d5b2ce099e9c75727a330a2fcda60cb4724d3dfe00587e
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
$ docker pull odoo@sha256:ed3e0573d8dc50a7f0d8a874b9e0dcdb42510f2f491f783cb3a9c7fc3d85f0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.8 MB (668821858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549291bfd3cb5580386caf6e6cbecbfe6e75147fb39a08b857f776ba870ce60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93c8457230a63c5fefa8a18a55154a4d9e66501ea9798169b1c202be5870e64`  
		Last Modified: Mon, 10 Feb 2025 20:13:11 GMT  
		Size: 254.5 MB (254514665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d65c04e02a60a679132af7431d0de40543254188f4388470d5a270764bff527`  
		Last Modified: Mon, 10 Feb 2025 20:12:51 GMT  
		Size: 16.6 MB (16634870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e32a3c71a37305f330e98d26d05f4813c2c3db9e6491f1de9e2c08853e931`  
		Last Modified: Mon, 10 Feb 2025 20:12:55 GMT  
		Size: 485.7 KB (485725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ffdf7ada3d25bc89191e5ab5ed201fc562e0357359cb5a57e71042a35faa99`  
		Last Modified: Mon, 10 Feb 2025 20:13:08 GMT  
		Size: 367.4 MB (367429874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a02c62c359d99d7749234c7dbc7ea7ba86e12d9234f7413a0af21333ee0d5d`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2fb41ec4dfebf94ae4caeb265eebe9141bce36c484ca20f2c8ffe94a298d1e`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec91224c0307bdc867bbd18a3867c214e7ac92aff1b326e10520c817997e9a4`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b87f359ce03e621bd093d9c62c2c21bc913f9f78dd786abb6cd76aa2c14e9`  
		Last Modified: Mon, 10 Feb 2025 20:12:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d6dea5db3797508ad116f48e44d8db4a86507e00ddba7b55343ec2e69a792227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58502815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4ae0831eae72c2bb41b56ffe25e7e7b22ef73e148a9581b0dd95449ccd287d`

```dockerfile
```

-	Layers:
	-	`sha256:2c72ce9fa2d675776ea4f1d90eeb1a6d55e6ac52cf6f53f6b311d1734f34db4c`  
		Last Modified: Tue, 11 Feb 2025 10:02:47 GMT  
		Size: 58.5 MB (58475679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769c881a6e94e403056206373113ed66c5cf22e0c6a6a7e902620745b4997963`  
		Last Modified: Tue, 11 Feb 2025 10:02:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a62bd3145fc5c753e4fcd2d8c30eec4afa4cbfbdcea6a2e2257b6f00c9d080c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 MB (665205895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81af33182b1229b54babc7d46ac4a8db7b86c8f3eb2678d1ff52d31e285e8e0`
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
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 20:19:59 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 20:19:48 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 20:56:29 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c170fc6f3a93f27a45563edadd842fccfa276908110f763a5c925fda6ec1ca4c`  
		Last Modified: Mon, 10 Feb 2025 20:19:58 GMT  
		Size: 367.3 MB (367299757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfae44fbb129501505113d1e98aa82cc0012c80cbba4e9480b5f5ede8d9f5178`  
		Last Modified: Mon, 10 Feb 2025 20:19:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36565f0b254fe5085e6637cf18b71ecdff18aceccb4f701a38a81420c228d79`  
		Last Modified: Mon, 10 Feb 2025 20:19:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0d7729a69ffae57421fc62aabba7b44213db3a99dfc556d4459b98068e329`  
		Last Modified: Mon, 10 Feb 2025 20:19:51 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35be8019f78f6aeeed2353b8b526f1dd15df9939de788076eef3c70a08e6b1d1`  
		Last Modified: Mon, 10 Feb 2025 20:25:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:59ccc0584a4a870b931ab3ec2af0fe87bb92e165ada2a52e62054d615da7c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58510270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71051e33e0a726f5b2b6981e7042ac5504d75c8e9f0e8939043e8c1151d127d`

```dockerfile
```

-	Layers:
	-	`sha256:f575e9c1a9ac1b41123a687b20ad6d8cd3b5aa009b0ab3595ef98d6d4828fb2d`  
		Last Modified: Mon, 17 Feb 2025 08:12:36 GMT  
		Size: 58.5 MB (58482970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd59be01d2a10a58f34db4d5f1ff9ee63bd876e295ac01bc9ee47d9a89d609b`  
		Last Modified: Tue, 11 Feb 2025 10:03:49 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:d5a9b7740facb0f73384c72fe37478836d7d6f3be8dff8ee07b8c7f6bd44b516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.2 MB (685228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ce4e1a930429c3a87189a3c10030f98850d5f109952c5cc8fa3489a9e8db82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=ppc64le
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Tue, 11 Feb 2025 10:04:05 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Tue, 11 Feb 2025 10:05:22 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Tue, 11 Feb 2025 10:03:56 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ebdfd5cae90e665bc71c3b7d9d9c22c23f9250b65886700ff84958ca60188`  
		Last Modified: Tue, 11 Feb 2025 10:04:09 GMT  
		Size: 368.0 MB (367970253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db94ad5e4581072bac30b1f283b3bc048bce683f7ca053367d9d120d991ecc4`  
		Last Modified: Tue, 11 Feb 2025 06:06:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a28c04c6e61973e5fec7cca066fa13d7307f4ced12163423b98e9d253bcb6`  
		Last Modified: Tue, 11 Feb 2025 10:03:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38722995d30c6e2d4be74ac5fc9b2aa8b4e9150f0a02354d5bd256145c7d3133`  
		Last Modified: Thu, 13 Feb 2025 18:23:50 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372cd5fbdde7a18b51116b89d043b2ca11d9156e29347b9b7397625aa89c13d`  
		Last Modified: Tue, 11 Feb 2025 06:06:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c653f00151186ce57500a66373bbf59853f49b78c0baf99f098f56110748b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58511040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646e1861ab8ab4e07f770835468c074727dd94e048aee7697ba88ad5be79852f`

```dockerfile
```

-	Layers:
	-	`sha256:2907c1ff3ac8deeedf25cd92fe2c9f6e92274fad98df7dab14597bcdea953fa8`  
		Last Modified: Tue, 11 Feb 2025 10:05:35 GMT  
		Size: 58.5 MB (58483842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c31ecbd9f32c3486ef587e4763db0650fbe21afee1a24bb28c561f837cdd0ca`  
		Last Modified: Tue, 11 Feb 2025 10:05:31 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
