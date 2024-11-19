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
$ docker pull odoo@sha256:1f569b29c5e3257a74625e29c71e9442bed6f740fe48701cb52862e63f727231
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
$ docker pull odoo@sha256:e71c88462bcde2837da71553d43a22edd5351f824bb8af46c9773dfb1f3a8b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614681339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023424a3e4fb58a3d6ba427be88520c119662be8d086f971c6c1dad232609b04`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Nov 2024 10:31:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Nov 2024 10:31:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
USER odoo
# Fri, 08 Nov 2024 10:31:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 10:31:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb24c7d470fc45c29a851561d281016df8f8caf37ee0b788f211955a003125d`  
		Last Modified: Fri, 08 Nov 2024 23:44:21 GMT  
		Size: 243.3 MB (243296698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b29df9bc9facc009f995251e6f6b4c8f29d8658ba6df185d5a0b26c87eb9`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 2.7 MB (2708491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e436d14cb20b9e94d971a6c72ce8bf56a6c8d3fc91e103979bd4b058ec904d`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 469.9 KB (469859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787453aca0858398fac2807e56cddd2e6953d525b20bc5591b11f2d727221e5d`  
		Last Modified: Fri, 08 Nov 2024 23:44:24 GMT  
		Size: 333.8 MB (333755604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de0e4e3c2ec1606e5508e2403c9e36de2616dee3a732a224d5e9055c869409`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec7226883c6f7aee991281b8982fc66c8de1ca8fab6fcecdd1225377e9587c`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0fe525e8bf98c9b835463c548f852b6308c99732774d808ae1758b2d89c9bd`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3f640220aff27fd34df564b4bbc24552c2d6a18c968dd243749c290d1f046`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d3ad6bf2ba1cdbbd423332b35a409960b83bfbf75ea1dd3d175603547f8e1fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e95bc618fbff69d6d5c41afc695e8fbed5475b69963625ab8480b3a189cc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d5594c17001bc579117a8fc3838a57c5ef60c4b6773311a1d97c5bfc16265`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 39.6 MB (39599107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9a709dfa62d34ba86a3f8983fe3e679396a74dec8b0cb070809259afa62cec`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:1f569b29c5e3257a74625e29c71e9442bed6f740fe48701cb52862e63f727231
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
$ docker pull odoo@sha256:e71c88462bcde2837da71553d43a22edd5351f824bb8af46c9773dfb1f3a8b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614681339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023424a3e4fb58a3d6ba427be88520c119662be8d086f971c6c1dad232609b04`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Nov 2024 10:31:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Nov 2024 10:31:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
USER odoo
# Fri, 08 Nov 2024 10:31:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 10:31:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb24c7d470fc45c29a851561d281016df8f8caf37ee0b788f211955a003125d`  
		Last Modified: Fri, 08 Nov 2024 23:44:21 GMT  
		Size: 243.3 MB (243296698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b29df9bc9facc009f995251e6f6b4c8f29d8658ba6df185d5a0b26c87eb9`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 2.7 MB (2708491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e436d14cb20b9e94d971a6c72ce8bf56a6c8d3fc91e103979bd4b058ec904d`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 469.9 KB (469859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787453aca0858398fac2807e56cddd2e6953d525b20bc5591b11f2d727221e5d`  
		Last Modified: Fri, 08 Nov 2024 23:44:24 GMT  
		Size: 333.8 MB (333755604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de0e4e3c2ec1606e5508e2403c9e36de2616dee3a732a224d5e9055c869409`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec7226883c6f7aee991281b8982fc66c8de1ca8fab6fcecdd1225377e9587c`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0fe525e8bf98c9b835463c548f852b6308c99732774d808ae1758b2d89c9bd`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3f640220aff27fd34df564b4bbc24552c2d6a18c968dd243749c290d1f046`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d3ad6bf2ba1cdbbd423332b35a409960b83bfbf75ea1dd3d175603547f8e1fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e95bc618fbff69d6d5c41afc695e8fbed5475b69963625ab8480b3a189cc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d5594c17001bc579117a8fc3838a57c5ef60c4b6773311a1d97c5bfc16265`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 39.6 MB (39599107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9a709dfa62d34ba86a3f8983fe3e679396a74dec8b0cb070809259afa62cec`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241118`

```console
$ docker pull odoo@sha256:303e8f39e48977e0f6661065eee28112e0191bc13cad39aeaee46c21ae7c7f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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

## `odoo:18`

```console
$ docker pull odoo@sha256:ce162277d5d4c5749a0095f7bac4fffb7945f5cc94b666edbe7a43e2742fa1ab
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
$ docker pull odoo@sha256:340a5bf63bc2fc3aa0663cc2699208ac14cd208ff8ce241157c3ee3587300af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673485802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72209b810e7c03a90e1302d1cdf65519f21a851ce1bae5a680ace7feb1efb09a`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH=ppc64le
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=18.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Nov 2024 10:31:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Nov 2024 10:31:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
USER odoo
# Fri, 08 Nov 2024 10:31:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:8ce447a254bc792745bb555d659b8570eb45b78857c9f33c10c4385ec6adff9c`  
		Last Modified: Sat, 16 Nov 2024 03:26:20 GMT  
		Size: 358.7 MB (358713640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf14132444dbbc50de4ebe2ce68febb45bf5ec43727376dbc4efa0cb071610`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06809f175fbe14aa96cedf61d4c9d32eff7a34b7f55f84824d98236b7797241a`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12b23d972c03b0aa31bf060e706565ec93ad2b360dda1bda5356f1f9a2d513`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a1aa9136a4acf671cfeaed4605678bf84aac4926c2c1077f5b416112623060`  
		Last Modified: Sat, 16 Nov 2024 03:25:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:9899f7a6f770a2b964a449814007a151172779306701c5012d102904792c9b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56244134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42dc5c9cc4536282e7cecf3a21cb3636a2ae5daa2cc734c243207301340c013`

```dockerfile
```

-	Layers:
	-	`sha256:d0218e9110853cc6bbc61f6c3dc242ae94dcbe9b3316f39f86e6fa8499e56cd0`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 56.2 MB (56216936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874e08d8c63b2defede13b4a514fa7b34609d35445469b3a1599e8546c4abc76`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:ce162277d5d4c5749a0095f7bac4fffb7945f5cc94b666edbe7a43e2742fa1ab
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
$ docker pull odoo@sha256:340a5bf63bc2fc3aa0663cc2699208ac14cd208ff8ce241157c3ee3587300af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673485802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72209b810e7c03a90e1302d1cdf65519f21a851ce1bae5a680ace7feb1efb09a`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH=ppc64le
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=18.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Nov 2024 10:31:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Nov 2024 10:31:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
USER odoo
# Fri, 08 Nov 2024 10:31:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:8ce447a254bc792745bb555d659b8570eb45b78857c9f33c10c4385ec6adff9c`  
		Last Modified: Sat, 16 Nov 2024 03:26:20 GMT  
		Size: 358.7 MB (358713640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf14132444dbbc50de4ebe2ce68febb45bf5ec43727376dbc4efa0cb071610`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06809f175fbe14aa96cedf61d4c9d32eff7a34b7f55f84824d98236b7797241a`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12b23d972c03b0aa31bf060e706565ec93ad2b360dda1bda5356f1f9a2d513`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a1aa9136a4acf671cfeaed4605678bf84aac4926c2c1077f5b416112623060`  
		Last Modified: Sat, 16 Nov 2024 03:25:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9899f7a6f770a2b964a449814007a151172779306701c5012d102904792c9b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56244134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42dc5c9cc4536282e7cecf3a21cb3636a2ae5daa2cc734c243207301340c013`

```dockerfile
```

-	Layers:
	-	`sha256:d0218e9110853cc6bbc61f6c3dc242ae94dcbe9b3316f39f86e6fa8499e56cd0`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 56.2 MB (56216936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874e08d8c63b2defede13b4a514fa7b34609d35445469b3a1599e8546c4abc76`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241118`

```console
$ docker pull odoo@sha256:b8915be60cdc430e93a5fea9d03d7102c5c6717f214899030a0edc5725c76cc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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

## `odoo:latest`

```console
$ docker pull odoo@sha256:ce162277d5d4c5749a0095f7bac4fffb7945f5cc94b666edbe7a43e2742fa1ab
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
$ docker pull odoo@sha256:340a5bf63bc2fc3aa0663cc2699208ac14cd208ff8ce241157c3ee3587300af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673485802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72209b810e7c03a90e1302d1cdf65519f21a851ce1bae5a680ace7feb1efb09a`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH=ppc64le
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=18.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Nov 2024 10:31:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Nov 2024 10:31:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
USER odoo
# Fri, 08 Nov 2024 10:31:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:8ce447a254bc792745bb555d659b8570eb45b78857c9f33c10c4385ec6adff9c`  
		Last Modified: Sat, 16 Nov 2024 03:26:20 GMT  
		Size: 358.7 MB (358713640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf14132444dbbc50de4ebe2ce68febb45bf5ec43727376dbc4efa0cb071610`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06809f175fbe14aa96cedf61d4c9d32eff7a34b7f55f84824d98236b7797241a`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12b23d972c03b0aa31bf060e706565ec93ad2b360dda1bda5356f1f9a2d513`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a1aa9136a4acf671cfeaed4605678bf84aac4926c2c1077f5b416112623060`  
		Last Modified: Sat, 16 Nov 2024 03:25:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9899f7a6f770a2b964a449814007a151172779306701c5012d102904792c9b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56244134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42dc5c9cc4536282e7cecf3a21cb3636a2ae5daa2cc734c243207301340c013`

```dockerfile
```

-	Layers:
	-	`sha256:d0218e9110853cc6bbc61f6c3dc242ae94dcbe9b3316f39f86e6fa8499e56cd0`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 56.2 MB (56216936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874e08d8c63b2defede13b4a514fa7b34609d35445469b3a1599e8546c4abc76`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
