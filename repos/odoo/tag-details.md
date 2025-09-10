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
$ docker pull odoo@sha256:80d2b5ae7b4cdccbc5ecf8c6e229b8e25c79b078cf068128f41bc7309ad363c5
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
$ docker pull odoo@sha256:0726912fb97fd080a36429c0c32859e4c07aedcb4be13693c0d1d8b14d6e383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676215234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d699fd8d15abd5eb5cd963ec7bd0c29e4d9264521c6aee07027c652e6fffe577`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15abf9ac2e90cdd6fc0d23656800d40baa9e957fc8b8d783c8e3e23685e54ad8`  
		Last Modified: Wed, 10 Sep 2025 00:07:50 GMT  
		Size: 254.5 MB (254531491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a64b4bd3c8d43a8d314a3681a52e84934c0f98bbed45e11769bd4a70b1961`  
		Last Modified: Tue, 09 Sep 2025 23:46:58 GMT  
		Size: 14.3 MB (14286079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f771c7423af66dd7bc88b506556fdba16526d8bf83b461a4184a35710681d40e`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 481.0 KB (481034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3775d79bd23b3a1dc543d1f00123ca372733422f2d9e472c57b153d22a0d68f`  
		Last Modified: Wed, 10 Sep 2025 00:08:01 GMT  
		Size: 377.2 MB (377191128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c2f973a14998ff6aba4fac741a1187f9af679a194d3ab0fb5189970d20fc1c`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ece3bc429b4f07b65d0e69b466f7dbdbb81b2ea9cfd840849ddf58ab689059`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d0f254e22664b40a9f99040e50adb1eed16f720fd5f184a4ce35275059ddd`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10865c54339d59aebecbbb4f57ce5e08e1e723b66dea51def5ead59b2f7f69d`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:cd21ad1ee50317294ab14bca47560b04abcb55de37035e3f7e75318b9c26ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ce9974768f29e271c15ddbd6513a3f96cf0ec38c4f03d0e9dc29f554596f1b`

```dockerfile
```

-	Layers:
	-	`sha256:ba11fb293c9aa8265a98fe2054ee4a623249b26b559b15a1fd0fc9edaa6536f5`  
		Last Modified: Wed, 10 Sep 2025 01:13:00 GMT  
		Size: 60.9 MB (60862948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc5c21acb458bd4459c3c1d34a4717555e5638d1f54ec005604f7fd043376a0`  
		Last Modified: Wed, 10 Sep 2025 01:13:02 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5822470459b19e7a6f960f86c4086becaa54f902f6ba59808d7ad406bae5fd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672549955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674a000a110da502630255d2c854dcffd760e389110e73c4069891ad2403154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e470e8ba0c90cdcc3f8cc8d05f41ddad14d8764785917260aec32fec42760b`  
		Last Modified: Wed, 10 Sep 2025 00:08:07 GMT  
		Size: 251.9 MB (251920834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb892a24fc191b674df19cc7c4078bb96b2f8730678c1d71627d1ffd16dd19`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 14.3 MB (14263163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89089c77029aef967ca0482c24ed5a1c56cba191f604f0c633015b5905307e5c`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 481.0 KB (480977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf7f185d5da878f4cc6ca467bf600115dc6b1d355ffea1851afa3aaaa5d3b27`  
		Last Modified: Wed, 10 Sep 2025 00:08:28 GMT  
		Size: 377.0 MB (377022301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2b71a6a09bb3837ba4ca9087520e3e714ad947956a9c21b52e9cf1f784203`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c91c438aef96f62c777cd031eb1523086efe0541c88d74224d2ec6194cc52d`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887d724d85aa3a4ae8b61150efacbb89f74631c4c5e45cde5296b5054014ffe7`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632167b4e024dbb2cc3e40339216d8687e72bb699d5315591f0131ae7897a8fb`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:bfe60d33b68036699688aa98ca9bce4e712fa3410f90645178a5af8c86832d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1ee769604e75ce73c239cf4e3327e74cde58cce61fcf5de14561e3ae1f62b9`

```dockerfile
```

-	Layers:
	-	`sha256:28f2c88bb9a83ff28ab5d86402d279f33bef4ade4ff99e3bd62628524a9a1147`  
		Last Modified: Wed, 10 Sep 2025 01:14:47 GMT  
		Size: 60.9 MB (60870235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c01e7a369c0a57b922b7f5edf2c5390bf1f5ebe6064404b682b88997c1b63a13`  
		Last Modified: Wed, 10 Sep 2025 01:14:48 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d03a04d63e5d1ce58ab138683ee5ceae42c58c42e53c1715cbb9f5c01712670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692426085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdf547430466f5b7d27ef351705e84bdc244efb154180ebf508839dff44f1cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:40:27 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:40:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:40:31 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 14:40:31 GMT
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a6c04d444e89339a4249db2817e2f4b1a9a211390699c987bccd444b3674e`  
		Last Modified: Wed, 10 Sep 2025 12:07:49 GMT  
		Size: 377.7 MB (377724547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed9e393f8e9428ec48e9b0f2b0c05d582ff10144869cd6b54c7f13c0a8c739c`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff8a56b553a8644e1340a053a2aa64a63a19fdf9399e9571bf36198cd062d3`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3892aa05e19b05c9db67cbf4a07da8f2bdde50b02c18fcb3b8cc7b863c5bfc2d`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9cdaf2b3e84404fe15fac805498bb5a72d6c0ac92c30197fb6982e353227b`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:09c39ca3dc4c9d3f81b4006903eff2226eb114a0ed9c9ec8f06475bc10a501fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6f403af48ac4fa76535762c7e13a50e7e4776c73b181eb64039d62681cd5a1`

```dockerfile
```

-	Layers:
	-	`sha256:21cfe9ae7077240303cf5c69debf923f8ab7ebee21bae51fbc5fae1edf9b883d`  
		Last Modified: Wed, 10 Sep 2025 13:15:58 GMT  
		Size: 60.9 MB (60871337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbf59a4fca7d0450e2254c2f9ad55ac96b92c4b9a1a26e85c5eb963ffe97d01`  
		Last Modified: Wed, 10 Sep 2025 13:16:00 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:80d2b5ae7b4cdccbc5ecf8c6e229b8e25c79b078cf068128f41bc7309ad363c5
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
$ docker pull odoo@sha256:0726912fb97fd080a36429c0c32859e4c07aedcb4be13693c0d1d8b14d6e383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676215234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d699fd8d15abd5eb5cd963ec7bd0c29e4d9264521c6aee07027c652e6fffe577`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15abf9ac2e90cdd6fc0d23656800d40baa9e957fc8b8d783c8e3e23685e54ad8`  
		Last Modified: Wed, 10 Sep 2025 00:07:50 GMT  
		Size: 254.5 MB (254531491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a64b4bd3c8d43a8d314a3681a52e84934c0f98bbed45e11769bd4a70b1961`  
		Last Modified: Tue, 09 Sep 2025 23:46:58 GMT  
		Size: 14.3 MB (14286079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f771c7423af66dd7bc88b506556fdba16526d8bf83b461a4184a35710681d40e`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 481.0 KB (481034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3775d79bd23b3a1dc543d1f00123ca372733422f2d9e472c57b153d22a0d68f`  
		Last Modified: Wed, 10 Sep 2025 00:08:01 GMT  
		Size: 377.2 MB (377191128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c2f973a14998ff6aba4fac741a1187f9af679a194d3ab0fb5189970d20fc1c`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ece3bc429b4f07b65d0e69b466f7dbdbb81b2ea9cfd840849ddf58ab689059`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d0f254e22664b40a9f99040e50adb1eed16f720fd5f184a4ce35275059ddd`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10865c54339d59aebecbbb4f57ce5e08e1e723b66dea51def5ead59b2f7f69d`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cd21ad1ee50317294ab14bca47560b04abcb55de37035e3f7e75318b9c26ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ce9974768f29e271c15ddbd6513a3f96cf0ec38c4f03d0e9dc29f554596f1b`

```dockerfile
```

-	Layers:
	-	`sha256:ba11fb293c9aa8265a98fe2054ee4a623249b26b559b15a1fd0fc9edaa6536f5`  
		Last Modified: Wed, 10 Sep 2025 01:13:00 GMT  
		Size: 60.9 MB (60862948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc5c21acb458bd4459c3c1d34a4717555e5638d1f54ec005604f7fd043376a0`  
		Last Modified: Wed, 10 Sep 2025 01:13:02 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5822470459b19e7a6f960f86c4086becaa54f902f6ba59808d7ad406bae5fd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672549955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674a000a110da502630255d2c854dcffd760e389110e73c4069891ad2403154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e470e8ba0c90cdcc3f8cc8d05f41ddad14d8764785917260aec32fec42760b`  
		Last Modified: Wed, 10 Sep 2025 00:08:07 GMT  
		Size: 251.9 MB (251920834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb892a24fc191b674df19cc7c4078bb96b2f8730678c1d71627d1ffd16dd19`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 14.3 MB (14263163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89089c77029aef967ca0482c24ed5a1c56cba191f604f0c633015b5905307e5c`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 481.0 KB (480977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf7f185d5da878f4cc6ca467bf600115dc6b1d355ffea1851afa3aaaa5d3b27`  
		Last Modified: Wed, 10 Sep 2025 00:08:28 GMT  
		Size: 377.0 MB (377022301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2b71a6a09bb3837ba4ca9087520e3e714ad947956a9c21b52e9cf1f784203`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c91c438aef96f62c777cd031eb1523086efe0541c88d74224d2ec6194cc52d`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887d724d85aa3a4ae8b61150efacbb89f74631c4c5e45cde5296b5054014ffe7`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632167b4e024dbb2cc3e40339216d8687e72bb699d5315591f0131ae7897a8fb`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:bfe60d33b68036699688aa98ca9bce4e712fa3410f90645178a5af8c86832d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1ee769604e75ce73c239cf4e3327e74cde58cce61fcf5de14561e3ae1f62b9`

```dockerfile
```

-	Layers:
	-	`sha256:28f2c88bb9a83ff28ab5d86402d279f33bef4ade4ff99e3bd62628524a9a1147`  
		Last Modified: Wed, 10 Sep 2025 01:14:47 GMT  
		Size: 60.9 MB (60870235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c01e7a369c0a57b922b7f5edf2c5390bf1f5ebe6064404b682b88997c1b63a13`  
		Last Modified: Wed, 10 Sep 2025 01:14:48 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d03a04d63e5d1ce58ab138683ee5ceae42c58c42e53c1715cbb9f5c01712670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692426085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdf547430466f5b7d27ef351705e84bdc244efb154180ebf508839dff44f1cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:40:27 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:40:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:40:31 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 14:40:31 GMT
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a6c04d444e89339a4249db2817e2f4b1a9a211390699c987bccd444b3674e`  
		Last Modified: Wed, 10 Sep 2025 12:07:49 GMT  
		Size: 377.7 MB (377724547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed9e393f8e9428ec48e9b0f2b0c05d582ff10144869cd6b54c7f13c0a8c739c`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff8a56b553a8644e1340a053a2aa64a63a19fdf9399e9571bf36198cd062d3`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3892aa05e19b05c9db67cbf4a07da8f2bdde50b02c18fcb3b8cc7b863c5bfc2d`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9cdaf2b3e84404fe15fac805498bb5a72d6c0ac92c30197fb6982e353227b`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:09c39ca3dc4c9d3f81b4006903eff2226eb114a0ed9c9ec8f06475bc10a501fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6f403af48ac4fa76535762c7e13a50e7e4776c73b181eb64039d62681cd5a1`

```dockerfile
```

-	Layers:
	-	`sha256:21cfe9ae7077240303cf5c69debf923f8ab7ebee21bae51fbc5fae1edf9b883d`  
		Last Modified: Wed, 10 Sep 2025 13:15:58 GMT  
		Size: 60.9 MB (60871337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbf59a4fca7d0450e2254c2f9ad55ac96b92c4b9a1a26e85c5eb963ffe97d01`  
		Last Modified: Wed, 10 Sep 2025 13:16:00 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250909`

```console
$ docker pull odoo@sha256:80d2b5ae7b4cdccbc5ecf8c6e229b8e25c79b078cf068128f41bc7309ad363c5
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
$ docker pull odoo@sha256:0726912fb97fd080a36429c0c32859e4c07aedcb4be13693c0d1d8b14d6e383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676215234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d699fd8d15abd5eb5cd963ec7bd0c29e4d9264521c6aee07027c652e6fffe577`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15abf9ac2e90cdd6fc0d23656800d40baa9e957fc8b8d783c8e3e23685e54ad8`  
		Last Modified: Wed, 10 Sep 2025 00:07:50 GMT  
		Size: 254.5 MB (254531491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a64b4bd3c8d43a8d314a3681a52e84934c0f98bbed45e11769bd4a70b1961`  
		Last Modified: Tue, 09 Sep 2025 23:46:58 GMT  
		Size: 14.3 MB (14286079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f771c7423af66dd7bc88b506556fdba16526d8bf83b461a4184a35710681d40e`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 481.0 KB (481034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3775d79bd23b3a1dc543d1f00123ca372733422f2d9e472c57b153d22a0d68f`  
		Last Modified: Wed, 10 Sep 2025 00:08:01 GMT  
		Size: 377.2 MB (377191128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c2f973a14998ff6aba4fac741a1187f9af679a194d3ab0fb5189970d20fc1c`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ece3bc429b4f07b65d0e69b466f7dbdbb81b2ea9cfd840849ddf58ab689059`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d0f254e22664b40a9f99040e50adb1eed16f720fd5f184a4ce35275059ddd`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10865c54339d59aebecbbb4f57ce5e08e1e723b66dea51def5ead59b2f7f69d`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:cd21ad1ee50317294ab14bca47560b04abcb55de37035e3f7e75318b9c26ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ce9974768f29e271c15ddbd6513a3f96cf0ec38c4f03d0e9dc29f554596f1b`

```dockerfile
```

-	Layers:
	-	`sha256:ba11fb293c9aa8265a98fe2054ee4a623249b26b559b15a1fd0fc9edaa6536f5`  
		Last Modified: Wed, 10 Sep 2025 01:13:00 GMT  
		Size: 60.9 MB (60862948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc5c21acb458bd4459c3c1d34a4717555e5638d1f54ec005604f7fd043376a0`  
		Last Modified: Wed, 10 Sep 2025 01:13:02 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250909` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5822470459b19e7a6f960f86c4086becaa54f902f6ba59808d7ad406bae5fd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672549955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674a000a110da502630255d2c854dcffd760e389110e73c4069891ad2403154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e470e8ba0c90cdcc3f8cc8d05f41ddad14d8764785917260aec32fec42760b`  
		Last Modified: Wed, 10 Sep 2025 00:08:07 GMT  
		Size: 251.9 MB (251920834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb892a24fc191b674df19cc7c4078bb96b2f8730678c1d71627d1ffd16dd19`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 14.3 MB (14263163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89089c77029aef967ca0482c24ed5a1c56cba191f604f0c633015b5905307e5c`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 481.0 KB (480977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf7f185d5da878f4cc6ca467bf600115dc6b1d355ffea1851afa3aaaa5d3b27`  
		Last Modified: Wed, 10 Sep 2025 00:08:28 GMT  
		Size: 377.0 MB (377022301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2b71a6a09bb3837ba4ca9087520e3e714ad947956a9c21b52e9cf1f784203`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c91c438aef96f62c777cd031eb1523086efe0541c88d74224d2ec6194cc52d`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887d724d85aa3a4ae8b61150efacbb89f74631c4c5e45cde5296b5054014ffe7`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632167b4e024dbb2cc3e40339216d8687e72bb699d5315591f0131ae7897a8fb`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:bfe60d33b68036699688aa98ca9bce4e712fa3410f90645178a5af8c86832d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1ee769604e75ce73c239cf4e3327e74cde58cce61fcf5de14561e3ae1f62b9`

```dockerfile
```

-	Layers:
	-	`sha256:28f2c88bb9a83ff28ab5d86402d279f33bef4ade4ff99e3bd62628524a9a1147`  
		Last Modified: Wed, 10 Sep 2025 01:14:47 GMT  
		Size: 60.9 MB (60870235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c01e7a369c0a57b922b7f5edf2c5390bf1f5ebe6064404b682b88997c1b63a13`  
		Last Modified: Wed, 10 Sep 2025 01:14:48 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250909` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d03a04d63e5d1ce58ab138683ee5ceae42c58c42e53c1715cbb9f5c01712670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692426085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdf547430466f5b7d27ef351705e84bdc244efb154180ebf508839dff44f1cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:40:27 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:40:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:40:31 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 14:40:31 GMT
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a6c04d444e89339a4249db2817e2f4b1a9a211390699c987bccd444b3674e`  
		Last Modified: Wed, 10 Sep 2025 12:07:49 GMT  
		Size: 377.7 MB (377724547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed9e393f8e9428ec48e9b0f2b0c05d582ff10144869cd6b54c7f13c0a8c739c`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff8a56b553a8644e1340a053a2aa64a63a19fdf9399e9571bf36198cd062d3`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3892aa05e19b05c9db67cbf4a07da8f2bdde50b02c18fcb3b8cc7b863c5bfc2d`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9cdaf2b3e84404fe15fac805498bb5a72d6c0ac92c30197fb6982e353227b`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250909` - unknown; unknown

```console
$ docker pull odoo@sha256:09c39ca3dc4c9d3f81b4006903eff2226eb114a0ed9c9ec8f06475bc10a501fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6f403af48ac4fa76535762c7e13a50e7e4776c73b181eb64039d62681cd5a1`

```dockerfile
```

-	Layers:
	-	`sha256:21cfe9ae7077240303cf5c69debf923f8ab7ebee21bae51fbc5fae1edf9b883d`  
		Last Modified: Wed, 10 Sep 2025 13:15:58 GMT  
		Size: 60.9 MB (60871337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbf59a4fca7d0450e2254c2f9ad55ac96b92c4b9a1a26e85c5eb963ffe97d01`  
		Last Modified: Wed, 10 Sep 2025 13:16:00 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:80d2b5ae7b4cdccbc5ecf8c6e229b8e25c79b078cf068128f41bc7309ad363c5
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
$ docker pull odoo@sha256:0726912fb97fd080a36429c0c32859e4c07aedcb4be13693c0d1d8b14d6e383f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.2 MB (676215234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d699fd8d15abd5eb5cd963ec7bd0c29e4d9264521c6aee07027c652e6fffe577`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15abf9ac2e90cdd6fc0d23656800d40baa9e957fc8b8d783c8e3e23685e54ad8`  
		Last Modified: Wed, 10 Sep 2025 00:07:50 GMT  
		Size: 254.5 MB (254531491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949a64b4bd3c8d43a8d314a3681a52e84934c0f98bbed45e11769bd4a70b1961`  
		Last Modified: Tue, 09 Sep 2025 23:46:58 GMT  
		Size: 14.3 MB (14286079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f771c7423af66dd7bc88b506556fdba16526d8bf83b461a4184a35710681d40e`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 481.0 KB (481034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3775d79bd23b3a1dc543d1f00123ca372733422f2d9e472c57b153d22a0d68f`  
		Last Modified: Wed, 10 Sep 2025 00:08:01 GMT  
		Size: 377.2 MB (377191128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c2f973a14998ff6aba4fac741a1187f9af679a194d3ab0fb5189970d20fc1c`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ece3bc429b4f07b65d0e69b466f7dbdbb81b2ea9cfd840849ddf58ab689059`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d0f254e22664b40a9f99040e50adb1eed16f720fd5f184a4ce35275059ddd`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10865c54339d59aebecbbb4f57ce5e08e1e723b66dea51def5ead59b2f7f69d`  
		Last Modified: Tue, 09 Sep 2025 23:46:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cd21ad1ee50317294ab14bca47560b04abcb55de37035e3f7e75318b9c26ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60890084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ce9974768f29e271c15ddbd6513a3f96cf0ec38c4f03d0e9dc29f554596f1b`

```dockerfile
```

-	Layers:
	-	`sha256:ba11fb293c9aa8265a98fe2054ee4a623249b26b559b15a1fd0fc9edaa6536f5`  
		Last Modified: Wed, 10 Sep 2025 01:13:00 GMT  
		Size: 60.9 MB (60862948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc5c21acb458bd4459c3c1d34a4717555e5638d1f54ec005604f7fd043376a0`  
		Last Modified: Wed, 10 Sep 2025 01:13:02 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5822470459b19e7a6f960f86c4086becaa54f902f6ba59808d7ad406bae5fd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.5 MB (672549955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1674a000a110da502630255d2c854dcffd760e389110e73c4069891ad2403154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e470e8ba0c90cdcc3f8cc8d05f41ddad14d8764785917260aec32fec42760b`  
		Last Modified: Wed, 10 Sep 2025 00:08:07 GMT  
		Size: 251.9 MB (251920834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb892a24fc191b674df19cc7c4078bb96b2f8730678c1d71627d1ffd16dd19`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 14.3 MB (14263163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89089c77029aef967ca0482c24ed5a1c56cba191f604f0c633015b5905307e5c`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 481.0 KB (480977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf7f185d5da878f4cc6ca467bf600115dc6b1d355ffea1851afa3aaaa5d3b27`  
		Last Modified: Wed, 10 Sep 2025 00:08:28 GMT  
		Size: 377.0 MB (377022301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca2b71a6a09bb3837ba4ca9087520e3e714ad947956a9c21b52e9cf1f784203`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c91c438aef96f62c777cd031eb1523086efe0541c88d74224d2ec6194cc52d`  
		Last Modified: Tue, 09 Sep 2025 23:48:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887d724d85aa3a4ae8b61150efacbb89f74631c4c5e45cde5296b5054014ffe7`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632167b4e024dbb2cc3e40339216d8687e72bb699d5315591f0131ae7897a8fb`  
		Last Modified: Tue, 09 Sep 2025 23:48:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:bfe60d33b68036699688aa98ca9bce4e712fa3410f90645178a5af8c86832d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60897535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1ee769604e75ce73c239cf4e3327e74cde58cce61fcf5de14561e3ae1f62b9`

```dockerfile
```

-	Layers:
	-	`sha256:28f2c88bb9a83ff28ab5d86402d279f33bef4ade4ff99e3bd62628524a9a1147`  
		Last Modified: Wed, 10 Sep 2025 01:14:47 GMT  
		Size: 60.9 MB (60870235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c01e7a369c0a57b922b7f5edf2c5390bf1f5ebe6064404b682b88997c1b63a13`  
		Last Modified: Wed, 10 Sep 2025 01:14:48 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d03a04d63e5d1ce58ab138683ee5ceae42c58c42e53c1715cbb9f5c01712670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.4 MB (692426085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdf547430466f5b7d27ef351705e84bdc244efb154180ebf508839dff44f1cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 14:40:27 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:40:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:40:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:40:31 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 14:40:31 GMT
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
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a6c04d444e89339a4249db2817e2f4b1a9a211390699c987bccd444b3674e`  
		Last Modified: Wed, 10 Sep 2025 12:07:49 GMT  
		Size: 377.7 MB (377724547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed9e393f8e9428ec48e9b0f2b0c05d582ff10144869cd6b54c7f13c0a8c739c`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff8a56b553a8644e1340a053a2aa64a63a19fdf9399e9571bf36198cd062d3`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3892aa05e19b05c9db67cbf4a07da8f2bdde50b02c18fcb3b8cc7b863c5bfc2d`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9cdaf2b3e84404fe15fac805498bb5a72d6c0ac92c30197fb6982e353227b`  
		Last Modified: Wed, 10 Sep 2025 12:05:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:09c39ca3dc4c9d3f81b4006903eff2226eb114a0ed9c9ec8f06475bc10a501fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60898535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6f403af48ac4fa76535762c7e13a50e7e4776c73b181eb64039d62681cd5a1`

```dockerfile
```

-	Layers:
	-	`sha256:21cfe9ae7077240303cf5c69debf923f8ab7ebee21bae51fbc5fae1edf9b883d`  
		Last Modified: Wed, 10 Sep 2025 13:15:58 GMT  
		Size: 60.9 MB (60871337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbf59a4fca7d0450e2254c2f9ad55ac96b92c4b9a1a26e85c5eb963ffe97d01`  
		Last Modified: Wed, 10 Sep 2025 13:16:00 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
