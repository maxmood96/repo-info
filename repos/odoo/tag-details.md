<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250819`](#odoo160-20250819)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250819`](#odoo170-20250819)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250819`](#odoo180-20250819)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:33ed10c152bf6c76ae78bd9a3a2e9fec02f0a7d7c321de3a30e97216bf91e678
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:2a5c796375c99a3501c5ce5331aaa03e11081f2b095945344deba0c6e340ce99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585312648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd2dc9af71db771e4b6dbfac4948cefe9c4ebd40b910428c44e509b669227d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b41fa7b3781cf4e1d2ccda46608f8f7cd16806ce02227f21adb87f98026c64`  
		Last Modified: Tue, 19 Aug 2025 19:12:38 GMT  
		Size: 219.6 MB (219626043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3055daa1c817c13c4d7b55ab4b060cc5e86d729807a87e7f8e645387206db8`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 2.6 MB (2632418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f569f4af5f7de620d3699fe3a75da2ad4ea1d83584246e417099acd0ec435ab`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 479.3 KB (479317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08586793517190ff64406c433770cba1d7d8d21af824230437d0260c51d12b4d`  
		Last Modified: Tue, 19 Aug 2025 19:12:48 GMT  
		Size: 332.3 MB (332316320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f6b5aeadb97a699fdddf1cf617c334385023db8aa194aecd32b2367adaf4a6`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f60eec26e0832b30b927ff2f12fd532b5f07970917db6c3c9500cb4d1f5af6`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6def8a0cb7c0d1c6bb11109530660fac4d73b43333229d78943a49c76159c`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06ad6b533db5dc87b04b87f06cfc4c872b0a3e919f296a23ef009fab21dd038`  
		Last Modified: Tue, 19 Aug 2025 16:45:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:1414ecd22822e70c205abe5bf7c0d4aaee6c31716dbbf0cc9f7493fd8a6885b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68893a2323e782b92ecf8fefcd0cd6e8fbca1699cdf0f94b3dff987858b9adc`

```dockerfile
```

-	Layers:
	-	`sha256:4c566e66ab224d64c0b474b3e64a86b129bff013d1ca3f4fb6c968bae1aae94d`  
		Last Modified: Tue, 19 Aug 2025 19:12:26 GMT  
		Size: 39.5 MB (39531942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46323f8953f3a5ef106fc2dd5f9c6926f822c24bad387ebebdbf481989a6fe35`  
		Last Modified: Tue, 19 Aug 2025 19:12:28 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a7baeafca3e21666e41b33d7f3fb6187d9f998711036b34ddd21786f68cdfcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580763695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002e720016a3f7fc461be30990ebc0a515b3f54755c9635952ead4254df1b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5867d8bc0929feba262d9b8266362ada6cd80d2b5169017d578ae2bec08c70`  
		Last Modified: Tue, 19 Aug 2025 19:13:13 GMT  
		Size: 216.9 MB (216919368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e689e6f3a4b44284e1f83173f09a5eb4c7b65d543d7716c8b80ea70f9094d`  
		Last Modified: Tue, 19 Aug 2025 16:59:09 GMT  
		Size: 2.6 MB (2639118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3d913835ce316fce598cbbe6920a9f52ec39b930f5534f1fd1ea7ed0345277`  
		Last Modified: Tue, 19 Aug 2025 16:59:09 GMT  
		Size: 479.3 KB (479337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48afa5f9170d08673858648769d2aab74e163eea4a1a76cda261ff59015326d6`  
		Last Modified: Tue, 19 Aug 2025 19:12:58 GMT  
		Size: 332.0 MB (331972948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8a49d3ebc7e4755dba3b2f9bf173588850056c2a58066b0252d7b2750aa53c`  
		Last Modified: Tue, 19 Aug 2025 16:59:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dc627e687a0810687ed34b1252f2fb90f878b1808eb531359c69787ea1be1e`  
		Last Modified: Tue, 19 Aug 2025 16:59:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a1ffb8b356dd2ae591ddb9ba738a933638a0154d8a97ff2903ad84cf23ba81`  
		Last Modified: Tue, 19 Aug 2025 16:59:10 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4727881c142efad8105af73ff40cacdec11404b8b5824a8b5e9ed5dd4ce242db`  
		Last Modified: Tue, 19 Aug 2025 16:59:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:3917b6c82f21cba4a6796222c3038fc76db2758b041540e13d211330c41d9e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f7949a05e03f54926752c1d88186b94b8d7ba6ddcd0af1602eda746b59c380`

```dockerfile
```

-	Layers:
	-	`sha256:232a2685cbea3735e39b2721dc8a9331102f41b97eb841ea7310b5579490c62b`  
		Last Modified: Tue, 19 Aug 2025 19:13:24 GMT  
		Size: 39.5 MB (39538408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9d429d612aa94d8c86bd7a119b034ae7f8dbaabab5afd232639b2598c9f1eb`  
		Last Modified: Tue, 19 Aug 2025 19:13:25 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:33ed10c152bf6c76ae78bd9a3a2e9fec02f0a7d7c321de3a30e97216bf91e678
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:2a5c796375c99a3501c5ce5331aaa03e11081f2b095945344deba0c6e340ce99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585312648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd2dc9af71db771e4b6dbfac4948cefe9c4ebd40b910428c44e509b669227d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b41fa7b3781cf4e1d2ccda46608f8f7cd16806ce02227f21adb87f98026c64`  
		Last Modified: Tue, 19 Aug 2025 19:12:38 GMT  
		Size: 219.6 MB (219626043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3055daa1c817c13c4d7b55ab4b060cc5e86d729807a87e7f8e645387206db8`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 2.6 MB (2632418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f569f4af5f7de620d3699fe3a75da2ad4ea1d83584246e417099acd0ec435ab`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 479.3 KB (479317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08586793517190ff64406c433770cba1d7d8d21af824230437d0260c51d12b4d`  
		Last Modified: Tue, 19 Aug 2025 19:12:48 GMT  
		Size: 332.3 MB (332316320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f6b5aeadb97a699fdddf1cf617c334385023db8aa194aecd32b2367adaf4a6`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f60eec26e0832b30b927ff2f12fd532b5f07970917db6c3c9500cb4d1f5af6`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6def8a0cb7c0d1c6bb11109530660fac4d73b43333229d78943a49c76159c`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06ad6b533db5dc87b04b87f06cfc4c872b0a3e919f296a23ef009fab21dd038`  
		Last Modified: Tue, 19 Aug 2025 16:45:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1414ecd22822e70c205abe5bf7c0d4aaee6c31716dbbf0cc9f7493fd8a6885b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68893a2323e782b92ecf8fefcd0cd6e8fbca1699cdf0f94b3dff987858b9adc`

```dockerfile
```

-	Layers:
	-	`sha256:4c566e66ab224d64c0b474b3e64a86b129bff013d1ca3f4fb6c968bae1aae94d`  
		Last Modified: Tue, 19 Aug 2025 19:12:26 GMT  
		Size: 39.5 MB (39531942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46323f8953f3a5ef106fc2dd5f9c6926f822c24bad387ebebdbf481989a6fe35`  
		Last Modified: Tue, 19 Aug 2025 19:12:28 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a7baeafca3e21666e41b33d7f3fb6187d9f998711036b34ddd21786f68cdfcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580763695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002e720016a3f7fc461be30990ebc0a515b3f54755c9635952ead4254df1b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5867d8bc0929feba262d9b8266362ada6cd80d2b5169017d578ae2bec08c70`  
		Last Modified: Tue, 19 Aug 2025 19:13:13 GMT  
		Size: 216.9 MB (216919368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e689e6f3a4b44284e1f83173f09a5eb4c7b65d543d7716c8b80ea70f9094d`  
		Last Modified: Tue, 19 Aug 2025 16:59:09 GMT  
		Size: 2.6 MB (2639118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3d913835ce316fce598cbbe6920a9f52ec39b930f5534f1fd1ea7ed0345277`  
		Last Modified: Tue, 19 Aug 2025 16:59:09 GMT  
		Size: 479.3 KB (479337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48afa5f9170d08673858648769d2aab74e163eea4a1a76cda261ff59015326d6`  
		Last Modified: Tue, 19 Aug 2025 19:12:58 GMT  
		Size: 332.0 MB (331972948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8a49d3ebc7e4755dba3b2f9bf173588850056c2a58066b0252d7b2750aa53c`  
		Last Modified: Tue, 19 Aug 2025 16:59:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dc627e687a0810687ed34b1252f2fb90f878b1808eb531359c69787ea1be1e`  
		Last Modified: Tue, 19 Aug 2025 16:59:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a1ffb8b356dd2ae591ddb9ba738a933638a0154d8a97ff2903ad84cf23ba81`  
		Last Modified: Tue, 19 Aug 2025 16:59:10 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4727881c142efad8105af73ff40cacdec11404b8b5824a8b5e9ed5dd4ce242db`  
		Last Modified: Tue, 19 Aug 2025 16:59:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3917b6c82f21cba4a6796222c3038fc76db2758b041540e13d211330c41d9e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f7949a05e03f54926752c1d88186b94b8d7ba6ddcd0af1602eda746b59c380`

```dockerfile
```

-	Layers:
	-	`sha256:232a2685cbea3735e39b2721dc8a9331102f41b97eb841ea7310b5579490c62b`  
		Last Modified: Tue, 19 Aug 2025 19:13:24 GMT  
		Size: 39.5 MB (39538408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9d429d612aa94d8c86bd7a119b034ae7f8dbaabab5afd232639b2598c9f1eb`  
		Last Modified: Tue, 19 Aug 2025 19:13:25 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250819`

```console
$ docker pull odoo@sha256:33ed10c152bf6c76ae78bd9a3a2e9fec02f0a7d7c321de3a30e97216bf91e678
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250819` - linux; amd64

```console
$ docker pull odoo@sha256:2a5c796375c99a3501c5ce5331aaa03e11081f2b095945344deba0c6e340ce99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585312648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd2dc9af71db771e4b6dbfac4948cefe9c4ebd40b910428c44e509b669227d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b41fa7b3781cf4e1d2ccda46608f8f7cd16806ce02227f21adb87f98026c64`  
		Last Modified: Tue, 19 Aug 2025 19:12:38 GMT  
		Size: 219.6 MB (219626043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3055daa1c817c13c4d7b55ab4b060cc5e86d729807a87e7f8e645387206db8`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 2.6 MB (2632418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f569f4af5f7de620d3699fe3a75da2ad4ea1d83584246e417099acd0ec435ab`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 479.3 KB (479317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08586793517190ff64406c433770cba1d7d8d21af824230437d0260c51d12b4d`  
		Last Modified: Tue, 19 Aug 2025 19:12:48 GMT  
		Size: 332.3 MB (332316320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f6b5aeadb97a699fdddf1cf617c334385023db8aa194aecd32b2367adaf4a6`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f60eec26e0832b30b927ff2f12fd532b5f07970917db6c3c9500cb4d1f5af6`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6def8a0cb7c0d1c6bb11109530660fac4d73b43333229d78943a49c76159c`  
		Last Modified: Tue, 19 Aug 2025 16:45:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06ad6b533db5dc87b04b87f06cfc4c872b0a3e919f296a23ef009fab21dd038`  
		Last Modified: Tue, 19 Aug 2025 16:45:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:1414ecd22822e70c205abe5bf7c0d4aaee6c31716dbbf0cc9f7493fd8a6885b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68893a2323e782b92ecf8fefcd0cd6e8fbca1699cdf0f94b3dff987858b9adc`

```dockerfile
```

-	Layers:
	-	`sha256:4c566e66ab224d64c0b474b3e64a86b129bff013d1ca3f4fb6c968bae1aae94d`  
		Last Modified: Tue, 19 Aug 2025 19:12:26 GMT  
		Size: 39.5 MB (39531942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46323f8953f3a5ef106fc2dd5f9c6926f822c24bad387ebebdbf481989a6fe35`  
		Last Modified: Tue, 19 Aug 2025 19:12:28 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250819` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a7baeafca3e21666e41b33d7f3fb6187d9f998711036b34ddd21786f68cdfcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580763695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002e720016a3f7fc461be30990ebc0a515b3f54755c9635952ead4254df1b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5867d8bc0929feba262d9b8266362ada6cd80d2b5169017d578ae2bec08c70`  
		Last Modified: Tue, 19 Aug 2025 19:13:13 GMT  
		Size: 216.9 MB (216919368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e689e6f3a4b44284e1f83173f09a5eb4c7b65d543d7716c8b80ea70f9094d`  
		Last Modified: Tue, 19 Aug 2025 16:59:09 GMT  
		Size: 2.6 MB (2639118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3d913835ce316fce598cbbe6920a9f52ec39b930f5534f1fd1ea7ed0345277`  
		Last Modified: Tue, 19 Aug 2025 16:59:09 GMT  
		Size: 479.3 KB (479337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48afa5f9170d08673858648769d2aab74e163eea4a1a76cda261ff59015326d6`  
		Last Modified: Tue, 19 Aug 2025 19:12:58 GMT  
		Size: 332.0 MB (331972948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8a49d3ebc7e4755dba3b2f9bf173588850056c2a58066b0252d7b2750aa53c`  
		Last Modified: Tue, 19 Aug 2025 16:59:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dc627e687a0810687ed34b1252f2fb90f878b1808eb531359c69787ea1be1e`  
		Last Modified: Tue, 19 Aug 2025 16:59:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a1ffb8b356dd2ae591ddb9ba738a933638a0154d8a97ff2903ad84cf23ba81`  
		Last Modified: Tue, 19 Aug 2025 16:59:10 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4727881c142efad8105af73ff40cacdec11404b8b5824a8b5e9ed5dd4ce242db`  
		Last Modified: Tue, 19 Aug 2025 16:59:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:3917b6c82f21cba4a6796222c3038fc76db2758b041540e13d211330c41d9e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f7949a05e03f54926752c1d88186b94b8d7ba6ddcd0af1602eda746b59c380`

```dockerfile
```

-	Layers:
	-	`sha256:232a2685cbea3735e39b2721dc8a9331102f41b97eb841ea7310b5579490c62b`  
		Last Modified: Tue, 19 Aug 2025 19:13:24 GMT  
		Size: 39.5 MB (39538408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e9d429d612aa94d8c86bd7a119b034ae7f8dbaabab5afd232639b2598c9f1eb`  
		Last Modified: Tue, 19 Aug 2025 19:13:25 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:44d432c3dfff3d022df16945526c55b230f9d8baa9d5e3f36da2eb69a4b1eea1
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
$ docker pull odoo@sha256:aa17a5acd75fd372c20c674157afbe690795d8e91fa44fa4f6f84496aa89d479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605854096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceba6159458f361ad244a42135397e27c1a68742abc0557f15d441b82d42208a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29318572e8a89f691681090fc2030a21dc9dade302a307ffe1921aaab8407ec`  
		Last Modified: Tue, 19 Aug 2025 19:13:27 GMT  
		Size: 234.7 MB (234712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ee7b4e65e561a01aa736a46eda8e1bd1c926f51f5e2a33f1161011d0bb377`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 2.5 MB (2532617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9db8f08a8a93c50e8e3cbc9ed6297fe068914eb1d16bd20741ad99f4099e82`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 480.4 KB (480414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f91a657a585a56aaa1305cdf295400da8c46bb0881b3bc39a5cbcaa717053f`  
		Last Modified: Tue, 19 Aug 2025 19:12:51 GMT  
		Size: 338.6 MB (338589244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830894130eef75908084ffc6467a13d50f86f8707f2b34ce8c8c15f7507a0a84`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc12572f6d284b48cba20cc27e20a0ba92e30b7226369cde64bdab1115e8d13`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc1ae70b7f95c082faf8068dc5b8f9fb2c4a4b03acac5ab01821e39740d6a`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50589ceed2a5ad1a5cb38fddded3d91cce2e15bd5acfaac4ba015632b89d4a2e`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d7d92cb4bbf1a39d844fd4289017d79dd099d501563736866627953a5e904f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a108fef8a8a3f430fbb33908d5a9bf6b263253fc87ff31b33500f706bef58d`

```dockerfile
```

-	Layers:
	-	`sha256:5676549b5fb4ca77a8a7a854bb5839892ea551fb1cc599821d1c94e48c1bdff4`  
		Last Modified: Tue, 19 Aug 2025 19:12:44 GMT  
		Size: 41.4 MB (41390545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4aee800b2178134d49cde4e197016f6caf1651290a5d03ef703ade1bab26aa`  
		Last Modified: Tue, 19 Aug 2025 19:12:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:be10d6d54ad453e63a102a9f5284b833e896e924056ddcdb71fe4b73a61dfe86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600596710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21c281055118c1f473e8fab1ed35c992c8982f1fda4b3f28dc488266eb62fad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b175d5b1101180519da9e24fb3817efdd4360ed3047d852df3d47fc5776f1ed`  
		Last Modified: Tue, 19 Aug 2025 16:55:59 GMT  
		Size: 232.0 MB (232037576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a2e127c5ea4cda999997230bbf3d188d8191c1aed5bf1bed00b65c708bc007`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 2.5 MB (2521872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113056f8ed3e2e353e10be6d2bcb1308bf5d6c40739d109c5395a7976ace0b3c`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 480.4 KB (480391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a035da75521cce9421e8d864b8f7c2e292a7aac71a58342323214c1b05407e5`  
		Last Modified: Tue, 19 Aug 2025 16:56:40 GMT  
		Size: 338.2 MB (338195185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac9b2cbe44fe6d6f7b71f4205330149add79e941e7d1ab53881e4911118352a`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dd4190bfc89a53775a4c38abee37dbb99929be21187b48ca1c621209a264c8`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5aab1eeee4e6c884c6e45d5d712dbc6e7cb8845918f7b5e38654ae9e0df17`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034dd5b0e6716ae64c99c395167d52a5c4d6f542ca7e33dd48c015fb6a9bab5`  
		Last Modified: Tue, 19 Aug 2025 16:55:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:48216fe16d022158df99a7324e6a4c9ac4991626e9a51a015bd189766fb3a70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41424039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b570acc74ed58134f2b6390f1a58a1317ab6b4696fb2890e4af5eb06d51b93d9`

```dockerfile
```

-	Layers:
	-	`sha256:b91797dd215eb66bed0071a16cb18d8ea105c80615cc95c43be09f29c8030b15`  
		Last Modified: Tue, 19 Aug 2025 19:13:29 GMT  
		Size: 41.4 MB (41397052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba174b2fe0782ae5dd60df74a0c7504389f5c54f095fb23a283cb07f7fd17f68`  
		Last Modified: Tue, 19 Aug 2025 19:13:30 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:4628ac05ec2240e4e3f812bb10251b8fea442c06d575986bb86ff6984fe3ef5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622446198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe72175b7fe8c941b93012410d281072f4c48f2885e566c7b56499c5ec2bfbce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005062d77ece997f63dc5de28d3b084c8559954324800793937573b387af45e`  
		Last Modified: Tue, 19 Aug 2025 17:04:31 GMT  
		Size: 244.3 MB (244344376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07489779e7e95d8bfaf24486b8a48e9948c2a263353cc0af19779b0d8ed904`  
		Last Modified: Tue, 19 Aug 2025 17:05:05 GMT  
		Size: 2.8 MB (2849820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1345e1fe0af83a0a2cf55804f6623e038bf7aeac5f4c41a79df9faf5c0f7c42d`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 480.4 KB (480443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2018d729fe4c4648936802b1753cceef2301f84e71a37b4d882e13448017d3`  
		Last Modified: Tue, 19 Aug 2025 17:04:34 GMT  
		Size: 340.3 MB (340325979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5cd0481d4b5c6c18c45f35eefa587289d39c738fd8ad5c4e9f30a01b4a4bf7`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb5e4eb9e1a268b88cdebfe8a5ac54720d88480073720db150c8527e07d72e7`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c419950670c77e3c1507b67ea5bf16736b6d95f9f87fa62ce40333402ffb246`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f424de1d591819426aac02b5ddd7788dd0cfa5463524b9f4208529fda1e23f3`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:43c8a0a54a844a1a5595dccbf0ae208acb873714cb04264ac560362dd158a1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41426042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd7d4c2d0199e12e59d8800091ce57f778c135af5e3aa73fcc7368aa4a23380`

```dockerfile
```

-	Layers:
	-	`sha256:194a5075ff667183ad83960ebfd7fb7106e3f31010dc53dd40966bee1fb99d6d`  
		Last Modified: Tue, 19 Aug 2025 19:14:12 GMT  
		Size: 41.4 MB (41399152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0871f83fef364ab1953fca35474a294db73bfdf9b2af47d25bd4d323d684631a`  
		Last Modified: Tue, 19 Aug 2025 19:14:13 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:44d432c3dfff3d022df16945526c55b230f9d8baa9d5e3f36da2eb69a4b1eea1
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
$ docker pull odoo@sha256:aa17a5acd75fd372c20c674157afbe690795d8e91fa44fa4f6f84496aa89d479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605854096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceba6159458f361ad244a42135397e27c1a68742abc0557f15d441b82d42208a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29318572e8a89f691681090fc2030a21dc9dade302a307ffe1921aaab8407ec`  
		Last Modified: Tue, 19 Aug 2025 19:13:27 GMT  
		Size: 234.7 MB (234712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ee7b4e65e561a01aa736a46eda8e1bd1c926f51f5e2a33f1161011d0bb377`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 2.5 MB (2532617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9db8f08a8a93c50e8e3cbc9ed6297fe068914eb1d16bd20741ad99f4099e82`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 480.4 KB (480414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f91a657a585a56aaa1305cdf295400da8c46bb0881b3bc39a5cbcaa717053f`  
		Last Modified: Tue, 19 Aug 2025 19:12:51 GMT  
		Size: 338.6 MB (338589244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830894130eef75908084ffc6467a13d50f86f8707f2b34ce8c8c15f7507a0a84`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc12572f6d284b48cba20cc27e20a0ba92e30b7226369cde64bdab1115e8d13`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc1ae70b7f95c082faf8068dc5b8f9fb2c4a4b03acac5ab01821e39740d6a`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50589ceed2a5ad1a5cb38fddded3d91cce2e15bd5acfaac4ba015632b89d4a2e`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d7d92cb4bbf1a39d844fd4289017d79dd099d501563736866627953a5e904f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a108fef8a8a3f430fbb33908d5a9bf6b263253fc87ff31b33500f706bef58d`

```dockerfile
```

-	Layers:
	-	`sha256:5676549b5fb4ca77a8a7a854bb5839892ea551fb1cc599821d1c94e48c1bdff4`  
		Last Modified: Tue, 19 Aug 2025 19:12:44 GMT  
		Size: 41.4 MB (41390545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4aee800b2178134d49cde4e197016f6caf1651290a5d03ef703ade1bab26aa`  
		Last Modified: Tue, 19 Aug 2025 19:12:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:be10d6d54ad453e63a102a9f5284b833e896e924056ddcdb71fe4b73a61dfe86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600596710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21c281055118c1f473e8fab1ed35c992c8982f1fda4b3f28dc488266eb62fad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b175d5b1101180519da9e24fb3817efdd4360ed3047d852df3d47fc5776f1ed`  
		Last Modified: Tue, 19 Aug 2025 16:55:59 GMT  
		Size: 232.0 MB (232037576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a2e127c5ea4cda999997230bbf3d188d8191c1aed5bf1bed00b65c708bc007`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 2.5 MB (2521872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113056f8ed3e2e353e10be6d2bcb1308bf5d6c40739d109c5395a7976ace0b3c`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 480.4 KB (480391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a035da75521cce9421e8d864b8f7c2e292a7aac71a58342323214c1b05407e5`  
		Last Modified: Tue, 19 Aug 2025 16:56:40 GMT  
		Size: 338.2 MB (338195185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac9b2cbe44fe6d6f7b71f4205330149add79e941e7d1ab53881e4911118352a`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dd4190bfc89a53775a4c38abee37dbb99929be21187b48ca1c621209a264c8`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5aab1eeee4e6c884c6e45d5d712dbc6e7cb8845918f7b5e38654ae9e0df17`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034dd5b0e6716ae64c99c395167d52a5c4d6f542ca7e33dd48c015fb6a9bab5`  
		Last Modified: Tue, 19 Aug 2025 16:55:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:48216fe16d022158df99a7324e6a4c9ac4991626e9a51a015bd189766fb3a70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41424039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b570acc74ed58134f2b6390f1a58a1317ab6b4696fb2890e4af5eb06d51b93d9`

```dockerfile
```

-	Layers:
	-	`sha256:b91797dd215eb66bed0071a16cb18d8ea105c80615cc95c43be09f29c8030b15`  
		Last Modified: Tue, 19 Aug 2025 19:13:29 GMT  
		Size: 41.4 MB (41397052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba174b2fe0782ae5dd60df74a0c7504389f5c54f095fb23a283cb07f7fd17f68`  
		Last Modified: Tue, 19 Aug 2025 19:13:30 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:4628ac05ec2240e4e3f812bb10251b8fea442c06d575986bb86ff6984fe3ef5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622446198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe72175b7fe8c941b93012410d281072f4c48f2885e566c7b56499c5ec2bfbce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005062d77ece997f63dc5de28d3b084c8559954324800793937573b387af45e`  
		Last Modified: Tue, 19 Aug 2025 17:04:31 GMT  
		Size: 244.3 MB (244344376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07489779e7e95d8bfaf24486b8a48e9948c2a263353cc0af19779b0d8ed904`  
		Last Modified: Tue, 19 Aug 2025 17:05:05 GMT  
		Size: 2.8 MB (2849820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1345e1fe0af83a0a2cf55804f6623e038bf7aeac5f4c41a79df9faf5c0f7c42d`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 480.4 KB (480443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2018d729fe4c4648936802b1753cceef2301f84e71a37b4d882e13448017d3`  
		Last Modified: Tue, 19 Aug 2025 17:04:34 GMT  
		Size: 340.3 MB (340325979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5cd0481d4b5c6c18c45f35eefa587289d39c738fd8ad5c4e9f30a01b4a4bf7`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb5e4eb9e1a268b88cdebfe8a5ac54720d88480073720db150c8527e07d72e7`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c419950670c77e3c1507b67ea5bf16736b6d95f9f87fa62ce40333402ffb246`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f424de1d591819426aac02b5ddd7788dd0cfa5463524b9f4208529fda1e23f3`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:43c8a0a54a844a1a5595dccbf0ae208acb873714cb04264ac560362dd158a1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41426042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd7d4c2d0199e12e59d8800091ce57f778c135af5e3aa73fcc7368aa4a23380`

```dockerfile
```

-	Layers:
	-	`sha256:194a5075ff667183ad83960ebfd7fb7106e3f31010dc53dd40966bee1fb99d6d`  
		Last Modified: Tue, 19 Aug 2025 19:14:12 GMT  
		Size: 41.4 MB (41399152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0871f83fef364ab1953fca35474a294db73bfdf9b2af47d25bd4d323d684631a`  
		Last Modified: Tue, 19 Aug 2025 19:14:13 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250819`

```console
$ docker pull odoo@sha256:44d432c3dfff3d022df16945526c55b230f9d8baa9d5e3f36da2eb69a4b1eea1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250819` - linux; amd64

```console
$ docker pull odoo@sha256:aa17a5acd75fd372c20c674157afbe690795d8e91fa44fa4f6f84496aa89d479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605854096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceba6159458f361ad244a42135397e27c1a68742abc0557f15d441b82d42208a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29318572e8a89f691681090fc2030a21dc9dade302a307ffe1921aaab8407ec`  
		Last Modified: Tue, 19 Aug 2025 19:13:27 GMT  
		Size: 234.7 MB (234712388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ee7b4e65e561a01aa736a46eda8e1bd1c926f51f5e2a33f1161011d0bb377`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 2.5 MB (2532617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9db8f08a8a93c50e8e3cbc9ed6297fe068914eb1d16bd20741ad99f4099e82`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 480.4 KB (480414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f91a657a585a56aaa1305cdf295400da8c46bb0881b3bc39a5cbcaa717053f`  
		Last Modified: Tue, 19 Aug 2025 19:12:51 GMT  
		Size: 338.6 MB (338589244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830894130eef75908084ffc6467a13d50f86f8707f2b34ce8c8c15f7507a0a84`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc12572f6d284b48cba20cc27e20a0ba92e30b7226369cde64bdab1115e8d13`  
		Last Modified: Tue, 19 Aug 2025 16:46:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cc1ae70b7f95c082faf8068dc5b8f9fb2c4a4b03acac5ab01821e39740d6a`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50589ceed2a5ad1a5cb38fddded3d91cce2e15bd5acfaac4ba015632b89d4a2e`  
		Last Modified: Tue, 19 Aug 2025 16:46:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:d7d92cb4bbf1a39d844fd4289017d79dd099d501563736866627953a5e904f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a108fef8a8a3f430fbb33908d5a9bf6b263253fc87ff31b33500f706bef58d`

```dockerfile
```

-	Layers:
	-	`sha256:5676549b5fb4ca77a8a7a854bb5839892ea551fb1cc599821d1c94e48c1bdff4`  
		Last Modified: Tue, 19 Aug 2025 19:12:44 GMT  
		Size: 41.4 MB (41390545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4aee800b2178134d49cde4e197016f6caf1651290a5d03ef703ade1bab26aa`  
		Last Modified: Tue, 19 Aug 2025 19:12:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250819` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:be10d6d54ad453e63a102a9f5284b833e896e924056ddcdb71fe4b73a61dfe86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600596710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21c281055118c1f473e8fab1ed35c992c8982f1fda4b3f28dc488266eb62fad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b175d5b1101180519da9e24fb3817efdd4360ed3047d852df3d47fc5776f1ed`  
		Last Modified: Tue, 19 Aug 2025 16:55:59 GMT  
		Size: 232.0 MB (232037576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a2e127c5ea4cda999997230bbf3d188d8191c1aed5bf1bed00b65c708bc007`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 2.5 MB (2521872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113056f8ed3e2e353e10be6d2bcb1308bf5d6c40739d109c5395a7976ace0b3c`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 480.4 KB (480391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a035da75521cce9421e8d864b8f7c2e292a7aac71a58342323214c1b05407e5`  
		Last Modified: Tue, 19 Aug 2025 16:56:40 GMT  
		Size: 338.2 MB (338195185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac9b2cbe44fe6d6f7b71f4205330149add79e941e7d1ab53881e4911118352a`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dd4190bfc89a53775a4c38abee37dbb99929be21187b48ca1c621209a264c8`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5aab1eeee4e6c884c6e45d5d712dbc6e7cb8845918f7b5e38654ae9e0df17`  
		Last Modified: Tue, 19 Aug 2025 16:55:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034dd5b0e6716ae64c99c395167d52a5c4d6f542ca7e33dd48c015fb6a9bab5`  
		Last Modified: Tue, 19 Aug 2025 16:55:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:48216fe16d022158df99a7324e6a4c9ac4991626e9a51a015bd189766fb3a70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41424039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b570acc74ed58134f2b6390f1a58a1317ab6b4696fb2890e4af5eb06d51b93d9`

```dockerfile
```

-	Layers:
	-	`sha256:b91797dd215eb66bed0071a16cb18d8ea105c80615cc95c43be09f29c8030b15`  
		Last Modified: Tue, 19 Aug 2025 19:13:29 GMT  
		Size: 41.4 MB (41397052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba174b2fe0782ae5dd60df74a0c7504389f5c54f095fb23a283cb07f7fd17f68`  
		Last Modified: Tue, 19 Aug 2025 19:13:30 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250819` - linux; ppc64le

```console
$ docker pull odoo@sha256:4628ac05ec2240e4e3f812bb10251b8fea442c06d575986bb86ff6984fe3ef5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622446198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe72175b7fe8c941b93012410d281072f4c48f2885e566c7b56499c5ec2bfbce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005062d77ece997f63dc5de28d3b084c8559954324800793937573b387af45e`  
		Last Modified: Tue, 19 Aug 2025 17:04:31 GMT  
		Size: 244.3 MB (244344376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07489779e7e95d8bfaf24486b8a48e9948c2a263353cc0af19779b0d8ed904`  
		Last Modified: Tue, 19 Aug 2025 17:05:05 GMT  
		Size: 2.8 MB (2849820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1345e1fe0af83a0a2cf55804f6623e038bf7aeac5f4c41a79df9faf5c0f7c42d`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 480.4 KB (480443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2018d729fe4c4648936802b1753cceef2301f84e71a37b4d882e13448017d3`  
		Last Modified: Tue, 19 Aug 2025 17:04:34 GMT  
		Size: 340.3 MB (340325979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5cd0481d4b5c6c18c45f35eefa587289d39c738fd8ad5c4e9f30a01b4a4bf7`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb5e4eb9e1a268b88cdebfe8a5ac54720d88480073720db150c8527e07d72e7`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c419950670c77e3c1507b67ea5bf16736b6d95f9f87fa62ce40333402ffb246`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f424de1d591819426aac02b5ddd7788dd0cfa5463524b9f4208529fda1e23f3`  
		Last Modified: Tue, 19 Aug 2025 17:05:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:43c8a0a54a844a1a5595dccbf0ae208acb873714cb04264ac560362dd158a1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41426042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd7d4c2d0199e12e59d8800091ce57f778c135af5e3aa73fcc7368aa4a23380`

```dockerfile
```

-	Layers:
	-	`sha256:194a5075ff667183ad83960ebfd7fb7106e3f31010dc53dd40966bee1fb99d6d`  
		Last Modified: Tue, 19 Aug 2025 19:14:12 GMT  
		Size: 41.4 MB (41399152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0871f83fef364ab1953fca35474a294db73bfdf9b2af47d25bd4d323d684631a`  
		Last Modified: Tue, 19 Aug 2025 19:14:13 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:8e262fde438aa29c27609a19cb7677654a55b7b805a825e03b5b8b990e188c9b
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
$ docker pull odoo@sha256:e031d77afd1e029ece63ae214b6b9842d63b209af82d598e184fe40add09908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a26e5748f96753d4a5c4c5c28b077b4c363ea118bf897d28a263a84c832fc8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e98e8f894c15f6285c6c0bfd41c1dc15a02d05fab5171e12eff766455da8d`  
		Last Modified: Tue, 19 Aug 2025 16:53:08 GMT  
		Size: 254.5 MB (254529728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f19c8ff83ca9bb941b746ff541b70de95712e8ae7472f937cb7f824051053`  
		Last Modified: Tue, 19 Aug 2025 16:46:56 GMT  
		Size: 14.3 MB (14286033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a9d93fc1909f2ded0aeb6aaee3c03e6e682584c88b9f2ec6db18a8fc8a2d72`  
		Last Modified: Tue, 19 Aug 2025 16:46:55 GMT  
		Size: 480.1 KB (480143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98678ef3b1b6d50162cb55e6cad163060ebfc46a48c4e14d6065534ac4e1a76`  
		Last Modified: Tue, 19 Aug 2025 16:53:33 GMT  
		Size: 376.5 MB (376526325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8658a17dfefde24c7f667ff2472afdb3b7c0de26cf1ae96bf844b2214d612b3`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981189a05ac8f17359a480d50ecb597f78c20e7ef5b65b30c357010d91c7fcf0`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a067c3632be279e39bd5f9c2dc54993f59d0f357c1e2479af8914176ca453245`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14203f7f866a2f8fac7220858e8ae00555d5969707d4ecf85211bb7fd0c508`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1d049522d2d2a5acd6ae50e63088bb59544b8856d3012082720ca6364ac624cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3206e05d688d67de81c378dccd12c2cbae0d2fc71b11c02f0be64207e5b4d32`

```dockerfile
```

-	Layers:
	-	`sha256:575db8643c84e4da4c602576d366c26f7c03c1e9ba5034e47c3e39d6494b7eda`  
		Last Modified: Tue, 19 Aug 2025 19:12:59 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0bf910adebb6dccaacde172f745ba72784516ad2c5eb6a1a86f4ca928e4346`  
		Last Modified: Tue, 19 Aug 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:929d9591d35f5c8f9cc5428f8b820a91fe032e04cef854942d681de884e80336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671901266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c173b084ab53ccfe29a241802ffe03e0222ae116b95ab35ff1dcdae94cfb587f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed4f7f0d80cef8e295f63ca76ac27925ab6d6cd1fb5fe84827ff31868485798`  
		Last Modified: Tue, 19 Aug 2025 16:53:40 GMT  
		Size: 251.9 MB (251920604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e77bd0a7bc4f2f7f4d4a169256c65dffe04169ecd24822961ae2251f80a2b`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 14.3 MB (14263289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b8a95efcce9a8a17e1d4609ef36af9c55da17a4e592388fee173e35c5dc9d7`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 480.2 KB (480237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396a40e6ae51d21d6451aeef3599f1d2da46228dccabdc1d027b7a960d9b93f`  
		Last Modified: Tue, 19 Aug 2025 16:53:55 GMT  
		Size: 376.4 MB (376374323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59393059d7f8bb10efd20d5e06b856f59789fa47f7579bdee7d5aa21cf384e59`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b3f0c0895da93ab114046c3262c063ca8567ffb921d7448527e0a911c0c1e4`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70301fa2ae6e6ea05460595da717884a796ed8293333b21006f7bb97f2fc2b63`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def2f5a6c369a85191ebe6e5bd66b0f71ef5cc67f0f5bc622356caff01280862`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:8303e7ac5bf2dbae9bdde105971a18c3849babe58c40295b604265b2a43dcb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fd06b63d8a21ea2d3caea05cdf7c5a4456ebe468eeb68182b02269de4e2a15`

```dockerfile
```

-	Layers:
	-	`sha256:564ddf715338d355d396e69037387f0e2175feaadf989401610dbb499c13051d`  
		Last Modified: Tue, 19 Aug 2025 19:14:38 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453c76d159cf592c1bfe2a5def372bd34f54c660f40174c21ff5b2969aec7cf1`  
		Last Modified: Tue, 19 Aug 2025 19:14:39 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:deea46cd915fecf4563bfbed71b1f4d17f30ebcfb7faa263046f6c3d132a8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691757325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0fe309904f6ba317244a3b30d7038c3226e956109da00f300462f412bc9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c79351128f6f7cac5fc045c3bbbaf7ae7185cb182112cfafeee18aec1bfca`  
		Last Modified: Tue, 19 Aug 2025 16:55:55 GMT  
		Size: 265.1 MB (265079161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10275749e380cc91f4094284c7ddd14c5958ec6767f962ba79d75784ab9a6485`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 14.8 MB (14813053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086e1de9dd67c4e9ed47c407aa2628f609439a903ab5691acf764421e4f5045a`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 480.2 KB (480166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1268acb48180e093e596e8e7c2a313d401834fa4dec7a6f9f927078199a025c1`  
		Last Modified: Tue, 19 Aug 2025 16:56:43 GMT  
		Size: 377.1 MB (377052855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff315d590a32d57174964e1477c8a3e8cd7687f73e2a2ad5bb459d805da95b6`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3898a3561c759b52717a6af03c6fb38f7a4d97651dd3ca49650922c87c93382`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fd49aecb424e349aac8e57d6c80b319335fce9e4b0f416d071fba0b98c3e12`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e60a2c5280316c3322dc0bee6a984922d4f8bb7e209d308dd3b1d7fe5ac85b`  
		Last Modified: Tue, 19 Aug 2025 16:55:47 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:488f5675d5158aa1fb49b52344a7b8ec51c612bff4be26a8634d8b3c403d8cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f305ac416abb2e5b9d3beeb02720cfa1f8308ec8bffd05b43de4790d99c3f63a`

```dockerfile
```

-	Layers:
	-	`sha256:233592c78f8c1c4bf83c5235c8a7d0af6d49893bcbbae482d474ab9f503b967e`  
		Last Modified: Tue, 19 Aug 2025 19:16:09 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e838f029deddd9191c0eb3337e8f0453cb4c5e12b2acd1ce5e6e53921e33ce6`  
		Last Modified: Tue, 19 Aug 2025 19:16:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:8e262fde438aa29c27609a19cb7677654a55b7b805a825e03b5b8b990e188c9b
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
$ docker pull odoo@sha256:e031d77afd1e029ece63ae214b6b9842d63b209af82d598e184fe40add09908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a26e5748f96753d4a5c4c5c28b077b4c363ea118bf897d28a263a84c832fc8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e98e8f894c15f6285c6c0bfd41c1dc15a02d05fab5171e12eff766455da8d`  
		Last Modified: Tue, 19 Aug 2025 16:53:08 GMT  
		Size: 254.5 MB (254529728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f19c8ff83ca9bb941b746ff541b70de95712e8ae7472f937cb7f824051053`  
		Last Modified: Tue, 19 Aug 2025 16:46:56 GMT  
		Size: 14.3 MB (14286033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a9d93fc1909f2ded0aeb6aaee3c03e6e682584c88b9f2ec6db18a8fc8a2d72`  
		Last Modified: Tue, 19 Aug 2025 16:46:55 GMT  
		Size: 480.1 KB (480143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98678ef3b1b6d50162cb55e6cad163060ebfc46a48c4e14d6065534ac4e1a76`  
		Last Modified: Tue, 19 Aug 2025 16:53:33 GMT  
		Size: 376.5 MB (376526325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8658a17dfefde24c7f667ff2472afdb3b7c0de26cf1ae96bf844b2214d612b3`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981189a05ac8f17359a480d50ecb597f78c20e7ef5b65b30c357010d91c7fcf0`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a067c3632be279e39bd5f9c2dc54993f59d0f357c1e2479af8914176ca453245`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14203f7f866a2f8fac7220858e8ae00555d5969707d4ecf85211bb7fd0c508`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1d049522d2d2a5acd6ae50e63088bb59544b8856d3012082720ca6364ac624cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3206e05d688d67de81c378dccd12c2cbae0d2fc71b11c02f0be64207e5b4d32`

```dockerfile
```

-	Layers:
	-	`sha256:575db8643c84e4da4c602576d366c26f7c03c1e9ba5034e47c3e39d6494b7eda`  
		Last Modified: Tue, 19 Aug 2025 19:12:59 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0bf910adebb6dccaacde172f745ba72784516ad2c5eb6a1a86f4ca928e4346`  
		Last Modified: Tue, 19 Aug 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:929d9591d35f5c8f9cc5428f8b820a91fe032e04cef854942d681de884e80336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671901266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c173b084ab53ccfe29a241802ffe03e0222ae116b95ab35ff1dcdae94cfb587f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed4f7f0d80cef8e295f63ca76ac27925ab6d6cd1fb5fe84827ff31868485798`  
		Last Modified: Tue, 19 Aug 2025 16:53:40 GMT  
		Size: 251.9 MB (251920604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e77bd0a7bc4f2f7f4d4a169256c65dffe04169ecd24822961ae2251f80a2b`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 14.3 MB (14263289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b8a95efcce9a8a17e1d4609ef36af9c55da17a4e592388fee173e35c5dc9d7`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 480.2 KB (480237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396a40e6ae51d21d6451aeef3599f1d2da46228dccabdc1d027b7a960d9b93f`  
		Last Modified: Tue, 19 Aug 2025 16:53:55 GMT  
		Size: 376.4 MB (376374323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59393059d7f8bb10efd20d5e06b856f59789fa47f7579bdee7d5aa21cf384e59`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b3f0c0895da93ab114046c3262c063ca8567ffb921d7448527e0a911c0c1e4`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70301fa2ae6e6ea05460595da717884a796ed8293333b21006f7bb97f2fc2b63`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def2f5a6c369a85191ebe6e5bd66b0f71ef5cc67f0f5bc622356caff01280862`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8303e7ac5bf2dbae9bdde105971a18c3849babe58c40295b604265b2a43dcb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fd06b63d8a21ea2d3caea05cdf7c5a4456ebe468eeb68182b02269de4e2a15`

```dockerfile
```

-	Layers:
	-	`sha256:564ddf715338d355d396e69037387f0e2175feaadf989401610dbb499c13051d`  
		Last Modified: Tue, 19 Aug 2025 19:14:38 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453c76d159cf592c1bfe2a5def372bd34f54c660f40174c21ff5b2969aec7cf1`  
		Last Modified: Tue, 19 Aug 2025 19:14:39 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:deea46cd915fecf4563bfbed71b1f4d17f30ebcfb7faa263046f6c3d132a8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691757325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0fe309904f6ba317244a3b30d7038c3226e956109da00f300462f412bc9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c79351128f6f7cac5fc045c3bbbaf7ae7185cb182112cfafeee18aec1bfca`  
		Last Modified: Tue, 19 Aug 2025 16:55:55 GMT  
		Size: 265.1 MB (265079161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10275749e380cc91f4094284c7ddd14c5958ec6767f962ba79d75784ab9a6485`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 14.8 MB (14813053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086e1de9dd67c4e9ed47c407aa2628f609439a903ab5691acf764421e4f5045a`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 480.2 KB (480166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1268acb48180e093e596e8e7c2a313d401834fa4dec7a6f9f927078199a025c1`  
		Last Modified: Tue, 19 Aug 2025 16:56:43 GMT  
		Size: 377.1 MB (377052855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff315d590a32d57174964e1477c8a3e8cd7687f73e2a2ad5bb459d805da95b6`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3898a3561c759b52717a6af03c6fb38f7a4d97651dd3ca49650922c87c93382`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fd49aecb424e349aac8e57d6c80b319335fce9e4b0f416d071fba0b98c3e12`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e60a2c5280316c3322dc0bee6a984922d4f8bb7e209d308dd3b1d7fe5ac85b`  
		Last Modified: Tue, 19 Aug 2025 16:55:47 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:488f5675d5158aa1fb49b52344a7b8ec51c612bff4be26a8634d8b3c403d8cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f305ac416abb2e5b9d3beeb02720cfa1f8308ec8bffd05b43de4790d99c3f63a`

```dockerfile
```

-	Layers:
	-	`sha256:233592c78f8c1c4bf83c5235c8a7d0af6d49893bcbbae482d474ab9f503b967e`  
		Last Modified: Tue, 19 Aug 2025 19:16:09 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e838f029deddd9191c0eb3337e8f0453cb4c5e12b2acd1ce5e6e53921e33ce6`  
		Last Modified: Tue, 19 Aug 2025 19:16:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250819`

```console
$ docker pull odoo@sha256:8e262fde438aa29c27609a19cb7677654a55b7b805a825e03b5b8b990e188c9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250819` - linux; amd64

```console
$ docker pull odoo@sha256:e031d77afd1e029ece63ae214b6b9842d63b209af82d598e184fe40add09908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a26e5748f96753d4a5c4c5c28b077b4c363ea118bf897d28a263a84c832fc8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e98e8f894c15f6285c6c0bfd41c1dc15a02d05fab5171e12eff766455da8d`  
		Last Modified: Tue, 19 Aug 2025 16:53:08 GMT  
		Size: 254.5 MB (254529728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f19c8ff83ca9bb941b746ff541b70de95712e8ae7472f937cb7f824051053`  
		Last Modified: Tue, 19 Aug 2025 16:46:56 GMT  
		Size: 14.3 MB (14286033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a9d93fc1909f2ded0aeb6aaee3c03e6e682584c88b9f2ec6db18a8fc8a2d72`  
		Last Modified: Tue, 19 Aug 2025 16:46:55 GMT  
		Size: 480.1 KB (480143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98678ef3b1b6d50162cb55e6cad163060ebfc46a48c4e14d6065534ac4e1a76`  
		Last Modified: Tue, 19 Aug 2025 16:53:33 GMT  
		Size: 376.5 MB (376526325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8658a17dfefde24c7f667ff2472afdb3b7c0de26cf1ae96bf844b2214d612b3`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981189a05ac8f17359a480d50ecb597f78c20e7ef5b65b30c357010d91c7fcf0`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a067c3632be279e39bd5f9c2dc54993f59d0f357c1e2479af8914176ca453245`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14203f7f866a2f8fac7220858e8ae00555d5969707d4ecf85211bb7fd0c508`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:1d049522d2d2a5acd6ae50e63088bb59544b8856d3012082720ca6364ac624cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3206e05d688d67de81c378dccd12c2cbae0d2fc71b11c02f0be64207e5b4d32`

```dockerfile
```

-	Layers:
	-	`sha256:575db8643c84e4da4c602576d366c26f7c03c1e9ba5034e47c3e39d6494b7eda`  
		Last Modified: Tue, 19 Aug 2025 19:12:59 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0bf910adebb6dccaacde172f745ba72784516ad2c5eb6a1a86f4ca928e4346`  
		Last Modified: Tue, 19 Aug 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250819` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:929d9591d35f5c8f9cc5428f8b820a91fe032e04cef854942d681de884e80336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671901266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c173b084ab53ccfe29a241802ffe03e0222ae116b95ab35ff1dcdae94cfb587f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed4f7f0d80cef8e295f63ca76ac27925ab6d6cd1fb5fe84827ff31868485798`  
		Last Modified: Tue, 19 Aug 2025 16:53:40 GMT  
		Size: 251.9 MB (251920604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e77bd0a7bc4f2f7f4d4a169256c65dffe04169ecd24822961ae2251f80a2b`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 14.3 MB (14263289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b8a95efcce9a8a17e1d4609ef36af9c55da17a4e592388fee173e35c5dc9d7`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 480.2 KB (480237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396a40e6ae51d21d6451aeef3599f1d2da46228dccabdc1d027b7a960d9b93f`  
		Last Modified: Tue, 19 Aug 2025 16:53:55 GMT  
		Size: 376.4 MB (376374323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59393059d7f8bb10efd20d5e06b856f59789fa47f7579bdee7d5aa21cf384e59`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b3f0c0895da93ab114046c3262c063ca8567ffb921d7448527e0a911c0c1e4`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70301fa2ae6e6ea05460595da717884a796ed8293333b21006f7bb97f2fc2b63`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def2f5a6c369a85191ebe6e5bd66b0f71ef5cc67f0f5bc622356caff01280862`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:8303e7ac5bf2dbae9bdde105971a18c3849babe58c40295b604265b2a43dcb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fd06b63d8a21ea2d3caea05cdf7c5a4456ebe468eeb68182b02269de4e2a15`

```dockerfile
```

-	Layers:
	-	`sha256:564ddf715338d355d396e69037387f0e2175feaadf989401610dbb499c13051d`  
		Last Modified: Tue, 19 Aug 2025 19:14:38 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453c76d159cf592c1bfe2a5def372bd34f54c660f40174c21ff5b2969aec7cf1`  
		Last Modified: Tue, 19 Aug 2025 19:14:39 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250819` - linux; ppc64le

```console
$ docker pull odoo@sha256:deea46cd915fecf4563bfbed71b1f4d17f30ebcfb7faa263046f6c3d132a8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691757325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0fe309904f6ba317244a3b30d7038c3226e956109da00f300462f412bc9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c79351128f6f7cac5fc045c3bbbaf7ae7185cb182112cfafeee18aec1bfca`  
		Last Modified: Tue, 19 Aug 2025 16:55:55 GMT  
		Size: 265.1 MB (265079161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10275749e380cc91f4094284c7ddd14c5958ec6767f962ba79d75784ab9a6485`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 14.8 MB (14813053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086e1de9dd67c4e9ed47c407aa2628f609439a903ab5691acf764421e4f5045a`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 480.2 KB (480166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1268acb48180e093e596e8e7c2a313d401834fa4dec7a6f9f927078199a025c1`  
		Last Modified: Tue, 19 Aug 2025 16:56:43 GMT  
		Size: 377.1 MB (377052855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff315d590a32d57174964e1477c8a3e8cd7687f73e2a2ad5bb459d805da95b6`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3898a3561c759b52717a6af03c6fb38f7a4d97651dd3ca49650922c87c93382`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fd49aecb424e349aac8e57d6c80b319335fce9e4b0f416d071fba0b98c3e12`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e60a2c5280316c3322dc0bee6a984922d4f8bb7e209d308dd3b1d7fe5ac85b`  
		Last Modified: Tue, 19 Aug 2025 16:55:47 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:488f5675d5158aa1fb49b52344a7b8ec51c612bff4be26a8634d8b3c403d8cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f305ac416abb2e5b9d3beeb02720cfa1f8308ec8bffd05b43de4790d99c3f63a`

```dockerfile
```

-	Layers:
	-	`sha256:233592c78f8c1c4bf83c5235c8a7d0af6d49893bcbbae482d474ab9f503b967e`  
		Last Modified: Tue, 19 Aug 2025 19:16:09 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e838f029deddd9191c0eb3337e8f0453cb4c5e12b2acd1ce5e6e53921e33ce6`  
		Last Modified: Tue, 19 Aug 2025 19:16:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:8e262fde438aa29c27609a19cb7677654a55b7b805a825e03b5b8b990e188c9b
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
$ docker pull odoo@sha256:e031d77afd1e029ece63ae214b6b9842d63b209af82d598e184fe40add09908d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a26e5748f96753d4a5c4c5c28b077b4c363ea118bf897d28a263a84c832fc8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571e98e8f894c15f6285c6c0bfd41c1dc15a02d05fab5171e12eff766455da8d`  
		Last Modified: Tue, 19 Aug 2025 16:53:08 GMT  
		Size: 254.5 MB (254529728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f19c8ff83ca9bb941b746ff541b70de95712e8ae7472f937cb7f824051053`  
		Last Modified: Tue, 19 Aug 2025 16:46:56 GMT  
		Size: 14.3 MB (14286033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a9d93fc1909f2ded0aeb6aaee3c03e6e682584c88b9f2ec6db18a8fc8a2d72`  
		Last Modified: Tue, 19 Aug 2025 16:46:55 GMT  
		Size: 480.1 KB (480143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98678ef3b1b6d50162cb55e6cad163060ebfc46a48c4e14d6065534ac4e1a76`  
		Last Modified: Tue, 19 Aug 2025 16:53:33 GMT  
		Size: 376.5 MB (376526325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8658a17dfefde24c7f667ff2472afdb3b7c0de26cf1ae96bf844b2214d612b3`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981189a05ac8f17359a480d50ecb597f78c20e7ef5b65b30c357010d91c7fcf0`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a067c3632be279e39bd5f9c2dc54993f59d0f357c1e2479af8914176ca453245`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14203f7f866a2f8fac7220858e8ae00555d5969707d4ecf85211bb7fd0c508`  
		Last Modified: Tue, 19 Aug 2025 16:46:50 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1d049522d2d2a5acd6ae50e63088bb59544b8856d3012082720ca6364ac624cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3206e05d688d67de81c378dccd12c2cbae0d2fc71b11c02f0be64207e5b4d32`

```dockerfile
```

-	Layers:
	-	`sha256:575db8643c84e4da4c602576d366c26f7c03c1e9ba5034e47c3e39d6494b7eda`  
		Last Modified: Tue, 19 Aug 2025 19:12:59 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb0bf910adebb6dccaacde172f745ba72784516ad2c5eb6a1a86f4ca928e4346`  
		Last Modified: Tue, 19 Aug 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:929d9591d35f5c8f9cc5428f8b820a91fe032e04cef854942d681de884e80336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671901266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c173b084ab53ccfe29a241802ffe03e0222ae116b95ab35ff1dcdae94cfb587f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed4f7f0d80cef8e295f63ca76ac27925ab6d6cd1fb5fe84827ff31868485798`  
		Last Modified: Tue, 19 Aug 2025 16:53:40 GMT  
		Size: 251.9 MB (251920604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e77bd0a7bc4f2f7f4d4a169256c65dffe04169ecd24822961ae2251f80a2b`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 14.3 MB (14263289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b8a95efcce9a8a17e1d4609ef36af9c55da17a4e592388fee173e35c5dc9d7`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 480.2 KB (480237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396a40e6ae51d21d6451aeef3599f1d2da46228dccabdc1d027b7a960d9b93f`  
		Last Modified: Tue, 19 Aug 2025 16:53:55 GMT  
		Size: 376.4 MB (376374323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59393059d7f8bb10efd20d5e06b856f59789fa47f7579bdee7d5aa21cf384e59`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b3f0c0895da93ab114046c3262c063ca8567ffb921d7448527e0a911c0c1e4`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70301fa2ae6e6ea05460595da717884a796ed8293333b21006f7bb97f2fc2b63`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def2f5a6c369a85191ebe6e5bd66b0f71ef5cc67f0f5bc622356caff01280862`  
		Last Modified: Tue, 19 Aug 2025 16:50:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:8303e7ac5bf2dbae9bdde105971a18c3849babe58c40295b604265b2a43dcb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fd06b63d8a21ea2d3caea05cdf7c5a4456ebe468eeb68182b02269de4e2a15`

```dockerfile
```

-	Layers:
	-	`sha256:564ddf715338d355d396e69037387f0e2175feaadf989401610dbb499c13051d`  
		Last Modified: Tue, 19 Aug 2025 19:14:38 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453c76d159cf592c1bfe2a5def372bd34f54c660f40174c21ff5b2969aec7cf1`  
		Last Modified: Tue, 19 Aug 2025 19:14:39 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:deea46cd915fecf4563bfbed71b1f4d17f30ebcfb7faa263046f6c3d132a8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691757325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fa0fe309904f6ba317244a3b30d7038c3226e956109da00f300462f412bc9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c79351128f6f7cac5fc045c3bbbaf7ae7185cb182112cfafeee18aec1bfca`  
		Last Modified: Tue, 19 Aug 2025 16:55:55 GMT  
		Size: 265.1 MB (265079161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10275749e380cc91f4094284c7ddd14c5958ec6767f962ba79d75784ab9a6485`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 14.8 MB (14813053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086e1de9dd67c4e9ed47c407aa2628f609439a903ab5691acf764421e4f5045a`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 480.2 KB (480166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1268acb48180e093e596e8e7c2a313d401834fa4dec7a6f9f927078199a025c1`  
		Last Modified: Tue, 19 Aug 2025 16:56:43 GMT  
		Size: 377.1 MB (377052855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff315d590a32d57174964e1477c8a3e8cd7687f73e2a2ad5bb459d805da95b6`  
		Last Modified: Tue, 19 Aug 2025 16:55:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3898a3561c759b52717a6af03c6fb38f7a4d97651dd3ca49650922c87c93382`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fd49aecb424e349aac8e57d6c80b319335fce9e4b0f416d071fba0b98c3e12`  
		Last Modified: Tue, 19 Aug 2025 16:55:46 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e60a2c5280316c3322dc0bee6a984922d4f8bb7e209d308dd3b1d7fe5ac85b`  
		Last Modified: Tue, 19 Aug 2025 16:55:47 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:488f5675d5158aa1fb49b52344a7b8ec51c612bff4be26a8634d8b3c403d8cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f305ac416abb2e5b9d3beeb02720cfa1f8308ec8bffd05b43de4790d99c3f63a`

```dockerfile
```

-	Layers:
	-	`sha256:233592c78f8c1c4bf83c5235c8a7d0af6d49893bcbbae482d474ab9f503b967e`  
		Last Modified: Tue, 19 Aug 2025 19:16:09 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e838f029deddd9191c0eb3337e8f0453cb4c5e12b2acd1ce5e6e53921e33ce6`  
		Last Modified: Tue, 19 Aug 2025 19:16:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
