<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241118`](#odoo160-20241118)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241118`](#odoo170-20241118)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241118`](#odoo180-20241118)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:5d971dd0cab1a1293d011bd48cd3ab12a4401b79737d46adfd25920e23d76baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:c0ae2f45e97e0d81b14cfaa50d496e7d565f4e07584066994232b6e6ec788b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584805606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54414ef7a30e4d2e07f7da98c46eab4312664317130deeaa83850379d2ffa5fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=C.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=16.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ae886894349380ce6bf29318b6bd99c6ad749af4c379d2f1fdd7fd16631db`  
		Last Modified: Mon, 18 Nov 2024 19:07:58 GMT  
		Size: 219.6 MB (219606475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6380a70b062f02b1480a50ced1a01f10a04d6fc2602a975adbc23e7266e727`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 2.6 MB (2575884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07dcedd9326eeeadf6cc84c2dbd288927ba155ea0f201cbbc3fb9a74cff32f2`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 469.0 KB (469003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985c2ef717573012d391c81fff67b77d78c7dab9edb138ad3f09acdf68aabb10`  
		Last Modified: Mon, 18 Nov 2024 19:08:06 GMT  
		Size: 330.7 MB (330700249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac5caaf6e73e80982166202223f1b5b24eb7210acd9e06360965be76bbba87`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418a14cdb7b9dbe398e0b1f7d3a13ef489599388a2b898fe9af2dcc45bd4948e`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0af888843a8ff6bfceb8361aacc7cea3fcdafdec57c4449071227a5a532764`  
		Last Modified: Mon, 18 Nov 2024 19:07:57 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6338c013315f69e4e1c75bd634e5615884296bc3bd3001b950e73bf7debd83`  
		Last Modified: Mon, 18 Nov 2024 19:07:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d18c5675d4bd6fbd2cbfebce5a5f39524c862c104bcd5ddd421516b9bf4bdc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38892875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2999696c03a9b6327e8bc326c3babf518d11cae33f82ace28e31f672c7964b`

```dockerfile
```

-	Layers:
	-	`sha256:6978eea98d76ba6754271b9e5e60d7847c9bdba108d7ae9a370a79611600b87f`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 38.9 MB (38866157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e391079ce005f63683ad879aa13baeea8d14bcfd2c89e518eeeec39b202aa54`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:762e90055d1cf6d89eaa670038f0ec0f819203b4e1e4a4009a2f31c69690db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580412069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024b98f52db3e2c8a2c9644f9ec1c8d7dc7848eb85b86375707f991028f270dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=C.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=16.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689abbf96956f625195182ac751906675f167eb79691c2d19bfa0593c6afa2c`  
		Last Modified: Mon, 18 Nov 2024 19:50:17 GMT  
		Size: 216.9 MB (216917317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073696c45fa176ea3f3fc4544f520fff34daacfdb49459ec9007c9702204c0b`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 2.6 MB (2583786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8a28c9d2e01dd95537d21c9026332df53afacfcd4af98db8dd25fa1dcec19`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 469.1 KB (469084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06d9c1ead3812f84edbb66c6da708342804148745fab481b92946a0f9a7aeec`  
		Last Modified: Mon, 18 Nov 2024 19:50:21 GMT  
		Size: 330.3 MB (330347848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0492df1521449d788db3473a95ccda629c266b6ec073149cb4a9f6e702452da0`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9adbf5d49c07defaf15094d541c0486868399e98806932a8194032643fd33`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd611dbd6765ada78f2f9039f19c3da61c6ea97915a958a052ef932522c5f39`  
		Last Modified: Mon, 18 Nov 2024 19:50:14 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b38f5ef2ae908ff431b974488e69112e0eb15816d833f4d0f12b2d2ce33d72f`  
		Last Modified: Mon, 18 Nov 2024 19:50:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:20a067c0e1bdb2af305cf57fe8774cf65274484b8b5968b47ef37092fca2080b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e61d02d195a16a3033222f1859602a898a11d0641f1769bcd87fdff81b296f`

```dockerfile
```

-	Layers:
	-	`sha256:e24a67bbe52a8dad7cd3de3ff41833bd804b10d4597f2cfe03c97c8bacb401e1`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 38.9 MB (38872633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfae6fc67ace16afbccfde6a84c83fdd22214347fadca460c629e35383905e8`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:5d971dd0cab1a1293d011bd48cd3ab12a4401b79737d46adfd25920e23d76baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:c0ae2f45e97e0d81b14cfaa50d496e7d565f4e07584066994232b6e6ec788b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584805606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54414ef7a30e4d2e07f7da98c46eab4312664317130deeaa83850379d2ffa5fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=C.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=16.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ae886894349380ce6bf29318b6bd99c6ad749af4c379d2f1fdd7fd16631db`  
		Last Modified: Mon, 18 Nov 2024 19:07:58 GMT  
		Size: 219.6 MB (219606475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6380a70b062f02b1480a50ced1a01f10a04d6fc2602a975adbc23e7266e727`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 2.6 MB (2575884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07dcedd9326eeeadf6cc84c2dbd288927ba155ea0f201cbbc3fb9a74cff32f2`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 469.0 KB (469003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985c2ef717573012d391c81fff67b77d78c7dab9edb138ad3f09acdf68aabb10`  
		Last Modified: Mon, 18 Nov 2024 19:08:06 GMT  
		Size: 330.7 MB (330700249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac5caaf6e73e80982166202223f1b5b24eb7210acd9e06360965be76bbba87`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418a14cdb7b9dbe398e0b1f7d3a13ef489599388a2b898fe9af2dcc45bd4948e`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0af888843a8ff6bfceb8361aacc7cea3fcdafdec57c4449071227a5a532764`  
		Last Modified: Mon, 18 Nov 2024 19:07:57 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6338c013315f69e4e1c75bd634e5615884296bc3bd3001b950e73bf7debd83`  
		Last Modified: Mon, 18 Nov 2024 19:07:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d18c5675d4bd6fbd2cbfebce5a5f39524c862c104bcd5ddd421516b9bf4bdc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38892875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2999696c03a9b6327e8bc326c3babf518d11cae33f82ace28e31f672c7964b`

```dockerfile
```

-	Layers:
	-	`sha256:6978eea98d76ba6754271b9e5e60d7847c9bdba108d7ae9a370a79611600b87f`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 38.9 MB (38866157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e391079ce005f63683ad879aa13baeea8d14bcfd2c89e518eeeec39b202aa54`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:762e90055d1cf6d89eaa670038f0ec0f819203b4e1e4a4009a2f31c69690db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580412069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024b98f52db3e2c8a2c9644f9ec1c8d7dc7848eb85b86375707f991028f270dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=C.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=16.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689abbf96956f625195182ac751906675f167eb79691c2d19bfa0593c6afa2c`  
		Last Modified: Mon, 18 Nov 2024 19:50:17 GMT  
		Size: 216.9 MB (216917317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073696c45fa176ea3f3fc4544f520fff34daacfdb49459ec9007c9702204c0b`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 2.6 MB (2583786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8a28c9d2e01dd95537d21c9026332df53afacfcd4af98db8dd25fa1dcec19`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 469.1 KB (469084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06d9c1ead3812f84edbb66c6da708342804148745fab481b92946a0f9a7aeec`  
		Last Modified: Mon, 18 Nov 2024 19:50:21 GMT  
		Size: 330.3 MB (330347848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0492df1521449d788db3473a95ccda629c266b6ec073149cb4a9f6e702452da0`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9adbf5d49c07defaf15094d541c0486868399e98806932a8194032643fd33`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd611dbd6765ada78f2f9039f19c3da61c6ea97915a958a052ef932522c5f39`  
		Last Modified: Mon, 18 Nov 2024 19:50:14 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b38f5ef2ae908ff431b974488e69112e0eb15816d833f4d0f12b2d2ce33d72f`  
		Last Modified: Mon, 18 Nov 2024 19:50:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:20a067c0e1bdb2af305cf57fe8774cf65274484b8b5968b47ef37092fca2080b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e61d02d195a16a3033222f1859602a898a11d0641f1769bcd87fdff81b296f`

```dockerfile
```

-	Layers:
	-	`sha256:e24a67bbe52a8dad7cd3de3ff41833bd804b10d4597f2cfe03c97c8bacb401e1`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 38.9 MB (38872633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfae6fc67ace16afbccfde6a84c83fdd22214347fadca460c629e35383905e8`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241118`

```console
$ docker pull odoo@sha256:5d971dd0cab1a1293d011bd48cd3ab12a4401b79737d46adfd25920e23d76baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241118` - linux; amd64

```console
$ docker pull odoo@sha256:c0ae2f45e97e0d81b14cfaa50d496e7d565f4e07584066994232b6e6ec788b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584805606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54414ef7a30e4d2e07f7da98c46eab4312664317130deeaa83850379d2ffa5fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=C.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=16.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22ae886894349380ce6bf29318b6bd99c6ad749af4c379d2f1fdd7fd16631db`  
		Last Modified: Mon, 18 Nov 2024 19:07:58 GMT  
		Size: 219.6 MB (219606475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6380a70b062f02b1480a50ced1a01f10a04d6fc2602a975adbc23e7266e727`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 2.6 MB (2575884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07dcedd9326eeeadf6cc84c2dbd288927ba155ea0f201cbbc3fb9a74cff32f2`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 469.0 KB (469003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985c2ef717573012d391c81fff67b77d78c7dab9edb138ad3f09acdf68aabb10`  
		Last Modified: Mon, 18 Nov 2024 19:08:06 GMT  
		Size: 330.7 MB (330700249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac5caaf6e73e80982166202223f1b5b24eb7210acd9e06360965be76bbba87`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418a14cdb7b9dbe398e0b1f7d3a13ef489599388a2b898fe9af2dcc45bd4948e`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0af888843a8ff6bfceb8361aacc7cea3fcdafdec57c4449071227a5a532764`  
		Last Modified: Mon, 18 Nov 2024 19:07:57 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6338c013315f69e4e1c75bd634e5615884296bc3bd3001b950e73bf7debd83`  
		Last Modified: Mon, 18 Nov 2024 19:07:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:d18c5675d4bd6fbd2cbfebce5a5f39524c862c104bcd5ddd421516b9bf4bdc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38892875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2999696c03a9b6327e8bc326c3babf518d11cae33f82ace28e31f672c7964b`

```dockerfile
```

-	Layers:
	-	`sha256:6978eea98d76ba6754271b9e5e60d7847c9bdba108d7ae9a370a79611600b87f`  
		Last Modified: Mon, 18 Nov 2024 19:07:56 GMT  
		Size: 38.9 MB (38866157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e391079ce005f63683ad879aa13baeea8d14bcfd2c89e518eeeec39b202aa54`  
		Last Modified: Mon, 18 Nov 2024 19:07:55 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241118` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:762e90055d1cf6d89eaa670038f0ec0f819203b4e1e4a4009a2f31c69690db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.4 MB (580412069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024b98f52db3e2c8a2c9644f9ec1c8d7dc7848eb85b86375707f991028f270dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=C.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=16.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=105ceca6241c08e989d505eafc29307cb5c47eb1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689abbf96956f625195182ac751906675f167eb79691c2d19bfa0593c6afa2c`  
		Last Modified: Mon, 18 Nov 2024 19:50:17 GMT  
		Size: 216.9 MB (216917317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073696c45fa176ea3f3fc4544f520fff34daacfdb49459ec9007c9702204c0b`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 2.6 MB (2583786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8a28c9d2e01dd95537d21c9026332df53afacfcd4af98db8dd25fa1dcec19`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 469.1 KB (469084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06d9c1ead3812f84edbb66c6da708342804148745fab481b92946a0f9a7aeec`  
		Last Modified: Mon, 18 Nov 2024 19:50:21 GMT  
		Size: 330.3 MB (330347848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0492df1521449d788db3473a95ccda629c266b6ec073149cb4a9f6e702452da0`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9adbf5d49c07defaf15094d541c0486868399e98806932a8194032643fd33`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd611dbd6765ada78f2f9039f19c3da61c6ea97915a958a052ef932522c5f39`  
		Last Modified: Mon, 18 Nov 2024 19:50:14 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b38f5ef2ae908ff431b974488e69112e0eb15816d833f4d0f12b2d2ce33d72f`  
		Last Modified: Mon, 18 Nov 2024 19:50:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:20a067c0e1bdb2af305cf57fe8774cf65274484b8b5968b47ef37092fca2080b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e61d02d195a16a3033222f1859602a898a11d0641f1769bcd87fdff81b296f`

```dockerfile
```

-	Layers:
	-	`sha256:e24a67bbe52a8dad7cd3de3ff41833bd804b10d4597f2cfe03c97c8bacb401e1`  
		Last Modified: Mon, 18 Nov 2024 19:50:13 GMT  
		Size: 38.9 MB (38872633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfae6fc67ace16afbccfde6a84c83fdd22214347fadca460c629e35383905e8`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:4eee6b6d3ba79440bc7b2f54a34a5c69c1bb8e7c3665c1cf5a9705be2650c0a2
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
$ docker pull odoo@sha256:78a580138f9c06607829ea4f9bc3919f582e9a6da2b39bdebdadb8b0bfec6e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 MB (598512630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9304d206a239223520390a4fe6971f0609037212b5aa457f9b5c5e2d9d9a8a4f`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b284802b65f2bd68714d7fbcdeaea4c110590011486f08ca37c60ae06bfc44`  
		Last Modified: Mon, 18 Nov 2024 19:08:05 GMT  
		Size: 233.8 MB (233765462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe4ec250cbe27dd70cfd65698ae1565c9a42f41d246832933fa4a820feb53b7`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 2.5 MB (2492885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01c5cc2001f69253b79838c6f1302b9c3dfedd53ab24b02951b83ce8f7966cc`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 470.0 KB (469981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1a48199090aaa825f2f7eae6b702c9ec218ebf45728d21581cd0128285c897`  
		Last Modified: Mon, 18 Nov 2024 19:08:07 GMT  
		Size: 332.2 MB (332246171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6729da7d119141b7a8b3a0c6fbd9769b56dfcac873511e29bf2343156bcc4b`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc371bd4222e1f28b69fae1784acf4d3712c6549196675e8d643ccb3d672dc5e`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b632f09e29e458d6c5fca7f5e9c8045c5d8401b27fc74135d25129e6786f26`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5063da10a29872c52d8ac4a1945bd9342dd9a3d986101b645f524417944f9f0b`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:78c62102ea0614dcbd314e74652483fef19e1a15046b140d9e16e2595c68511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39632578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c14f8e9854a08167899f5f4fde1c1e1324799bb04bc5620817aab7037c8b737`

```dockerfile
```

-	Layers:
	-	`sha256:af41c6871f7936feb4acbd6635dd8dd8e2ac60523b08b27cc1efba0300d4bb1a`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 39.6 MB (39605744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624d635cfe5a40d0647fff3f2fa02e46c29f2b4c9e9cd33b6a6b50a8ec387d8c`  
		Last Modified: Mon, 18 Nov 2024 19:08:01 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:804d3693b0e4ca589987741a3ed4b3e6326b52a76cd6c1f2fab4107dcea5f109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.3 MB (593298808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1ba124f4ab1310a4543f01363c574fa55a2c0bf8a2977e5ab15b237e9e7748`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b62bcbfceaf3aaab1f04f7d3bbd9e2331a5d5779873b89e583f0b38d3bf8b`  
		Last Modified: Mon, 18 Nov 2024 19:46:21 GMT  
		Size: 331.8 MB (331828667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a353d6d8526bb85ee4c32e0e55e8745b5cdfa72ac23560da4f6ff193011c8250`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac88945cbe7bd1e2cea1b6d938ae4c60f295b5dc96dfedae4fa204f2999c30e`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a7f5a613792d4f2c77f5f6deb25640804eb67253a1d012fad8f5933346c95`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e4fb5ccb37dacfcf6bece0b2c0f406e2796432e0cb44169486bc7ea673cc1`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:13baf54d05f9dcbae4fc7244e9e284b4a0b7f42c05bebe6425f206f1c916a8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39639248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6be92394e0f234ec976840235e0e56326b76c8059482d7ef2f0d94192fc4d`

```dockerfile
```

-	Layers:
	-	`sha256:88601f3ea6ea683a993aba97e650c1eed21a78501a405394da1dddf7887e47f8`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 39.6 MB (39612261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810e7ea38968b44800dbb88b4ada85d07a11cc844de2e134dd0371bb406b4498`  
		Last Modified: Mon, 18 Nov 2024 19:46:12 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:29db9ea3281920cec4a8eee8e282fc3e52c6d7dbd73d4a644bfbd23196127c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.0 MB (614979738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4672401559a0315707bb0d1411304b7cb599ce98a0d3d0c9517a1572b89ae65b`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b1b1a2be8dca791e400bacb192b1286c7889770cd1f72a4798f08914e09f7e`  
		Last Modified: Mon, 18 Nov 2024 23:19:51 GMT  
		Size: 334.0 MB (333963123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414120e0d30356154fdec29a85a6066bcda8ef3dd71bcc1d699c7c9ec43d6cb4`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9123a2301bcc7226439197b89bd9cf294532da25dd5564c70ac4a001d4f9be`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7257cb29bb83a656fcb5cf99b24b3a841c7e05c17ea05da744538f51c725e51`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a21c8d7870da40c2458047d6feb1c2bff309eb2475a0343a4dd01ef32a5d0f9`  
		Last Modified: Mon, 18 Nov 2024 23:19:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:7d6c1aa6888f9bda0ac55e15871bc499292fc099b3c6e0c9ea53d671b2e55e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39640962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fea4901cc1f9d6705549b870396003c2b162282d02a455f3691d9e811fe505`

```dockerfile
```

-	Layers:
	-	`sha256:272058d1dbf458f53345407e409e43a0db1e4bd42b8eb048c0b0a05443d96a5a`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 39.6 MB (39614071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d975e2720833d2afe8c1e9ca4bc802e30ec4497f2a1a911d9c336a05420ef5cb`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:4eee6b6d3ba79440bc7b2f54a34a5c69c1bb8e7c3665c1cf5a9705be2650c0a2
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
$ docker pull odoo@sha256:78a580138f9c06607829ea4f9bc3919f582e9a6da2b39bdebdadb8b0bfec6e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 MB (598512630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9304d206a239223520390a4fe6971f0609037212b5aa457f9b5c5e2d9d9a8a4f`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b284802b65f2bd68714d7fbcdeaea4c110590011486f08ca37c60ae06bfc44`  
		Last Modified: Mon, 18 Nov 2024 19:08:05 GMT  
		Size: 233.8 MB (233765462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe4ec250cbe27dd70cfd65698ae1565c9a42f41d246832933fa4a820feb53b7`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 2.5 MB (2492885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01c5cc2001f69253b79838c6f1302b9c3dfedd53ab24b02951b83ce8f7966cc`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 470.0 KB (469981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1a48199090aaa825f2f7eae6b702c9ec218ebf45728d21581cd0128285c897`  
		Last Modified: Mon, 18 Nov 2024 19:08:07 GMT  
		Size: 332.2 MB (332246171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6729da7d119141b7a8b3a0c6fbd9769b56dfcac873511e29bf2343156bcc4b`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc371bd4222e1f28b69fae1784acf4d3712c6549196675e8d643ccb3d672dc5e`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b632f09e29e458d6c5fca7f5e9c8045c5d8401b27fc74135d25129e6786f26`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5063da10a29872c52d8ac4a1945bd9342dd9a3d986101b645f524417944f9f0b`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78c62102ea0614dcbd314e74652483fef19e1a15046b140d9e16e2595c68511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39632578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c14f8e9854a08167899f5f4fde1c1e1324799bb04bc5620817aab7037c8b737`

```dockerfile
```

-	Layers:
	-	`sha256:af41c6871f7936feb4acbd6635dd8dd8e2ac60523b08b27cc1efba0300d4bb1a`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 39.6 MB (39605744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624d635cfe5a40d0647fff3f2fa02e46c29f2b4c9e9cd33b6a6b50a8ec387d8c`  
		Last Modified: Mon, 18 Nov 2024 19:08:01 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:804d3693b0e4ca589987741a3ed4b3e6326b52a76cd6c1f2fab4107dcea5f109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.3 MB (593298808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1ba124f4ab1310a4543f01363c574fa55a2c0bf8a2977e5ab15b237e9e7748`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b62bcbfceaf3aaab1f04f7d3bbd9e2331a5d5779873b89e583f0b38d3bf8b`  
		Last Modified: Mon, 18 Nov 2024 19:46:21 GMT  
		Size: 331.8 MB (331828667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a353d6d8526bb85ee4c32e0e55e8745b5cdfa72ac23560da4f6ff193011c8250`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac88945cbe7bd1e2cea1b6d938ae4c60f295b5dc96dfedae4fa204f2999c30e`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a7f5a613792d4f2c77f5f6deb25640804eb67253a1d012fad8f5933346c95`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e4fb5ccb37dacfcf6bece0b2c0f406e2796432e0cb44169486bc7ea673cc1`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:13baf54d05f9dcbae4fc7244e9e284b4a0b7f42c05bebe6425f206f1c916a8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39639248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6be92394e0f234ec976840235e0e56326b76c8059482d7ef2f0d94192fc4d`

```dockerfile
```

-	Layers:
	-	`sha256:88601f3ea6ea683a993aba97e650c1eed21a78501a405394da1dddf7887e47f8`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 39.6 MB (39612261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810e7ea38968b44800dbb88b4ada85d07a11cc844de2e134dd0371bb406b4498`  
		Last Modified: Mon, 18 Nov 2024 19:46:12 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:29db9ea3281920cec4a8eee8e282fc3e52c6d7dbd73d4a644bfbd23196127c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.0 MB (614979738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4672401559a0315707bb0d1411304b7cb599ce98a0d3d0c9517a1572b89ae65b`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b1b1a2be8dca791e400bacb192b1286c7889770cd1f72a4798f08914e09f7e`  
		Last Modified: Mon, 18 Nov 2024 23:19:51 GMT  
		Size: 334.0 MB (333963123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414120e0d30356154fdec29a85a6066bcda8ef3dd71bcc1d699c7c9ec43d6cb4`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9123a2301bcc7226439197b89bd9cf294532da25dd5564c70ac4a001d4f9be`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7257cb29bb83a656fcb5cf99b24b3a841c7e05c17ea05da744538f51c725e51`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a21c8d7870da40c2458047d6feb1c2bff309eb2475a0343a4dd01ef32a5d0f9`  
		Last Modified: Mon, 18 Nov 2024 23:19:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7d6c1aa6888f9bda0ac55e15871bc499292fc099b3c6e0c9ea53d671b2e55e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39640962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fea4901cc1f9d6705549b870396003c2b162282d02a455f3691d9e811fe505`

```dockerfile
```

-	Layers:
	-	`sha256:272058d1dbf458f53345407e409e43a0db1e4bd42b8eb048c0b0a05443d96a5a`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 39.6 MB (39614071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d975e2720833d2afe8c1e9ca4bc802e30ec4497f2a1a911d9c336a05420ef5cb`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241118`

```console
$ docker pull odoo@sha256:4eee6b6d3ba79440bc7b2f54a34a5c69c1bb8e7c3665c1cf5a9705be2650c0a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241118` - linux; amd64

```console
$ docker pull odoo@sha256:78a580138f9c06607829ea4f9bc3919f582e9a6da2b39bdebdadb8b0bfec6e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 MB (598512630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9304d206a239223520390a4fe6971f0609037212b5aa457f9b5c5e2d9d9a8a4f`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b284802b65f2bd68714d7fbcdeaea4c110590011486f08ca37c60ae06bfc44`  
		Last Modified: Mon, 18 Nov 2024 19:08:05 GMT  
		Size: 233.8 MB (233765462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe4ec250cbe27dd70cfd65698ae1565c9a42f41d246832933fa4a820feb53b7`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 2.5 MB (2492885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01c5cc2001f69253b79838c6f1302b9c3dfedd53ab24b02951b83ce8f7966cc`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 470.0 KB (469981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1a48199090aaa825f2f7eae6b702c9ec218ebf45728d21581cd0128285c897`  
		Last Modified: Mon, 18 Nov 2024 19:08:07 GMT  
		Size: 332.2 MB (332246171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6729da7d119141b7a8b3a0c6fbd9769b56dfcac873511e29bf2343156bcc4b`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc371bd4222e1f28b69fae1784acf4d3712c6549196675e8d643ccb3d672dc5e`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b632f09e29e458d6c5fca7f5e9c8045c5d8401b27fc74135d25129e6786f26`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5063da10a29872c52d8ac4a1945bd9342dd9a3d986101b645f524417944f9f0b`  
		Last Modified: Mon, 18 Nov 2024 19:08:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:78c62102ea0614dcbd314e74652483fef19e1a15046b140d9e16e2595c68511f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39632578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c14f8e9854a08167899f5f4fde1c1e1324799bb04bc5620817aab7037c8b737`

```dockerfile
```

-	Layers:
	-	`sha256:af41c6871f7936feb4acbd6635dd8dd8e2ac60523b08b27cc1efba0300d4bb1a`  
		Last Modified: Mon, 18 Nov 2024 19:08:02 GMT  
		Size: 39.6 MB (39605744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624d635cfe5a40d0647fff3f2fa02e46c29f2b4c9e9cd33b6a6b50a8ec387d8c`  
		Last Modified: Mon, 18 Nov 2024 19:08:01 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241118` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:804d3693b0e4ca589987741a3ed4b3e6326b52a76cd6c1f2fab4107dcea5f109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.3 MB (593298808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1ba124f4ab1310a4543f01363c574fa55a2c0bf8a2977e5ab15b237e9e7748`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b62bcbfceaf3aaab1f04f7d3bbd9e2331a5d5779873b89e583f0b38d3bf8b`  
		Last Modified: Mon, 18 Nov 2024 19:46:21 GMT  
		Size: 331.8 MB (331828667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a353d6d8526bb85ee4c32e0e55e8745b5cdfa72ac23560da4f6ff193011c8250`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac88945cbe7bd1e2cea1b6d938ae4c60f295b5dc96dfedae4fa204f2999c30e`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a7f5a613792d4f2c77f5f6deb25640804eb67253a1d012fad8f5933346c95`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e4fb5ccb37dacfcf6bece0b2c0f406e2796432e0cb44169486bc7ea673cc1`  
		Last Modified: Mon, 18 Nov 2024 19:46:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:13baf54d05f9dcbae4fc7244e9e284b4a0b7f42c05bebe6425f206f1c916a8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39639248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c6be92394e0f234ec976840235e0e56326b76c8059482d7ef2f0d94192fc4d`

```dockerfile
```

-	Layers:
	-	`sha256:88601f3ea6ea683a993aba97e650c1eed21a78501a405394da1dddf7887e47f8`  
		Last Modified: Mon, 18 Nov 2024 19:46:14 GMT  
		Size: 39.6 MB (39612261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810e7ea38968b44800dbb88b4ada85d07a11cc844de2e134dd0371bb406b4498`  
		Last Modified: Mon, 18 Nov 2024 19:46:12 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241118` - linux; ppc64le

```console
$ docker pull odoo@sha256:29db9ea3281920cec4a8eee8e282fc3e52c6d7dbd73d4a644bfbd23196127c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.0 MB (614979738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4672401559a0315707bb0d1411304b7cb599ce98a0d3d0c9517a1572b89ae65b`
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
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=17.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=dfe488ab08285c524b7ee4ea7fa3108e23fd3cc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b1b1a2be8dca791e400bacb192b1286c7889770cd1f72a4798f08914e09f7e`  
		Last Modified: Mon, 18 Nov 2024 23:19:51 GMT  
		Size: 334.0 MB (333963123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414120e0d30356154fdec29a85a6066bcda8ef3dd71bcc1d699c7c9ec43d6cb4`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9123a2301bcc7226439197b89bd9cf294532da25dd5564c70ac4a001d4f9be`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7257cb29bb83a656fcb5cf99b24b3a841c7e05c17ea05da744538f51c725e51`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a21c8d7870da40c2458047d6feb1c2bff309eb2475a0343a4dd01ef32a5d0f9`  
		Last Modified: Mon, 18 Nov 2024 23:19:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:7d6c1aa6888f9bda0ac55e15871bc499292fc099b3c6e0c9ea53d671b2e55e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39640962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fea4901cc1f9d6705549b870396003c2b162282d02a455f3691d9e811fe505`

```dockerfile
```

-	Layers:
	-	`sha256:272058d1dbf458f53345407e409e43a0db1e4bd42b8eb048c0b0a05443d96a5a`  
		Last Modified: Mon, 18 Nov 2024 23:19:36 GMT  
		Size: 39.6 MB (39614071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d975e2720833d2afe8c1e9ca4bc802e30ec4497f2a1a911d9c336a05420ef5cb`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:1d126af2c707dafebae3a68b20909c5066f8d9128b19304def1ca951e68470ff
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
$ docker pull odoo@sha256:44c9d6655704b4c808bfd7afc53552ca1119498c09e8c7ab0fbc600f412064bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.3 MB (661320497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01f61490654912d47a1dea92186b0ed4d025f65ffd660805a456a01f229bf19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c811f2769f5655f1b553436e1bd4ac7dbafb67fbfa24cf633f447496859e2`  
		Last Modified: Mon, 18 Nov 2024 19:08:52 GMT  
		Size: 254.5 MB (254518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c211ec785169346e1360589fc3e4f43e0afda8c2b4a4f9d4c3a44ec0952f17dc`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 14.2 MB (14229406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33fdea272cf641940b9da8ee256cf315556e27f5bcd2b7db3a90cbd0ab183d`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 469.7 KB (469720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f829bc51b2b5cb60228763f1e0b9fc104c07db459f40a7be09cefd11632cc732`  
		Last Modified: Mon, 18 Nov 2024 19:08:51 GMT  
		Size: 362.3 MB (362348225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c98ea5d4950ff0c3cf61e178ea96ea1d1f1c430674c9f9402d874a2e239766`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d68fec9796cc057fd575122afc4ecb3bd22775f8446b7b148ef9ad7573296`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a928543ef7a3ff998ebad925a3d67a110b89cb1da8e4c4b3ae2628b1e5eb3c`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124a8beecc6f7906280bb4a2fedec2399c912d20445f93064ee9623d2fbafd0`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:61e153527ed10347ea03987a880c29d759024dbf48dc44aa245774978ec4ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d11b46d10f0f18795facc88857c97241e49093681f8a94d332b1f95d1c315`

```dockerfile
```

-	Layers:
	-	`sha256:080368baa645d2e98594a7adb727369dd50165f521745d7e3fb02c6a840a38b3`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 57.1 MB (57134158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a78ecc4869b1944b966abb6bd3ab8b9c2b4b51ca594e35944aeb6219dc817e`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:17ef06bac5f5c6cf4b557407cce807a805b1aeb9943a51a58128314404ae6703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 MB (657715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb7453482fb703c5d73f9b33900550c000766c828805ea2de8dbcf6b1ccc199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587d98cf945cc8b8cb28976463626a968b75cfb85a7bc134788ca4acf3a2f07`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 251.9 MB (251945445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea938de0828dade1c18a83a12fb524e0eee9b0c70216313f5a11e1971311d3`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 14.2 MB (14202621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236ec3799ba5acb8613b5e789989e4eb51b91db56eac165301dd71ba9e697ac`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
		Size: 469.7 KB (469730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae744a10d78391b1110f44e4e2585783da7a29067fb0718b3b2398655b48f9`  
		Last Modified: Mon, 18 Nov 2024 19:39:38 GMT  
		Size: 362.2 MB (362202828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded0787ed2f89bc64a24e6a27e302391658fbaf6b5758fcb73113bb9098ffae`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4327210ce516c942bc9b45b3cf3d8c0c47495a2ddd46d950bb165bfebbf85`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b109be8ba62f57b86d0d64e12414ef04fe07e87e1955f307a974563a720b34d`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f03ff1ae92dbbe58ca9e9db750bc1ece93c801371abec4f4e39ad61dc26ca8`  
		Last Modified: Mon, 18 Nov 2024 19:39:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:80080bd49bf069e36c65c2bca225f09a9d2c99d026aaf0cb2281e2abdf8fa818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57168756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823669a151334d2bc22dce408fc214ffc70f433048525f44a99cd7b94cd135a2`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee007c2e5beb374719cac79457babe810a21a7602b732f62766779bfd2da01`  
		Last Modified: Mon, 18 Nov 2024 19:39:30 GMT  
		Size: 57.1 MB (57141456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31beb1a3516f7fdd51d49d2668fb6e177ff01104b86bafc07eddbb6868b014cf`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b1a172c86bc4d86e1f580ce0138165dbb288e84db03747756b7f2c4832edabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.7 MB (677683459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301356384212b5decc57778b4a3484046acfec2f554ddf32b0428b0bd890d0f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ece3150b789ddce6e306870839a2059e2166b1c870f50ce72bb0f64f7afb0`  
		Last Modified: Sat, 16 Nov 2024 03:26:15 GMT  
		Size: 265.1 MB (265135565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a057cad9c1029c466b8b4485c7e9959db3377ccb15d544d27fa01baa45706`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 14.8 MB (14775605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086a5a3d25f4fd37742c7ca85a30675397dbfa6a99c4be7c0ab236712db1ef5`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 469.7 KB (469725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926e21d23ab0bd395000afc00a0c1d28075d46f78faad263deed070d4e7cda82`  
		Last Modified: Mon, 18 Nov 2024 23:02:13 GMT  
		Size: 362.9 MB (362911302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395b54181e17d6d0c5d0b1c04b8d2de901677e66557a18cd9ae75eb59b7ce87`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32609d3e82eda8889946ee25fe630dd2117e8840886771e4d4b18ff33d457912`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53c36089601e5690180f93f0fa4a12f9749616b2b5c7d24397ef34b8f2c1c2`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9f307d5ac0ec936cf0e305ac5ec0acffc3e6bf75d2f12484cc91183998de5`  
		Last Modified: Mon, 18 Nov 2024 23:02:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:6874f0716ac1a2edbc3722a1889e12a4001254bc2c54584a888655d849c422f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57169519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b394b91e5419b72be7f3caeafe25c5c20a5cfba47398d2b99104e5a46d8dc8b`

```dockerfile
```

-	Layers:
	-	`sha256:5ed34c4b8cd1fecc5b3592864f214bd143c994cdc71cb454bbaa2a9247e2c994`  
		Last Modified: Mon, 18 Nov 2024 23:02:06 GMT  
		Size: 57.1 MB (57142321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de760f82434fafaed6015fbf70f4e40e92a2825188700830d8f11f5812ca87b`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:1d126af2c707dafebae3a68b20909c5066f8d9128b19304def1ca951e68470ff
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
$ docker pull odoo@sha256:44c9d6655704b4c808bfd7afc53552ca1119498c09e8c7ab0fbc600f412064bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.3 MB (661320497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01f61490654912d47a1dea92186b0ed4d025f65ffd660805a456a01f229bf19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c811f2769f5655f1b553436e1bd4ac7dbafb67fbfa24cf633f447496859e2`  
		Last Modified: Mon, 18 Nov 2024 19:08:52 GMT  
		Size: 254.5 MB (254518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c211ec785169346e1360589fc3e4f43e0afda8c2b4a4f9d4c3a44ec0952f17dc`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 14.2 MB (14229406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33fdea272cf641940b9da8ee256cf315556e27f5bcd2b7db3a90cbd0ab183d`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 469.7 KB (469720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f829bc51b2b5cb60228763f1e0b9fc104c07db459f40a7be09cefd11632cc732`  
		Last Modified: Mon, 18 Nov 2024 19:08:51 GMT  
		Size: 362.3 MB (362348225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c98ea5d4950ff0c3cf61e178ea96ea1d1f1c430674c9f9402d874a2e239766`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d68fec9796cc057fd575122afc4ecb3bd22775f8446b7b148ef9ad7573296`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a928543ef7a3ff998ebad925a3d67a110b89cb1da8e4c4b3ae2628b1e5eb3c`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124a8beecc6f7906280bb4a2fedec2399c912d20445f93064ee9623d2fbafd0`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:61e153527ed10347ea03987a880c29d759024dbf48dc44aa245774978ec4ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d11b46d10f0f18795facc88857c97241e49093681f8a94d332b1f95d1c315`

```dockerfile
```

-	Layers:
	-	`sha256:080368baa645d2e98594a7adb727369dd50165f521745d7e3fb02c6a840a38b3`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 57.1 MB (57134158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a78ecc4869b1944b966abb6bd3ab8b9c2b4b51ca594e35944aeb6219dc817e`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:17ef06bac5f5c6cf4b557407cce807a805b1aeb9943a51a58128314404ae6703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 MB (657715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb7453482fb703c5d73f9b33900550c000766c828805ea2de8dbcf6b1ccc199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587d98cf945cc8b8cb28976463626a968b75cfb85a7bc134788ca4acf3a2f07`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 251.9 MB (251945445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea938de0828dade1c18a83a12fb524e0eee9b0c70216313f5a11e1971311d3`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 14.2 MB (14202621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236ec3799ba5acb8613b5e789989e4eb51b91db56eac165301dd71ba9e697ac`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
		Size: 469.7 KB (469730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae744a10d78391b1110f44e4e2585783da7a29067fb0718b3b2398655b48f9`  
		Last Modified: Mon, 18 Nov 2024 19:39:38 GMT  
		Size: 362.2 MB (362202828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded0787ed2f89bc64a24e6a27e302391658fbaf6b5758fcb73113bb9098ffae`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4327210ce516c942bc9b45b3cf3d8c0c47495a2ddd46d950bb165bfebbf85`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b109be8ba62f57b86d0d64e12414ef04fe07e87e1955f307a974563a720b34d`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f03ff1ae92dbbe58ca9e9db750bc1ece93c801371abec4f4e39ad61dc26ca8`  
		Last Modified: Mon, 18 Nov 2024 19:39:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:80080bd49bf069e36c65c2bca225f09a9d2c99d026aaf0cb2281e2abdf8fa818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57168756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823669a151334d2bc22dce408fc214ffc70f433048525f44a99cd7b94cd135a2`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee007c2e5beb374719cac79457babe810a21a7602b732f62766779bfd2da01`  
		Last Modified: Mon, 18 Nov 2024 19:39:30 GMT  
		Size: 57.1 MB (57141456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31beb1a3516f7fdd51d49d2668fb6e177ff01104b86bafc07eddbb6868b014cf`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b1a172c86bc4d86e1f580ce0138165dbb288e84db03747756b7f2c4832edabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.7 MB (677683459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301356384212b5decc57778b4a3484046acfec2f554ddf32b0428b0bd890d0f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ece3150b789ddce6e306870839a2059e2166b1c870f50ce72bb0f64f7afb0`  
		Last Modified: Sat, 16 Nov 2024 03:26:15 GMT  
		Size: 265.1 MB (265135565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a057cad9c1029c466b8b4485c7e9959db3377ccb15d544d27fa01baa45706`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 14.8 MB (14775605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086a5a3d25f4fd37742c7ca85a30675397dbfa6a99c4be7c0ab236712db1ef5`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 469.7 KB (469725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926e21d23ab0bd395000afc00a0c1d28075d46f78faad263deed070d4e7cda82`  
		Last Modified: Mon, 18 Nov 2024 23:02:13 GMT  
		Size: 362.9 MB (362911302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395b54181e17d6d0c5d0b1c04b8d2de901677e66557a18cd9ae75eb59b7ce87`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32609d3e82eda8889946ee25fe630dd2117e8840886771e4d4b18ff33d457912`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53c36089601e5690180f93f0fa4a12f9749616b2b5c7d24397ef34b8f2c1c2`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9f307d5ac0ec936cf0e305ac5ec0acffc3e6bf75d2f12484cc91183998de5`  
		Last Modified: Mon, 18 Nov 2024 23:02:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6874f0716ac1a2edbc3722a1889e12a4001254bc2c54584a888655d849c422f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57169519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b394b91e5419b72be7f3caeafe25c5c20a5cfba47398d2b99104e5a46d8dc8b`

```dockerfile
```

-	Layers:
	-	`sha256:5ed34c4b8cd1fecc5b3592864f214bd143c994cdc71cb454bbaa2a9247e2c994`  
		Last Modified: Mon, 18 Nov 2024 23:02:06 GMT  
		Size: 57.1 MB (57142321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de760f82434fafaed6015fbf70f4e40e92a2825188700830d8f11f5812ca87b`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241118`

```console
$ docker pull odoo@sha256:1d126af2c707dafebae3a68b20909c5066f8d9128b19304def1ca951e68470ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241118` - linux; amd64

```console
$ docker pull odoo@sha256:44c9d6655704b4c808bfd7afc53552ca1119498c09e8c7ab0fbc600f412064bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.3 MB (661320497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01f61490654912d47a1dea92186b0ed4d025f65ffd660805a456a01f229bf19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c811f2769f5655f1b553436e1bd4ac7dbafb67fbfa24cf633f447496859e2`  
		Last Modified: Mon, 18 Nov 2024 19:08:52 GMT  
		Size: 254.5 MB (254518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c211ec785169346e1360589fc3e4f43e0afda8c2b4a4f9d4c3a44ec0952f17dc`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 14.2 MB (14229406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33fdea272cf641940b9da8ee256cf315556e27f5bcd2b7db3a90cbd0ab183d`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 469.7 KB (469720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f829bc51b2b5cb60228763f1e0b9fc104c07db459f40a7be09cefd11632cc732`  
		Last Modified: Mon, 18 Nov 2024 19:08:51 GMT  
		Size: 362.3 MB (362348225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c98ea5d4950ff0c3cf61e178ea96ea1d1f1c430674c9f9402d874a2e239766`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d68fec9796cc057fd575122afc4ecb3bd22775f8446b7b148ef9ad7573296`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a928543ef7a3ff998ebad925a3d67a110b89cb1da8e4c4b3ae2628b1e5eb3c`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124a8beecc6f7906280bb4a2fedec2399c912d20445f93064ee9623d2fbafd0`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:61e153527ed10347ea03987a880c29d759024dbf48dc44aa245774978ec4ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d11b46d10f0f18795facc88857c97241e49093681f8a94d332b1f95d1c315`

```dockerfile
```

-	Layers:
	-	`sha256:080368baa645d2e98594a7adb727369dd50165f521745d7e3fb02c6a840a38b3`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 57.1 MB (57134158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a78ecc4869b1944b966abb6bd3ab8b9c2b4b51ca594e35944aeb6219dc817e`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241118` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:17ef06bac5f5c6cf4b557407cce807a805b1aeb9943a51a58128314404ae6703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 MB (657715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb7453482fb703c5d73f9b33900550c000766c828805ea2de8dbcf6b1ccc199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587d98cf945cc8b8cb28976463626a968b75cfb85a7bc134788ca4acf3a2f07`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 251.9 MB (251945445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea938de0828dade1c18a83a12fb524e0eee9b0c70216313f5a11e1971311d3`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 14.2 MB (14202621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236ec3799ba5acb8613b5e789989e4eb51b91db56eac165301dd71ba9e697ac`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
		Size: 469.7 KB (469730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae744a10d78391b1110f44e4e2585783da7a29067fb0718b3b2398655b48f9`  
		Last Modified: Mon, 18 Nov 2024 19:39:38 GMT  
		Size: 362.2 MB (362202828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded0787ed2f89bc64a24e6a27e302391658fbaf6b5758fcb73113bb9098ffae`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4327210ce516c942bc9b45b3cf3d8c0c47495a2ddd46d950bb165bfebbf85`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b109be8ba62f57b86d0d64e12414ef04fe07e87e1955f307a974563a720b34d`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f03ff1ae92dbbe58ca9e9db750bc1ece93c801371abec4f4e39ad61dc26ca8`  
		Last Modified: Mon, 18 Nov 2024 19:39:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:80080bd49bf069e36c65c2bca225f09a9d2c99d026aaf0cb2281e2abdf8fa818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57168756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823669a151334d2bc22dce408fc214ffc70f433048525f44a99cd7b94cd135a2`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee007c2e5beb374719cac79457babe810a21a7602b732f62766779bfd2da01`  
		Last Modified: Mon, 18 Nov 2024 19:39:30 GMT  
		Size: 57.1 MB (57141456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31beb1a3516f7fdd51d49d2668fb6e177ff01104b86bafc07eddbb6868b014cf`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241118` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b1a172c86bc4d86e1f580ce0138165dbb288e84db03747756b7f2c4832edabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.7 MB (677683459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301356384212b5decc57778b4a3484046acfec2f554ddf32b0428b0bd890d0f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ece3150b789ddce6e306870839a2059e2166b1c870f50ce72bb0f64f7afb0`  
		Last Modified: Sat, 16 Nov 2024 03:26:15 GMT  
		Size: 265.1 MB (265135565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a057cad9c1029c466b8b4485c7e9959db3377ccb15d544d27fa01baa45706`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 14.8 MB (14775605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086a5a3d25f4fd37742c7ca85a30675397dbfa6a99c4be7c0ab236712db1ef5`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 469.7 KB (469725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926e21d23ab0bd395000afc00a0c1d28075d46f78faad263deed070d4e7cda82`  
		Last Modified: Mon, 18 Nov 2024 23:02:13 GMT  
		Size: 362.9 MB (362911302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395b54181e17d6d0c5d0b1c04b8d2de901677e66557a18cd9ae75eb59b7ce87`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32609d3e82eda8889946ee25fe630dd2117e8840886771e4d4b18ff33d457912`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53c36089601e5690180f93f0fa4a12f9749616b2b5c7d24397ef34b8f2c1c2`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9f307d5ac0ec936cf0e305ac5ec0acffc3e6bf75d2f12484cc91183998de5`  
		Last Modified: Mon, 18 Nov 2024 23:02:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241118` - unknown; unknown

```console
$ docker pull odoo@sha256:6874f0716ac1a2edbc3722a1889e12a4001254bc2c54584a888655d849c422f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57169519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b394b91e5419b72be7f3caeafe25c5c20a5cfba47398d2b99104e5a46d8dc8b`

```dockerfile
```

-	Layers:
	-	`sha256:5ed34c4b8cd1fecc5b3592864f214bd143c994cdc71cb454bbaa2a9247e2c994`  
		Last Modified: Mon, 18 Nov 2024 23:02:06 GMT  
		Size: 57.1 MB (57142321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de760f82434fafaed6015fbf70f4e40e92a2825188700830d8f11f5812ca87b`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:1d126af2c707dafebae3a68b20909c5066f8d9128b19304def1ca951e68470ff
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
$ docker pull odoo@sha256:44c9d6655704b4c808bfd7afc53552ca1119498c09e8c7ab0fbc600f412064bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.3 MB (661320497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01f61490654912d47a1dea92186b0ed4d025f65ffd660805a456a01f229bf19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c811f2769f5655f1b553436e1bd4ac7dbafb67fbfa24cf633f447496859e2`  
		Last Modified: Mon, 18 Nov 2024 19:08:52 GMT  
		Size: 254.5 MB (254518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c211ec785169346e1360589fc3e4f43e0afda8c2b4a4f9d4c3a44ec0952f17dc`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 14.2 MB (14229406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33fdea272cf641940b9da8ee256cf315556e27f5bcd2b7db3a90cbd0ab183d`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 469.7 KB (469720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f829bc51b2b5cb60228763f1e0b9fc104c07db459f40a7be09cefd11632cc732`  
		Last Modified: Mon, 18 Nov 2024 19:08:51 GMT  
		Size: 362.3 MB (362348225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c98ea5d4950ff0c3cf61e178ea96ea1d1f1c430674c9f9402d874a2e239766`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d68fec9796cc057fd575122afc4ecb3bd22775f8446b7b148ef9ad7573296`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a928543ef7a3ff998ebad925a3d67a110b89cb1da8e4c4b3ae2628b1e5eb3c`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124a8beecc6f7906280bb4a2fedec2399c912d20445f93064ee9623d2fbafd0`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:61e153527ed10347ea03987a880c29d759024dbf48dc44aa245774978ec4ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d11b46d10f0f18795facc88857c97241e49093681f8a94d332b1f95d1c315`

```dockerfile
```

-	Layers:
	-	`sha256:080368baa645d2e98594a7adb727369dd50165f521745d7e3fb02c6a840a38b3`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 57.1 MB (57134158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a78ecc4869b1944b966abb6bd3ab8b9c2b4b51ca594e35944aeb6219dc817e`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:17ef06bac5f5c6cf4b557407cce807a805b1aeb9943a51a58128314404ae6703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 MB (657715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb7453482fb703c5d73f9b33900550c000766c828805ea2de8dbcf6b1ccc199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587d98cf945cc8b8cb28976463626a968b75cfb85a7bc134788ca4acf3a2f07`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 251.9 MB (251945445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea938de0828dade1c18a83a12fb524e0eee9b0c70216313f5a11e1971311d3`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 14.2 MB (14202621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236ec3799ba5acb8613b5e789989e4eb51b91db56eac165301dd71ba9e697ac`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
		Size: 469.7 KB (469730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae744a10d78391b1110f44e4e2585783da7a29067fb0718b3b2398655b48f9`  
		Last Modified: Mon, 18 Nov 2024 19:39:38 GMT  
		Size: 362.2 MB (362202828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded0787ed2f89bc64a24e6a27e302391658fbaf6b5758fcb73113bb9098ffae`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4327210ce516c942bc9b45b3cf3d8c0c47495a2ddd46d950bb165bfebbf85`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b109be8ba62f57b86d0d64e12414ef04fe07e87e1955f307a974563a720b34d`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f03ff1ae92dbbe58ca9e9db750bc1ece93c801371abec4f4e39ad61dc26ca8`  
		Last Modified: Mon, 18 Nov 2024 19:39:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:80080bd49bf069e36c65c2bca225f09a9d2c99d026aaf0cb2281e2abdf8fa818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57168756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823669a151334d2bc22dce408fc214ffc70f433048525f44a99cd7b94cd135a2`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee007c2e5beb374719cac79457babe810a21a7602b732f62766779bfd2da01`  
		Last Modified: Mon, 18 Nov 2024 19:39:30 GMT  
		Size: 57.1 MB (57141456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31beb1a3516f7fdd51d49d2668fb6e177ff01104b86bafc07eddbb6868b014cf`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b1a172c86bc4d86e1f580ce0138165dbb288e84db03747756b7f2c4832edabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.7 MB (677683459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301356384212b5decc57778b4a3484046acfec2f554ddf32b0428b0bd890d0f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=ppc64le
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ece3150b789ddce6e306870839a2059e2166b1c870f50ce72bb0f64f7afb0`  
		Last Modified: Sat, 16 Nov 2024 03:26:15 GMT  
		Size: 265.1 MB (265135565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a057cad9c1029c466b8b4485c7e9959db3377ccb15d544d27fa01baa45706`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 14.8 MB (14775605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086a5a3d25f4fd37742c7ca85a30675397dbfa6a99c4be7c0ab236712db1ef5`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 469.7 KB (469725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926e21d23ab0bd395000afc00a0c1d28075d46f78faad263deed070d4e7cda82`  
		Last Modified: Mon, 18 Nov 2024 23:02:13 GMT  
		Size: 362.9 MB (362911302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395b54181e17d6d0c5d0b1c04b8d2de901677e66557a18cd9ae75eb59b7ce87`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32609d3e82eda8889946ee25fe630dd2117e8840886771e4d4b18ff33d457912`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53c36089601e5690180f93f0fa4a12f9749616b2b5c7d24397ef34b8f2c1c2`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9f307d5ac0ec936cf0e305ac5ec0acffc3e6bf75d2f12484cc91183998de5`  
		Last Modified: Mon, 18 Nov 2024 23:02:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6874f0716ac1a2edbc3722a1889e12a4001254bc2c54584a888655d849c422f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57169519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b394b91e5419b72be7f3caeafe25c5c20a5cfba47398d2b99104e5a46d8dc8b`

```dockerfile
```

-	Layers:
	-	`sha256:5ed34c4b8cd1fecc5b3592864f214bd143c994cdc71cb454bbaa2a9247e2c994`  
		Last Modified: Mon, 18 Nov 2024 23:02:06 GMT  
		Size: 57.1 MB (57142321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de760f82434fafaed6015fbf70f4e40e92a2825188700830d8f11f5812ca87b`  
		Last Modified: Mon, 18 Nov 2024 23:02:04 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
