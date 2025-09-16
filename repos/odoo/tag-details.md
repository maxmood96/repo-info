<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250909`](#odoo160-20250909)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250909`](#odoo170-20250909)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250909`](#odoo180-20250909)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:0f36a5002a200bb1649771c2cb9403ca5392d7ac4bb23f9ad500b339df3f5a3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:99cde0c810d80e93a0284d985d6e586553783368196715c845a7aa1caa02ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585317983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af0a1080e73ad7fc93dc7dbc4e828c629940d55754fed1339526b09099a798`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=16.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59752bccf5a7becf6a3fd7c15a328a397ded5ebe08cdf6797f258c23888052e`  
		Last Modified: Wed, 10 Sep 2025 01:12:31 GMT  
		Size: 219.6 MB (219626031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0e51c2d18d4d7a9b421844ece8236b339a74b3cf1282b18f1137971bc051c`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 2.6 MB (2632402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1868e5257880d1dd6cb513d7b1d935bf58460716f390c768779bd9714629ad5c`  
		Last Modified: Tue, 09 Sep 2025 23:45:58 GMT  
		Size: 480.2 KB (480175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7584aa22f9f7aa397a04b311dfe66f71995d5db678c9cbef73a803b4afe43390`  
		Last Modified: Wed, 10 Sep 2025 01:12:40 GMT  
		Size: 332.3 MB (332320882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19ed431de01387513f193eec7c95fda354d80970e75ea4c970c0590303dadf7`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab8b9bc7a9b3864bd91749886e4e621a003d3e258be61a1c0c1c864427de59`  
		Last Modified: Tue, 09 Sep 2025 23:45:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b6a98c4399298618479607b247ee8d03e195c93396e743fb6656e784d498b`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd352db127f36ac3a5fc37d4c16697de83c30e9a21bb990668dd1fb88ef4799c`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e7155420672c588186e9abc1a07cdf45ca55b4f66db01ff892a1aeb321e1e95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39564040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b71e33acf92566effeeda0f1fe3a26cad6876faa90d6537ca49ee5b34f3658`

```dockerfile
```

-	Layers:
	-	`sha256:320ed1d8d0cec1d99c7b5aa6dd90da319f7a781416e23c1496734b876a4b2d7b`  
		Last Modified: Wed, 10 Sep 2025 01:12:27 GMT  
		Size: 39.5 MB (39537322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c6b634fe35e02a052cf9cd54e805f3a157d687e00e7b62bc6eb076a3c83707`  
		Last Modified: Wed, 10 Sep 2025 01:12:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e9e379d198aa2a5dd94b662a0e4396a5b3032be3e1d6cb0b20ff96f6ff2694e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580766854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cbdb2232d30c30191e4aaee67a6d158a8bc82fa49f9226637cb46c8c96c587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=16.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f2020c009be280a3735e3e8ef8dabd99aac95dc4dd8fbc422323a3a339f68`  
		Last Modified: Wed, 10 Sep 2025 01:12:32 GMT  
		Size: 216.9 MB (216919215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45deae93115ba27a1791f72c63a7a9427ba934674b8c9abd8ee3f0ba018d0009`  
		Last Modified: Tue, 09 Sep 2025 23:50:58 GMT  
		Size: 2.6 MB (2639101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003efeed71e33fbd02aae92c5ee0d62ed9638e29c2d8b094987e50fa793b400`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 480.2 KB (480162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f333b0177f2fe6b046df53422d38499cd135b4f536bfc57fc8a7f8bfe51ce`  
		Last Modified: Wed, 10 Sep 2025 01:12:37 GMT  
		Size: 332.0 MB (331975485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3e1350d9532631437712521c295036ca735eaf73932a5ef6ab57beee67ff66`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15fe5f9c0d1ea4cc167ebcc82fb43f9fbf6434e4fef095985dd615969a3466c`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9f4521bdda89924364a3332314b95042abe2f2360dd826160507408382d46`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc7316471a019367eb84b18344515fc3d19c19bf0f8bc85aa29071f372ea13`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:083a68492d59fd151c276f14a398e25c96adb844aaf326087512d9668d6e8d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39570658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fe9d21e5079321c53209948f484e43ef0d39235f399fb59a759e756a669af0`

```dockerfile
```

-	Layers:
	-	`sha256:bf1ff4909791a7daafd28176debf41dabd01126e1897078baebbe2a4e151ad06`  
		Last Modified: Wed, 10 Sep 2025 01:13:19 GMT  
		Size: 39.5 MB (39543788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb134572950bd9643ae875ec93e14c77dd92f43d917d41b1dab6e8e5a8b2d11`  
		Last Modified: Wed, 10 Sep 2025 01:13:20 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:0f36a5002a200bb1649771c2cb9403ca5392d7ac4bb23f9ad500b339df3f5a3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:99cde0c810d80e93a0284d985d6e586553783368196715c845a7aa1caa02ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585317983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af0a1080e73ad7fc93dc7dbc4e828c629940d55754fed1339526b09099a798`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=16.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59752bccf5a7becf6a3fd7c15a328a397ded5ebe08cdf6797f258c23888052e`  
		Last Modified: Wed, 10 Sep 2025 01:12:31 GMT  
		Size: 219.6 MB (219626031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0e51c2d18d4d7a9b421844ece8236b339a74b3cf1282b18f1137971bc051c`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 2.6 MB (2632402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1868e5257880d1dd6cb513d7b1d935bf58460716f390c768779bd9714629ad5c`  
		Last Modified: Tue, 09 Sep 2025 23:45:58 GMT  
		Size: 480.2 KB (480175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7584aa22f9f7aa397a04b311dfe66f71995d5db678c9cbef73a803b4afe43390`  
		Last Modified: Wed, 10 Sep 2025 01:12:40 GMT  
		Size: 332.3 MB (332320882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19ed431de01387513f193eec7c95fda354d80970e75ea4c970c0590303dadf7`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab8b9bc7a9b3864bd91749886e4e621a003d3e258be61a1c0c1c864427de59`  
		Last Modified: Tue, 09 Sep 2025 23:45:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b6a98c4399298618479607b247ee8d03e195c93396e743fb6656e784d498b`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd352db127f36ac3a5fc37d4c16697de83c30e9a21bb990668dd1fb88ef4799c`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e7155420672c588186e9abc1a07cdf45ca55b4f66db01ff892a1aeb321e1e95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39564040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b71e33acf92566effeeda0f1fe3a26cad6876faa90d6537ca49ee5b34f3658`

```dockerfile
```

-	Layers:
	-	`sha256:320ed1d8d0cec1d99c7b5aa6dd90da319f7a781416e23c1496734b876a4b2d7b`  
		Last Modified: Wed, 10 Sep 2025 01:12:27 GMT  
		Size: 39.5 MB (39537322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c6b634fe35e02a052cf9cd54e805f3a157d687e00e7b62bc6eb076a3c83707`  
		Last Modified: Wed, 10 Sep 2025 01:12:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e9e379d198aa2a5dd94b662a0e4396a5b3032be3e1d6cb0b20ff96f6ff2694e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580766854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cbdb2232d30c30191e4aaee67a6d158a8bc82fa49f9226637cb46c8c96c587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=16.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f2020c009be280a3735e3e8ef8dabd99aac95dc4dd8fbc422323a3a339f68`  
		Last Modified: Wed, 10 Sep 2025 01:12:32 GMT  
		Size: 216.9 MB (216919215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45deae93115ba27a1791f72c63a7a9427ba934674b8c9abd8ee3f0ba018d0009`  
		Last Modified: Tue, 09 Sep 2025 23:50:58 GMT  
		Size: 2.6 MB (2639101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003efeed71e33fbd02aae92c5ee0d62ed9638e29c2d8b094987e50fa793b400`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 480.2 KB (480162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f333b0177f2fe6b046df53422d38499cd135b4f536bfc57fc8a7f8bfe51ce`  
		Last Modified: Wed, 10 Sep 2025 01:12:37 GMT  
		Size: 332.0 MB (331975485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3e1350d9532631437712521c295036ca735eaf73932a5ef6ab57beee67ff66`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15fe5f9c0d1ea4cc167ebcc82fb43f9fbf6434e4fef095985dd615969a3466c`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9f4521bdda89924364a3332314b95042abe2f2360dd826160507408382d46`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc7316471a019367eb84b18344515fc3d19c19bf0f8bc85aa29071f372ea13`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:083a68492d59fd151c276f14a398e25c96adb844aaf326087512d9668d6e8d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39570658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fe9d21e5079321c53209948f484e43ef0d39235f399fb59a759e756a669af0`

```dockerfile
```

-	Layers:
	-	`sha256:bf1ff4909791a7daafd28176debf41dabd01126e1897078baebbe2a4e151ad06`  
		Last Modified: Wed, 10 Sep 2025 01:13:19 GMT  
		Size: 39.5 MB (39543788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb134572950bd9643ae875ec93e14c77dd92f43d917d41b1dab6e8e5a8b2d11`  
		Last Modified: Wed, 10 Sep 2025 01:13:20 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250909`

```console
$ docker pull odoo@sha256:0f36a5002a200bb1649771c2cb9403ca5392d7ac4bb23f9ad500b339df3f5a3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250909` - linux; amd64

```console
$ docker pull odoo@sha256:99cde0c810d80e93a0284d985d6e586553783368196715c845a7aa1caa02ec8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585317983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af0a1080e73ad7fc93dc7dbc4e828c629940d55754fed1339526b09099a798`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=16.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59752bccf5a7becf6a3fd7c15a328a397ded5ebe08cdf6797f258c23888052e`  
		Last Modified: Wed, 10 Sep 2025 01:12:31 GMT  
		Size: 219.6 MB (219626031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d0e51c2d18d4d7a9b421844ece8236b339a74b3cf1282b18f1137971bc051c`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 2.6 MB (2632402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1868e5257880d1dd6cb513d7b1d935bf58460716f390c768779bd9714629ad5c`  
		Last Modified: Tue, 09 Sep 2025 23:45:58 GMT  
		Size: 480.2 KB (480175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7584aa22f9f7aa397a04b311dfe66f71995d5db678c9cbef73a803b4afe43390`  
		Last Modified: Wed, 10 Sep 2025 01:12:40 GMT  
		Size: 332.3 MB (332320882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19ed431de01387513f193eec7c95fda354d80970e75ea4c970c0590303dadf7`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab8b9bc7a9b3864bd91749886e4e621a003d3e258be61a1c0c1c864427de59`  
		Last Modified: Tue, 09 Sep 2025 23:45:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b6a98c4399298618479607b247ee8d03e195c93396e743fb6656e784d498b`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd352db127f36ac3a5fc37d4c16697de83c30e9a21bb990668dd1fb88ef4799c`  
		Last Modified: Tue, 09 Sep 2025 23:45:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:e7155420672c588186e9abc1a07cdf45ca55b4f66db01ff892a1aeb321e1e95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39564040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b71e33acf92566effeeda0f1fe3a26cad6876faa90d6537ca49ee5b34f3658`

```dockerfile
```

-	Layers:
	-	`sha256:320ed1d8d0cec1d99c7b5aa6dd90da319f7a781416e23c1496734b876a4b2d7b`  
		Last Modified: Wed, 10 Sep 2025 01:12:27 GMT  
		Size: 39.5 MB (39537322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c6b634fe35e02a052cf9cd54e805f3a157d687e00e7b62bc6eb076a3c83707`  
		Last Modified: Wed, 10 Sep 2025 01:12:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250909` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e9e379d198aa2a5dd94b662a0e4396a5b3032be3e1d6cb0b20ff96f6ff2694e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580766854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cbdb2232d30c30191e4aaee67a6d158a8bc82fa49f9226637cb46c8c96c587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=C.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=16.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=86371b3510555e464caae06eba3373f75fbbb4f5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f2020c009be280a3735e3e8ef8dabd99aac95dc4dd8fbc422323a3a339f68`  
		Last Modified: Wed, 10 Sep 2025 01:12:32 GMT  
		Size: 216.9 MB (216919215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45deae93115ba27a1791f72c63a7a9427ba934674b8c9abd8ee3f0ba018d0009`  
		Last Modified: Tue, 09 Sep 2025 23:50:58 GMT  
		Size: 2.6 MB (2639101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003efeed71e33fbd02aae92c5ee0d62ed9638e29c2d8b094987e50fa793b400`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 480.2 KB (480162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f333b0177f2fe6b046df53422d38499cd135b4f536bfc57fc8a7f8bfe51ce`  
		Last Modified: Wed, 10 Sep 2025 01:12:37 GMT  
		Size: 332.0 MB (331975485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3e1350d9532631437712521c295036ca735eaf73932a5ef6ab57beee67ff66`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15fe5f9c0d1ea4cc167ebcc82fb43f9fbf6434e4fef095985dd615969a3466c`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9f4521bdda89924364a3332314b95042abe2f2360dd826160507408382d46`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfc7316471a019367eb84b18344515fc3d19c19bf0f8bc85aa29071f372ea13`  
		Last Modified: Tue, 09 Sep 2025 23:50:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:083a68492d59fd151c276f14a398e25c96adb844aaf326087512d9668d6e8d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39570658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fe9d21e5079321c53209948f484e43ef0d39235f399fb59a759e756a669af0`

```dockerfile
```

-	Layers:
	-	`sha256:bf1ff4909791a7daafd28176debf41dabd01126e1897078baebbe2a4e151ad06`  
		Last Modified: Wed, 10 Sep 2025 01:13:19 GMT  
		Size: 39.5 MB (39543788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb134572950bd9643ae875ec93e14c77dd92f43d917d41b1dab6e8e5a8b2d11`  
		Last Modified: Wed, 10 Sep 2025 01:13:20 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:615ccd10312e50acb1d9e520c4980ae6e9f5e08ef495d1940197c9e2ad34ac19
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
$ docker pull odoo@sha256:b8b34da1a1d5a3a546ae9ec2a82acd7202bd62db7184a143605a5ac9d21baf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605120422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0395886d55ac808316fe0ac6a9537fe3b6272a980575e7ebe5a57e84c217b520`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c1b68737b0b22b2a953eb8272f8ab2bf0fd7b5638227f2b71a8eb7a3c64f6`  
		Last Modified: Wed, 10 Sep 2025 01:13:13 GMT  
		Size: 233.8 MB (233786362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199f063616b008da6ef9f216808a46053561c67c95b45c66e9afb6b8ba68da1`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 2.5 MB (2532317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23711127af7d2f2d4f4dd16f1a6a3e34f098316eff49301ca9cd8d99b6747189`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 481.3 KB (481304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4516a96fef45959b0f262198c1565066e4794431d889cdc535b301767bffdeb5`  
		Last Modified: Wed, 10 Sep 2025 01:12:48 GMT  
		Size: 338.8 MB (338781064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43833a910374a23f591f7f9f60e698f59ca42b3a15d99270ac6dad9356b2364a`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6caf68f2a608833b455b588bd21284af15ae6a478c40cfe6734d4af9a743177`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2cfcdfd3d4f4b7902f0882ba298a740d49fae4421e3b77caa36aceffae09d6`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2ca4007de3ea698dcbdb4218d4a57ed0102b9a8c1f3a9b60f3e8e5a4eab0d4`  
		Last Modified: Tue, 09 Sep 2025 23:45:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:dd96bf6bf7b87135f78260fae536bf4bd0c27a4126631162fdb5573020aa31ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41476824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704c008112893e5682124bc5fdbe031020f34e5adb81707b73b1b134d82a8224`

```dockerfile
```

-	Layers:
	-	`sha256:72230cb9a7c84d924785739983b4f71398837c1f63e50da1ade8a232df2e9b95`  
		Last Modified: Wed, 10 Sep 2025 01:12:38 GMT  
		Size: 41.4 MB (41449989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbf124fc420bb609e662cd037dca2efdedf4080cc643d9c62bf349028fb1c8`  
		Last Modified: Wed, 10 Sep 2025 01:12:39 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9af573bb86c111852d94d9e0bdccc62da47dbfc0e0a5ffaaab79f5c14c3132ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599927065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e3005a66d31dbe5a9545222598f6b58b75a0c2894f1ed887fec62f6bf966b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cf08c18e12e6987cd601382fcfc589a074a420a1e544a6c02bf8a1339d811b`  
		Last Modified: Wed, 10 Sep 2025 01:20:18 GMT  
		Size: 231.2 MB (231158906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc3f9e9ff7ea3c17bd4faae8502ab213ff98a37b2e70a2b8d5eede7c82b6e23`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 2.5 MB (2521563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c13512c75a42e4864c3a7e86744c633952f699bdd62153da885341b2360381a`  
		Last Modified: Tue, 09 Sep 2025 23:48:30 GMT  
		Size: 481.3 KB (481322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca243850f456eaf93e4b824fb70b5353659f1b5e44346c82ea1b689e0126f45`  
		Last Modified: Wed, 10 Sep 2025 01:14:21 GMT  
		Size: 338.4 MB (338401368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988d44e2bf0463f459e04d3de122f02b353a119346eee7202c865e951757d807`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f1c7f5b185faafafc19c517458189804874210fc838723dde2802eda22bc2`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187142457fd486b4f16336da225a8a99431041f1e0180ec3ed4f4e8fa7f5c4e4`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f8f082829c1e671d5b9ab64c8d4e9bbf1a5b215f234324c9db9bd6b3f0e07`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:3c084432cd197e0f6378e7468e4b6669254ff6a8bcc186d6dfb8ebf1c138183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41483483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fb752717a6f8b44ddf0da19b53a0373ff259d4519f8db52ef660a34b4685d2`

```dockerfile
```

-	Layers:
	-	`sha256:cb87e3d6c6c7981141a08fea73c7067a21800e9b00f91fb59e682cdad1626d6c`  
		Last Modified: Wed, 10 Sep 2025 01:13:41 GMT  
		Size: 41.5 MB (41456496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5ff24138d47bc0605b5392583e6057bcbb36a21b3575ca530b1960ce47f531`  
		Last Modified: Wed, 10 Sep 2025 01:13:42 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:cadf5633e4ddcbac6c78b65f3ebd857b9a0f534c73f4e3db86ac39313081fc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621553605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a933f439e5296cd3ef5fd8b8323798926bc26391d0b25f52cb72e481baca722d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0244576ff338cb147bce56c2933253a7a9b13693e7a2a4fab239f787971b79e`  
		Last Modified: Fri, 05 Sep 2025 16:46:24 GMT  
		Size: 243.3 MB (243255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b7193b511593404db1da58c5c82ec824298a9b689a2b09266a88226fd23e`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 2.8 MB (2849712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e332f93026970e0b3ca80b7bc515ce4e41367ed2492efb6ead672fb111fd4e5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 480.5 KB (480460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc958ad1b0354301fa8bc608af6f979e09ad2d84316ab8fa24e0aad8fd7f287b`  
		Last Modified: Wed, 10 Sep 2025 13:12:36 GMT  
		Size: 340.5 MB (340522061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8dcfefe051ae40b7f0d0ffd8296c56fad5d0462a1324dee62c6fab366bbcd`  
		Last Modified: Wed, 10 Sep 2025 13:04:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d5200cc256f793a3099f44fdc8f3429eeb19fe497cfdc45609afa956714500`  
		Last Modified: Wed, 10 Sep 2025 13:04:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186b389efb5fcd004faeca74799dc6c4a72eaec9ee31f292bb987df58d389bf1`  
		Last Modified: Wed, 10 Sep 2025 13:04:39 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c34f1eb8387cb5188c7ed2e94f152b3bc1ef39c8f4e826e2009cb47ce4aaac`  
		Last Modified: Wed, 10 Sep 2025 13:04:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e86adbdc527e27b0f52156c17e4d85d6de34f6f1c9f44290e26e062053eb0d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41485487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42122a3cf72b824a6c0ee159bb2a3b768a1683e36d187bdc41cce85543220685`

```dockerfile
```

-	Layers:
	-	`sha256:3b9b17d2731d775435358d0244504a56fe37cb57ce7f384c45bab56e5fe72bc8`  
		Last Modified: Wed, 10 Sep 2025 13:13:50 GMT  
		Size: 41.5 MB (41458596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb542fb4ab4b1dd5db42b7eebe94596b19ff93d1ed89d4955fedcefc6721d637`  
		Last Modified: Wed, 10 Sep 2025 13:13:51 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:615ccd10312e50acb1d9e520c4980ae6e9f5e08ef495d1940197c9e2ad34ac19
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
$ docker pull odoo@sha256:b8b34da1a1d5a3a546ae9ec2a82acd7202bd62db7184a143605a5ac9d21baf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605120422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0395886d55ac808316fe0ac6a9537fe3b6272a980575e7ebe5a57e84c217b520`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c1b68737b0b22b2a953eb8272f8ab2bf0fd7b5638227f2b71a8eb7a3c64f6`  
		Last Modified: Wed, 10 Sep 2025 01:13:13 GMT  
		Size: 233.8 MB (233786362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199f063616b008da6ef9f216808a46053561c67c95b45c66e9afb6b8ba68da1`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 2.5 MB (2532317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23711127af7d2f2d4f4dd16f1a6a3e34f098316eff49301ca9cd8d99b6747189`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 481.3 KB (481304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4516a96fef45959b0f262198c1565066e4794431d889cdc535b301767bffdeb5`  
		Last Modified: Wed, 10 Sep 2025 01:12:48 GMT  
		Size: 338.8 MB (338781064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43833a910374a23f591f7f9f60e698f59ca42b3a15d99270ac6dad9356b2364a`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6caf68f2a608833b455b588bd21284af15ae6a478c40cfe6734d4af9a743177`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2cfcdfd3d4f4b7902f0882ba298a740d49fae4421e3b77caa36aceffae09d6`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2ca4007de3ea698dcbdb4218d4a57ed0102b9a8c1f3a9b60f3e8e5a4eab0d4`  
		Last Modified: Tue, 09 Sep 2025 23:45:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:dd96bf6bf7b87135f78260fae536bf4bd0c27a4126631162fdb5573020aa31ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41476824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704c008112893e5682124bc5fdbe031020f34e5adb81707b73b1b134d82a8224`

```dockerfile
```

-	Layers:
	-	`sha256:72230cb9a7c84d924785739983b4f71398837c1f63e50da1ade8a232df2e9b95`  
		Last Modified: Wed, 10 Sep 2025 01:12:38 GMT  
		Size: 41.4 MB (41449989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbf124fc420bb609e662cd037dca2efdedf4080cc643d9c62bf349028fb1c8`  
		Last Modified: Wed, 10 Sep 2025 01:12:39 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9af573bb86c111852d94d9e0bdccc62da47dbfc0e0a5ffaaab79f5c14c3132ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599927065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e3005a66d31dbe5a9545222598f6b58b75a0c2894f1ed887fec62f6bf966b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cf08c18e12e6987cd601382fcfc589a074a420a1e544a6c02bf8a1339d811b`  
		Last Modified: Wed, 10 Sep 2025 01:20:18 GMT  
		Size: 231.2 MB (231158906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc3f9e9ff7ea3c17bd4faae8502ab213ff98a37b2e70a2b8d5eede7c82b6e23`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 2.5 MB (2521563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c13512c75a42e4864c3a7e86744c633952f699bdd62153da885341b2360381a`  
		Last Modified: Tue, 09 Sep 2025 23:48:30 GMT  
		Size: 481.3 KB (481322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca243850f456eaf93e4b824fb70b5353659f1b5e44346c82ea1b689e0126f45`  
		Last Modified: Wed, 10 Sep 2025 01:14:21 GMT  
		Size: 338.4 MB (338401368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988d44e2bf0463f459e04d3de122f02b353a119346eee7202c865e951757d807`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f1c7f5b185faafafc19c517458189804874210fc838723dde2802eda22bc2`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187142457fd486b4f16336da225a8a99431041f1e0180ec3ed4f4e8fa7f5c4e4`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f8f082829c1e671d5b9ab64c8d4e9bbf1a5b215f234324c9db9bd6b3f0e07`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3c084432cd197e0f6378e7468e4b6669254ff6a8bcc186d6dfb8ebf1c138183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41483483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fb752717a6f8b44ddf0da19b53a0373ff259d4519f8db52ef660a34b4685d2`

```dockerfile
```

-	Layers:
	-	`sha256:cb87e3d6c6c7981141a08fea73c7067a21800e9b00f91fb59e682cdad1626d6c`  
		Last Modified: Wed, 10 Sep 2025 01:13:41 GMT  
		Size: 41.5 MB (41456496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5ff24138d47bc0605b5392583e6057bcbb36a21b3575ca530b1960ce47f531`  
		Last Modified: Wed, 10 Sep 2025 01:13:42 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:cadf5633e4ddcbac6c78b65f3ebd857b9a0f534c73f4e3db86ac39313081fc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621553605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a933f439e5296cd3ef5fd8b8323798926bc26391d0b25f52cb72e481baca722d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0244576ff338cb147bce56c2933253a7a9b13693e7a2a4fab239f787971b79e`  
		Last Modified: Fri, 05 Sep 2025 16:46:24 GMT  
		Size: 243.3 MB (243255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b7193b511593404db1da58c5c82ec824298a9b689a2b09266a88226fd23e`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 2.8 MB (2849712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e332f93026970e0b3ca80b7bc515ce4e41367ed2492efb6ead672fb111fd4e5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 480.5 KB (480460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc958ad1b0354301fa8bc608af6f979e09ad2d84316ab8fa24e0aad8fd7f287b`  
		Last Modified: Wed, 10 Sep 2025 13:12:36 GMT  
		Size: 340.5 MB (340522061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8dcfefe051ae40b7f0d0ffd8296c56fad5d0462a1324dee62c6fab366bbcd`  
		Last Modified: Wed, 10 Sep 2025 13:04:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d5200cc256f793a3099f44fdc8f3429eeb19fe497cfdc45609afa956714500`  
		Last Modified: Wed, 10 Sep 2025 13:04:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186b389efb5fcd004faeca74799dc6c4a72eaec9ee31f292bb987df58d389bf1`  
		Last Modified: Wed, 10 Sep 2025 13:04:39 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c34f1eb8387cb5188c7ed2e94f152b3bc1ef39c8f4e826e2009cb47ce4aaac`  
		Last Modified: Wed, 10 Sep 2025 13:04:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e86adbdc527e27b0f52156c17e4d85d6de34f6f1c9f44290e26e062053eb0d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41485487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42122a3cf72b824a6c0ee159bb2a3b768a1683e36d187bdc41cce85543220685`

```dockerfile
```

-	Layers:
	-	`sha256:3b9b17d2731d775435358d0244504a56fe37cb57ce7f384c45bab56e5fe72bc8`  
		Last Modified: Wed, 10 Sep 2025 13:13:50 GMT  
		Size: 41.5 MB (41458596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb542fb4ab4b1dd5db42b7eebe94596b19ff93d1ed89d4955fedcefc6721d637`  
		Last Modified: Wed, 10 Sep 2025 13:13:51 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250909`

```console
$ docker pull odoo@sha256:615ccd10312e50acb1d9e520c4980ae6e9f5e08ef495d1940197c9e2ad34ac19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250909` - linux; amd64

```console
$ docker pull odoo@sha256:b8b34da1a1d5a3a546ae9ec2a82acd7202bd62db7184a143605a5ac9d21baf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605120422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0395886d55ac808316fe0ac6a9537fe3b6272a980575e7ebe5a57e84c217b520`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c1b68737b0b22b2a953eb8272f8ab2bf0fd7b5638227f2b71a8eb7a3c64f6`  
		Last Modified: Wed, 10 Sep 2025 01:13:13 GMT  
		Size: 233.8 MB (233786362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a199f063616b008da6ef9f216808a46053561c67c95b45c66e9afb6b8ba68da1`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 2.5 MB (2532317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23711127af7d2f2d4f4dd16f1a6a3e34f098316eff49301ca9cd8d99b6747189`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 481.3 KB (481304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4516a96fef45959b0f262198c1565066e4794431d889cdc535b301767bffdeb5`  
		Last Modified: Wed, 10 Sep 2025 01:12:48 GMT  
		Size: 338.8 MB (338781064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43833a910374a23f591f7f9f60e698f59ca42b3a15d99270ac6dad9356b2364a`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6caf68f2a608833b455b588bd21284af15ae6a478c40cfe6734d4af9a743177`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2cfcdfd3d4f4b7902f0882ba298a740d49fae4421e3b77caa36aceffae09d6`  
		Last Modified: Tue, 09 Sep 2025 23:45:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2ca4007de3ea698dcbdb4218d4a57ed0102b9a8c1f3a9b60f3e8e5a4eab0d4`  
		Last Modified: Tue, 09 Sep 2025 23:45:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:dd96bf6bf7b87135f78260fae536bf4bd0c27a4126631162fdb5573020aa31ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41476824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704c008112893e5682124bc5fdbe031020f34e5adb81707b73b1b134d82a8224`

```dockerfile
```

-	Layers:
	-	`sha256:72230cb9a7c84d924785739983b4f71398837c1f63e50da1ade8a232df2e9b95`  
		Last Modified: Wed, 10 Sep 2025 01:12:38 GMT  
		Size: 41.4 MB (41449989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93bbf124fc420bb609e662cd037dca2efdedf4080cc643d9c62bf349028fb1c8`  
		Last Modified: Wed, 10 Sep 2025 01:12:39 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250909` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9af573bb86c111852d94d9e0bdccc62da47dbfc0e0a5ffaaab79f5c14c3132ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599927065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e3005a66d31dbe5a9545222598f6b58b75a0c2894f1ed887fec62f6bf966b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cf08c18e12e6987cd601382fcfc589a074a420a1e544a6c02bf8a1339d811b`  
		Last Modified: Wed, 10 Sep 2025 01:20:18 GMT  
		Size: 231.2 MB (231158906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc3f9e9ff7ea3c17bd4faae8502ab213ff98a37b2e70a2b8d5eede7c82b6e23`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 2.5 MB (2521563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c13512c75a42e4864c3a7e86744c633952f699bdd62153da885341b2360381a`  
		Last Modified: Tue, 09 Sep 2025 23:48:30 GMT  
		Size: 481.3 KB (481322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca243850f456eaf93e4b824fb70b5353659f1b5e44346c82ea1b689e0126f45`  
		Last Modified: Wed, 10 Sep 2025 01:14:21 GMT  
		Size: 338.4 MB (338401368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988d44e2bf0463f459e04d3de122f02b353a119346eee7202c865e951757d807`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f1c7f5b185faafafc19c517458189804874210fc838723dde2802eda22bc2`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187142457fd486b4f16336da225a8a99431041f1e0180ec3ed4f4e8fa7f5c4e4`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f8f082829c1e671d5b9ab64c8d4e9bbf1a5b215f234324c9db9bd6b3f0e07`  
		Last Modified: Tue, 09 Sep 2025 23:48:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:3c084432cd197e0f6378e7468e4b6669254ff6a8bcc186d6dfb8ebf1c138183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41483483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fb752717a6f8b44ddf0da19b53a0373ff259d4519f8db52ef660a34b4685d2`

```dockerfile
```

-	Layers:
	-	`sha256:cb87e3d6c6c7981141a08fea73c7067a21800e9b00f91fb59e682cdad1626d6c`  
		Last Modified: Wed, 10 Sep 2025 01:13:41 GMT  
		Size: 41.5 MB (41456496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5ff24138d47bc0605b5392583e6057bcbb36a21b3575ca530b1960ce47f531`  
		Last Modified: Wed, 10 Sep 2025 01:13:42 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250909` - linux; ppc64le

```console
$ docker pull odoo@sha256:cadf5633e4ddcbac6c78b65f3ebd857b9a0f534c73f4e3db86ac39313081fc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621553605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a933f439e5296cd3ef5fd8b8323798926bc26391d0b25f52cb72e481baca722d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=cef7734a1be7f33bea6804ea2408c52bc448d1c0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0244576ff338cb147bce56c2933253a7a9b13693e7a2a4fab239f787971b79e`  
		Last Modified: Fri, 05 Sep 2025 16:46:24 GMT  
		Size: 243.3 MB (243255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b7193b511593404db1da58c5c82ec824298a9b689a2b09266a88226fd23e`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 2.8 MB (2849712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e332f93026970e0b3ca80b7bc515ce4e41367ed2492efb6ead672fb111fd4e5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 480.5 KB (480460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc958ad1b0354301fa8bc608af6f979e09ad2d84316ab8fa24e0aad8fd7f287b`  
		Last Modified: Wed, 10 Sep 2025 13:12:36 GMT  
		Size: 340.5 MB (340522061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8dcfefe051ae40b7f0d0ffd8296c56fad5d0462a1324dee62c6fab366bbcd`  
		Last Modified: Wed, 10 Sep 2025 13:04:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d5200cc256f793a3099f44fdc8f3429eeb19fe497cfdc45609afa956714500`  
		Last Modified: Wed, 10 Sep 2025 13:04:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186b389efb5fcd004faeca74799dc6c4a72eaec9ee31f292bb987df58d389bf1`  
		Last Modified: Wed, 10 Sep 2025 13:04:39 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c34f1eb8387cb5188c7ed2e94f152b3bc1ef39c8f4e826e2009cb47ce4aaac`  
		Last Modified: Wed, 10 Sep 2025 13:04:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:e86adbdc527e27b0f52156c17e4d85d6de34f6f1c9f44290e26e062053eb0d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41485487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42122a3cf72b824a6c0ee159bb2a3b768a1683e36d187bdc41cce85543220685`

```dockerfile
```

-	Layers:
	-	`sha256:3b9b17d2731d775435358d0244504a56fe37cb57ce7f384c45bab56e5fe72bc8`  
		Last Modified: Wed, 10 Sep 2025 13:13:50 GMT  
		Size: 41.5 MB (41458596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb542fb4ab4b1dd5db42b7eebe94596b19ff93d1ed89d4955fedcefc6721d637`  
		Last Modified: Wed, 10 Sep 2025 13:13:51 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:624d493b541d0d919b33c857196827df93a928d2652c5a196fa2601a1286f1a1
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
$ docker pull odoo@sha256:217142296443977e50965e267e273e017a0d3f198c6e31b15f8f1821de4d78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676213267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d28b6ba718f921cfe92dd322ef8724da1e9e6dc3bdb2cf5b7389f913d3a2de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c29165224085f25ffd560cc3971a90d61cf7968a905d7e54fdf1f3843f51`  
		Last Modified: Mon, 15 Sep 2025 23:20:32 GMT  
		Size: 254.5 MB (254528712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65342fcb7a292e5215f4ed5901d7e32801f09ad4976100446df11023a06863bf`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 14.3 MB (14286402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f18de9da6584b0f56f7f6bed55ba6a802d9333fab55adb526fb0a0db30cfb4`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9b99696abd94f9c906a667d34d69f0c077b5de97451dfd20e8667b481bfa5a`  
		Last Modified: Mon, 15 Sep 2025 23:19:57 GMT  
		Size: 377.2 MB (377191302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7efb479f44f6154d1360e28fff72c0709f1cf8d80e4f11b3a9194d84b33a68`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f82a8644a9bea5be3a71f286ddf4b8b62c6f2940d88647c03f16e783a81154`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31f8e2949800fa043602d3fd003ed73d04b7af25710ec736411d8c9d9563dd`  
		Last Modified: Mon, 15 Sep 2025 22:25:39 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4182630c6d44de1fb500f5c59fd17d73d881d318fe94f9cde19616287c120`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:20bc410a2a431e9a15b9aae383a2d56ec79381ea8ada5056540e9ac64f2133ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda5e519749c6d03090787ae247b38153ab96195b90cb65ac2221cac9fa8b560`

```dockerfile
```

-	Layers:
	-	`sha256:d3bdc1d2a732a112070613fd179a0487aca7fa1ee272e790d91412f865aa6a4d`  
		Last Modified: Tue, 16 Sep 2025 01:12:38 GMT  
		Size: 60.9 MB (60862952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee77b4e9ae0374124e1b760486b3cae53967fd944862f9e356a794657391563`  
		Last Modified: Tue, 16 Sep 2025 01:12:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bad7d239b8c8eaaed045478246b21d54d55e613067b6722f8703d33615e9ffcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672546869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1052baf2c85d54329532084ca5fa6609cfdba9ed0863cea3dde90a37b7f78d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e7817fae6f931bd30374ad2b3b9de5f335f3f28f12a865375e928c442b612`  
		Last Modified: Mon, 15 Sep 2025 23:19:09 GMT  
		Size: 251.9 MB (251921200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e7f6c0540edca43a9e107463bf254ee9ad1819ca57f85dad64c7d5f309c53`  
		Last Modified: Mon, 15 Sep 2025 22:25:36 GMT  
		Size: 14.3 MB (14263259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577f0ca7a4bc915dd6079ef18d9069d9180fc6a375b1d6edaa9ea2c9d628009`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 481.0 KB (481002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67abdb79db3bf1c3a7e6c2a2fb49a48b28246a248b9a3d97626f529c5ca92aa7`  
		Last Modified: Mon, 15 Sep 2025 23:18:57 GMT  
		Size: 377.0 MB (377017654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe2a5c66e0124064c63db7cde0ba3adbb3880d19c419d6fff5170d0344fafc`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5944aecb9910fdbb71b75782f0a720981b8cede2a8d93da881fa5da07f6329`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154c5e98fd2beff959a7060f5a5aa8bcc130b83f1940248f8fee8147fd702e4`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2fcab419389ca83d6e574c1befad30960c3167cdec2d6359d1cb20dd78a538`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0670e14e3536ab98fd0f0e042f7d3338774420cd76ae3a7081d4734754767784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7820d294b3d8b1e91be0718f67c1a4aecd85d24c274e66af7eb60e7d0de4c`

```dockerfile
```

-	Layers:
	-	`sha256:089508277db87d67099852e5bfed50844018e797384772f8f56d3b4ef756e984`  
		Last Modified: Tue, 16 Sep 2025 01:14:07 GMT  
		Size: 60.9 MB (60870239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b77f9a3229e31804fd93c8728a1f0bfe02c40ca1e8276ade7caf9c1fbb0eb81`  
		Last Modified: Tue, 16 Sep 2025 01:14:09 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:04069748a4a9b264dde5afbc9855200660962b12f91543e28eb88e1cf08586f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692394989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23ab2e943a99c8b1b60345fe3d0beb5bfdfbaf9cf8f5a34475953d4b9bd796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdcfccf853b72753e393c1ae0e64cef5da7ad9163b690ad9cd8c01601482981`  
		Last Modified: Tue, 16 Sep 2025 00:14:45 GMT  
		Size: 377.7 MB (377719226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5025579c855d0ab62a68dad00aeb139f409dd5c86c7c194e6f57af10ad6c11`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db823d5ebd60d162a74661da39dfdd352131b9307fe6e98b14e30dc50973398`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ee91d77dd9e47b975b4a81fdea63838e8f543e8e113f7bdaf28c2e71481be0`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e62edc1567fd4903b7efd08419e461620e7f04e7736620db7fc42fa40d04793`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e0cb8f145809f34c3b68783cbbf02e6725ed5c6f494fdb5a144ab1e4129e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c516082378adf0094c322b17dc804d2c20e2e00c3f0262507d6f9f955b85c8c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca8913c9c4656a40d73648afd48de6a981c41aa9612fe3f459db269316275e2e`  
		Last Modified: Tue, 16 Sep 2025 01:15:43 GMT  
		Size: 60.9 MB (60871341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850ee6733d67e6909bfe0d79151333d25c62d4516c7f823274dc8c05e74e6e11`  
		Last Modified: Tue, 16 Sep 2025 01:15:44 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:624d493b541d0d919b33c857196827df93a928d2652c5a196fa2601a1286f1a1
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
$ docker pull odoo@sha256:217142296443977e50965e267e273e017a0d3f198c6e31b15f8f1821de4d78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676213267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d28b6ba718f921cfe92dd322ef8724da1e9e6dc3bdb2cf5b7389f913d3a2de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c29165224085f25ffd560cc3971a90d61cf7968a905d7e54fdf1f3843f51`  
		Last Modified: Mon, 15 Sep 2025 23:20:32 GMT  
		Size: 254.5 MB (254528712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65342fcb7a292e5215f4ed5901d7e32801f09ad4976100446df11023a06863bf`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 14.3 MB (14286402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f18de9da6584b0f56f7f6bed55ba6a802d9333fab55adb526fb0a0db30cfb4`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9b99696abd94f9c906a667d34d69f0c077b5de97451dfd20e8667b481bfa5a`  
		Last Modified: Mon, 15 Sep 2025 23:19:57 GMT  
		Size: 377.2 MB (377191302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7efb479f44f6154d1360e28fff72c0709f1cf8d80e4f11b3a9194d84b33a68`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f82a8644a9bea5be3a71f286ddf4b8b62c6f2940d88647c03f16e783a81154`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31f8e2949800fa043602d3fd003ed73d04b7af25710ec736411d8c9d9563dd`  
		Last Modified: Mon, 15 Sep 2025 22:25:39 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4182630c6d44de1fb500f5c59fd17d73d881d318fe94f9cde19616287c120`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:20bc410a2a431e9a15b9aae383a2d56ec79381ea8ada5056540e9ac64f2133ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda5e519749c6d03090787ae247b38153ab96195b90cb65ac2221cac9fa8b560`

```dockerfile
```

-	Layers:
	-	`sha256:d3bdc1d2a732a112070613fd179a0487aca7fa1ee272e790d91412f865aa6a4d`  
		Last Modified: Tue, 16 Sep 2025 01:12:38 GMT  
		Size: 60.9 MB (60862952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee77b4e9ae0374124e1b760486b3cae53967fd944862f9e356a794657391563`  
		Last Modified: Tue, 16 Sep 2025 01:12:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bad7d239b8c8eaaed045478246b21d54d55e613067b6722f8703d33615e9ffcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672546869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1052baf2c85d54329532084ca5fa6609cfdba9ed0863cea3dde90a37b7f78d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e7817fae6f931bd30374ad2b3b9de5f335f3f28f12a865375e928c442b612`  
		Last Modified: Mon, 15 Sep 2025 23:19:09 GMT  
		Size: 251.9 MB (251921200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e7f6c0540edca43a9e107463bf254ee9ad1819ca57f85dad64c7d5f309c53`  
		Last Modified: Mon, 15 Sep 2025 22:25:36 GMT  
		Size: 14.3 MB (14263259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577f0ca7a4bc915dd6079ef18d9069d9180fc6a375b1d6edaa9ea2c9d628009`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 481.0 KB (481002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67abdb79db3bf1c3a7e6c2a2fb49a48b28246a248b9a3d97626f529c5ca92aa7`  
		Last Modified: Mon, 15 Sep 2025 23:18:57 GMT  
		Size: 377.0 MB (377017654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe2a5c66e0124064c63db7cde0ba3adbb3880d19c419d6fff5170d0344fafc`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5944aecb9910fdbb71b75782f0a720981b8cede2a8d93da881fa5da07f6329`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154c5e98fd2beff959a7060f5a5aa8bcc130b83f1940248f8fee8147fd702e4`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2fcab419389ca83d6e574c1befad30960c3167cdec2d6359d1cb20dd78a538`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0670e14e3536ab98fd0f0e042f7d3338774420cd76ae3a7081d4734754767784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7820d294b3d8b1e91be0718f67c1a4aecd85d24c274e66af7eb60e7d0de4c`

```dockerfile
```

-	Layers:
	-	`sha256:089508277db87d67099852e5bfed50844018e797384772f8f56d3b4ef756e984`  
		Last Modified: Tue, 16 Sep 2025 01:14:07 GMT  
		Size: 60.9 MB (60870239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b77f9a3229e31804fd93c8728a1f0bfe02c40ca1e8276ade7caf9c1fbb0eb81`  
		Last Modified: Tue, 16 Sep 2025 01:14:09 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:04069748a4a9b264dde5afbc9855200660962b12f91543e28eb88e1cf08586f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692394989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23ab2e943a99c8b1b60345fe3d0beb5bfdfbaf9cf8f5a34475953d4b9bd796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdcfccf853b72753e393c1ae0e64cef5da7ad9163b690ad9cd8c01601482981`  
		Last Modified: Tue, 16 Sep 2025 00:14:45 GMT  
		Size: 377.7 MB (377719226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5025579c855d0ab62a68dad00aeb139f409dd5c86c7c194e6f57af10ad6c11`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db823d5ebd60d162a74661da39dfdd352131b9307fe6e98b14e30dc50973398`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ee91d77dd9e47b975b4a81fdea63838e8f543e8e113f7bdaf28c2e71481be0`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e62edc1567fd4903b7efd08419e461620e7f04e7736620db7fc42fa40d04793`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e0cb8f145809f34c3b68783cbbf02e6725ed5c6f494fdb5a144ab1e4129e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c516082378adf0094c322b17dc804d2c20e2e00c3f0262507d6f9f955b85c8c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca8913c9c4656a40d73648afd48de6a981c41aa9612fe3f459db269316275e2e`  
		Last Modified: Tue, 16 Sep 2025 01:15:43 GMT  
		Size: 60.9 MB (60871341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850ee6733d67e6909bfe0d79151333d25c62d4516c7f823274dc8c05e74e6e11`  
		Last Modified: Tue, 16 Sep 2025 01:15:44 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250909`

```console
$ docker pull odoo@sha256:624d493b541d0d919b33c857196827df93a928d2652c5a196fa2601a1286f1a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250909` - linux; amd64

```console
$ docker pull odoo@sha256:217142296443977e50965e267e273e017a0d3f198c6e31b15f8f1821de4d78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676213267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d28b6ba718f921cfe92dd322ef8724da1e9e6dc3bdb2cf5b7389f913d3a2de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c29165224085f25ffd560cc3971a90d61cf7968a905d7e54fdf1f3843f51`  
		Last Modified: Mon, 15 Sep 2025 23:20:32 GMT  
		Size: 254.5 MB (254528712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65342fcb7a292e5215f4ed5901d7e32801f09ad4976100446df11023a06863bf`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 14.3 MB (14286402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f18de9da6584b0f56f7f6bed55ba6a802d9333fab55adb526fb0a0db30cfb4`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9b99696abd94f9c906a667d34d69f0c077b5de97451dfd20e8667b481bfa5a`  
		Last Modified: Mon, 15 Sep 2025 23:19:57 GMT  
		Size: 377.2 MB (377191302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7efb479f44f6154d1360e28fff72c0709f1cf8d80e4f11b3a9194d84b33a68`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f82a8644a9bea5be3a71f286ddf4b8b62c6f2940d88647c03f16e783a81154`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31f8e2949800fa043602d3fd003ed73d04b7af25710ec736411d8c9d9563dd`  
		Last Modified: Mon, 15 Sep 2025 22:25:39 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4182630c6d44de1fb500f5c59fd17d73d881d318fe94f9cde19616287c120`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:20bc410a2a431e9a15b9aae383a2d56ec79381ea8ada5056540e9ac64f2133ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda5e519749c6d03090787ae247b38153ab96195b90cb65ac2221cac9fa8b560`

```dockerfile
```

-	Layers:
	-	`sha256:d3bdc1d2a732a112070613fd179a0487aca7fa1ee272e790d91412f865aa6a4d`  
		Last Modified: Tue, 16 Sep 2025 01:12:38 GMT  
		Size: 60.9 MB (60862952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee77b4e9ae0374124e1b760486b3cae53967fd944862f9e356a794657391563`  
		Last Modified: Tue, 16 Sep 2025 01:12:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250909` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bad7d239b8c8eaaed045478246b21d54d55e613067b6722f8703d33615e9ffcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672546869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1052baf2c85d54329532084ca5fa6609cfdba9ed0863cea3dde90a37b7f78d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e7817fae6f931bd30374ad2b3b9de5f335f3f28f12a865375e928c442b612`  
		Last Modified: Mon, 15 Sep 2025 23:19:09 GMT  
		Size: 251.9 MB (251921200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e7f6c0540edca43a9e107463bf254ee9ad1819ca57f85dad64c7d5f309c53`  
		Last Modified: Mon, 15 Sep 2025 22:25:36 GMT  
		Size: 14.3 MB (14263259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577f0ca7a4bc915dd6079ef18d9069d9180fc6a375b1d6edaa9ea2c9d628009`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 481.0 KB (481002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67abdb79db3bf1c3a7e6c2a2fb49a48b28246a248b9a3d97626f529c5ca92aa7`  
		Last Modified: Mon, 15 Sep 2025 23:18:57 GMT  
		Size: 377.0 MB (377017654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe2a5c66e0124064c63db7cde0ba3adbb3880d19c419d6fff5170d0344fafc`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5944aecb9910fdbb71b75782f0a720981b8cede2a8d93da881fa5da07f6329`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154c5e98fd2beff959a7060f5a5aa8bcc130b83f1940248f8fee8147fd702e4`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2fcab419389ca83d6e574c1befad30960c3167cdec2d6359d1cb20dd78a538`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:0670e14e3536ab98fd0f0e042f7d3338774420cd76ae3a7081d4734754767784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7820d294b3d8b1e91be0718f67c1a4aecd85d24c274e66af7eb60e7d0de4c`

```dockerfile
```

-	Layers:
	-	`sha256:089508277db87d67099852e5bfed50844018e797384772f8f56d3b4ef756e984`  
		Last Modified: Tue, 16 Sep 2025 01:14:07 GMT  
		Size: 60.9 MB (60870239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b77f9a3229e31804fd93c8728a1f0bfe02c40ca1e8276ade7caf9c1fbb0eb81`  
		Last Modified: Tue, 16 Sep 2025 01:14:09 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250909` - linux; ppc64le

```console
$ docker pull odoo@sha256:04069748a4a9b264dde5afbc9855200660962b12f91543e28eb88e1cf08586f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692394989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23ab2e943a99c8b1b60345fe3d0beb5bfdfbaf9cf8f5a34475953d4b9bd796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdcfccf853b72753e393c1ae0e64cef5da7ad9163b690ad9cd8c01601482981`  
		Last Modified: Tue, 16 Sep 2025 00:14:45 GMT  
		Size: 377.7 MB (377719226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5025579c855d0ab62a68dad00aeb139f409dd5c86c7c194e6f57af10ad6c11`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db823d5ebd60d162a74661da39dfdd352131b9307fe6e98b14e30dc50973398`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ee91d77dd9e47b975b4a81fdea63838e8f543e8e113f7bdaf28c2e71481be0`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e62edc1567fd4903b7efd08419e461620e7f04e7736620db7fc42fa40d04793`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e0cb8f145809f34c3b68783cbbf02e6725ed5c6f494fdb5a144ab1e4129e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c516082378adf0094c322b17dc804d2c20e2e00c3f0262507d6f9f955b85c8c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca8913c9c4656a40d73648afd48de6a981c41aa9612fe3f459db269316275e2e`  
		Last Modified: Tue, 16 Sep 2025 01:15:43 GMT  
		Size: 60.9 MB (60871341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850ee6733d67e6909bfe0d79151333d25c62d4516c7f823274dc8c05e74e6e11`  
		Last Modified: Tue, 16 Sep 2025 01:15:44 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:624d493b541d0d919b33c857196827df93a928d2652c5a196fa2601a1286f1a1
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
$ docker pull odoo@sha256:217142296443977e50965e267e273e017a0d3f198c6e31b15f8f1821de4d78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676213267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d28b6ba718f921cfe92dd322ef8724da1e9e6dc3bdb2cf5b7389f913d3a2de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c29165224085f25ffd560cc3971a90d61cf7968a905d7e54fdf1f3843f51`  
		Last Modified: Mon, 15 Sep 2025 23:20:32 GMT  
		Size: 254.5 MB (254528712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65342fcb7a292e5215f4ed5901d7e32801f09ad4976100446df11023a06863bf`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 14.3 MB (14286402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f18de9da6584b0f56f7f6bed55ba6a802d9333fab55adb526fb0a0db30cfb4`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9b99696abd94f9c906a667d34d69f0c077b5de97451dfd20e8667b481bfa5a`  
		Last Modified: Mon, 15 Sep 2025 23:19:57 GMT  
		Size: 377.2 MB (377191302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7efb479f44f6154d1360e28fff72c0709f1cf8d80e4f11b3a9194d84b33a68`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f82a8644a9bea5be3a71f286ddf4b8b62c6f2940d88647c03f16e783a81154`  
		Last Modified: Mon, 15 Sep 2025 22:25:37 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31f8e2949800fa043602d3fd003ed73d04b7af25710ec736411d8c9d9563dd`  
		Last Modified: Mon, 15 Sep 2025 22:25:39 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4182630c6d44de1fb500f5c59fd17d73d881d318fe94f9cde19616287c120`  
		Last Modified: Mon, 15 Sep 2025 22:25:38 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:20bc410a2a431e9a15b9aae383a2d56ec79381ea8ada5056540e9ac64f2133ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda5e519749c6d03090787ae247b38153ab96195b90cb65ac2221cac9fa8b560`

```dockerfile
```

-	Layers:
	-	`sha256:d3bdc1d2a732a112070613fd179a0487aca7fa1ee272e790d91412f865aa6a4d`  
		Last Modified: Tue, 16 Sep 2025 01:12:38 GMT  
		Size: 60.9 MB (60862952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee77b4e9ae0374124e1b760486b3cae53967fd944862f9e356a794657391563`  
		Last Modified: Tue, 16 Sep 2025 01:12:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bad7d239b8c8eaaed045478246b21d54d55e613067b6722f8703d33615e9ffcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672546869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1052baf2c85d54329532084ca5fa6609cfdba9ed0863cea3dde90a37b7f78d0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=arm64
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e7817fae6f931bd30374ad2b3b9de5f335f3f28f12a865375e928c442b612`  
		Last Modified: Mon, 15 Sep 2025 23:19:09 GMT  
		Size: 251.9 MB (251921200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e7f6c0540edca43a9e107463bf254ee9ad1819ca57f85dad64c7d5f309c53`  
		Last Modified: Mon, 15 Sep 2025 22:25:36 GMT  
		Size: 14.3 MB (14263259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0577f0ca7a4bc915dd6079ef18d9069d9180fc6a375b1d6edaa9ea2c9d628009`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 481.0 KB (481002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67abdb79db3bf1c3a7e6c2a2fb49a48b28246a248b9a3d97626f529c5ca92aa7`  
		Last Modified: Mon, 15 Sep 2025 23:18:57 GMT  
		Size: 377.0 MB (377017654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe2a5c66e0124064c63db7cde0ba3adbb3880d19c419d6fff5170d0344fafc`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5944aecb9910fdbb71b75782f0a720981b8cede2a8d93da881fa5da07f6329`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f154c5e98fd2beff959a7060f5a5aa8bcc130b83f1940248f8fee8147fd702e4`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2fcab419389ca83d6e574c1befad30960c3167cdec2d6359d1cb20dd78a538`  
		Last Modified: Mon, 15 Sep 2025 22:25:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:0670e14e3536ab98fd0f0e042f7d3338774420cd76ae3a7081d4734754767784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c7820d294b3d8b1e91be0718f67c1a4aecd85d24c274e66af7eb60e7d0de4c`

```dockerfile
```

-	Layers:
	-	`sha256:089508277db87d67099852e5bfed50844018e797384772f8f56d3b4ef756e984`  
		Last Modified: Tue, 16 Sep 2025 01:14:07 GMT  
		Size: 60.9 MB (60870239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b77f9a3229e31804fd93c8728a1f0bfe02c40ca1e8276ade7caf9c1fbb0eb81`  
		Last Modified: Tue, 16 Sep 2025 01:14:09 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:04069748a4a9b264dde5afbc9855200660962b12f91543e28eb88e1cf08586f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692394989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23ab2e943a99c8b1b60345fe3d0beb5bfdfbaf9cf8f5a34475953d4b9bd796`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Sep 2025 13:16:03 GMT
ARG RELEASE
# Tue, 09 Sep 2025 13:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Sep 2025 13:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 09 Sep 2025 13:16:03 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Sep 2025 13:16:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Sep 2025 13:16:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Sep 2025 13:16:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_RELEASE=20250909
# Tue, 09 Sep 2025 13:16:03 GMT
ARG ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250909 ODOO_SHA=3bdf96c966b7b0434b6358e07e7027e3d9b6d92f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Sep 2025 13:16:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Sep 2025 13:16:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Sep 2025 13:16:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Sep 2025 13:16:03 GMT
USER odoo
# Tue, 09 Sep 2025 13:16:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 13:16:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdcfccf853b72753e393c1ae0e64cef5da7ad9163b690ad9cd8c01601482981`  
		Last Modified: Tue, 16 Sep 2025 00:14:45 GMT  
		Size: 377.7 MB (377719226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5025579c855d0ab62a68dad00aeb139f409dd5c86c7c194e6f57af10ad6c11`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db823d5ebd60d162a74661da39dfdd352131b9307fe6e98b14e30dc50973398`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ee91d77dd9e47b975b4a81fdea63838e8f543e8e113f7bdaf28c2e71481be0`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e62edc1567fd4903b7efd08419e461620e7f04e7736620db7fc42fa40d04793`  
		Last Modified: Mon, 15 Sep 2025 23:52:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c2e0cb8f145809f34c3b68783cbbf02e6725ed5c6f494fdb5a144ab1e4129e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c516082378adf0094c322b17dc804d2c20e2e00c3f0262507d6f9f955b85c8c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca8913c9c4656a40d73648afd48de6a981c41aa9612fe3f459db269316275e2e`  
		Last Modified: Tue, 16 Sep 2025 01:15:43 GMT  
		Size: 60.9 MB (60871341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850ee6733d67e6909bfe0d79151333d25c62d4516c7f823274dc8c05e74e6e11`  
		Last Modified: Tue, 16 Sep 2025 01:15:44 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
