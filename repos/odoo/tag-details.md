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
$ docker pull odoo@sha256:acf828b575764391cec81bc48d445cfd4353ad70127ce9b9491deba3b6925d44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:a293d60f06a7d5e3a92390a805fb56338ab44323a98e44b1d877261fd03a87a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584602040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff4a437c878b1c8f2e62b777f7cad23dbbe233a12bd848b46ec82ee5b3101a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1da938bdf8c67f4f4ab1f1dddccf4499f94b5e8865d525851932bbf2047571`  
		Last Modified: Tue, 01 Apr 2025 17:17:00 GMT  
		Size: 219.6 MB (219625948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df52d979dbc49ac90528306246bc896e4cdb98aab912fe7da3b24c5588995cb4`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 2.6 MB (2623288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb440a9fbf96c7f9a3dfe73f10905a59047743f0895e3ddf0fc1f88bb959dfd7`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4538045727934a23e5ebaf67b73c66d9f6e043863314180e4348f002da604c0`  
		Last Modified: Tue, 01 Apr 2025 17:17:04 GMT  
		Size: 331.6 MB (331618749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6691934ed618e53642433148d38fe9f1a690934671d69927398027f28a68ac`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2df8078d1f3ed48e929f5aa46e0e97822f15cd1baee0c7d67291c22da3e98`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbdde75268e8d13a2c6ca9e7fabca8060cdd46ea0228a87a16238468f7289d9`  
		Last Modified: Tue, 01 Apr 2025 17:16:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a0cde0ef2b24598c147a1471795cd1669ce0c20a918fd76a37b910d1c40de`  
		Last Modified: Tue, 01 Apr 2025 17:16:58 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:cab118b30ba41be93724f7c39cf4ea346ae46b58d23e6cfe37ba3fd12e4fc127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bf95aba41f78bd86d0e81e6c83eb9bc106864820e65481ab939e6608aa862f`

```dockerfile
```

-	Layers:
	-	`sha256:a6645d8559709f9c2a0f911614b54088969d02505cff8adc72e4ed599b421b8c`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 38.9 MB (38865118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cf701e6569e963c3bad60a88525e59beacc8be32940d7142a53bcd32e7849d`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:999ea5f42885e55040c3706a243610f605edebeda51c6ecc6adbad0b1e4fc65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579970439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba5b56e739012ce1e14dd9f4bd454fdf71b63e48c475f1d68702268b175388d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=C.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=16.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e736f9b985beb974a2bd295bbaf99da6900ef8aede20aa931dc24675c621fbe`  
		Last Modified: Thu, 20 Mar 2025 17:29:26 GMT  
		Size: 216.9 MB (216915362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943d9dd8ac42795a490e591eae030070f9fd16aef76453212f5974b065650223`  
		Last Modified: Thu, 20 Mar 2025 17:29:21 GMT  
		Size: 2.6 MB (2631410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab9611e197186fd7990a9069b729b1357d7fb711af5f253de952684331e31f`  
		Last Modified: Thu, 20 Mar 2025 17:29:21 GMT  
		Size: 477.8 KB (477840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab3fab69715ede3ad1038ec87853f3c5101024d433b0a63e15bea3f1e1e0ab`  
		Last Modified: Thu, 20 Mar 2025 17:29:28 GMT  
		Size: 331.2 MB (331197475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e880b39b8d436cb4706f6fbaff1bb37351d8de709bf09d7de82bc60aafc1b16`  
		Last Modified: Thu, 20 Mar 2025 17:29:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b75efbbf7a5cc1fc6761d9e208a8e605f3a1905b9e809af602a3bde7da68a66`  
		Last Modified: Thu, 20 Mar 2025 17:29:22 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b668bc91dc1c86df96d2e3cde809b896f3ffdd66aff137a05971fc7b77ca129`  
		Last Modified: Thu, 20 Mar 2025 17:29:23 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f050c5e0b7807c30b98507c3bdd3329112fbea1eb1923be391642a72b95f4c`  
		Last Modified: Thu, 20 Mar 2025 17:29:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:725e58a33d6d4dd842489da77091660d565cc8d17190b28cbe479aa8a752f269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a0583113927e4bdee78c17d0f40c72ac3dcf835a09f3749b03fd1c5c811905`

```dockerfile
```

-	Layers:
	-	`sha256:d6417fdade20b68e6de8152efb8a9167f82bc362667fb34da36385df5de00eae`  
		Last Modified: Thu, 20 Mar 2025 17:29:22 GMT  
		Size: 38.9 MB (38866729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398f494e93877fa96d77aa12c62602729606aee8ad7cf843a7fcd4cd26605025`  
		Last Modified: Thu, 20 Mar 2025 17:29:21 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:acf828b575764391cec81bc48d445cfd4353ad70127ce9b9491deba3b6925d44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:a293d60f06a7d5e3a92390a805fb56338ab44323a98e44b1d877261fd03a87a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584602040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff4a437c878b1c8f2e62b777f7cad23dbbe233a12bd848b46ec82ee5b3101a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1da938bdf8c67f4f4ab1f1dddccf4499f94b5e8865d525851932bbf2047571`  
		Last Modified: Tue, 01 Apr 2025 17:17:00 GMT  
		Size: 219.6 MB (219625948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df52d979dbc49ac90528306246bc896e4cdb98aab912fe7da3b24c5588995cb4`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 2.6 MB (2623288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb440a9fbf96c7f9a3dfe73f10905a59047743f0895e3ddf0fc1f88bb959dfd7`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4538045727934a23e5ebaf67b73c66d9f6e043863314180e4348f002da604c0`  
		Last Modified: Tue, 01 Apr 2025 17:17:04 GMT  
		Size: 331.6 MB (331618749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6691934ed618e53642433148d38fe9f1a690934671d69927398027f28a68ac`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2df8078d1f3ed48e929f5aa46e0e97822f15cd1baee0c7d67291c22da3e98`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbdde75268e8d13a2c6ca9e7fabca8060cdd46ea0228a87a16238468f7289d9`  
		Last Modified: Tue, 01 Apr 2025 17:16:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a0cde0ef2b24598c147a1471795cd1669ce0c20a918fd76a37b910d1c40de`  
		Last Modified: Tue, 01 Apr 2025 17:16:58 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cab118b30ba41be93724f7c39cf4ea346ae46b58d23e6cfe37ba3fd12e4fc127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bf95aba41f78bd86d0e81e6c83eb9bc106864820e65481ab939e6608aa862f`

```dockerfile
```

-	Layers:
	-	`sha256:a6645d8559709f9c2a0f911614b54088969d02505cff8adc72e4ed599b421b8c`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 38.9 MB (38865118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cf701e6569e963c3bad60a88525e59beacc8be32940d7142a53bcd32e7849d`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:999ea5f42885e55040c3706a243610f605edebeda51c6ecc6adbad0b1e4fc65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579970439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba5b56e739012ce1e14dd9f4bd454fdf71b63e48c475f1d68702268b175388d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=C.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=16.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e736f9b985beb974a2bd295bbaf99da6900ef8aede20aa931dc24675c621fbe`  
		Last Modified: Thu, 20 Mar 2025 17:29:26 GMT  
		Size: 216.9 MB (216915362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943d9dd8ac42795a490e591eae030070f9fd16aef76453212f5974b065650223`  
		Last Modified: Thu, 20 Mar 2025 17:29:21 GMT  
		Size: 2.6 MB (2631410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab9611e197186fd7990a9069b729b1357d7fb711af5f253de952684331e31f`  
		Last Modified: Thu, 20 Mar 2025 17:29:21 GMT  
		Size: 477.8 KB (477840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab3fab69715ede3ad1038ec87853f3c5101024d433b0a63e15bea3f1e1e0ab`  
		Last Modified: Thu, 20 Mar 2025 17:29:28 GMT  
		Size: 331.2 MB (331197475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e880b39b8d436cb4706f6fbaff1bb37351d8de709bf09d7de82bc60aafc1b16`  
		Last Modified: Thu, 20 Mar 2025 17:29:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b75efbbf7a5cc1fc6761d9e208a8e605f3a1905b9e809af602a3bde7da68a66`  
		Last Modified: Thu, 20 Mar 2025 17:29:22 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b668bc91dc1c86df96d2e3cde809b896f3ffdd66aff137a05971fc7b77ca129`  
		Last Modified: Thu, 20 Mar 2025 17:29:23 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f050c5e0b7807c30b98507c3bdd3329112fbea1eb1923be391642a72b95f4c`  
		Last Modified: Thu, 20 Mar 2025 17:29:23 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:725e58a33d6d4dd842489da77091660d565cc8d17190b28cbe479aa8a752f269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a0583113927e4bdee78c17d0f40c72ac3dcf835a09f3749b03fd1c5c811905`

```dockerfile
```

-	Layers:
	-	`sha256:d6417fdade20b68e6de8152efb8a9167f82bc362667fb34da36385df5de00eae`  
		Last Modified: Thu, 20 Mar 2025 17:29:22 GMT  
		Size: 38.9 MB (38866729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398f494e93877fa96d77aa12c62602729606aee8ad7cf843a7fcd4cd26605025`  
		Last Modified: Thu, 20 Mar 2025 17:29:21 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250401`

```console
$ docker pull odoo@sha256:9b06d501093d5d6364420e11c264893578139e91efa51ab1ad879b930782a65e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:16.0-20250401` - linux; amd64

```console
$ docker pull odoo@sha256:a293d60f06a7d5e3a92390a805fb56338ab44323a98e44b1d877261fd03a87a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.6 MB (584602040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff4a437c878b1c8f2e62b777f7cad23dbbe233a12bd848b46ec82ee5b3101a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1da938bdf8c67f4f4ab1f1dddccf4499f94b5e8865d525851932bbf2047571`  
		Last Modified: Tue, 01 Apr 2025 17:17:00 GMT  
		Size: 219.6 MB (219625948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df52d979dbc49ac90528306246bc896e4cdb98aab912fe7da3b24c5588995cb4`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 2.6 MB (2623288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb440a9fbf96c7f9a3dfe73f10905a59047743f0895e3ddf0fc1f88bb959dfd7`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 477.8 KB (477785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4538045727934a23e5ebaf67b73c66d9f6e043863314180e4348f002da604c0`  
		Last Modified: Tue, 01 Apr 2025 17:17:04 GMT  
		Size: 331.6 MB (331618749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6691934ed618e53642433148d38fe9f1a690934671d69927398027f28a68ac`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2df8078d1f3ed48e929f5aa46e0e97822f15cd1baee0c7d67291c22da3e98`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbdde75268e8d13a2c6ca9e7fabca8060cdd46ea0228a87a16238468f7289d9`  
		Last Modified: Tue, 01 Apr 2025 17:16:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a0cde0ef2b24598c147a1471795cd1669ce0c20a918fd76a37b910d1c40de`  
		Last Modified: Tue, 01 Apr 2025 17:16:58 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:cab118b30ba41be93724f7c39cf4ea346ae46b58d23e6cfe37ba3fd12e4fc127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bf95aba41f78bd86d0e81e6c83eb9bc106864820e65481ab939e6608aa862f`

```dockerfile
```

-	Layers:
	-	`sha256:a6645d8559709f9c2a0f911614b54088969d02505cff8adc72e4ed599b421b8c`  
		Last Modified: Tue, 01 Apr 2025 17:16:57 GMT  
		Size: 38.9 MB (38865118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cf701e6569e963c3bad60a88525e59beacc8be32940d7142a53bcd32e7849d`  
		Last Modified: Tue, 01 Apr 2025 17:16:56 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:14eea5fd0116fc4c99148b2b1fc3a1eaa95d523c50865e2396173549a7f315d4
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
$ docker pull odoo@sha256:c8c97b7992d11a2f7439534246de198b5b05e746b2895bb18962f225cf2b8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602672253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2a09a457c789691da386e4da9d388c7754dfd9c66f1cbf2420f4f8c77d5fc`
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e950fda80ef7503467a6a4cf05873a145ed4bee1dabdb21d2858e0ba3f1b2`  
		Last Modified: Tue, 01 Apr 2025 17:19:44 GMT  
		Size: 236.1 MB (236052068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa27e90f74d4e34a691ac3ea6f358d98768aa3a9be61d6f6f58e223cd65ef6e`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 2.5 MB (2520311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b8e915172db6c043a83ad8c2310258e3b6cecdcb1bc352baf255b037847a1d`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 478.8 KB (478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691e09b346afd875bb5d27efeba4f706e8c1025696e45308ed4eaf8414f34f8`  
		Last Modified: Tue, 01 Apr 2025 17:19:46 GMT  
		Size: 334.1 MB (334082663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6b82d8ed8c571934d70fa3fb048da478916cf8d8b70ec1e563df82508ccce`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4057a215046248eba510298c9fbfa5ce70dfa377b9c17946edb95933f7cbc35a`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f777d71b92a2a7535aacb6206411ad7a670c368ddd217296193066c565d7bba`  
		Last Modified: Tue, 01 Apr 2025 17:19:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c82e2bd8093602cefc7fc436aff305f44c9d7f12c4894e32180671f7e8c24ce`  
		Last Modified: Tue, 01 Apr 2025 17:19:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:000dfc066443e45909ee9e73f2c925005496f7d5b352e0d262042505552e607e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39787324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9611de5dded78ee0002a7ccfdafc76421aac9a8168da1b3dd613600a9b2a0bd9`

```dockerfile
```

-	Layers:
	-	`sha256:4fc99466ff31dcd8faf77e5849da91766cc633653752aa0f073989d2dd713def`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 39.8 MB (39760490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c3169e72bdc4581f4527212adf1468434fdb10441c1356e7d16bdb90367157`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:02c0bf294eaeabe296ba7d376634b2e4844c41c19eb82d276811351db283ba77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597169940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5ee5dfc37a6f3795cce3d8e4e7cf45bb96ebbe78c38841a2e7b140624df982`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
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
	-	`sha256:a1bf46fc87ad713e5c7e054408a75fd85372bf1d5960b7917f3a946f6c555148`  
		Last Modified: Thu, 20 Mar 2025 17:25:48 GMT  
		Size: 333.6 MB (333569108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e8c5615209c45414f53f38668e9be8f6a816ebfc950f582a1e366a4291cc3`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29c7989c5453ba2e58a543519430dd0deffb741d14bff6ff726c2d3605b3864`  
		Last Modified: Thu, 20 Mar 2025 17:25:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8159aebb6c67e49aada1ade8ea5b1bbae06d7d043107c35c988379a556b632`  
		Last Modified: Thu, 20 Mar 2025 17:25:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abd4fdc7654431d7cfe51c1bec98024d3cd86786751fd013f065a12f28750f`  
		Last Modified: Thu, 20 Mar 2025 17:25:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a0d8c451ab19aea7dc80fd8fa1e7243ce29a642af7a1802d01553308d8a1a4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39773256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d2e2f4879e0f35d3f62410de4904543cc2859cacfc17aa43fbfde5fdd36c83`

```dockerfile
```

-	Layers:
	-	`sha256:b84ec393502f0439370cc595588b18dc7285e398eb13d8100844d75df5b7ebd2`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 39.7 MB (39746269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d6c2ed6886289a1ab6e3840265940a75e5e313587a54b36b9d93668d136d5d`  
		Last Modified: Thu, 20 Mar 2025 17:25:39 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:b1153b5260e4adbfb9906ebc2045a6c7cfcc3019651548805107def3de263217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.5 MB (619493550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc913e12acec1c74f4d1770f995e495f0a617fa22beffc4f501b859c1e2c8ebe`
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdab9e1cb6312a197f2c815098e2f009e2030d4cc96665132addfc0e4118238`  
		Last Modified: Thu, 20 Mar 2025 17:33:20 GMT  
		Size: 245.9 MB (245919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96999404235ec65a6d9ebb03f30182d58af041bd6fe90a4e748b5df7de63d`  
		Last Modified: Thu, 20 Mar 2025 17:32:55 GMT  
		Size: 2.8 MB (2838323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1206e99df372f5d8c8eef13e99786291d8ef66d5e745a1e34f6c5ff59d379b6`  
		Last Modified: Thu, 20 Mar 2025 17:32:54 GMT  
		Size: 478.9 KB (478948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17dca96e8f691012d0843d7af1fa48e15e60a677eeedd194d73cfd023dce9a1`  
		Last Modified: Tue, 01 Apr 2025 17:36:57 GMT  
		Size: 335.8 MB (335806091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fb163c0cab93aba00ddd14a3fb39fd51479c1e6f2022a4852fac7be3afd68f`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1284c70f4716fd3bf53a40493fdff685fdbb7d53cd48f6d2780ef4d69c7e7f1f`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e88bca144bde5c14a28a48b72b9470f8687e98e271db678ee7642227fb00b1`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528d3a8abc8cb0b400ffa8e73a81173fe76b8b6a065fa584dcd8c1cb6084965`  
		Last Modified: Tue, 01 Apr 2025 17:36:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:264edd71ccc11614bf975f5ea23bac6b1c67383bba157cdbc915638b8e4ada88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f0c46376dbb9d672061c01d187ec8f363f6177ca09aba23f914f327dcbca3`

```dockerfile
```

-	Layers:
	-	`sha256:66c639d9444f4c658178ffc85e990a7075a70e4d961996f2a92560e171d33910`  
		Last Modified: Tue, 01 Apr 2025 17:36:44 GMT  
		Size: 39.8 MB (39768181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcb283156e35737c759af237866e1a867875d23f215fd1addd6321476327517`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:14eea5fd0116fc4c99148b2b1fc3a1eaa95d523c50865e2396173549a7f315d4
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
$ docker pull odoo@sha256:c8c97b7992d11a2f7439534246de198b5b05e746b2895bb18962f225cf2b8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602672253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2a09a457c789691da386e4da9d388c7754dfd9c66f1cbf2420f4f8c77d5fc`
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e950fda80ef7503467a6a4cf05873a145ed4bee1dabdb21d2858e0ba3f1b2`  
		Last Modified: Tue, 01 Apr 2025 17:19:44 GMT  
		Size: 236.1 MB (236052068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa27e90f74d4e34a691ac3ea6f358d98768aa3a9be61d6f6f58e223cd65ef6e`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 2.5 MB (2520311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b8e915172db6c043a83ad8c2310258e3b6cecdcb1bc352baf255b037847a1d`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 478.8 KB (478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691e09b346afd875bb5d27efeba4f706e8c1025696e45308ed4eaf8414f34f8`  
		Last Modified: Tue, 01 Apr 2025 17:19:46 GMT  
		Size: 334.1 MB (334082663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6b82d8ed8c571934d70fa3fb048da478916cf8d8b70ec1e563df82508ccce`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4057a215046248eba510298c9fbfa5ce70dfa377b9c17946edb95933f7cbc35a`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f777d71b92a2a7535aacb6206411ad7a670c368ddd217296193066c565d7bba`  
		Last Modified: Tue, 01 Apr 2025 17:19:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c82e2bd8093602cefc7fc436aff305f44c9d7f12c4894e32180671f7e8c24ce`  
		Last Modified: Tue, 01 Apr 2025 17:19:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:000dfc066443e45909ee9e73f2c925005496f7d5b352e0d262042505552e607e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39787324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9611de5dded78ee0002a7ccfdafc76421aac9a8168da1b3dd613600a9b2a0bd9`

```dockerfile
```

-	Layers:
	-	`sha256:4fc99466ff31dcd8faf77e5849da91766cc633653752aa0f073989d2dd713def`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 39.8 MB (39760490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c3169e72bdc4581f4527212adf1468434fdb10441c1356e7d16bdb90367157`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:02c0bf294eaeabe296ba7d376634b2e4844c41c19eb82d276811351db283ba77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597169940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5ee5dfc37a6f3795cce3d8e4e7cf45bb96ebbe78c38841a2e7b140624df982`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
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
	-	`sha256:a1bf46fc87ad713e5c7e054408a75fd85372bf1d5960b7917f3a946f6c555148`  
		Last Modified: Thu, 20 Mar 2025 17:25:48 GMT  
		Size: 333.6 MB (333569108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e8c5615209c45414f53f38668e9be8f6a816ebfc950f582a1e366a4291cc3`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29c7989c5453ba2e58a543519430dd0deffb741d14bff6ff726c2d3605b3864`  
		Last Modified: Thu, 20 Mar 2025 17:25:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8159aebb6c67e49aada1ade8ea5b1bbae06d7d043107c35c988379a556b632`  
		Last Modified: Thu, 20 Mar 2025 17:25:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abd4fdc7654431d7cfe51c1bec98024d3cd86786751fd013f065a12f28750f`  
		Last Modified: Thu, 20 Mar 2025 17:25:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a0d8c451ab19aea7dc80fd8fa1e7243ce29a642af7a1802d01553308d8a1a4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39773256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d2e2f4879e0f35d3f62410de4904543cc2859cacfc17aa43fbfde5fdd36c83`

```dockerfile
```

-	Layers:
	-	`sha256:b84ec393502f0439370cc595588b18dc7285e398eb13d8100844d75df5b7ebd2`  
		Last Modified: Thu, 20 Mar 2025 17:25:40 GMT  
		Size: 39.7 MB (39746269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d6c2ed6886289a1ab6e3840265940a75e5e313587a54b36b9d93668d136d5d`  
		Last Modified: Thu, 20 Mar 2025 17:25:39 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b1153b5260e4adbfb9906ebc2045a6c7cfcc3019651548805107def3de263217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.5 MB (619493550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc913e12acec1c74f4d1770f995e495f0a617fa22beffc4f501b859c1e2c8ebe`
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdab9e1cb6312a197f2c815098e2f009e2030d4cc96665132addfc0e4118238`  
		Last Modified: Thu, 20 Mar 2025 17:33:20 GMT  
		Size: 245.9 MB (245919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96999404235ec65a6d9ebb03f30182d58af041bd6fe90a4e748b5df7de63d`  
		Last Modified: Thu, 20 Mar 2025 17:32:55 GMT  
		Size: 2.8 MB (2838323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1206e99df372f5d8c8eef13e99786291d8ef66d5e745a1e34f6c5ff59d379b6`  
		Last Modified: Thu, 20 Mar 2025 17:32:54 GMT  
		Size: 478.9 KB (478948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17dca96e8f691012d0843d7af1fa48e15e60a677eeedd194d73cfd023dce9a1`  
		Last Modified: Tue, 01 Apr 2025 17:36:57 GMT  
		Size: 335.8 MB (335806091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fb163c0cab93aba00ddd14a3fb39fd51479c1e6f2022a4852fac7be3afd68f`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1284c70f4716fd3bf53a40493fdff685fdbb7d53cd48f6d2780ef4d69c7e7f1f`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e88bca144bde5c14a28a48b72b9470f8687e98e271db678ee7642227fb00b1`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528d3a8abc8cb0b400ffa8e73a81173fe76b8b6a065fa584dcd8c1cb6084965`  
		Last Modified: Tue, 01 Apr 2025 17:36:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:264edd71ccc11614bf975f5ea23bac6b1c67383bba157cdbc915638b8e4ada88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f0c46376dbb9d672061c01d187ec8f363f6177ca09aba23f914f327dcbca3`

```dockerfile
```

-	Layers:
	-	`sha256:66c639d9444f4c658178ffc85e990a7075a70e4d961996f2a92560e171d33910`  
		Last Modified: Tue, 01 Apr 2025 17:36:44 GMT  
		Size: 39.8 MB (39768181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcb283156e35737c759af237866e1a867875d23f215fd1addd6321476327517`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250401`

```console
$ docker pull odoo@sha256:d9ffabd9202b4808eb58782bf1804b0a471afb660ac1928df56ef84f9677595f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250401` - linux; amd64

```console
$ docker pull odoo@sha256:c8c97b7992d11a2f7439534246de198b5b05e746b2895bb18962f225cf2b8c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602672253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a2a09a457c789691da386e4da9d388c7754dfd9c66f1cbf2420f4f8c77d5fc`
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e950fda80ef7503467a6a4cf05873a145ed4bee1dabdb21d2858e0ba3f1b2`  
		Last Modified: Tue, 01 Apr 2025 17:19:44 GMT  
		Size: 236.1 MB (236052068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa27e90f74d4e34a691ac3ea6f358d98768aa3a9be61d6f6f58e223cd65ef6e`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 2.5 MB (2520311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b8e915172db6c043a83ad8c2310258e3b6cecdcb1bc352baf255b037847a1d`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 478.8 KB (478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691e09b346afd875bb5d27efeba4f706e8c1025696e45308ed4eaf8414f34f8`  
		Last Modified: Tue, 01 Apr 2025 17:19:46 GMT  
		Size: 334.1 MB (334082663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6b82d8ed8c571934d70fa3fb048da478916cf8d8b70ec1e563df82508ccce`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4057a215046248eba510298c9fbfa5ce70dfa377b9c17946edb95933f7cbc35a`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f777d71b92a2a7535aacb6206411ad7a670c368ddd217296193066c565d7bba`  
		Last Modified: Tue, 01 Apr 2025 17:19:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c82e2bd8093602cefc7fc436aff305f44c9d7f12c4894e32180671f7e8c24ce`  
		Last Modified: Tue, 01 Apr 2025 17:19:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:000dfc066443e45909ee9e73f2c925005496f7d5b352e0d262042505552e607e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39787324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9611de5dded78ee0002a7ccfdafc76421aac9a8168da1b3dd613600a9b2a0bd9`

```dockerfile
```

-	Layers:
	-	`sha256:4fc99466ff31dcd8faf77e5849da91766cc633653752aa0f073989d2dd713def`  
		Last Modified: Tue, 01 Apr 2025 17:19:41 GMT  
		Size: 39.8 MB (39760490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c3169e72bdc4581f4527212adf1468434fdb10441c1356e7d16bdb90367157`  
		Last Modified: Tue, 01 Apr 2025 17:19:40 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250401` - linux; ppc64le

```console
$ docker pull odoo@sha256:b1153b5260e4adbfb9906ebc2045a6c7cfcc3019651548805107def3de263217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.5 MB (619493550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc913e12acec1c74f4d1770f995e495f0a617fa22beffc4f501b859c1e2c8ebe`
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdab9e1cb6312a197f2c815098e2f009e2030d4cc96665132addfc0e4118238`  
		Last Modified: Thu, 20 Mar 2025 17:33:20 GMT  
		Size: 245.9 MB (245919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96999404235ec65a6d9ebb03f30182d58af041bd6fe90a4e748b5df7de63d`  
		Last Modified: Thu, 20 Mar 2025 17:32:55 GMT  
		Size: 2.8 MB (2838323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1206e99df372f5d8c8eef13e99786291d8ef66d5e745a1e34f6c5ff59d379b6`  
		Last Modified: Thu, 20 Mar 2025 17:32:54 GMT  
		Size: 478.9 KB (478948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17dca96e8f691012d0843d7af1fa48e15e60a677eeedd194d73cfd023dce9a1`  
		Last Modified: Tue, 01 Apr 2025 17:36:57 GMT  
		Size: 335.8 MB (335806091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fb163c0cab93aba00ddd14a3fb39fd51479c1e6f2022a4852fac7be3afd68f`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1284c70f4716fd3bf53a40493fdff685fdbb7d53cd48f6d2780ef4d69c7e7f1f`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e88bca144bde5c14a28a48b72b9470f8687e98e271db678ee7642227fb00b1`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528d3a8abc8cb0b400ffa8e73a81173fe76b8b6a065fa584dcd8c1cb6084965`  
		Last Modified: Tue, 01 Apr 2025 17:36:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:264edd71ccc11614bf975f5ea23bac6b1c67383bba157cdbc915638b8e4ada88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39795072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f0c46376dbb9d672061c01d187ec8f363f6177ca09aba23f914f327dcbca3`

```dockerfile
```

-	Layers:
	-	`sha256:66c639d9444f4c658178ffc85e990a7075a70e4d961996f2a92560e171d33910`  
		Last Modified: Tue, 01 Apr 2025 17:36:44 GMT  
		Size: 39.8 MB (39768181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcb283156e35737c759af237866e1a867875d23f215fd1addd6321476327517`  
		Last Modified: Tue, 01 Apr 2025 17:36:42 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:11ec69d0d41a26b8ceaf7430637e556a226e4a35e5cce5511b53b86555350a2b
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
$ docker pull odoo@sha256:11915bf322efb5fa4371b1baabdac639c984e73c8d6fe076cde9f22f02000790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.9 MB (674938432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31294ed50b232a360d5052b9b8ac4b0f79b80e0bca8e6cfd0fd96c8b6f2ff047`
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6649e3d58a0d0b8784b9841145a38f28833c1e1843512168c5faf55063e49`  
		Last Modified: Tue, 01 Apr 2025 17:17:45 GMT  
		Size: 256.9 MB (256920087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7cdb5b6d46543dd0ae496333c3341fc26e1f7903ee205da7d0c7305aa5786`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 16.7 MB (16679841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4368ac54be95afda32beac0a5d938c2d22a44d7d4ffdb2d5288852e6433c38`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 478.6 KB (478631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b81e6dd4358e484db83bf7137711920744fa7ae817fb7b5aae821d2cd75115`  
		Last Modified: Tue, 01 Apr 2025 17:17:47 GMT  
		Size: 371.1 MB (371103144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b2ab46d8292b3e6e8656a6aa5f9d2022e99040eed1b6b692aa3da4ad9be223`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e51ac74ed12296ea5d0afcff54cf5dd9d235b6f5cc2a3d3d0a3a1258ac5855`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abff459f547feac64f046cf976feba44de557ffee0cebb6b37f798ce8e17109`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5e89477b21c6c57e0daa68cd114e2c2828b5560be8e5139aef14bc084ce98`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0bc99842e9caccabba0b21955277d1521625d66bd4e627944de883af56fc16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59211986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881845c37f6ef69622d56949434e3f93f0cb78c0af761e5df7eb8085f43fde41`

```dockerfile
```

-	Layers:
	-	`sha256:59706d74b4a7c1fcc1c5b321fe7152a1bc5ffd48fc4ce125ca224db9441eaf07`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 59.2 MB (59184851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11c81002107ccfd779072a1f7a5f3dff323e3394218abad6a956cc86e1d7b40`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6138adf199dce157a7b9ccb0f7ede6722a7209f2011dec46d7100a79edaeb922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.7 MB (670701306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd39fd06eba7900ac2a4f173c864b12804a8849128d54dbb678a90ddecd9ccf2`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
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
	-	`sha256:a8d77f068fa67f17ced6f5216b2234e2912333dc124282e8afadf7dd23c73397`  
		Last Modified: Thu, 20 Mar 2025 17:19:12 GMT  
		Size: 370.5 MB (370548829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09246ae991ed7d432c1e88bbdc50ec8292f5276b8fe5a6ab9f4480c211f89984`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d53e88c6c7f74c8281ae5b3457d77f12ead4038f0c72a735fda09fa0bfdd44`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ebe002e971520488811d202dfb62c61cf04b4648716544cd73f719dda09f63`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d90cdb34f68681d23720f704d47101a3e8a9503473370a98f353e63b8da472e`  
		Last Modified: Thu, 20 Mar 2025 17:19:07 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:6ed1a95549d8dafc1b93c5f89b3f2b0fe75de5179261c6d6e639aadc2fee728d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59172966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533558d65bf86a325e5109360a3068e83e2b5bddaddaa678fec954e34b28584e`

```dockerfile
```

-	Layers:
	-	`sha256:e550d71a8de7750dc0ac2410ffea29403a1064db9af93fa6afbbe9a8be85d638`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 59.1 MB (59145666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3974d4b5fe20ecc8f23483d86f84443d827077a1169798f7ad190012774a22d2`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:e6359e6c77f001ceeb361efc63d07b6cd8fd9b402257c7aad09b1ffb6e836065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691583226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8641c36c1aace922eae6f8a576092797d9f7e981e66f3c4ab6ccaf1571fa87ec`
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a6cdf7bee77bd813b26e458404c51906e2c26ee33151f4494a4384cbbceb`  
		Last Modified: Thu, 20 Mar 2025 17:23:28 GMT  
		Size: 267.7 MB (267709874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266984176781c453c9676a0655e2600e985f7c298ed73730eba450762c46dc9e`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 17.4 MB (17357354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdec516c786264ba6ff83229ba8621ca81da021db675f524db6969367779215`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 478.6 KB (478571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e41278a9a3e9bbdbe7589c9b68e944ba6fb06be8b59373016da666817881c`  
		Last Modified: Tue, 01 Apr 2025 17:31:20 GMT  
		Size: 371.6 MB (371645163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e31cd8ee8b7a522177f93f796cdeaf41d295ec8d06d554d81a81f6f5b7cfc77`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2f907bfb5a21e58d3ec64d6dcef4d8f8d6d63a2a9aa4a025bba0ac9710122`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e559a2d0c0cc1a7ac017e0cf846eb3bdcfa1ca2c06db9958a475cb04fab0dc3`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d34ebc171a7331741597ebdd77f2ea5d03fd9a0e0d6fc2293617a0efd1ea3`  
		Last Modified: Tue, 01 Apr 2025 17:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:a433252570c36776fd9d0bc8cdc75caae553ae927a9ab6d72b9b8ac5a930c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ac41726d2a7dd9cc2661ed583418133b53ba912b5a2402b373d1e663744fbb`

```dockerfile
```

-	Layers:
	-	`sha256:cbe7a1280e2616c51f4871d9c148f3513a80c9afb3f879e1186817e39f90e36d`  
		Last Modified: Tue, 01 Apr 2025 17:31:12 GMT  
		Size: 59.2 MB (59192998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788016454f0a74828fbe2def6f9a0f308b4decbbd2ed7659d6fa5900e349c855`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:11ec69d0d41a26b8ceaf7430637e556a226e4a35e5cce5511b53b86555350a2b
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
$ docker pull odoo@sha256:11915bf322efb5fa4371b1baabdac639c984e73c8d6fe076cde9f22f02000790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.9 MB (674938432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31294ed50b232a360d5052b9b8ac4b0f79b80e0bca8e6cfd0fd96c8b6f2ff047`
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6649e3d58a0d0b8784b9841145a38f28833c1e1843512168c5faf55063e49`  
		Last Modified: Tue, 01 Apr 2025 17:17:45 GMT  
		Size: 256.9 MB (256920087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7cdb5b6d46543dd0ae496333c3341fc26e1f7903ee205da7d0c7305aa5786`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 16.7 MB (16679841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4368ac54be95afda32beac0a5d938c2d22a44d7d4ffdb2d5288852e6433c38`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 478.6 KB (478631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b81e6dd4358e484db83bf7137711920744fa7ae817fb7b5aae821d2cd75115`  
		Last Modified: Tue, 01 Apr 2025 17:17:47 GMT  
		Size: 371.1 MB (371103144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b2ab46d8292b3e6e8656a6aa5f9d2022e99040eed1b6b692aa3da4ad9be223`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e51ac74ed12296ea5d0afcff54cf5dd9d235b6f5cc2a3d3d0a3a1258ac5855`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abff459f547feac64f046cf976feba44de557ffee0cebb6b37f798ce8e17109`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5e89477b21c6c57e0daa68cd114e2c2828b5560be8e5139aef14bc084ce98`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0bc99842e9caccabba0b21955277d1521625d66bd4e627944de883af56fc16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59211986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881845c37f6ef69622d56949434e3f93f0cb78c0af761e5df7eb8085f43fde41`

```dockerfile
```

-	Layers:
	-	`sha256:59706d74b4a7c1fcc1c5b321fe7152a1bc5ffd48fc4ce125ca224db9441eaf07`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 59.2 MB (59184851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11c81002107ccfd779072a1f7a5f3dff323e3394218abad6a956cc86e1d7b40`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6138adf199dce157a7b9ccb0f7ede6722a7209f2011dec46d7100a79edaeb922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.7 MB (670701306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd39fd06eba7900ac2a4f173c864b12804a8849128d54dbb678a90ddecd9ccf2`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
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
	-	`sha256:a8d77f068fa67f17ced6f5216b2234e2912333dc124282e8afadf7dd23c73397`  
		Last Modified: Thu, 20 Mar 2025 17:19:12 GMT  
		Size: 370.5 MB (370548829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09246ae991ed7d432c1e88bbdc50ec8292f5276b8fe5a6ab9f4480c211f89984`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d53e88c6c7f74c8281ae5b3457d77f12ead4038f0c72a735fda09fa0bfdd44`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ebe002e971520488811d202dfb62c61cf04b4648716544cd73f719dda09f63`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d90cdb34f68681d23720f704d47101a3e8a9503473370a98f353e63b8da472e`  
		Last Modified: Thu, 20 Mar 2025 17:19:07 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6ed1a95549d8dafc1b93c5f89b3f2b0fe75de5179261c6d6e639aadc2fee728d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59172966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533558d65bf86a325e5109360a3068e83e2b5bddaddaa678fec954e34b28584e`

```dockerfile
```

-	Layers:
	-	`sha256:e550d71a8de7750dc0ac2410ffea29403a1064db9af93fa6afbbe9a8be85d638`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 59.1 MB (59145666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3974d4b5fe20ecc8f23483d86f84443d827077a1169798f7ad190012774a22d2`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e6359e6c77f001ceeb361efc63d07b6cd8fd9b402257c7aad09b1ffb6e836065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691583226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8641c36c1aace922eae6f8a576092797d9f7e981e66f3c4ab6ccaf1571fa87ec`
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a6cdf7bee77bd813b26e458404c51906e2c26ee33151f4494a4384cbbceb`  
		Last Modified: Thu, 20 Mar 2025 17:23:28 GMT  
		Size: 267.7 MB (267709874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266984176781c453c9676a0655e2600e985f7c298ed73730eba450762c46dc9e`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 17.4 MB (17357354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdec516c786264ba6ff83229ba8621ca81da021db675f524db6969367779215`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 478.6 KB (478571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e41278a9a3e9bbdbe7589c9b68e944ba6fb06be8b59373016da666817881c`  
		Last Modified: Tue, 01 Apr 2025 17:31:20 GMT  
		Size: 371.6 MB (371645163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e31cd8ee8b7a522177f93f796cdeaf41d295ec8d06d554d81a81f6f5b7cfc77`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2f907bfb5a21e58d3ec64d6dcef4d8f8d6d63a2a9aa4a025bba0ac9710122`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e559a2d0c0cc1a7ac017e0cf846eb3bdcfa1ca2c06db9958a475cb04fab0dc3`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d34ebc171a7331741597ebdd77f2ea5d03fd9a0e0d6fc2293617a0efd1ea3`  
		Last Modified: Tue, 01 Apr 2025 17:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a433252570c36776fd9d0bc8cdc75caae553ae927a9ab6d72b9b8ac5a930c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ac41726d2a7dd9cc2661ed583418133b53ba912b5a2402b373d1e663744fbb`

```dockerfile
```

-	Layers:
	-	`sha256:cbe7a1280e2616c51f4871d9c148f3513a80c9afb3f879e1186817e39f90e36d`  
		Last Modified: Tue, 01 Apr 2025 17:31:12 GMT  
		Size: 59.2 MB (59192998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788016454f0a74828fbe2def6f9a0f308b4decbbd2ed7659d6fa5900e349c855`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250401`

```console
$ docker pull odoo@sha256:24ee578a34a554744ff9949d22a7719145b0d212cd19d991ee0d6194d079ddd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250401` - linux; amd64

```console
$ docker pull odoo@sha256:11915bf322efb5fa4371b1baabdac639c984e73c8d6fe076cde9f22f02000790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.9 MB (674938432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31294ed50b232a360d5052b9b8ac4b0f79b80e0bca8e6cfd0fd96c8b6f2ff047`
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6649e3d58a0d0b8784b9841145a38f28833c1e1843512168c5faf55063e49`  
		Last Modified: Tue, 01 Apr 2025 17:17:45 GMT  
		Size: 256.9 MB (256920087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7cdb5b6d46543dd0ae496333c3341fc26e1f7903ee205da7d0c7305aa5786`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 16.7 MB (16679841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4368ac54be95afda32beac0a5d938c2d22a44d7d4ffdb2d5288852e6433c38`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 478.6 KB (478631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b81e6dd4358e484db83bf7137711920744fa7ae817fb7b5aae821d2cd75115`  
		Last Modified: Tue, 01 Apr 2025 17:17:47 GMT  
		Size: 371.1 MB (371103144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b2ab46d8292b3e6e8656a6aa5f9d2022e99040eed1b6b692aa3da4ad9be223`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e51ac74ed12296ea5d0afcff54cf5dd9d235b6f5cc2a3d3d0a3a1258ac5855`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abff459f547feac64f046cf976feba44de557ffee0cebb6b37f798ce8e17109`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5e89477b21c6c57e0daa68cd114e2c2828b5560be8e5139aef14bc084ce98`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:0bc99842e9caccabba0b21955277d1521625d66bd4e627944de883af56fc16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59211986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881845c37f6ef69622d56949434e3f93f0cb78c0af761e5df7eb8085f43fde41`

```dockerfile
```

-	Layers:
	-	`sha256:59706d74b4a7c1fcc1c5b321fe7152a1bc5ffd48fc4ce125ca224db9441eaf07`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 59.2 MB (59184851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11c81002107ccfd779072a1f7a5f3dff323e3394218abad6a956cc86e1d7b40`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250401` - linux; ppc64le

```console
$ docker pull odoo@sha256:e6359e6c77f001ceeb361efc63d07b6cd8fd9b402257c7aad09b1ffb6e836065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691583226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8641c36c1aace922eae6f8a576092797d9f7e981e66f3c4ab6ccaf1571fa87ec`
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a6cdf7bee77bd813b26e458404c51906e2c26ee33151f4494a4384cbbceb`  
		Last Modified: Thu, 20 Mar 2025 17:23:28 GMT  
		Size: 267.7 MB (267709874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266984176781c453c9676a0655e2600e985f7c298ed73730eba450762c46dc9e`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 17.4 MB (17357354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdec516c786264ba6ff83229ba8621ca81da021db675f524db6969367779215`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 478.6 KB (478571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e41278a9a3e9bbdbe7589c9b68e944ba6fb06be8b59373016da666817881c`  
		Last Modified: Tue, 01 Apr 2025 17:31:20 GMT  
		Size: 371.6 MB (371645163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e31cd8ee8b7a522177f93f796cdeaf41d295ec8d06d554d81a81f6f5b7cfc77`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2f907bfb5a21e58d3ec64d6dcef4d8f8d6d63a2a9aa4a025bba0ac9710122`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e559a2d0c0cc1a7ac017e0cf846eb3bdcfa1ca2c06db9958a475cb04fab0dc3`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d34ebc171a7331741597ebdd77f2ea5d03fd9a0e0d6fc2293617a0efd1ea3`  
		Last Modified: Tue, 01 Apr 2025 17:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250401` - unknown; unknown

```console
$ docker pull odoo@sha256:a433252570c36776fd9d0bc8cdc75caae553ae927a9ab6d72b9b8ac5a930c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ac41726d2a7dd9cc2661ed583418133b53ba912b5a2402b373d1e663744fbb`

```dockerfile
```

-	Layers:
	-	`sha256:cbe7a1280e2616c51f4871d9c148f3513a80c9afb3f879e1186817e39f90e36d`  
		Last Modified: Tue, 01 Apr 2025 17:31:12 GMT  
		Size: 59.2 MB (59192998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788016454f0a74828fbe2def6f9a0f308b4decbbd2ed7659d6fa5900e349c855`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:11ec69d0d41a26b8ceaf7430637e556a226e4a35e5cce5511b53b86555350a2b
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
$ docker pull odoo@sha256:11915bf322efb5fa4371b1baabdac639c984e73c8d6fe076cde9f22f02000790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.9 MB (674938432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31294ed50b232a360d5052b9b8ac4b0f79b80e0bca8e6cfd0fd96c8b6f2ff047`
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6649e3d58a0d0b8784b9841145a38f28833c1e1843512168c5faf55063e49`  
		Last Modified: Tue, 01 Apr 2025 17:17:45 GMT  
		Size: 256.9 MB (256920087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7cdb5b6d46543dd0ae496333c3341fc26e1f7903ee205da7d0c7305aa5786`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 16.7 MB (16679841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4368ac54be95afda32beac0a5d938c2d22a44d7d4ffdb2d5288852e6433c38`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 478.6 KB (478631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b81e6dd4358e484db83bf7137711920744fa7ae817fb7b5aae821d2cd75115`  
		Last Modified: Tue, 01 Apr 2025 17:17:47 GMT  
		Size: 371.1 MB (371103144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b2ab46d8292b3e6e8656a6aa5f9d2022e99040eed1b6b692aa3da4ad9be223`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e51ac74ed12296ea5d0afcff54cf5dd9d235b6f5cc2a3d3d0a3a1258ac5855`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abff459f547feac64f046cf976feba44de557ffee0cebb6b37f798ce8e17109`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5e89477b21c6c57e0daa68cd114e2c2828b5560be8e5139aef14bc084ce98`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:0bc99842e9caccabba0b21955277d1521625d66bd4e627944de883af56fc16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59211986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881845c37f6ef69622d56949434e3f93f0cb78c0af761e5df7eb8085f43fde41`

```dockerfile
```

-	Layers:
	-	`sha256:59706d74b4a7c1fcc1c5b321fe7152a1bc5ffd48fc4ce125ca224db9441eaf07`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 59.2 MB (59184851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11c81002107ccfd779072a1f7a5f3dff323e3394218abad6a956cc86e1d7b40`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6138adf199dce157a7b9ccb0f7ede6722a7209f2011dec46d7100a79edaeb922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.7 MB (670701306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd39fd06eba7900ac2a4f173c864b12804a8849128d54dbb678a90ddecd9ccf2`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
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
	-	`sha256:a8d77f068fa67f17ced6f5216b2234e2912333dc124282e8afadf7dd23c73397`  
		Last Modified: Thu, 20 Mar 2025 17:19:12 GMT  
		Size: 370.5 MB (370548829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09246ae991ed7d432c1e88bbdc50ec8292f5276b8fe5a6ab9f4480c211f89984`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d53e88c6c7f74c8281ae5b3457d77f12ead4038f0c72a735fda09fa0bfdd44`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ebe002e971520488811d202dfb62c61cf04b4648716544cd73f719dda09f63`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d90cdb34f68681d23720f704d47101a3e8a9503473370a98f353e63b8da472e`  
		Last Modified: Thu, 20 Mar 2025 17:19:07 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6ed1a95549d8dafc1b93c5f89b3f2b0fe75de5179261c6d6e639aadc2fee728d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59172966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533558d65bf86a325e5109360a3068e83e2b5bddaddaa678fec954e34b28584e`

```dockerfile
```

-	Layers:
	-	`sha256:e550d71a8de7750dc0ac2410ffea29403a1064db9af93fa6afbbe9a8be85d638`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 59.1 MB (59145666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3974d4b5fe20ecc8f23483d86f84443d827077a1169798f7ad190012774a22d2`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:e6359e6c77f001ceeb361efc63d07b6cd8fd9b402257c7aad09b1ffb6e836065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691583226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8641c36c1aace922eae6f8a576092797d9f7e981e66f3c4ab6ccaf1571fa87ec`
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a6cdf7bee77bd813b26e458404c51906e2c26ee33151f4494a4384cbbceb`  
		Last Modified: Thu, 20 Mar 2025 17:23:28 GMT  
		Size: 267.7 MB (267709874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266984176781c453c9676a0655e2600e985f7c298ed73730eba450762c46dc9e`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 17.4 MB (17357354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdec516c786264ba6ff83229ba8621ca81da021db675f524db6969367779215`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 478.6 KB (478571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e41278a9a3e9bbdbe7589c9b68e944ba6fb06be8b59373016da666817881c`  
		Last Modified: Tue, 01 Apr 2025 17:31:20 GMT  
		Size: 371.6 MB (371645163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e31cd8ee8b7a522177f93f796cdeaf41d295ec8d06d554d81a81f6f5b7cfc77`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2f907bfb5a21e58d3ec64d6dcef4d8f8d6d63a2a9aa4a025bba0ac9710122`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e559a2d0c0cc1a7ac017e0cf846eb3bdcfa1ca2c06db9958a475cb04fab0dc3`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d34ebc171a7331741597ebdd77f2ea5d03fd9a0e0d6fc2293617a0efd1ea3`  
		Last Modified: Tue, 01 Apr 2025 17:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a433252570c36776fd9d0bc8cdc75caae553ae927a9ab6d72b9b8ac5a930c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ac41726d2a7dd9cc2661ed583418133b53ba912b5a2402b373d1e663744fbb`

```dockerfile
```

-	Layers:
	-	`sha256:cbe7a1280e2616c51f4871d9c148f3513a80c9afb3f879e1186817e39f90e36d`  
		Last Modified: Tue, 01 Apr 2025 17:31:12 GMT  
		Size: 59.2 MB (59192998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788016454f0a74828fbe2def6f9a0f308b4decbbd2ed7659d6fa5900e349c855`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
