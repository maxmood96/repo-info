<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250320`](#odoo160-20250320)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250320`](#odoo170-20250320)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250320`](#odoo180-20250320)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:e6e718dc48626eb4f0b821b843f4934f2e1bde652c5228c664d540b9aa226205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:1a21273e6dc882d27fad11db16c9e6ad3a17fb833537f7d3d3ae986ea504a358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584522712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b48b0192727141344f933b7b5d7a1d58908fb335880bd89acdb7eefbe8acafc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=C.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=16.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c0c8387a25f95b2b96e4f86d44dd6b6ee0b2321887ebcc3664e7225cd9a0c9`  
		Last Modified: Thu, 20 Mar 2025 17:13:38 GMT  
		Size: 219.6 MB (219626219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf8b73f14eb980724fb9d7bf85258fb217b283830be42478a9b3568dba0d04c`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 2.6 MB (2623287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b03f7279ad823cd486d51af379980cee7e282a325eccd1da0d3c4c8e04ced15`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 477.8 KB (477826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8caceee829e822020664f73defacbe1a11f4a7ab959c996441dd9bea449762`  
		Last Modified: Thu, 20 Mar 2025 17:13:44 GMT  
		Size: 331.5 MB (331539107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78331f47571e7685e8b70d6e31d76d24f7e0004a238897a1bf8d6cf228409`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8eaf90b2593de56257166eaf0f868d5c88bdad39d8832ce20bac2bad7f5e89`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87060e37c8b77f5f6cc4e0e1773d9dccc7360e8b1d8bc30d81aec2c7a7f026`  
		Last Modified: Thu, 20 Mar 2025 17:13:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f6a34d725083bb866a877574dad62c8a76981984173cf4c746c516a4bd414a`  
		Last Modified: Thu, 20 Mar 2025 17:13:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c35d485d46b8e52e98298f87acb7421a64f53d2aa7af00f09c1644a2178c5e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38886981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04789fc649fc99fa5ece2512695449ce1c5eeb7f03865c5df30f4da1559b4514`

```dockerfile
```

-	Layers:
	-	`sha256:c514017c8090474d5f3936551ba8ddf56d4176d5da9c0cac88dcea042b52a898`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 38.9 MB (38860263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7437f8df4750ea371236ea917a36963325eafbb43270369b86ca42d5dc6aba37`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
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
$ docker pull odoo@sha256:e6e718dc48626eb4f0b821b843f4934f2e1bde652c5228c664d540b9aa226205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:1a21273e6dc882d27fad11db16c9e6ad3a17fb833537f7d3d3ae986ea504a358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584522712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b48b0192727141344f933b7b5d7a1d58908fb335880bd89acdb7eefbe8acafc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=C.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=16.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c0c8387a25f95b2b96e4f86d44dd6b6ee0b2321887ebcc3664e7225cd9a0c9`  
		Last Modified: Thu, 20 Mar 2025 17:13:38 GMT  
		Size: 219.6 MB (219626219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf8b73f14eb980724fb9d7bf85258fb217b283830be42478a9b3568dba0d04c`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 2.6 MB (2623287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b03f7279ad823cd486d51af379980cee7e282a325eccd1da0d3c4c8e04ced15`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 477.8 KB (477826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8caceee829e822020664f73defacbe1a11f4a7ab959c996441dd9bea449762`  
		Last Modified: Thu, 20 Mar 2025 17:13:44 GMT  
		Size: 331.5 MB (331539107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78331f47571e7685e8b70d6e31d76d24f7e0004a238897a1bf8d6cf228409`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8eaf90b2593de56257166eaf0f868d5c88bdad39d8832ce20bac2bad7f5e89`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87060e37c8b77f5f6cc4e0e1773d9dccc7360e8b1d8bc30d81aec2c7a7f026`  
		Last Modified: Thu, 20 Mar 2025 17:13:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f6a34d725083bb866a877574dad62c8a76981984173cf4c746c516a4bd414a`  
		Last Modified: Thu, 20 Mar 2025 17:13:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c35d485d46b8e52e98298f87acb7421a64f53d2aa7af00f09c1644a2178c5e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38886981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04789fc649fc99fa5ece2512695449ce1c5eeb7f03865c5df30f4da1559b4514`

```dockerfile
```

-	Layers:
	-	`sha256:c514017c8090474d5f3936551ba8ddf56d4176d5da9c0cac88dcea042b52a898`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 38.9 MB (38860263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7437f8df4750ea371236ea917a36963325eafbb43270369b86ca42d5dc6aba37`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
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

## `odoo:16.0-20250320`

```console
$ docker pull odoo@sha256:e6e718dc48626eb4f0b821b843f4934f2e1bde652c5228c664d540b9aa226205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250320` - linux; amd64

```console
$ docker pull odoo@sha256:1a21273e6dc882d27fad11db16c9e6ad3a17fb833537f7d3d3ae986ea504a358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584522712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b48b0192727141344f933b7b5d7a1d58908fb335880bd89acdb7eefbe8acafc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=C.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=16.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=afeb7a27c193173e499ad6c9e7d6c391e53b7834
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c0c8387a25f95b2b96e4f86d44dd6b6ee0b2321887ebcc3664e7225cd9a0c9`  
		Last Modified: Thu, 20 Mar 2025 17:13:38 GMT  
		Size: 219.6 MB (219626219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf8b73f14eb980724fb9d7bf85258fb217b283830be42478a9b3568dba0d04c`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 2.6 MB (2623287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b03f7279ad823cd486d51af379980cee7e282a325eccd1da0d3c4c8e04ced15`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 477.8 KB (477826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8caceee829e822020664f73defacbe1a11f4a7ab959c996441dd9bea449762`  
		Last Modified: Thu, 20 Mar 2025 17:13:44 GMT  
		Size: 331.5 MB (331539107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78331f47571e7685e8b70d6e31d76d24f7e0004a238897a1bf8d6cf228409`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8eaf90b2593de56257166eaf0f868d5c88bdad39d8832ce20bac2bad7f5e89`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87060e37c8b77f5f6cc4e0e1773d9dccc7360e8b1d8bc30d81aec2c7a7f026`  
		Last Modified: Thu, 20 Mar 2025 17:13:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f6a34d725083bb866a877574dad62c8a76981984173cf4c746c516a4bd414a`  
		Last Modified: Thu, 20 Mar 2025 17:13:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250320` - unknown; unknown

```console
$ docker pull odoo@sha256:c35d485d46b8e52e98298f87acb7421a64f53d2aa7af00f09c1644a2178c5e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38886981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04789fc649fc99fa5ece2512695449ce1c5eeb7f03865c5df30f4da1559b4514`

```dockerfile
```

-	Layers:
	-	`sha256:c514017c8090474d5f3936551ba8ddf56d4176d5da9c0cac88dcea042b52a898`  
		Last Modified: Thu, 20 Mar 2025 17:13:36 GMT  
		Size: 38.9 MB (38860263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7437f8df4750ea371236ea917a36963325eafbb43270369b86ca42d5dc6aba37`  
		Last Modified: Thu, 20 Mar 2025 17:13:35 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250320` - linux; arm64 variant v8

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

### `odoo:16.0-20250320` - unknown; unknown

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

## `odoo:17`

```console
$ docker pull odoo@sha256:b74295c9491a103d202d1ddef8ed78edb95e9c057414230abcfd4cccc89b7636
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
$ docker pull odoo@sha256:e1fde1c3d64596ca708f6d20c6e18553d8005314e6aba0d924bee0274a50e88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602540827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467934ca6d062381ede966869886f21cb2c798904e75ffb359a6b8e4154c4515`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e1cf0c07be1638b4efc0cac61262b9c483a3247f48aec95d764c0f424f28ca`  
		Last Modified: Thu, 20 Mar 2025 17:13:52 GMT  
		Size: 236.1 MB (236052005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91316351da6e66e833730fc931ad29efd21933bba699cf9e18a132c2957d3763`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 2.5 MB (2520293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cec8bd76128bfe37c7bb100e32aed80f57ae85ffa308a7c2094da21bf18a2d`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 478.9 KB (478927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144037137d9a4a16b4b00cb33af40555fd62a87c1f600e1f5b52b74c53469435`  
		Last Modified: Thu, 20 Mar 2025 17:13:51 GMT  
		Size: 334.0 MB (333951222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c22955ae3c38f1d52f9e5d53873a2117eae6af1f0a43e9d388d6773cd588b`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea01101a4520bbf7253ca373c889e13dabc89eef87fa4c33e789add45d7304`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd841422592ea8c9ed2475786fe8f6c0b5bd873fc20fbfdb45b0379fd0c638f`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d7db0c9bd638da214870db257f6e91d6fb81dff269de8880b0dc567c007c4d`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:38b9cf6c87fb141f919046850cd5732b733a718c27158bc385b643c8ac5e4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39766597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b6074cf7e21f034e6fddd894a698b88703441e91459c0ee2fbab02801ea570`

```dockerfile
```

-	Layers:
	-	`sha256:a73b87df1845418efd6870a4cc572fbea022061df85482258e7dfe58114c431d`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 39.7 MB (39739762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3a93071037bad3e3ba49a38534221af615ac41adaac8e5f1d5063cb0fbcc8a`  
		Last Modified: Thu, 20 Mar 2025 17:13:46 GMT  
		Size: 26.8 KB (26835 bytes)  
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
$ docker pull odoo@sha256:ff09670425b6db7c2c929a9b95c4b9c8981161433cdb463a0b3c0e5ffe930175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.4 MB (619383465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5b35d65a5a8ce27b82600388b80e06f5a38f261da4a1f46d643184500b8913`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
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
	-	`sha256:cac03071a94be7285c982a98542cac74ea31b152950b41f3f12740a91cd7454a`  
		Last Modified: Thu, 20 Mar 2025 17:33:06 GMT  
		Size: 335.7 MB (335696001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a4d1271046db533f073596d9a7e8645974b915efc8fed9b0d3ed09bfce224`  
		Last Modified: Thu, 20 Mar 2025 17:32:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764c1d4b0730370056a2ba540c973927823f94246d5fca044b8f29254e4b4354`  
		Last Modified: Thu, 20 Mar 2025 17:32:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4910c10d360d03c7d85b2f497828ce058c1c97d3d1593cd64feed1f98efef1bd`  
		Last Modified: Thu, 20 Mar 2025 17:32:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a1393bc53db4f76b806f6c92aa3bf7ed21b9668b40aff4f4e6753bf52b3e21`  
		Last Modified: Thu, 20 Mar 2025 17:32:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c93d314f7f8ea5929d87b05fddfd100507c39b2e53b9c99c995760df6d1be498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39774960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6bd88043b07ca00d015105658a44c105afd07625736872c3328c4173aa73eb`

```dockerfile
```

-	Layers:
	-	`sha256:ad6b11a0f8bd84f4ceb527eb4acd2a4d337ee2f716bc44d5e4b92c1c1b1cd61b`  
		Last Modified: Thu, 20 Mar 2025 17:32:57 GMT  
		Size: 39.7 MB (39748069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814244da0d826ff9aa874de8c8ea7ac56f1b657b13a3b1eb3dda36f95a7357e1`  
		Last Modified: Thu, 20 Mar 2025 17:32:54 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:b74295c9491a103d202d1ddef8ed78edb95e9c057414230abcfd4cccc89b7636
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
$ docker pull odoo@sha256:e1fde1c3d64596ca708f6d20c6e18553d8005314e6aba0d924bee0274a50e88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602540827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467934ca6d062381ede966869886f21cb2c798904e75ffb359a6b8e4154c4515`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e1cf0c07be1638b4efc0cac61262b9c483a3247f48aec95d764c0f424f28ca`  
		Last Modified: Thu, 20 Mar 2025 17:13:52 GMT  
		Size: 236.1 MB (236052005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91316351da6e66e833730fc931ad29efd21933bba699cf9e18a132c2957d3763`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 2.5 MB (2520293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cec8bd76128bfe37c7bb100e32aed80f57ae85ffa308a7c2094da21bf18a2d`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 478.9 KB (478927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144037137d9a4a16b4b00cb33af40555fd62a87c1f600e1f5b52b74c53469435`  
		Last Modified: Thu, 20 Mar 2025 17:13:51 GMT  
		Size: 334.0 MB (333951222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c22955ae3c38f1d52f9e5d53873a2117eae6af1f0a43e9d388d6773cd588b`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea01101a4520bbf7253ca373c889e13dabc89eef87fa4c33e789add45d7304`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd841422592ea8c9ed2475786fe8f6c0b5bd873fc20fbfdb45b0379fd0c638f`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d7db0c9bd638da214870db257f6e91d6fb81dff269de8880b0dc567c007c4d`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:38b9cf6c87fb141f919046850cd5732b733a718c27158bc385b643c8ac5e4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39766597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b6074cf7e21f034e6fddd894a698b88703441e91459c0ee2fbab02801ea570`

```dockerfile
```

-	Layers:
	-	`sha256:a73b87df1845418efd6870a4cc572fbea022061df85482258e7dfe58114c431d`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 39.7 MB (39739762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3a93071037bad3e3ba49a38534221af615ac41adaac8e5f1d5063cb0fbcc8a`  
		Last Modified: Thu, 20 Mar 2025 17:13:46 GMT  
		Size: 26.8 KB (26835 bytes)  
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
$ docker pull odoo@sha256:ff09670425b6db7c2c929a9b95c4b9c8981161433cdb463a0b3c0e5ffe930175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.4 MB (619383465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5b35d65a5a8ce27b82600388b80e06f5a38f261da4a1f46d643184500b8913`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
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
	-	`sha256:cac03071a94be7285c982a98542cac74ea31b152950b41f3f12740a91cd7454a`  
		Last Modified: Thu, 20 Mar 2025 17:33:06 GMT  
		Size: 335.7 MB (335696001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a4d1271046db533f073596d9a7e8645974b915efc8fed9b0d3ed09bfce224`  
		Last Modified: Thu, 20 Mar 2025 17:32:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764c1d4b0730370056a2ba540c973927823f94246d5fca044b8f29254e4b4354`  
		Last Modified: Thu, 20 Mar 2025 17:32:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4910c10d360d03c7d85b2f497828ce058c1c97d3d1593cd64feed1f98efef1bd`  
		Last Modified: Thu, 20 Mar 2025 17:32:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a1393bc53db4f76b806f6c92aa3bf7ed21b9668b40aff4f4e6753bf52b3e21`  
		Last Modified: Thu, 20 Mar 2025 17:32:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c93d314f7f8ea5929d87b05fddfd100507c39b2e53b9c99c995760df6d1be498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39774960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6bd88043b07ca00d015105658a44c105afd07625736872c3328c4173aa73eb`

```dockerfile
```

-	Layers:
	-	`sha256:ad6b11a0f8bd84f4ceb527eb4acd2a4d337ee2f716bc44d5e4b92c1c1b1cd61b`  
		Last Modified: Thu, 20 Mar 2025 17:32:57 GMT  
		Size: 39.7 MB (39748069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814244da0d826ff9aa874de8c8ea7ac56f1b657b13a3b1eb3dda36f95a7357e1`  
		Last Modified: Thu, 20 Mar 2025 17:32:54 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250320`

```console
$ docker pull odoo@sha256:b74295c9491a103d202d1ddef8ed78edb95e9c057414230abcfd4cccc89b7636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250320` - linux; amd64

```console
$ docker pull odoo@sha256:e1fde1c3d64596ca708f6d20c6e18553d8005314e6aba0d924bee0274a50e88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602540827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467934ca6d062381ede966869886f21cb2c798904e75ffb359a6b8e4154c4515`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e1cf0c07be1638b4efc0cac61262b9c483a3247f48aec95d764c0f424f28ca`  
		Last Modified: Thu, 20 Mar 2025 17:13:52 GMT  
		Size: 236.1 MB (236052005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91316351da6e66e833730fc931ad29efd21933bba699cf9e18a132c2957d3763`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 2.5 MB (2520293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cec8bd76128bfe37c7bb100e32aed80f57ae85ffa308a7c2094da21bf18a2d`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 478.9 KB (478927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144037137d9a4a16b4b00cb33af40555fd62a87c1f600e1f5b52b74c53469435`  
		Last Modified: Thu, 20 Mar 2025 17:13:51 GMT  
		Size: 334.0 MB (333951222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c22955ae3c38f1d52f9e5d53873a2117eae6af1f0a43e9d388d6773cd588b`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea01101a4520bbf7253ca373c889e13dabc89eef87fa4c33e789add45d7304`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd841422592ea8c9ed2475786fe8f6c0b5bd873fc20fbfdb45b0379fd0c638f`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d7db0c9bd638da214870db257f6e91d6fb81dff269de8880b0dc567c007c4d`  
		Last Modified: Thu, 20 Mar 2025 17:13:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250320` - unknown; unknown

```console
$ docker pull odoo@sha256:38b9cf6c87fb141f919046850cd5732b733a718c27158bc385b643c8ac5e4151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39766597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b6074cf7e21f034e6fddd894a698b88703441e91459c0ee2fbab02801ea570`

```dockerfile
```

-	Layers:
	-	`sha256:a73b87df1845418efd6870a4cc572fbea022061df85482258e7dfe58114c431d`  
		Last Modified: Thu, 20 Mar 2025 17:13:47 GMT  
		Size: 39.7 MB (39739762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3a93071037bad3e3ba49a38534221af615ac41adaac8e5f1d5063cb0fbcc8a`  
		Last Modified: Thu, 20 Mar 2025 17:13:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250320` - linux; arm64 variant v8

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

### `odoo:17.0-20250320` - unknown; unknown

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

### `odoo:17.0-20250320` - linux; ppc64le

```console
$ docker pull odoo@sha256:ff09670425b6db7c2c929a9b95c4b9c8981161433cdb463a0b3c0e5ffe930175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.4 MB (619383465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5b35d65a5a8ce27b82600388b80e06f5a38f261da4a1f46d643184500b8913`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=17.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=c427512d5be13d9f7de37564f291b96edc556919
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
	-	`sha256:cac03071a94be7285c982a98542cac74ea31b152950b41f3f12740a91cd7454a`  
		Last Modified: Thu, 20 Mar 2025 17:33:06 GMT  
		Size: 335.7 MB (335696001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a4d1271046db533f073596d9a7e8645974b915efc8fed9b0d3ed09bfce224`  
		Last Modified: Thu, 20 Mar 2025 17:32:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764c1d4b0730370056a2ba540c973927823f94246d5fca044b8f29254e4b4354`  
		Last Modified: Thu, 20 Mar 2025 17:32:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4910c10d360d03c7d85b2f497828ce058c1c97d3d1593cd64feed1f98efef1bd`  
		Last Modified: Thu, 20 Mar 2025 17:32:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a1393bc53db4f76b806f6c92aa3bf7ed21b9668b40aff4f4e6753bf52b3e21`  
		Last Modified: Thu, 20 Mar 2025 17:32:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250320` - unknown; unknown

```console
$ docker pull odoo@sha256:c93d314f7f8ea5929d87b05fddfd100507c39b2e53b9c99c995760df6d1be498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39774960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6bd88043b07ca00d015105658a44c105afd07625736872c3328c4173aa73eb`

```dockerfile
```

-	Layers:
	-	`sha256:ad6b11a0f8bd84f4ceb527eb4acd2a4d337ee2f716bc44d5e4b92c1c1b1cd61b`  
		Last Modified: Thu, 20 Mar 2025 17:32:57 GMT  
		Size: 39.7 MB (39748069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814244da0d826ff9aa874de8c8ea7ac56f1b657b13a3b1eb3dda36f95a7357e1`  
		Last Modified: Thu, 20 Mar 2025 17:32:54 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:89b4f1047a5d378f77ec932300edf3e7b3333a4c488caf0d0b56318b65e9f7be
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
$ docker pull odoo@sha256:9113f20e2b2df5bdf380bdab69f8e07681f1f5eae99be3a6ef1c14589db70ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.6 MB (674564801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852d128f4309cbfffa8b7355b2f6b827bde6b38257f5378305458723f207d1f1`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3a547727e5e1d87cabfc53d8cc41a94b2f74d7369c5240ef42b1209a10756`  
		Last Modified: Thu, 20 Mar 2025 17:14:58 GMT  
		Size: 256.9 MB (256918465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774a827cff4a81b72b45d82721190975d469a29faa35ed3beccc136e74cb5a4a`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 16.7 MB (16679969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fd936ba40931ad7fd426bbd90fe6f37367f253faae1f121056da0a8a3d69d`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 478.6 KB (478594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fa1c2310434deef52e6e717970777caf3dda493af94cc0b02f8c460e744f2c`  
		Last Modified: Thu, 20 Mar 2025 17:15:02 GMT  
		Size: 370.7 MB (370731044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687b48e647c51eeda3f448de31cda32a73f5e68161902154edb81d29ccb69a88`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd27b84a9ac66dbbedaba73ad05ae00bcc145a55f34d2990700ca3babd392e65`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b9c2054f2d673e5a061fe94d20d7ff219fdcb5427cd7a79222a593f97cf5ee`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d500071f7cbd250f9efccb197497e068b1fb4bcfe58d8f0b83d31d35e8a96`  
		Last Modified: Thu, 20 Mar 2025 17:14:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:063d2bb2ebfc1810de5deebd170d24913f8b2ce022ddc53c7d038e859bdbc158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59165515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941bd55c3d86af5aa18b111b1dd8cc90c3e25e9b65cd4186aa00bd8ad895f37c`

```dockerfile
```

-	Layers:
	-	`sha256:dc44d7d37a8a0f1a86053c323f7fb9f6a19e3bd2c8b698eebf33938f31a60349`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 59.1 MB (59138379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43dafd97fdd9152dbee3410a0599d0dffe46214b2544c8bad2c2bdf85ad95d5e`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 27.1 KB (27136 bytes)  
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
$ docker pull odoo@sha256:8ca3fe7f139299b22a707f549698d1366be6c5821170e39cf5891cb5278becb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.2 MB (691200766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d09efad1c1bfde2715bbba86dca46b535e1e69fd533b31dca729abbd3f0b9f`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:67abd1eedb8a5f65db44c48c528cde4a5e16318c4802bdd398cdd493e5eec8b8`  
		Last Modified: Thu, 20 Mar 2025 17:23:40 GMT  
		Size: 371.3 MB (371262700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b9e5146152fa553d7f4d1cad69b22a385d6410f1563271bda17fa8e183637`  
		Last Modified: Thu, 20 Mar 2025 17:23:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c224f4e0285d44acf9764bd35baecdb3228c8c668f7d486adf4f98df97612`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a1938c7725bfa722e2206f6b2b077dc8b70f0a6cb6990963065fcc01cebd30`  
		Last Modified: Thu, 20 Mar 2025 17:23:15 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844c9eaa4fead6de7aa4e21b61d85978c724987981b032317998ff8fdc1dc41`  
		Last Modified: Thu, 20 Mar 2025 17:23:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:804d41500241ebb36f0586d704a0d8207e9ba1c4bb264c12674c2eaa4f9c2a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59173719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c10dd32d6e8ae97f16d6f9be75b8994c5f65bdae2800c8e5cf4cf2c3ccbbed0`

```dockerfile
```

-	Layers:
	-	`sha256:cb0dafcc9e72ce50387cb91ac4bcf8c3e2d96ec9868f1ab114968be4aee0070f`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 59.1 MB (59146522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccf84f45ef2f34bc054c6680073cec3780a97810b7794d5cefcd51bd4d9eea5`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:89b4f1047a5d378f77ec932300edf3e7b3333a4c488caf0d0b56318b65e9f7be
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
$ docker pull odoo@sha256:9113f20e2b2df5bdf380bdab69f8e07681f1f5eae99be3a6ef1c14589db70ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.6 MB (674564801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852d128f4309cbfffa8b7355b2f6b827bde6b38257f5378305458723f207d1f1`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3a547727e5e1d87cabfc53d8cc41a94b2f74d7369c5240ef42b1209a10756`  
		Last Modified: Thu, 20 Mar 2025 17:14:58 GMT  
		Size: 256.9 MB (256918465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774a827cff4a81b72b45d82721190975d469a29faa35ed3beccc136e74cb5a4a`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 16.7 MB (16679969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fd936ba40931ad7fd426bbd90fe6f37367f253faae1f121056da0a8a3d69d`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 478.6 KB (478594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fa1c2310434deef52e6e717970777caf3dda493af94cc0b02f8c460e744f2c`  
		Last Modified: Thu, 20 Mar 2025 17:15:02 GMT  
		Size: 370.7 MB (370731044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687b48e647c51eeda3f448de31cda32a73f5e68161902154edb81d29ccb69a88`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd27b84a9ac66dbbedaba73ad05ae00bcc145a55f34d2990700ca3babd392e65`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b9c2054f2d673e5a061fe94d20d7ff219fdcb5427cd7a79222a593f97cf5ee`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d500071f7cbd250f9efccb197497e068b1fb4bcfe58d8f0b83d31d35e8a96`  
		Last Modified: Thu, 20 Mar 2025 17:14:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:063d2bb2ebfc1810de5deebd170d24913f8b2ce022ddc53c7d038e859bdbc158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59165515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941bd55c3d86af5aa18b111b1dd8cc90c3e25e9b65cd4186aa00bd8ad895f37c`

```dockerfile
```

-	Layers:
	-	`sha256:dc44d7d37a8a0f1a86053c323f7fb9f6a19e3bd2c8b698eebf33938f31a60349`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 59.1 MB (59138379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43dafd97fdd9152dbee3410a0599d0dffe46214b2544c8bad2c2bdf85ad95d5e`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 27.1 KB (27136 bytes)  
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
$ docker pull odoo@sha256:8ca3fe7f139299b22a707f549698d1366be6c5821170e39cf5891cb5278becb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.2 MB (691200766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d09efad1c1bfde2715bbba86dca46b535e1e69fd533b31dca729abbd3f0b9f`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:67abd1eedb8a5f65db44c48c528cde4a5e16318c4802bdd398cdd493e5eec8b8`  
		Last Modified: Thu, 20 Mar 2025 17:23:40 GMT  
		Size: 371.3 MB (371262700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b9e5146152fa553d7f4d1cad69b22a385d6410f1563271bda17fa8e183637`  
		Last Modified: Thu, 20 Mar 2025 17:23:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c224f4e0285d44acf9764bd35baecdb3228c8c668f7d486adf4f98df97612`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a1938c7725bfa722e2206f6b2b077dc8b70f0a6cb6990963065fcc01cebd30`  
		Last Modified: Thu, 20 Mar 2025 17:23:15 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844c9eaa4fead6de7aa4e21b61d85978c724987981b032317998ff8fdc1dc41`  
		Last Modified: Thu, 20 Mar 2025 17:23:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:804d41500241ebb36f0586d704a0d8207e9ba1c4bb264c12674c2eaa4f9c2a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59173719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c10dd32d6e8ae97f16d6f9be75b8994c5f65bdae2800c8e5cf4cf2c3ccbbed0`

```dockerfile
```

-	Layers:
	-	`sha256:cb0dafcc9e72ce50387cb91ac4bcf8c3e2d96ec9868f1ab114968be4aee0070f`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 59.1 MB (59146522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccf84f45ef2f34bc054c6680073cec3780a97810b7794d5cefcd51bd4d9eea5`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250320`

```console
$ docker pull odoo@sha256:89b4f1047a5d378f77ec932300edf3e7b3333a4c488caf0d0b56318b65e9f7be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250320` - linux; amd64

```console
$ docker pull odoo@sha256:9113f20e2b2df5bdf380bdab69f8e07681f1f5eae99be3a6ef1c14589db70ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.6 MB (674564801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852d128f4309cbfffa8b7355b2f6b827bde6b38257f5378305458723f207d1f1`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3a547727e5e1d87cabfc53d8cc41a94b2f74d7369c5240ef42b1209a10756`  
		Last Modified: Thu, 20 Mar 2025 17:14:58 GMT  
		Size: 256.9 MB (256918465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774a827cff4a81b72b45d82721190975d469a29faa35ed3beccc136e74cb5a4a`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 16.7 MB (16679969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fd936ba40931ad7fd426bbd90fe6f37367f253faae1f121056da0a8a3d69d`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 478.6 KB (478594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fa1c2310434deef52e6e717970777caf3dda493af94cc0b02f8c460e744f2c`  
		Last Modified: Thu, 20 Mar 2025 17:15:02 GMT  
		Size: 370.7 MB (370731044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687b48e647c51eeda3f448de31cda32a73f5e68161902154edb81d29ccb69a88`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd27b84a9ac66dbbedaba73ad05ae00bcc145a55f34d2990700ca3babd392e65`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b9c2054f2d673e5a061fe94d20d7ff219fdcb5427cd7a79222a593f97cf5ee`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d500071f7cbd250f9efccb197497e068b1fb4bcfe58d8f0b83d31d35e8a96`  
		Last Modified: Thu, 20 Mar 2025 17:14:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250320` - unknown; unknown

```console
$ docker pull odoo@sha256:063d2bb2ebfc1810de5deebd170d24913f8b2ce022ddc53c7d038e859bdbc158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59165515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941bd55c3d86af5aa18b111b1dd8cc90c3e25e9b65cd4186aa00bd8ad895f37c`

```dockerfile
```

-	Layers:
	-	`sha256:dc44d7d37a8a0f1a86053c323f7fb9f6a19e3bd2c8b698eebf33938f31a60349`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 59.1 MB (59138379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43dafd97fdd9152dbee3410a0599d0dffe46214b2544c8bad2c2bdf85ad95d5e`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250320` - linux; arm64 variant v8

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

### `odoo:18.0-20250320` - unknown; unknown

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

### `odoo:18.0-20250320` - linux; ppc64le

```console
$ docker pull odoo@sha256:8ca3fe7f139299b22a707f549698d1366be6c5821170e39cf5891cb5278becb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.2 MB (691200766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d09efad1c1bfde2715bbba86dca46b535e1e69fd533b31dca729abbd3f0b9f`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:67abd1eedb8a5f65db44c48c528cde4a5e16318c4802bdd398cdd493e5eec8b8`  
		Last Modified: Thu, 20 Mar 2025 17:23:40 GMT  
		Size: 371.3 MB (371262700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b9e5146152fa553d7f4d1cad69b22a385d6410f1563271bda17fa8e183637`  
		Last Modified: Thu, 20 Mar 2025 17:23:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c224f4e0285d44acf9764bd35baecdb3228c8c668f7d486adf4f98df97612`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a1938c7725bfa722e2206f6b2b077dc8b70f0a6cb6990963065fcc01cebd30`  
		Last Modified: Thu, 20 Mar 2025 17:23:15 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844c9eaa4fead6de7aa4e21b61d85978c724987981b032317998ff8fdc1dc41`  
		Last Modified: Thu, 20 Mar 2025 17:23:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250320` - unknown; unknown

```console
$ docker pull odoo@sha256:804d41500241ebb36f0586d704a0d8207e9ba1c4bb264c12674c2eaa4f9c2a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59173719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c10dd32d6e8ae97f16d6f9be75b8994c5f65bdae2800c8e5cf4cf2c3ccbbed0`

```dockerfile
```

-	Layers:
	-	`sha256:cb0dafcc9e72ce50387cb91ac4bcf8c3e2d96ec9868f1ab114968be4aee0070f`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 59.1 MB (59146522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccf84f45ef2f34bc054c6680073cec3780a97810b7794d5cefcd51bd4d9eea5`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:89b4f1047a5d378f77ec932300edf3e7b3333a4c488caf0d0b56318b65e9f7be
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
$ docker pull odoo@sha256:9113f20e2b2df5bdf380bdab69f8e07681f1f5eae99be3a6ef1c14589db70ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.6 MB (674564801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852d128f4309cbfffa8b7355b2f6b827bde6b38257f5378305458723f207d1f1`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=amd64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d3a547727e5e1d87cabfc53d8cc41a94b2f74d7369c5240ef42b1209a10756`  
		Last Modified: Thu, 20 Mar 2025 17:14:58 GMT  
		Size: 256.9 MB (256918465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774a827cff4a81b72b45d82721190975d469a29faa35ed3beccc136e74cb5a4a`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 16.7 MB (16679969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fd936ba40931ad7fd426bbd90fe6f37367f253faae1f121056da0a8a3d69d`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 478.6 KB (478594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fa1c2310434deef52e6e717970777caf3dda493af94cc0b02f8c460e744f2c`  
		Last Modified: Thu, 20 Mar 2025 17:15:02 GMT  
		Size: 370.7 MB (370731044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687b48e647c51eeda3f448de31cda32a73f5e68161902154edb81d29ccb69a88`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd27b84a9ac66dbbedaba73ad05ae00bcc145a55f34d2990700ca3babd392e65`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b9c2054f2d673e5a061fe94d20d7ff219fdcb5427cd7a79222a593f97cf5ee`  
		Last Modified: Thu, 20 Mar 2025 17:14:54 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d500071f7cbd250f9efccb197497e068b1fb4bcfe58d8f0b83d31d35e8a96`  
		Last Modified: Thu, 20 Mar 2025 17:14:55 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:063d2bb2ebfc1810de5deebd170d24913f8b2ce022ddc53c7d038e859bdbc158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59165515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941bd55c3d86af5aa18b111b1dd8cc90c3e25e9b65cd4186aa00bd8ad895f37c`

```dockerfile
```

-	Layers:
	-	`sha256:dc44d7d37a8a0f1a86053c323f7fb9f6a19e3bd2c8b698eebf33938f31a60349`  
		Last Modified: Thu, 20 Mar 2025 17:14:53 GMT  
		Size: 59.1 MB (59138379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43dafd97fdd9152dbee3410a0599d0dffe46214b2544c8bad2c2bdf85ad95d5e`  
		Last Modified: Thu, 20 Mar 2025 17:14:52 GMT  
		Size: 27.1 KB (27136 bytes)  
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
$ docker pull odoo@sha256:8ca3fe7f139299b22a707f549698d1366be6c5821170e39cf5891cb5278becb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.2 MB (691200766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d09efad1c1bfde2715bbba86dca46b535e1e69fd533b31dca729abbd3f0b9f`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=ppc64le
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
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
	-	`sha256:67abd1eedb8a5f65db44c48c528cde4a5e16318c4802bdd398cdd493e5eec8b8`  
		Last Modified: Thu, 20 Mar 2025 17:23:40 GMT  
		Size: 371.3 MB (371262700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b9e5146152fa553d7f4d1cad69b22a385d6410f1563271bda17fa8e183637`  
		Last Modified: Thu, 20 Mar 2025 17:23:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c224f4e0285d44acf9764bd35baecdb3228c8c668f7d486adf4f98df97612`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a1938c7725bfa722e2206f6b2b077dc8b70f0a6cb6990963065fcc01cebd30`  
		Last Modified: Thu, 20 Mar 2025 17:23:15 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844c9eaa4fead6de7aa4e21b61d85978c724987981b032317998ff8fdc1dc41`  
		Last Modified: Thu, 20 Mar 2025 17:23:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:804d41500241ebb36f0586d704a0d8207e9ba1c4bb264c12674c2eaa4f9c2a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59173719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c10dd32d6e8ae97f16d6f9be75b8994c5f65bdae2800c8e5cf4cf2c3ccbbed0`

```dockerfile
```

-	Layers:
	-	`sha256:cb0dafcc9e72ce50387cb91ac4bcf8c3e2d96ec9868f1ab114968be4aee0070f`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 59.1 MB (59146522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccf84f45ef2f34bc054c6680073cec3780a97810b7794d5cefcd51bd4d9eea5`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json
