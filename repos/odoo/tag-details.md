<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250428`](#odoo160-20250428)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250428`](#odoo170-20250428)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250428`](#odoo180-20250428)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:f4db5859f3568e5481a73e6c363dcff1b338d03575cdd5d36d1fb0882982d9e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:06c4f7fb374b6c1f581d131ca7db337f1d1be3d0eb0ccb96eb907aa898b6403e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.7 MB (584714818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe282bc9e1b545117d8c7276f35cc5be02041e9644743526711844b7b745a018`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=16.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc3d2694a9535d44ebe4cdc4e265ccd6e11b2fc384d8c8a3064a7d2f06061c`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 219.6 MB (219625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce79bff642752384d613eb8ad282b7ec3912a88ab0e8ae940e12a838f9a8fdd`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22234ed6960f2e860004387bb7145fe1d8ca93650689b1fcfd4ac7adef62454f`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 477.8 KB (477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ccfea0c7fb06851f9a4392eaeb351a48d826be0cfbb8d17c9b512530fdc32c`  
		Last Modified: Thu, 08 May 2025 17:17:36 GMT  
		Size: 331.7 MB (331731054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5aa632510c9161c37d36a39c524a83bb9ff3f9b0172d6a220452387bac968d`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde1dbe10fe5194b88642d2bc1e1d536d74df91018ce2bb919d751feca982d3`  
		Last Modified: Thu, 08 May 2025 17:05:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eea53f86d9fc1018138ebf566b5a74f370533884b18bd000feeac6f9c68929`  
		Last Modified: Thu, 08 May 2025 17:05:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e636801dfcb4292bf11c52c48bb004b25d2f814d87f8d1e09d58f110c19390`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e05a96eb4aae69e38618f729e26e480e8decf0d6a183e9ce7ee0efe54ed4a954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38900487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053244ef8b1aebd23005845d6b98d55bb96e172060aa43a055250db3fc8f1e08`

```dockerfile
```

-	Layers:
	-	`sha256:23c69aaa4d55b2d0d05256f9cf8eb6fc2e35207d34d6f8eb7d47009f2eaeb496`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 38.9 MB (38873769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e227498488efe3a637f5c4dba7c57bfc58a1c99f1dd3b98868035c83a75d8c06`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9518f05c300e6c9db9e3bc20924de7223f935174eb96a47a4bd655cc6e648ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580155365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5686b6fa4f4f00d73d3230670feb52af1de4f24b06a1d5f9a8a181a4f53bda2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=16.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8898a111cb7795903aad38781d056ef7246acc4cb7098e7f5cfacadf75039b`  
		Last Modified: Thu, 08 May 2025 18:04:14 GMT  
		Size: 216.9 MB (216914768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291742f5c05b276033981f860375c1ad5ad1974467d7a102c9224d157627a54`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 2.6 MB (2631541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd22cbb8e8ba0c4c65f67f7f4b037a3652c304d626a6de3daf5ba3d7aa7667`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 477.8 KB (477837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6986edcf8253e2b1a959fcc6402cc04093c13cb11acb93973c18b8d4fe184`  
		Last Modified: Thu, 08 May 2025 18:04:24 GMT  
		Size: 331.4 MB (331384141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a870bda0f8c2f986b3a7074e144ebe235c2386078dc02240c2b7e4010ab60`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e5ec4a71884c0201e0697ee2cf2ba0e260e087bd7b2733dcdb9262ea9a43a`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a049aa55e6bc1263e4d92f0a2db7da8c38b82f5f32b403edd228568f5f4d5e2`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71eb056ba076cf5441347a4a91319378d3f2c8927363395803147354f4ce629`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:297b25776b09c96892f01b838ad7490e36af9ec04cf30e21b6b9e523a80f1f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38907105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67183570a945d99eaa3c0a84226c29c7fde6d800b67d6f395b02993588c196c2`

```dockerfile
```

-	Layers:
	-	`sha256:9c25f486b74755b9d522ac5841089cb02de94ba364f99a193d06caa5179d505e`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 38.9 MB (38880235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98c8b604c225c9d3f729ffe67b92586cbf71c20bfd8d4d7dd00df9fb1f91204`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:f4db5859f3568e5481a73e6c363dcff1b338d03575cdd5d36d1fb0882982d9e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:06c4f7fb374b6c1f581d131ca7db337f1d1be3d0eb0ccb96eb907aa898b6403e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.7 MB (584714818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe282bc9e1b545117d8c7276f35cc5be02041e9644743526711844b7b745a018`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=16.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc3d2694a9535d44ebe4cdc4e265ccd6e11b2fc384d8c8a3064a7d2f06061c`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 219.6 MB (219625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce79bff642752384d613eb8ad282b7ec3912a88ab0e8ae940e12a838f9a8fdd`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22234ed6960f2e860004387bb7145fe1d8ca93650689b1fcfd4ac7adef62454f`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 477.8 KB (477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ccfea0c7fb06851f9a4392eaeb351a48d826be0cfbb8d17c9b512530fdc32c`  
		Last Modified: Thu, 08 May 2025 17:17:36 GMT  
		Size: 331.7 MB (331731054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5aa632510c9161c37d36a39c524a83bb9ff3f9b0172d6a220452387bac968d`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde1dbe10fe5194b88642d2bc1e1d536d74df91018ce2bb919d751feca982d3`  
		Last Modified: Thu, 08 May 2025 17:05:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eea53f86d9fc1018138ebf566b5a74f370533884b18bd000feeac6f9c68929`  
		Last Modified: Thu, 08 May 2025 17:05:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e636801dfcb4292bf11c52c48bb004b25d2f814d87f8d1e09d58f110c19390`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e05a96eb4aae69e38618f729e26e480e8decf0d6a183e9ce7ee0efe54ed4a954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38900487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053244ef8b1aebd23005845d6b98d55bb96e172060aa43a055250db3fc8f1e08`

```dockerfile
```

-	Layers:
	-	`sha256:23c69aaa4d55b2d0d05256f9cf8eb6fc2e35207d34d6f8eb7d47009f2eaeb496`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 38.9 MB (38873769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e227498488efe3a637f5c4dba7c57bfc58a1c99f1dd3b98868035c83a75d8c06`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9518f05c300e6c9db9e3bc20924de7223f935174eb96a47a4bd655cc6e648ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580155365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5686b6fa4f4f00d73d3230670feb52af1de4f24b06a1d5f9a8a181a4f53bda2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=16.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8898a111cb7795903aad38781d056ef7246acc4cb7098e7f5cfacadf75039b`  
		Last Modified: Thu, 08 May 2025 18:04:14 GMT  
		Size: 216.9 MB (216914768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291742f5c05b276033981f860375c1ad5ad1974467d7a102c9224d157627a54`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 2.6 MB (2631541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd22cbb8e8ba0c4c65f67f7f4b037a3652c304d626a6de3daf5ba3d7aa7667`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 477.8 KB (477837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6986edcf8253e2b1a959fcc6402cc04093c13cb11acb93973c18b8d4fe184`  
		Last Modified: Thu, 08 May 2025 18:04:24 GMT  
		Size: 331.4 MB (331384141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a870bda0f8c2f986b3a7074e144ebe235c2386078dc02240c2b7e4010ab60`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e5ec4a71884c0201e0697ee2cf2ba0e260e087bd7b2733dcdb9262ea9a43a`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a049aa55e6bc1263e4d92f0a2db7da8c38b82f5f32b403edd228568f5f4d5e2`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71eb056ba076cf5441347a4a91319378d3f2c8927363395803147354f4ce629`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:297b25776b09c96892f01b838ad7490e36af9ec04cf30e21b6b9e523a80f1f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38907105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67183570a945d99eaa3c0a84226c29c7fde6d800b67d6f395b02993588c196c2`

```dockerfile
```

-	Layers:
	-	`sha256:9c25f486b74755b9d522ac5841089cb02de94ba364f99a193d06caa5179d505e`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 38.9 MB (38880235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98c8b604c225c9d3f729ffe67b92586cbf71c20bfd8d4d7dd00df9fb1f91204`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250428`

```console
$ docker pull odoo@sha256:f4db5859f3568e5481a73e6c363dcff1b338d03575cdd5d36d1fb0882982d9e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250428` - linux; amd64

```console
$ docker pull odoo@sha256:06c4f7fb374b6c1f581d131ca7db337f1d1be3d0eb0ccb96eb907aa898b6403e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.7 MB (584714818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe282bc9e1b545117d8c7276f35cc5be02041e9644743526711844b7b745a018`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=16.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc3d2694a9535d44ebe4cdc4e265ccd6e11b2fc384d8c8a3064a7d2f06061c`  
		Last Modified: Thu, 08 May 2025 17:06:57 GMT  
		Size: 219.6 MB (219625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce79bff642752384d613eb8ad282b7ec3912a88ab0e8ae940e12a838f9a8fdd`  
		Last Modified: Thu, 08 May 2025 17:05:04 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22234ed6960f2e860004387bb7145fe1d8ca93650689b1fcfd4ac7adef62454f`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 477.8 KB (477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ccfea0c7fb06851f9a4392eaeb351a48d826be0cfbb8d17c9b512530fdc32c`  
		Last Modified: Thu, 08 May 2025 17:17:36 GMT  
		Size: 331.7 MB (331731054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5aa632510c9161c37d36a39c524a83bb9ff3f9b0172d6a220452387bac968d`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde1dbe10fe5194b88642d2bc1e1d536d74df91018ce2bb919d751feca982d3`  
		Last Modified: Thu, 08 May 2025 17:05:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eea53f86d9fc1018138ebf566b5a74f370533884b18bd000feeac6f9c68929`  
		Last Modified: Thu, 08 May 2025 17:05:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e636801dfcb4292bf11c52c48bb004b25d2f814d87f8d1e09d58f110c19390`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:e05a96eb4aae69e38618f729e26e480e8decf0d6a183e9ce7ee0efe54ed4a954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38900487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053244ef8b1aebd23005845d6b98d55bb96e172060aa43a055250db3fc8f1e08`

```dockerfile
```

-	Layers:
	-	`sha256:23c69aaa4d55b2d0d05256f9cf8eb6fc2e35207d34d6f8eb7d47009f2eaeb496`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 38.9 MB (38873769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e227498488efe3a637f5c4dba7c57bfc58a1c99f1dd3b98868035c83a75d8c06`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250428` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9518f05c300e6c9db9e3bc20924de7223f935174eb96a47a4bd655cc6e648ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580155365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5686b6fa4f4f00d73d3230670feb52af1de4f24b06a1d5f9a8a181a4f53bda2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=C.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=16.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=e5d936d73b4c08ce62eedebf7aa6d626507cee8b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8898a111cb7795903aad38781d056ef7246acc4cb7098e7f5cfacadf75039b`  
		Last Modified: Thu, 08 May 2025 18:04:14 GMT  
		Size: 216.9 MB (216914768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291742f5c05b276033981f860375c1ad5ad1974467d7a102c9224d157627a54`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 2.6 MB (2631541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd22cbb8e8ba0c4c65f67f7f4b037a3652c304d626a6de3daf5ba3d7aa7667`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 477.8 KB (477837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6986edcf8253e2b1a959fcc6402cc04093c13cb11acb93973c18b8d4fe184`  
		Last Modified: Thu, 08 May 2025 18:04:24 GMT  
		Size: 331.4 MB (331384141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a870bda0f8c2f986b3a7074e144ebe235c2386078dc02240c2b7e4010ab60`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e5ec4a71884c0201e0697ee2cf2ba0e260e087bd7b2733dcdb9262ea9a43a`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a049aa55e6bc1263e4d92f0a2db7da8c38b82f5f32b403edd228568f5f4d5e2`  
		Last Modified: Thu, 08 May 2025 18:04:01 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71eb056ba076cf5441347a4a91319378d3f2c8927363395803147354f4ce629`  
		Last Modified: Thu, 08 May 2025 18:04:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:297b25776b09c96892f01b838ad7490e36af9ec04cf30e21b6b9e523a80f1f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38907105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67183570a945d99eaa3c0a84226c29c7fde6d800b67d6f395b02993588c196c2`

```dockerfile
```

-	Layers:
	-	`sha256:9c25f486b74755b9d522ac5841089cb02de94ba364f99a193d06caa5179d505e`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 38.9 MB (38880235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98c8b604c225c9d3f729ffe67b92586cbf71c20bfd8d4d7dd00df9fb1f91204`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:5084ac6297d2d7a90b86ddc7ab853e9ae92d0465e5b29903dbe0c9902ca90c7a
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
$ docker pull odoo@sha256:191be26cd096ffdaa0e903e6e098a1d135975d7fc93b075a809def903588798f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600621508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a996ab339aedce9501d6ef3be6dc4d050de8dcbd99693e289e5845a03ba308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26f43a90ac31dbcba652ab367d454816ef7307cedbc264250d4dfb61fb9f424`  
		Last Modified: Thu, 08 May 2025 17:07:08 GMT  
		Size: 233.8 MB (233777149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb2e030107cd8191c88e56968989e51e61dd84e1c7a3c046e5089211d4a256`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 2.5 MB (2520949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1968183defe24e06ba2710a144745ec56d0b5703b2dffa1c9ffa8aee5e14cf`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 478.8 KB (478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5806c13ce5f9e2b84eca8bbe60d16345f170d80d9d17cdca0d5b097495495ae`  
		Last Modified: Thu, 08 May 2025 17:11:11 GMT  
		Size: 334.3 MB (334309531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9258b785b2105bdb64a7acf89828b389b769e5d8a5d3e16b0b1d7406565e6`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520f625c4aa0f5c4cd8ccf2e9d8993c59165eea6e91cfe8fb6b7ea042b3af68`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f52a2710d51984f6704457fee103a5c3b5f136a3154c7a270523441a138cb`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f73e09af6a80d32f9a0e94288d069e08da167ab98f9e89a1fd56e5834a9bc0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037caf718ac616adbef35e02a0d97f289d3c3db6e255baa9d96908191d7b962`

```dockerfile
```

-	Layers:
	-	`sha256:4f34cfc5ac80b79475328193aaae7d293a45781656c1caaacdb0eee7b19257b4`  
		Last Modified: Mon, 05 May 2025 16:38:33 GMT  
		Size: 39.8 MB (39777889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eeb3eff32a751a4e3abb74bcbccffdd3a956f00de4b1b89f9beda72892c34b2`  
		Last Modified: Mon, 05 May 2025 16:38:32 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2827a9c8e06f4d072ccf186ae7451adf213c3c5c40cb1e73ba5de9ea4862f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595403132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc230dc6b7839686a9e2d5fec3a37aa0352921d5fb9c3737b0d6965f7c6da28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bd7108ec52dd78260ad4f80a04efbad121aeeb116b21b9c62b4be07d95faac`  
		Last Modified: Thu, 08 May 2025 17:44:35 GMT  
		Size: 231.1 MB (231147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81098c35c49b0dbb7a64923e445aa169b5be8372947d45fdcf43f9a26fded010`  
		Last Modified: Thu, 08 May 2025 17:24:35 GMT  
		Size: 2.5 MB (2513154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8197e625cbc330bb9780b13875799b00dcb7b4c37e7c30d9fb83921330052`  
		Last Modified: Thu, 08 May 2025 17:24:47 GMT  
		Size: 478.8 KB (478808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e771ad0f94d7b9da450fc7a4d674402b5be6101d6460c2eceb86f7d96ef232`  
		Last Modified: Thu, 08 May 2025 17:49:37 GMT  
		Size: 333.9 MB (333906676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f82080906a6f7ff7b5a21f90f2c1a79d2c5b6836fdaba883977f2fe1c45072c`  
		Last Modified: Thu, 08 May 2025 17:25:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a4b8f43484e2299b8b0fe93c372f6d44e0ab73f7c502b3ff3ffc298597d5b1`  
		Last Modified: Thu, 08 May 2025 17:25:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599ff20db53697be90d4def62516d0007e949dbec4db12425e691c5a2142449`  
		Last Modified: Thu, 08 May 2025 17:25:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87501cd4cce8ca18019416d50461e216b1463228b57187cfef6f016115a84ad`  
		Last Modified: Thu, 08 May 2025 17:25:26 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f0911e2523f211e8745cf3c90c9537a9965983455a9d853bab705aca6c829bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39811383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ae4e0fead40fb1b04d1816551483b933af03186cf42e5f16829b4b4e22d9e3`

```dockerfile
```

-	Layers:
	-	`sha256:5f3ad4c7d9e6c9031ae49db707335b846e41b490a55f04fd184e92ae31626797`  
		Last Modified: Mon, 05 May 2025 18:00:58 GMT  
		Size: 39.8 MB (39784396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a41d9a2ee607cfdf32fe1b7a05a2c37aec2731670e550e73890faa307cbbf5`  
		Last Modified: Mon, 05 May 2025 18:00:56 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:94ec505a4681a232796e6b952e13fa629683e0b2207ef5753d4aaea5f6956843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617049607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039dfc6f0a6488849e6220333f0b953f5ef91fb43b1fbed8f4468d79a5b3355e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7256933103373699f4c80ac5dca8cf274fbfaf35fe3b97b004dde6379400f230`  
		Last Modified: Mon, 05 May 2025 17:55:06 GMT  
		Size: 243.3 MB (243257313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6fb2c78472406615a55a954125ead4b4fa0f7dd1f95f3a3e7b8d96aabd9c8`  
		Last Modified: Mon, 05 May 2025 17:54:58 GMT  
		Size: 2.8 MB (2839410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816597fe11dc0154be787d2f241ce0339189981b886d2037475ffd9f8fe0a27c`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 478.9 KB (478884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d53dd7bc1b744e69fbffb30efb8b1c34098506f9832f8745c6f626a186c1fbb`  
		Last Modified: Mon, 05 May 2025 17:55:09 GMT  
		Size: 336.0 MB (336028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d2f286c481ac3716a72d5d063b2246c7b91662151a06d7cd7d756a33f69632`  
		Last Modified: Mon, 05 May 2025 17:54:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b29310ce3846410a3fc3f2a437ab9eff532e6705f6d3ec8472d49c34c125d`  
		Last Modified: Mon, 05 May 2025 17:54:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a673e00dc6b451c6874436a06e32656937cdd84462bbfeecba898cfd071f803`  
		Last Modified: Mon, 05 May 2025 17:55:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd8b7c9c2b9282e471168d65b0ce5aa478f67ec3b1e035bab33014bc90aa08f`  
		Last Modified: Mon, 05 May 2025 17:55:00 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:6c1f93c5ac4767c9ca02434eed47f038feb3e3d9f486ff8f3bf6be87f3ee6da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39813087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f33deb144acd17853bdecca065baa41766f1ac5e9d777fbf528a752921205b`

```dockerfile
```

-	Layers:
	-	`sha256:928f76ffa1c4cc070829ec5fc04853d66a7d233c1f4c3078fe0125a5e4381661`  
		Last Modified: Mon, 05 May 2025 17:55:01 GMT  
		Size: 39.8 MB (39786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9396ff56f3ecfc384f556bb7df9ff5e7350907c78a59fe2252a0e8456bf5b5`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:5084ac6297d2d7a90b86ddc7ab853e9ae92d0465e5b29903dbe0c9902ca90c7a
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
$ docker pull odoo@sha256:191be26cd096ffdaa0e903e6e098a1d135975d7fc93b075a809def903588798f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600621508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a996ab339aedce9501d6ef3be6dc4d050de8dcbd99693e289e5845a03ba308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26f43a90ac31dbcba652ab367d454816ef7307cedbc264250d4dfb61fb9f424`  
		Last Modified: Thu, 08 May 2025 17:07:08 GMT  
		Size: 233.8 MB (233777149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb2e030107cd8191c88e56968989e51e61dd84e1c7a3c046e5089211d4a256`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 2.5 MB (2520949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1968183defe24e06ba2710a144745ec56d0b5703b2dffa1c9ffa8aee5e14cf`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 478.8 KB (478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5806c13ce5f9e2b84eca8bbe60d16345f170d80d9d17cdca0d5b097495495ae`  
		Last Modified: Thu, 08 May 2025 17:11:11 GMT  
		Size: 334.3 MB (334309531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9258b785b2105bdb64a7acf89828b389b769e5d8a5d3e16b0b1d7406565e6`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520f625c4aa0f5c4cd8ccf2e9d8993c59165eea6e91cfe8fb6b7ea042b3af68`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f52a2710d51984f6704457fee103a5c3b5f136a3154c7a270523441a138cb`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f73e09af6a80d32f9a0e94288d069e08da167ab98f9e89a1fd56e5834a9bc0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037caf718ac616adbef35e02a0d97f289d3c3db6e255baa9d96908191d7b962`

```dockerfile
```

-	Layers:
	-	`sha256:4f34cfc5ac80b79475328193aaae7d293a45781656c1caaacdb0eee7b19257b4`  
		Last Modified: Mon, 05 May 2025 16:38:33 GMT  
		Size: 39.8 MB (39777889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eeb3eff32a751a4e3abb74bcbccffdd3a956f00de4b1b89f9beda72892c34b2`  
		Last Modified: Mon, 05 May 2025 16:38:32 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2827a9c8e06f4d072ccf186ae7451adf213c3c5c40cb1e73ba5de9ea4862f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595403132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc230dc6b7839686a9e2d5fec3a37aa0352921d5fb9c3737b0d6965f7c6da28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bd7108ec52dd78260ad4f80a04efbad121aeeb116b21b9c62b4be07d95faac`  
		Last Modified: Thu, 08 May 2025 17:44:35 GMT  
		Size: 231.1 MB (231147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81098c35c49b0dbb7a64923e445aa169b5be8372947d45fdcf43f9a26fded010`  
		Last Modified: Thu, 08 May 2025 17:24:35 GMT  
		Size: 2.5 MB (2513154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8197e625cbc330bb9780b13875799b00dcb7b4c37e7c30d9fb83921330052`  
		Last Modified: Thu, 08 May 2025 17:24:47 GMT  
		Size: 478.8 KB (478808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e771ad0f94d7b9da450fc7a4d674402b5be6101d6460c2eceb86f7d96ef232`  
		Last Modified: Thu, 08 May 2025 17:49:37 GMT  
		Size: 333.9 MB (333906676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f82080906a6f7ff7b5a21f90f2c1a79d2c5b6836fdaba883977f2fe1c45072c`  
		Last Modified: Thu, 08 May 2025 17:25:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a4b8f43484e2299b8b0fe93c372f6d44e0ab73f7c502b3ff3ffc298597d5b1`  
		Last Modified: Thu, 08 May 2025 17:25:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599ff20db53697be90d4def62516d0007e949dbec4db12425e691c5a2142449`  
		Last Modified: Thu, 08 May 2025 17:25:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87501cd4cce8ca18019416d50461e216b1463228b57187cfef6f016115a84ad`  
		Last Modified: Thu, 08 May 2025 17:25:26 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f0911e2523f211e8745cf3c90c9537a9965983455a9d853bab705aca6c829bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39811383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ae4e0fead40fb1b04d1816551483b933af03186cf42e5f16829b4b4e22d9e3`

```dockerfile
```

-	Layers:
	-	`sha256:5f3ad4c7d9e6c9031ae49db707335b846e41b490a55f04fd184e92ae31626797`  
		Last Modified: Mon, 05 May 2025 18:00:58 GMT  
		Size: 39.8 MB (39784396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a41d9a2ee607cfdf32fe1b7a05a2c37aec2731670e550e73890faa307cbbf5`  
		Last Modified: Mon, 05 May 2025 18:00:56 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:94ec505a4681a232796e6b952e13fa629683e0b2207ef5753d4aaea5f6956843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617049607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039dfc6f0a6488849e6220333f0b953f5ef91fb43b1fbed8f4468d79a5b3355e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7256933103373699f4c80ac5dca8cf274fbfaf35fe3b97b004dde6379400f230`  
		Last Modified: Mon, 05 May 2025 17:55:06 GMT  
		Size: 243.3 MB (243257313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6fb2c78472406615a55a954125ead4b4fa0f7dd1f95f3a3e7b8d96aabd9c8`  
		Last Modified: Mon, 05 May 2025 17:54:58 GMT  
		Size: 2.8 MB (2839410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816597fe11dc0154be787d2f241ce0339189981b886d2037475ffd9f8fe0a27c`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 478.9 KB (478884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d53dd7bc1b744e69fbffb30efb8b1c34098506f9832f8745c6f626a186c1fbb`  
		Last Modified: Mon, 05 May 2025 17:55:09 GMT  
		Size: 336.0 MB (336028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d2f286c481ac3716a72d5d063b2246c7b91662151a06d7cd7d756a33f69632`  
		Last Modified: Mon, 05 May 2025 17:54:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b29310ce3846410a3fc3f2a437ab9eff532e6705f6d3ec8472d49c34c125d`  
		Last Modified: Mon, 05 May 2025 17:54:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a673e00dc6b451c6874436a06e32656937cdd84462bbfeecba898cfd071f803`  
		Last Modified: Mon, 05 May 2025 17:55:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd8b7c9c2b9282e471168d65b0ce5aa478f67ec3b1e035bab33014bc90aa08f`  
		Last Modified: Mon, 05 May 2025 17:55:00 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6c1f93c5ac4767c9ca02434eed47f038feb3e3d9f486ff8f3bf6be87f3ee6da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39813087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f33deb144acd17853bdecca065baa41766f1ac5e9d777fbf528a752921205b`

```dockerfile
```

-	Layers:
	-	`sha256:928f76ffa1c4cc070829ec5fc04853d66a7d233c1f4c3078fe0125a5e4381661`  
		Last Modified: Mon, 05 May 2025 17:55:01 GMT  
		Size: 39.8 MB (39786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9396ff56f3ecfc384f556bb7df9ff5e7350907c78a59fe2252a0e8456bf5b5`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250428`

```console
$ docker pull odoo@sha256:5084ac6297d2d7a90b86ddc7ab853e9ae92d0465e5b29903dbe0c9902ca90c7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250428` - linux; amd64

```console
$ docker pull odoo@sha256:191be26cd096ffdaa0e903e6e098a1d135975d7fc93b075a809def903588798f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.6 MB (600621508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a996ab339aedce9501d6ef3be6dc4d050de8dcbd99693e289e5845a03ba308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26f43a90ac31dbcba652ab367d454816ef7307cedbc264250d4dfb61fb9f424`  
		Last Modified: Thu, 08 May 2025 17:07:08 GMT  
		Size: 233.8 MB (233777149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb2e030107cd8191c88e56968989e51e61dd84e1c7a3c046e5089211d4a256`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 2.5 MB (2520949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1968183defe24e06ba2710a144745ec56d0b5703b2dffa1c9ffa8aee5e14cf`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 478.8 KB (478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5806c13ce5f9e2b84eca8bbe60d16345f170d80d9d17cdca0d5b097495495ae`  
		Last Modified: Thu, 08 May 2025 17:11:11 GMT  
		Size: 334.3 MB (334309531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9258b785b2105bdb64a7acf89828b389b769e5d8a5d3e16b0b1d7406565e6`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520f625c4aa0f5c4cd8ccf2e9d8993c59165eea6e91cfe8fb6b7ea042b3af68`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f52a2710d51984f6704457fee103a5c3b5f136a3154c7a270523441a138cb`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:f73e09af6a80d32f9a0e94288d069e08da167ab98f9e89a1fd56e5834a9bc0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037caf718ac616adbef35e02a0d97f289d3c3db6e255baa9d96908191d7b962`

```dockerfile
```

-	Layers:
	-	`sha256:4f34cfc5ac80b79475328193aaae7d293a45781656c1caaacdb0eee7b19257b4`  
		Last Modified: Mon, 05 May 2025 16:38:33 GMT  
		Size: 39.8 MB (39777889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eeb3eff32a751a4e3abb74bcbccffdd3a956f00de4b1b89f9beda72892c34b2`  
		Last Modified: Mon, 05 May 2025 16:38:32 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250428` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2827a9c8e06f4d072ccf186ae7451adf213c3c5c40cb1e73ba5de9ea4862f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595403132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc230dc6b7839686a9e2d5fec3a37aa0352921d5fb9c3737b0d6965f7c6da28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bd7108ec52dd78260ad4f80a04efbad121aeeb116b21b9c62b4be07d95faac`  
		Last Modified: Thu, 08 May 2025 17:44:35 GMT  
		Size: 231.1 MB (231147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81098c35c49b0dbb7a64923e445aa169b5be8372947d45fdcf43f9a26fded010`  
		Last Modified: Thu, 08 May 2025 17:24:35 GMT  
		Size: 2.5 MB (2513154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8197e625cbc330bb9780b13875799b00dcb7b4c37e7c30d9fb83921330052`  
		Last Modified: Thu, 08 May 2025 17:24:47 GMT  
		Size: 478.8 KB (478808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e771ad0f94d7b9da450fc7a4d674402b5be6101d6460c2eceb86f7d96ef232`  
		Last Modified: Thu, 08 May 2025 17:49:37 GMT  
		Size: 333.9 MB (333906676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f82080906a6f7ff7b5a21f90f2c1a79d2c5b6836fdaba883977f2fe1c45072c`  
		Last Modified: Thu, 08 May 2025 17:25:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a4b8f43484e2299b8b0fe93c372f6d44e0ab73f7c502b3ff3ffc298597d5b1`  
		Last Modified: Thu, 08 May 2025 17:25:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599ff20db53697be90d4def62516d0007e949dbec4db12425e691c5a2142449`  
		Last Modified: Thu, 08 May 2025 17:25:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87501cd4cce8ca18019416d50461e216b1463228b57187cfef6f016115a84ad`  
		Last Modified: Thu, 08 May 2025 17:25:26 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:f0911e2523f211e8745cf3c90c9537a9965983455a9d853bab705aca6c829bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39811383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ae4e0fead40fb1b04d1816551483b933af03186cf42e5f16829b4b4e22d9e3`

```dockerfile
```

-	Layers:
	-	`sha256:5f3ad4c7d9e6c9031ae49db707335b846e41b490a55f04fd184e92ae31626797`  
		Last Modified: Mon, 05 May 2025 18:00:58 GMT  
		Size: 39.8 MB (39784396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a41d9a2ee607cfdf32fe1b7a05a2c37aec2731670e550e73890faa307cbbf5`  
		Last Modified: Mon, 05 May 2025 18:00:56 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250428` - linux; ppc64le

```console
$ docker pull odoo@sha256:94ec505a4681a232796e6b952e13fa629683e0b2207ef5753d4aaea5f6956843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (617049607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039dfc6f0a6488849e6220333f0b953f5ef91fb43b1fbed8f4468d79a5b3355e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=7c3973809e0cf91494cfa2e795a43378263ca6e8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7256933103373699f4c80ac5dca8cf274fbfaf35fe3b97b004dde6379400f230`  
		Last Modified: Mon, 05 May 2025 17:55:06 GMT  
		Size: 243.3 MB (243257313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6fb2c78472406615a55a954125ead4b4fa0f7dd1f95f3a3e7b8d96aabd9c8`  
		Last Modified: Mon, 05 May 2025 17:54:58 GMT  
		Size: 2.8 MB (2839410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816597fe11dc0154be787d2f241ce0339189981b886d2037475ffd9f8fe0a27c`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 478.9 KB (478884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d53dd7bc1b744e69fbffb30efb8b1c34098506f9832f8745c6f626a186c1fbb`  
		Last Modified: Mon, 05 May 2025 17:55:09 GMT  
		Size: 336.0 MB (336028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d2f286c481ac3716a72d5d063b2246c7b91662151a06d7cd7d756a33f69632`  
		Last Modified: Mon, 05 May 2025 17:54:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b29310ce3846410a3fc3f2a437ab9eff532e6705f6d3ec8472d49c34c125d`  
		Last Modified: Mon, 05 May 2025 17:54:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a673e00dc6b451c6874436a06e32656937cdd84462bbfeecba898cfd071f803`  
		Last Modified: Mon, 05 May 2025 17:55:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd8b7c9c2b9282e471168d65b0ce5aa478f67ec3b1e035bab33014bc90aa08f`  
		Last Modified: Mon, 05 May 2025 17:55:00 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:6c1f93c5ac4767c9ca02434eed47f038feb3e3d9f486ff8f3bf6be87f3ee6da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39813087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f33deb144acd17853bdecca065baa41766f1ac5e9d777fbf528a752921205b`

```dockerfile
```

-	Layers:
	-	`sha256:928f76ffa1c4cc070829ec5fc04853d66a7d233c1f4c3078fe0125a5e4381661`  
		Last Modified: Mon, 05 May 2025 17:55:01 GMT  
		Size: 39.8 MB (39786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9396ff56f3ecfc384f556bb7df9ff5e7350907c78a59fe2252a0e8456bf5b5`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:58ebecde97869ec72b45b79983a79e0edd9985f4785cf04f66204144c58d3045
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
$ docker pull odoo@sha256:c266ed8754b7b75d0a1f1b593d0a37f74f222264ee0753d5080e8b9cea6b42b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670649328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abb3b47c4f6002878a93d9d2cb61dc1ec6a17f4c51dade8bc4799dc8989d99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce721958af367d366bcbf4cc0ee90872028155903ecd43c32659de1f3d1c87b`  
		Last Modified: Thu, 08 May 2025 17:07:51 GMT  
		Size: 254.5 MB (254517355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2c29fb667652ad6c18d746e8ad288462540385972ecfac3323c6670c32521`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 14.3 MB (14273576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb20087d90cdf7c10c8527376ceca2eda87c3f5bf4802f72f6e312924367fe2`  
		Last Modified: Thu, 08 May 2025 17:04:59 GMT  
		Size: 478.6 KB (478564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eaecfb9eced1f1c656dc186fcd04d20e440c92d3b48f9cc9c08a9cbfc1c305`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 371.7 MB (371659858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b985cfc3bf52b8b4d1afab03f9cd1cdf41576682f9e0969cb9becc4309ac9`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b37e640faa7bbf58b7769f2b2a1fe1c1dafd86649e10acf8623d3660bab2a`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ad9dc624f13799cb91687a31bbf3de903abb7c0cbbe959fc69c48658d7819`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:6fd9f6f5ac437758f6678cadbf3d2de8731c772f5f2f82b0643f148435deb84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c7f50279bcb3d1bfa31b7d6d8c500e1f671467784b514405197003988d968`

```dockerfile
```

-	Layers:
	-	`sha256:d0e3a0c9ab6eab2a44f2dc22c7f6123d1aab8a628cb44c6e444a5b4b1dede834`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c4f60889b5258b26e4cee0b6ce615ba48b3e5420a9f63246b9201a03e067c1`  
		Last Modified: Mon, 05 May 2025 16:39:10 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:524adafe6d4f9a2c4e04c9cb482aaa789efeb8b80791c57a0ef976dec52a0227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667023965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bca2b47e1d7fe0110bcc62cbf0156b395be850c388ed97a4eeb1877df672ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Thu, 08 May 2025 17:34:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Thu, 08 May 2025 17:23:37 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Thu, 08 May 2025 17:23:34 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210231a7018b03ca69d746792d72651afa53b651cc383a68db63af86715963b9`  
		Last Modified: Thu, 08 May 2025 17:41:39 GMT  
		Size: 371.5 MB (371505156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe1d153489f07da43b7fc6cb0fc2eb233b7562cc975f998ad71800f58e3651e`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e03a48516d40c33711fd64f7d3d05b9fc34038d19b7150e15c861f438adb2`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c0a7e0c7951e596f08fdcdb9df230e8921d3be05578cf3c2cbbaad968a1e34`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734564f9643c922eaf02ec63d2e4176e816ea393cfed731e3e25d2077228437`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:f6c9dce6407f2adb17aa0eb93ebfb7ef63fe3f0f7ac2d9482ad0e5a2d329fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92e991458971cd9bc9201319f32960cf0f2de5e3a8c0463755ec29b62c6c41f`

```dockerfile
```

-	Layers:
	-	`sha256:4ab44bf49fd6495ea190b698e5d6af81147e405f7be32565e0e9aaa11eff112b`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 59.2 MB (59228776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edeff0f6a890cb2df40a6a2ebc071f167c07333b7fd59fc1a1b87f6bdebe3a1`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:186197d4e8c85b87ee28473f0d58cb36c850d385864b4fb8ea0ff8e8c9ecaf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686880694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9d75d450cc063f86f0aaf3c01327181d786f418bb63f59cc3d3a932e6df2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9fe1350f6e1b5a8c58ad71b50f7776c5fc07f2cc18a9726bb8dbdad6adc48`  
		Last Modified: Mon, 05 May 2025 17:46:24 GMT  
		Size: 372.2 MB (372183871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133719afd10b139102b254de89d3cde948dc05259b4c11a23e6cb4f0ab53a3cf`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893719c4cb9d31f610adad2128cd7881aefea728b4ae9de563812c7c907c3f4`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928368c5b8efeead48bab993fbf849c634ac24968677095841b050752a0d7128`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6772dd4d24330136e0bb55571c1f9e8d02b559d2ba6c5fa8e9bf09b953d45ffd`  
		Last Modified: Mon, 05 May 2025 17:45:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:32ea24da4e1ccb1814f0cc149c8becd759cb599af8338dc954349087cb9839ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3917ea9097ba151e4a2945ce013933d556a4d0a56bc669ece0fda4e8ec02e20f`

```dockerfile
```

-	Layers:
	-	`sha256:72d8b734aa153d1f5bad70b1907e28540c6a8d324a7a4335bc0c12fa61200cd5`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 59.2 MB (59229632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c8d19dd96517905493d8fb3a0abecc92e5d7a6c882725ca647a9a13b95eeaf`  
		Last Modified: Mon, 05 May 2025 17:45:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:58ebecde97869ec72b45b79983a79e0edd9985f4785cf04f66204144c58d3045
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
$ docker pull odoo@sha256:c266ed8754b7b75d0a1f1b593d0a37f74f222264ee0753d5080e8b9cea6b42b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670649328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abb3b47c4f6002878a93d9d2cb61dc1ec6a17f4c51dade8bc4799dc8989d99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce721958af367d366bcbf4cc0ee90872028155903ecd43c32659de1f3d1c87b`  
		Last Modified: Thu, 08 May 2025 17:07:51 GMT  
		Size: 254.5 MB (254517355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2c29fb667652ad6c18d746e8ad288462540385972ecfac3323c6670c32521`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 14.3 MB (14273576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb20087d90cdf7c10c8527376ceca2eda87c3f5bf4802f72f6e312924367fe2`  
		Last Modified: Thu, 08 May 2025 17:04:59 GMT  
		Size: 478.6 KB (478564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eaecfb9eced1f1c656dc186fcd04d20e440c92d3b48f9cc9c08a9cbfc1c305`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 371.7 MB (371659858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b985cfc3bf52b8b4d1afab03f9cd1cdf41576682f9e0969cb9becc4309ac9`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b37e640faa7bbf58b7769f2b2a1fe1c1dafd86649e10acf8623d3660bab2a`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ad9dc624f13799cb91687a31bbf3de903abb7c0cbbe959fc69c48658d7819`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6fd9f6f5ac437758f6678cadbf3d2de8731c772f5f2f82b0643f148435deb84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c7f50279bcb3d1bfa31b7d6d8c500e1f671467784b514405197003988d968`

```dockerfile
```

-	Layers:
	-	`sha256:d0e3a0c9ab6eab2a44f2dc22c7f6123d1aab8a628cb44c6e444a5b4b1dede834`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c4f60889b5258b26e4cee0b6ce615ba48b3e5420a9f63246b9201a03e067c1`  
		Last Modified: Mon, 05 May 2025 16:39:10 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:524adafe6d4f9a2c4e04c9cb482aaa789efeb8b80791c57a0ef976dec52a0227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667023965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bca2b47e1d7fe0110bcc62cbf0156b395be850c388ed97a4eeb1877df672ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Thu, 08 May 2025 17:34:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Thu, 08 May 2025 17:23:37 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Thu, 08 May 2025 17:23:34 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210231a7018b03ca69d746792d72651afa53b651cc383a68db63af86715963b9`  
		Last Modified: Thu, 08 May 2025 17:41:39 GMT  
		Size: 371.5 MB (371505156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe1d153489f07da43b7fc6cb0fc2eb233b7562cc975f998ad71800f58e3651e`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e03a48516d40c33711fd64f7d3d05b9fc34038d19b7150e15c861f438adb2`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c0a7e0c7951e596f08fdcdb9df230e8921d3be05578cf3c2cbbaad968a1e34`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734564f9643c922eaf02ec63d2e4176e816ea393cfed731e3e25d2077228437`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f6c9dce6407f2adb17aa0eb93ebfb7ef63fe3f0f7ac2d9482ad0e5a2d329fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92e991458971cd9bc9201319f32960cf0f2de5e3a8c0463755ec29b62c6c41f`

```dockerfile
```

-	Layers:
	-	`sha256:4ab44bf49fd6495ea190b698e5d6af81147e405f7be32565e0e9aaa11eff112b`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 59.2 MB (59228776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edeff0f6a890cb2df40a6a2ebc071f167c07333b7fd59fc1a1b87f6bdebe3a1`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:186197d4e8c85b87ee28473f0d58cb36c850d385864b4fb8ea0ff8e8c9ecaf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686880694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9d75d450cc063f86f0aaf3c01327181d786f418bb63f59cc3d3a932e6df2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9fe1350f6e1b5a8c58ad71b50f7776c5fc07f2cc18a9726bb8dbdad6adc48`  
		Last Modified: Mon, 05 May 2025 17:46:24 GMT  
		Size: 372.2 MB (372183871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133719afd10b139102b254de89d3cde948dc05259b4c11a23e6cb4f0ab53a3cf`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893719c4cb9d31f610adad2128cd7881aefea728b4ae9de563812c7c907c3f4`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928368c5b8efeead48bab993fbf849c634ac24968677095841b050752a0d7128`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6772dd4d24330136e0bb55571c1f9e8d02b559d2ba6c5fa8e9bf09b953d45ffd`  
		Last Modified: Mon, 05 May 2025 17:45:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:32ea24da4e1ccb1814f0cc149c8becd759cb599af8338dc954349087cb9839ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3917ea9097ba151e4a2945ce013933d556a4d0a56bc669ece0fda4e8ec02e20f`

```dockerfile
```

-	Layers:
	-	`sha256:72d8b734aa153d1f5bad70b1907e28540c6a8d324a7a4335bc0c12fa61200cd5`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 59.2 MB (59229632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c8d19dd96517905493d8fb3a0abecc92e5d7a6c882725ca647a9a13b95eeaf`  
		Last Modified: Mon, 05 May 2025 17:45:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250428`

```console
$ docker pull odoo@sha256:58ebecde97869ec72b45b79983a79e0edd9985f4785cf04f66204144c58d3045
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250428` - linux; amd64

```console
$ docker pull odoo@sha256:c266ed8754b7b75d0a1f1b593d0a37f74f222264ee0753d5080e8b9cea6b42b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670649328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abb3b47c4f6002878a93d9d2cb61dc1ec6a17f4c51dade8bc4799dc8989d99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce721958af367d366bcbf4cc0ee90872028155903ecd43c32659de1f3d1c87b`  
		Last Modified: Thu, 08 May 2025 17:07:51 GMT  
		Size: 254.5 MB (254517355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2c29fb667652ad6c18d746e8ad288462540385972ecfac3323c6670c32521`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 14.3 MB (14273576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb20087d90cdf7c10c8527376ceca2eda87c3f5bf4802f72f6e312924367fe2`  
		Last Modified: Thu, 08 May 2025 17:04:59 GMT  
		Size: 478.6 KB (478564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eaecfb9eced1f1c656dc186fcd04d20e440c92d3b48f9cc9c08a9cbfc1c305`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 371.7 MB (371659858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b985cfc3bf52b8b4d1afab03f9cd1cdf41576682f9e0969cb9becc4309ac9`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b37e640faa7bbf58b7769f2b2a1fe1c1dafd86649e10acf8623d3660bab2a`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ad9dc624f13799cb91687a31bbf3de903abb7c0cbbe959fc69c48658d7819`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:6fd9f6f5ac437758f6678cadbf3d2de8731c772f5f2f82b0643f148435deb84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c7f50279bcb3d1bfa31b7d6d8c500e1f671467784b514405197003988d968`

```dockerfile
```

-	Layers:
	-	`sha256:d0e3a0c9ab6eab2a44f2dc22c7f6123d1aab8a628cb44c6e444a5b4b1dede834`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c4f60889b5258b26e4cee0b6ce615ba48b3e5420a9f63246b9201a03e067c1`  
		Last Modified: Mon, 05 May 2025 16:39:10 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250428` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:524adafe6d4f9a2c4e04c9cb482aaa789efeb8b80791c57a0ef976dec52a0227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667023965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bca2b47e1d7fe0110bcc62cbf0156b395be850c388ed97a4eeb1877df672ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Thu, 08 May 2025 17:34:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Thu, 08 May 2025 17:23:37 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Thu, 08 May 2025 17:23:34 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210231a7018b03ca69d746792d72651afa53b651cc383a68db63af86715963b9`  
		Last Modified: Thu, 08 May 2025 17:41:39 GMT  
		Size: 371.5 MB (371505156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe1d153489f07da43b7fc6cb0fc2eb233b7562cc975f998ad71800f58e3651e`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e03a48516d40c33711fd64f7d3d05b9fc34038d19b7150e15c861f438adb2`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c0a7e0c7951e596f08fdcdb9df230e8921d3be05578cf3c2cbbaad968a1e34`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734564f9643c922eaf02ec63d2e4176e816ea393cfed731e3e25d2077228437`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:f6c9dce6407f2adb17aa0eb93ebfb7ef63fe3f0f7ac2d9482ad0e5a2d329fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92e991458971cd9bc9201319f32960cf0f2de5e3a8c0463755ec29b62c6c41f`

```dockerfile
```

-	Layers:
	-	`sha256:4ab44bf49fd6495ea190b698e5d6af81147e405f7be32565e0e9aaa11eff112b`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 59.2 MB (59228776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edeff0f6a890cb2df40a6a2ebc071f167c07333b7fd59fc1a1b87f6bdebe3a1`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250428` - linux; ppc64le

```console
$ docker pull odoo@sha256:186197d4e8c85b87ee28473f0d58cb36c850d385864b4fb8ea0ff8e8c9ecaf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686880694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9d75d450cc063f86f0aaf3c01327181d786f418bb63f59cc3d3a932e6df2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9fe1350f6e1b5a8c58ad71b50f7776c5fc07f2cc18a9726bb8dbdad6adc48`  
		Last Modified: Mon, 05 May 2025 17:46:24 GMT  
		Size: 372.2 MB (372183871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133719afd10b139102b254de89d3cde948dc05259b4c11a23e6cb4f0ab53a3cf`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893719c4cb9d31f610adad2128cd7881aefea728b4ae9de563812c7c907c3f4`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928368c5b8efeead48bab993fbf849c634ac24968677095841b050752a0d7128`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6772dd4d24330136e0bb55571c1f9e8d02b559d2ba6c5fa8e9bf09b953d45ffd`  
		Last Modified: Mon, 05 May 2025 17:45:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:32ea24da4e1ccb1814f0cc149c8becd759cb599af8338dc954349087cb9839ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3917ea9097ba151e4a2945ce013933d556a4d0a56bc669ece0fda4e8ec02e20f`

```dockerfile
```

-	Layers:
	-	`sha256:72d8b734aa153d1f5bad70b1907e28540c6a8d324a7a4335bc0c12fa61200cd5`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 59.2 MB (59229632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c8d19dd96517905493d8fb3a0abecc92e5d7a6c882725ca647a9a13b95eeaf`  
		Last Modified: Mon, 05 May 2025 17:45:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:58ebecde97869ec72b45b79983a79e0edd9985f4785cf04f66204144c58d3045
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
$ docker pull odoo@sha256:c266ed8754b7b75d0a1f1b593d0a37f74f222264ee0753d5080e8b9cea6b42b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670649328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abb3b47c4f6002878a93d9d2cb61dc1ec6a17f4c51dade8bc4799dc8989d99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce721958af367d366bcbf4cc0ee90872028155903ecd43c32659de1f3d1c87b`  
		Last Modified: Thu, 08 May 2025 17:07:51 GMT  
		Size: 254.5 MB (254517355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2c29fb667652ad6c18d746e8ad288462540385972ecfac3323c6670c32521`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 14.3 MB (14273576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb20087d90cdf7c10c8527376ceca2eda87c3f5bf4802f72f6e312924367fe2`  
		Last Modified: Thu, 08 May 2025 17:04:59 GMT  
		Size: 478.6 KB (478564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eaecfb9eced1f1c656dc186fcd04d20e440c92d3b48f9cc9c08a9cbfc1c305`  
		Last Modified: Thu, 08 May 2025 17:08:01 GMT  
		Size: 371.7 MB (371659858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Thu, 08 May 2025 17:04:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b985cfc3bf52b8b4d1afab03f9cd1cdf41576682f9e0969cb9becc4309ac9`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b37e640faa7bbf58b7769f2b2a1fe1c1dafd86649e10acf8623d3660bab2a`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ad9dc624f13799cb91687a31bbf3de903abb7c0cbbe959fc69c48658d7819`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6fd9f6f5ac437758f6678cadbf3d2de8731c772f5f2f82b0643f148435deb84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c7f50279bcb3d1bfa31b7d6d8c500e1f671467784b514405197003988d968`

```dockerfile
```

-	Layers:
	-	`sha256:d0e3a0c9ab6eab2a44f2dc22c7f6123d1aab8a628cb44c6e444a5b4b1dede834`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c4f60889b5258b26e4cee0b6ce615ba48b3e5420a9f63246b9201a03e067c1`  
		Last Modified: Mon, 05 May 2025 16:39:10 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:524adafe6d4f9a2c4e04c9cb482aaa789efeb8b80791c57a0ef976dec52a0227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667023965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bca2b47e1d7fe0110bcc62cbf0156b395be850c388ed97a4eeb1877df672ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Thu, 08 May 2025 17:34:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Thu, 08 May 2025 17:23:37 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Thu, 08 May 2025 17:23:34 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210231a7018b03ca69d746792d72651afa53b651cc383a68db63af86715963b9`  
		Last Modified: Thu, 08 May 2025 17:41:39 GMT  
		Size: 371.5 MB (371505156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe1d153489f07da43b7fc6cb0fc2eb233b7562cc975f998ad71800f58e3651e`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e03a48516d40c33711fd64f7d3d05b9fc34038d19b7150e15c861f438adb2`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c0a7e0c7951e596f08fdcdb9df230e8921d3be05578cf3c2cbbaad968a1e34`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734564f9643c922eaf02ec63d2e4176e816ea393cfed731e3e25d2077228437`  
		Last Modified: Thu, 08 May 2025 17:23:33 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f6c9dce6407f2adb17aa0eb93ebfb7ef63fe3f0f7ac2d9482ad0e5a2d329fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92e991458971cd9bc9201319f32960cf0f2de5e3a8c0463755ec29b62c6c41f`

```dockerfile
```

-	Layers:
	-	`sha256:4ab44bf49fd6495ea190b698e5d6af81147e405f7be32565e0e9aaa11eff112b`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 59.2 MB (59228776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edeff0f6a890cb2df40a6a2ebc071f167c07333b7fd59fc1a1b87f6bdebe3a1`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:186197d4e8c85b87ee28473f0d58cb36c850d385864b4fb8ea0ff8e8c9ecaf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686880694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9d75d450cc063f86f0aaf3c01327181d786f418bb63f59cc3d3a932e6df2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9fe1350f6e1b5a8c58ad71b50f7776c5fc07f2cc18a9726bb8dbdad6adc48`  
		Last Modified: Mon, 05 May 2025 17:46:24 GMT  
		Size: 372.2 MB (372183871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133719afd10b139102b254de89d3cde948dc05259b4c11a23e6cb4f0ab53a3cf`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893719c4cb9d31f610adad2128cd7881aefea728b4ae9de563812c7c907c3f4`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928368c5b8efeead48bab993fbf849c634ac24968677095841b050752a0d7128`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6772dd4d24330136e0bb55571c1f9e8d02b559d2ba6c5fa8e9bf09b953d45ffd`  
		Last Modified: Mon, 05 May 2025 17:45:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:32ea24da4e1ccb1814f0cc149c8becd759cb599af8338dc954349087cb9839ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3917ea9097ba151e4a2945ce013933d556a4d0a56bc669ece0fda4e8ec02e20f`

```dockerfile
```

-	Layers:
	-	`sha256:72d8b734aa153d1f5bad70b1907e28540c6a8d324a7a4335bc0c12fa61200cd5`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 59.2 MB (59229632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c8d19dd96517905493d8fb3a0abecc92e5d7a6c882725ca647a9a13b95eeaf`  
		Last Modified: Mon, 05 May 2025 17:45:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
