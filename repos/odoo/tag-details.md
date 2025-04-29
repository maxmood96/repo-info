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
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc3d2694a9535d44ebe4cdc4e265ccd6e11b2fc384d8c8a3064a7d2f06061c`  
		Last Modified: Mon, 28 Apr 2025 22:00:31 GMT  
		Size: 219.6 MB (219625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce79bff642752384d613eb8ad282b7ec3912a88ab0e8ae940e12a838f9a8fdd`  
		Last Modified: Mon, 28 Apr 2025 22:00:27 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22234ed6960f2e860004387bb7145fe1d8ca93650689b1fcfd4ac7adef62454f`  
		Last Modified: Mon, 28 Apr 2025 22:00:27 GMT  
		Size: 477.8 KB (477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ccfea0c7fb06851f9a4392eaeb351a48d826be0cfbb8d17c9b512530fdc32c`  
		Last Modified: Mon, 28 Apr 2025 22:00:33 GMT  
		Size: 331.7 MB (331731054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5aa632510c9161c37d36a39c524a83bb9ff3f9b0172d6a220452387bac968d`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde1dbe10fe5194b88642d2bc1e1d536d74df91018ce2bb919d751feca982d3`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eea53f86d9fc1018138ebf566b5a74f370533884b18bd000feeac6f9c68929`  
		Last Modified: Mon, 28 Apr 2025 22:00:29 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e636801dfcb4292bf11c52c48bb004b25d2f814d87f8d1e09d58f110c19390`  
		Last Modified: Mon, 28 Apr 2025 22:00:29 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8898a111cb7795903aad38781d056ef7246acc4cb7098e7f5cfacadf75039b`  
		Last Modified: Tue, 29 Apr 2025 20:29:26 GMT  
		Size: 216.9 MB (216914768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291742f5c05b276033981f860375c1ad5ad1974467d7a102c9224d157627a54`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 2.6 MB (2631541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd22cbb8e8ba0c4c65f67f7f4b037a3652c304d626a6de3daf5ba3d7aa7667`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 477.8 KB (477837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6986edcf8253e2b1a959fcc6402cc04093c13cb11acb93973c18b8d4fe184`  
		Last Modified: Tue, 29 Apr 2025 20:29:32 GMT  
		Size: 331.4 MB (331384141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a870bda0f8c2f986b3a7074e144ebe235c2386078dc02240c2b7e4010ab60`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e5ec4a71884c0201e0697ee2cf2ba0e260e087bd7b2733dcdb9262ea9a43a`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a049aa55e6bc1263e4d92f0a2db7da8c38b82f5f32b403edd228568f5f4d5e2`  
		Last Modified: Tue, 29 Apr 2025 20:29:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71eb056ba076cf5441347a4a91319378d3f2c8927363395803147354f4ce629`  
		Last Modified: Tue, 29 Apr 2025 20:29:24 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc3d2694a9535d44ebe4cdc4e265ccd6e11b2fc384d8c8a3064a7d2f06061c`  
		Last Modified: Mon, 28 Apr 2025 22:00:31 GMT  
		Size: 219.6 MB (219625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce79bff642752384d613eb8ad282b7ec3912a88ab0e8ae940e12a838f9a8fdd`  
		Last Modified: Mon, 28 Apr 2025 22:00:27 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22234ed6960f2e860004387bb7145fe1d8ca93650689b1fcfd4ac7adef62454f`  
		Last Modified: Mon, 28 Apr 2025 22:00:27 GMT  
		Size: 477.8 KB (477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ccfea0c7fb06851f9a4392eaeb351a48d826be0cfbb8d17c9b512530fdc32c`  
		Last Modified: Mon, 28 Apr 2025 22:00:33 GMT  
		Size: 331.7 MB (331731054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5aa632510c9161c37d36a39c524a83bb9ff3f9b0172d6a220452387bac968d`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde1dbe10fe5194b88642d2bc1e1d536d74df91018ce2bb919d751feca982d3`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eea53f86d9fc1018138ebf566b5a74f370533884b18bd000feeac6f9c68929`  
		Last Modified: Mon, 28 Apr 2025 22:00:29 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e636801dfcb4292bf11c52c48bb004b25d2f814d87f8d1e09d58f110c19390`  
		Last Modified: Mon, 28 Apr 2025 22:00:29 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8898a111cb7795903aad38781d056ef7246acc4cb7098e7f5cfacadf75039b`  
		Last Modified: Tue, 29 Apr 2025 20:29:26 GMT  
		Size: 216.9 MB (216914768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291742f5c05b276033981f860375c1ad5ad1974467d7a102c9224d157627a54`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 2.6 MB (2631541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd22cbb8e8ba0c4c65f67f7f4b037a3652c304d626a6de3daf5ba3d7aa7667`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 477.8 KB (477837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6986edcf8253e2b1a959fcc6402cc04093c13cb11acb93973c18b8d4fe184`  
		Last Modified: Tue, 29 Apr 2025 20:29:32 GMT  
		Size: 331.4 MB (331384141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a870bda0f8c2f986b3a7074e144ebe235c2386078dc02240c2b7e4010ab60`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e5ec4a71884c0201e0697ee2cf2ba0e260e087bd7b2733dcdb9262ea9a43a`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a049aa55e6bc1263e4d92f0a2db7da8c38b82f5f32b403edd228568f5f4d5e2`  
		Last Modified: Tue, 29 Apr 2025 20:29:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71eb056ba076cf5441347a4a91319378d3f2c8927363395803147354f4ce629`  
		Last Modified: Tue, 29 Apr 2025 20:29:24 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc3d2694a9535d44ebe4cdc4e265ccd6e11b2fc384d8c8a3064a7d2f06061c`  
		Last Modified: Mon, 28 Apr 2025 22:00:31 GMT  
		Size: 219.6 MB (219625601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce79bff642752384d613eb8ad282b7ec3912a88ab0e8ae940e12a838f9a8fdd`  
		Last Modified: Mon, 28 Apr 2025 22:00:27 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22234ed6960f2e860004387bb7145fe1d8ca93650689b1fcfd4ac7adef62454f`  
		Last Modified: Mon, 28 Apr 2025 22:00:27 GMT  
		Size: 477.8 KB (477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ccfea0c7fb06851f9a4392eaeb351a48d826be0cfbb8d17c9b512530fdc32c`  
		Last Modified: Mon, 28 Apr 2025 22:00:33 GMT  
		Size: 331.7 MB (331731054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5aa632510c9161c37d36a39c524a83bb9ff3f9b0172d6a220452387bac968d`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde1dbe10fe5194b88642d2bc1e1d536d74df91018ce2bb919d751feca982d3`  
		Last Modified: Mon, 28 Apr 2025 22:00:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eea53f86d9fc1018138ebf566b5a74f370533884b18bd000feeac6f9c68929`  
		Last Modified: Mon, 28 Apr 2025 22:00:29 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e636801dfcb4292bf11c52c48bb004b25d2f814d87f8d1e09d58f110c19390`  
		Last Modified: Mon, 28 Apr 2025 22:00:29 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8898a111cb7795903aad38781d056ef7246acc4cb7098e7f5cfacadf75039b`  
		Last Modified: Tue, 29 Apr 2025 20:29:26 GMT  
		Size: 216.9 MB (216914768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291742f5c05b276033981f860375c1ad5ad1974467d7a102c9224d157627a54`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 2.6 MB (2631541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd22cbb8e8ba0c4c65f67f7f4b037a3652c304d626a6de3daf5ba3d7aa7667`  
		Last Modified: Tue, 29 Apr 2025 20:29:21 GMT  
		Size: 477.8 KB (477837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6986edcf8253e2b1a959fcc6402cc04093c13cb11acb93973c18b8d4fe184`  
		Last Modified: Tue, 29 Apr 2025 20:29:32 GMT  
		Size: 331.4 MB (331384141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a870bda0f8c2f986b3a7074e144ebe235c2386078dc02240c2b7e4010ab60`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e5ec4a71884c0201e0697ee2cf2ba0e260e087bd7b2733dcdb9262ea9a43a`  
		Last Modified: Tue, 29 Apr 2025 20:29:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a049aa55e6bc1263e4d92f0a2db7da8c38b82f5f32b403edd228568f5f4d5e2`  
		Last Modified: Tue, 29 Apr 2025 20:29:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71eb056ba076cf5441347a4a91319378d3f2c8927363395803147354f4ce629`  
		Last Modified: Tue, 29 Apr 2025 20:29:24 GMT  
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
$ docker pull odoo@sha256:6ab9e48421a010fd58f9eec8c541932298f04774a4dba5bbd12eb96f4705fad2
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
$ docker pull odoo@sha256:92606fdaac7494c8fa94f3220db09316a42eb4456f3474e6ee52b5b71a328e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 MB (602933104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8f4866a40efdbc0426e9ee41d89735f3df9d81b3c665173228332ee8e8241c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e164585a9b2ab2376b4a61f33cdd04c5f633e88e0245e23f0c477f585bf360`  
		Last Modified: Mon, 28 Apr 2025 18:03:16 GMT  
		Size: 236.1 MB (236083694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e49a8f07ec95c79ecf58c4d0acfda748e36521d93595f5f57ead484d788300e`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 2.5 MB (2520995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdee84202f8ac2580c0dde0e1d46fc86b582725a643f14a078d3155ef3afb71`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85559947abfde093503134d3f5b1364aa74c1de1b1969cddca72a2e05c77f5ef`  
		Last Modified: Mon, 28 Apr 2025 18:03:17 GMT  
		Size: 334.3 MB (334314790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bfa8d80f606bca5a94b96a70db21424401550fa6905806b031da1c487f1968`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dfb5d91879ac991d488e6851a129e63b8ebd07ccbb2664d43a9576e397606f`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f04aa20bc8271f4cc8aa7f6199b3df8c81d306f00f0ad648903cb006e9c05`  
		Last Modified: Mon, 28 Apr 2025 18:03:14 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955b635fc44f92d77a918f27de4a4776ecdf2c58b09e7544b052f69dae926ef`  
		Last Modified: Mon, 28 Apr 2025 18:03:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:98ed5c4c2432f8cbef01fd9868abc70f2f9483050622674b5f8cc146ff409606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5aad374b975fc7757859d6ac0fc49392aa4cc949b69454a7f54147aa12dc1`

```dockerfile
```

-	Layers:
	-	`sha256:37b45e6f56347b458f91987573795cf511ea43729536f1c6ef25a04ba0aa1eba`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 39.8 MB (39777889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336f7a93fa3ad3d3e340570e1cdc5fb9c61d008e2cbc5544725ea7672cb27f6e`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cff529909fb5b1b99f4dc254604310c70ed29e93b46cbedb6e443edd5015965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595408050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa073c673131144ecec83a18ed3832f11fd20bac0ecb2b5f69f5e2316431ba0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0def44f1c28c355fc7e6000d95019736f1de630210f253651882fb9b1e660e`  
		Last Modified: Mon, 28 Apr 2025 19:09:49 GMT  
		Size: 333.9 MB (333904202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c08ecf97203f25375cf2cc05927414d5df2739605519c4c75e25f6995adcf7`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8b25bb6e02553a1d9fa7ed8427c6878e3f7d3244568d94b9cffad81ae3954`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa944b690065e88cb206f58134fb2a727826179efd59169397f3b9fedb616fb0`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771dcc8fe3ac6ce4a80dcc52d3a82b5648866b2f076e7fabdfca83f0b89c582`  
		Last Modified: Mon, 28 Apr 2025 19:09:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b8ef680395885aea5e79265436e6513ebdea8211c0f2068d60724e4558fc7437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39811383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c13d05b1c6ca6a5b80c6cc468732baef75019f761ad2ec91101d53d5733d84`

```dockerfile
```

-	Layers:
	-	`sha256:19aed45cc6c1e91254bba1b8d6f03bd3ed381193d440d8488d9dd1ab551918f8`  
		Last Modified: Mon, 28 Apr 2025 19:09:43 GMT  
		Size: 39.8 MB (39784396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892e76757bf2a250674ac91ab09c22511bb0604c5592ed202ca240571d71d4ab`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:0470ad5f2896c499da0300d5dae66fcb7c280c9e2bf645e949b7cb49ad864763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617059115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6940082682289006a3aaf2562bb82bb284f6c53d8d5f73df3bf02be6f99cade6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
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
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7bbca22dab44a0dcc617f21dbbbae1cac1fd8101626ea4d6b88bf1d5ea113`  
		Last Modified: Mon, 28 Apr 2025 19:08:32 GMT  
		Size: 336.0 MB (336028082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9bed58c917b371be4646ff921757523738a8f6dac8e0c041949b581a240408`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b125810aeec983d02aef479ffe94a4690e39bc3adcfa62cabdb245f1dbee45`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3287b2a9a8cd461d431dac2779e1061fc061bbaeb802f7634cf70d287d1fa68`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc65c103bf51f6fd3ab5d44dc71a76ad7b0004449bbae718432e481a8ad41812`  
		Last Modified: Mon, 28 Apr 2025 19:08:13 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:766372fb49c0d2158ecab3da58da88dda4b0ef524c9743a32914a0dfca52f0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39813085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e88ea20216dc295aaa5cd1a6b9e08b9ed8c8ba7b1948480967e90e05f22b78`

```dockerfile
```

-	Layers:
	-	`sha256:57f46b2d1f4722bfdb469af16cc6fa4412dd6dab7925eae53e06e454f31aa500`  
		Last Modified: Mon, 28 Apr 2025 19:08:14 GMT  
		Size: 39.8 MB (39786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a4a5b4209ff6d565bde02e51afc90e67f4b822b910e59d9ea8f00a124f5e49`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 26.9 KB (26889 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:6ab9e48421a010fd58f9eec8c541932298f04774a4dba5bbd12eb96f4705fad2
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
$ docker pull odoo@sha256:92606fdaac7494c8fa94f3220db09316a42eb4456f3474e6ee52b5b71a328e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 MB (602933104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8f4866a40efdbc0426e9ee41d89735f3df9d81b3c665173228332ee8e8241c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e164585a9b2ab2376b4a61f33cdd04c5f633e88e0245e23f0c477f585bf360`  
		Last Modified: Mon, 28 Apr 2025 18:03:16 GMT  
		Size: 236.1 MB (236083694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e49a8f07ec95c79ecf58c4d0acfda748e36521d93595f5f57ead484d788300e`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 2.5 MB (2520995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdee84202f8ac2580c0dde0e1d46fc86b582725a643f14a078d3155ef3afb71`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85559947abfde093503134d3f5b1364aa74c1de1b1969cddca72a2e05c77f5ef`  
		Last Modified: Mon, 28 Apr 2025 18:03:17 GMT  
		Size: 334.3 MB (334314790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bfa8d80f606bca5a94b96a70db21424401550fa6905806b031da1c487f1968`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dfb5d91879ac991d488e6851a129e63b8ebd07ccbb2664d43a9576e397606f`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f04aa20bc8271f4cc8aa7f6199b3df8c81d306f00f0ad648903cb006e9c05`  
		Last Modified: Mon, 28 Apr 2025 18:03:14 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955b635fc44f92d77a918f27de4a4776ecdf2c58b09e7544b052f69dae926ef`  
		Last Modified: Mon, 28 Apr 2025 18:03:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:98ed5c4c2432f8cbef01fd9868abc70f2f9483050622674b5f8cc146ff409606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5aad374b975fc7757859d6ac0fc49392aa4cc949b69454a7f54147aa12dc1`

```dockerfile
```

-	Layers:
	-	`sha256:37b45e6f56347b458f91987573795cf511ea43729536f1c6ef25a04ba0aa1eba`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 39.8 MB (39777889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336f7a93fa3ad3d3e340570e1cdc5fb9c61d008e2cbc5544725ea7672cb27f6e`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cff529909fb5b1b99f4dc254604310c70ed29e93b46cbedb6e443edd5015965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595408050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa073c673131144ecec83a18ed3832f11fd20bac0ecb2b5f69f5e2316431ba0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0def44f1c28c355fc7e6000d95019736f1de630210f253651882fb9b1e660e`  
		Last Modified: Mon, 28 Apr 2025 19:09:49 GMT  
		Size: 333.9 MB (333904202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c08ecf97203f25375cf2cc05927414d5df2739605519c4c75e25f6995adcf7`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8b25bb6e02553a1d9fa7ed8427c6878e3f7d3244568d94b9cffad81ae3954`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa944b690065e88cb206f58134fb2a727826179efd59169397f3b9fedb616fb0`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771dcc8fe3ac6ce4a80dcc52d3a82b5648866b2f076e7fabdfca83f0b89c582`  
		Last Modified: Mon, 28 Apr 2025 19:09:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b8ef680395885aea5e79265436e6513ebdea8211c0f2068d60724e4558fc7437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39811383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c13d05b1c6ca6a5b80c6cc468732baef75019f761ad2ec91101d53d5733d84`

```dockerfile
```

-	Layers:
	-	`sha256:19aed45cc6c1e91254bba1b8d6f03bd3ed381193d440d8488d9dd1ab551918f8`  
		Last Modified: Mon, 28 Apr 2025 19:09:43 GMT  
		Size: 39.8 MB (39784396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892e76757bf2a250674ac91ab09c22511bb0604c5592ed202ca240571d71d4ab`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0470ad5f2896c499da0300d5dae66fcb7c280c9e2bf645e949b7cb49ad864763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617059115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6940082682289006a3aaf2562bb82bb284f6c53d8d5f73df3bf02be6f99cade6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
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
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7bbca22dab44a0dcc617f21dbbbae1cac1fd8101626ea4d6b88bf1d5ea113`  
		Last Modified: Mon, 28 Apr 2025 19:08:32 GMT  
		Size: 336.0 MB (336028082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9bed58c917b371be4646ff921757523738a8f6dac8e0c041949b581a240408`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b125810aeec983d02aef479ffe94a4690e39bc3adcfa62cabdb245f1dbee45`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3287b2a9a8cd461d431dac2779e1061fc061bbaeb802f7634cf70d287d1fa68`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc65c103bf51f6fd3ab5d44dc71a76ad7b0004449bbae718432e481a8ad41812`  
		Last Modified: Mon, 28 Apr 2025 19:08:13 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:766372fb49c0d2158ecab3da58da88dda4b0ef524c9743a32914a0dfca52f0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39813085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e88ea20216dc295aaa5cd1a6b9e08b9ed8c8ba7b1948480967e90e05f22b78`

```dockerfile
```

-	Layers:
	-	`sha256:57f46b2d1f4722bfdb469af16cc6fa4412dd6dab7925eae53e06e454f31aa500`  
		Last Modified: Mon, 28 Apr 2025 19:08:14 GMT  
		Size: 39.8 MB (39786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a4a5b4209ff6d565bde02e51afc90e67f4b822b910e59d9ea8f00a124f5e49`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 26.9 KB (26889 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250428`

```console
$ docker pull odoo@sha256:6ab9e48421a010fd58f9eec8c541932298f04774a4dba5bbd12eb96f4705fad2
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
$ docker pull odoo@sha256:92606fdaac7494c8fa94f3220db09316a42eb4456f3474e6ee52b5b71a328e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 MB (602933104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8f4866a40efdbc0426e9ee41d89735f3df9d81b3c665173228332ee8e8241c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e164585a9b2ab2376b4a61f33cdd04c5f633e88e0245e23f0c477f585bf360`  
		Last Modified: Mon, 28 Apr 2025 18:03:16 GMT  
		Size: 236.1 MB (236083694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e49a8f07ec95c79ecf58c4d0acfda748e36521d93595f5f57ead484d788300e`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 2.5 MB (2520995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdee84202f8ac2580c0dde0e1d46fc86b582725a643f14a078d3155ef3afb71`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85559947abfde093503134d3f5b1364aa74c1de1b1969cddca72a2e05c77f5ef`  
		Last Modified: Mon, 28 Apr 2025 18:03:17 GMT  
		Size: 334.3 MB (334314790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bfa8d80f606bca5a94b96a70db21424401550fa6905806b031da1c487f1968`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dfb5d91879ac991d488e6851a129e63b8ebd07ccbb2664d43a9576e397606f`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f04aa20bc8271f4cc8aa7f6199b3df8c81d306f00f0ad648903cb006e9c05`  
		Last Modified: Mon, 28 Apr 2025 18:03:14 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955b635fc44f92d77a918f27de4a4776ecdf2c58b09e7544b052f69dae926ef`  
		Last Modified: Mon, 28 Apr 2025 18:03:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:98ed5c4c2432f8cbef01fd9868abc70f2f9483050622674b5f8cc146ff409606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e5aad374b975fc7757859d6ac0fc49392aa4cc949b69454a7f54147aa12dc1`

```dockerfile
```

-	Layers:
	-	`sha256:37b45e6f56347b458f91987573795cf511ea43729536f1c6ef25a04ba0aa1eba`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 39.8 MB (39777889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336f7a93fa3ad3d3e340570e1cdc5fb9c61d008e2cbc5544725ea7672cb27f6e`  
		Last Modified: Mon, 28 Apr 2025 18:03:12 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250428` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cff529909fb5b1b99f4dc254604310c70ed29e93b46cbedb6e443edd5015965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595408050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa073c673131144ecec83a18ed3832f11fd20bac0ecb2b5f69f5e2316431ba0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0def44f1c28c355fc7e6000d95019736f1de630210f253651882fb9b1e660e`  
		Last Modified: Mon, 28 Apr 2025 19:09:49 GMT  
		Size: 333.9 MB (333904202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c08ecf97203f25375cf2cc05927414d5df2739605519c4c75e25f6995adcf7`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8b25bb6e02553a1d9fa7ed8427c6878e3f7d3244568d94b9cffad81ae3954`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa944b690065e88cb206f58134fb2a727826179efd59169397f3b9fedb616fb0`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771dcc8fe3ac6ce4a80dcc52d3a82b5648866b2f076e7fabdfca83f0b89c582`  
		Last Modified: Mon, 28 Apr 2025 19:09:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:b8ef680395885aea5e79265436e6513ebdea8211c0f2068d60724e4558fc7437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39811383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c13d05b1c6ca6a5b80c6cc468732baef75019f761ad2ec91101d53d5733d84`

```dockerfile
```

-	Layers:
	-	`sha256:19aed45cc6c1e91254bba1b8d6f03bd3ed381193d440d8488d9dd1ab551918f8`  
		Last Modified: Mon, 28 Apr 2025 19:09:43 GMT  
		Size: 39.8 MB (39784396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892e76757bf2a250674ac91ab09c22511bb0604c5592ed202ca240571d71d4ab`  
		Last Modified: Mon, 28 Apr 2025 19:09:42 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250428` - linux; ppc64le

```console
$ docker pull odoo@sha256:0470ad5f2896c499da0300d5dae66fcb7c280c9e2bf645e949b7cb49ad864763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617059115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6940082682289006a3aaf2562bb82bb284f6c53d8d5f73df3bf02be6f99cade6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
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
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7bbca22dab44a0dcc617f21dbbbae1cac1fd8101626ea4d6b88bf1d5ea113`  
		Last Modified: Mon, 28 Apr 2025 19:08:32 GMT  
		Size: 336.0 MB (336028082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9bed58c917b371be4646ff921757523738a8f6dac8e0c041949b581a240408`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b125810aeec983d02aef479ffe94a4690e39bc3adcfa62cabdb245f1dbee45`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3287b2a9a8cd461d431dac2779e1061fc061bbaeb802f7634cf70d287d1fa68`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc65c103bf51f6fd3ab5d44dc71a76ad7b0004449bbae718432e481a8ad41812`  
		Last Modified: Mon, 28 Apr 2025 19:08:13 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:766372fb49c0d2158ecab3da58da88dda4b0ef524c9743a32914a0dfca52f0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39813085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e88ea20216dc295aaa5cd1a6b9e08b9ed8c8ba7b1948480967e90e05f22b78`

```dockerfile
```

-	Layers:
	-	`sha256:57f46b2d1f4722bfdb469af16cc6fa4412dd6dab7925eae53e06e454f31aa500`  
		Last Modified: Mon, 28 Apr 2025 19:08:14 GMT  
		Size: 39.8 MB (39786196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a4a5b4209ff6d565bde02e51afc90e67f4b822b910e59d9ea8f00a124f5e49`  
		Last Modified: Mon, 28 Apr 2025 19:08:12 GMT  
		Size: 26.9 KB (26889 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:96d2d731a8e8fdebf98976674855fcd7f5bd280620354a6e3a53b360f2195e10
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
$ docker pull odoo@sha256:2a725c03bdc69b12d46a38c3ad1a9cbc20814f4c2543e7f5fe0aeb79d38b8fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.1 MB (673054655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadffac1d71aa1239d797eecadcab98303f75492e18a5bd106bfb04f9b9e1704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c845233ace243ccd2a4da03b0061ecda5c9256c38bcc48465a6ec4f6ac9171c`  
		Last Modified: Mon, 28 Apr 2025 18:04:00 GMT  
		Size: 254.5 MB (254517502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf098f700e407d2e41787b15a9dd9cae366b5295ca9dcb30244bc8a9b26938f`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 16.7 MB (16680061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c8b45218ed6219b1fa7717e954f9baab36839ed0fc9cd6b5e5a6840f35f77`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79feab1d1ee45f6337d37a65a399d756da20815577043f50cf2dcd16161bf3`  
		Last Modified: Mon, 28 Apr 2025 18:04:04 GMT  
		Size: 371.7 MB (371658431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43114ca933f46ca1000431ed315dafdc93b2dc2ba16fa378608ff1631d8269f8`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1c45fc65af2f3a1384a1a1c97ea11be04908c8b439de2afb6f60018c779af`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c327be661111794ac12900c50b100f0af822e371f5bbb25e6b216044bdc60`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2335d426b21e2e05f33717ba71d09c305e2f027007663ce2cc234ed7bdd1daeb`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:a0a2b5af6662045702f4ea28171191d91787b9c2780db0e25ab69b3ad59d0615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51532af2258230380f1ad47c1803d22c462073bcfdadae53e52db9af36b2e4cd`

```dockerfile
```

-	Layers:
	-	`sha256:8308528b0456f39b3ae6e550340444f3eab7236f07e4ad867341482470624cfa`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb3838ffb75f139752640a86b4db1a3777102381fe4bccfebb65c5fd4cca18f`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:360ff64777f51618667eb028e964cc90db23372d16ec9b8a2c5f84c72569a1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667033860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348af820ad363feb6908707e3e827d3e02f58b357a6a9e0c8606aca149a173a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3f272f7633f9719c3d96500ba992964d1c2a746e81e646b86918bf4b43f0b3`  
		Last Modified: Mon, 28 Apr 2025 19:06:00 GMT  
		Size: 371.5 MB (371515145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ec02c0254e38af78403827ce8552e20ee69e1b0dc0d820a068be5818af48e`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7521f84a6835ed9917766d147b9aaeb6047e4f4523e0035acf69c816f941159`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff73f7a4a1c4ca80e131b7476a707f59ee24df0898759013a3eb726e436524a`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b34f591547b7004a0f7f8f6fede2af03e1ba23139b4ae9ec9b2bb05960871`  
		Last Modified: Mon, 28 Apr 2025 19:05:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:41b1b7b7b351d4aa9c21472ac86bb79a5b0622111ebb9103c6cde6d1e5ea8552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf45a0f495e1b842021b0a4d8e8008ba3da96c4eb9094c2df5c052d486d1c7ef`

```dockerfile
```

-	Layers:
	-	`sha256:cbf826b7195895f1790d5837dadb7bd49534e271e5e2a4e3a3d9cd853f061b7c`  
		Last Modified: Mon, 28 Apr 2025 19:05:55 GMT  
		Size: 59.2 MB (59228768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc55296f1144abe22077b159c18c5e8f84c54daedfa18a08ac005327e1ee0869`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:6bcd29dafc2b79c6b53f65a9027fcd57339fd74d33bdca4ad5b4e00d8b847186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686886395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e5734afacddc2bcb73b56eda535e63a60ca17234d6febd4d4cea09968691b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
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
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a762243c3403cabc393781e6569590668dfac1464fca5da7da22b17593d302d5`  
		Last Modified: Mon, 28 Apr 2025 19:02:16 GMT  
		Size: 372.2 MB (372186072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3f6569319b536b62acaa2c0996a2e5127c1adb8dd13bf239756e3128a1afa6`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f6e49fd857b4426138053a10774322b8754f5f70b7d82222db21951484c91`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e2a1e9880af255b763494202520e51298981dd5cff0df2c0c473633fd0e44`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b811158bcfd5f98c9f7090ab3dbe482eaccc9b4f15fd79040b4a7fa1185e8`  
		Last Modified: Mon, 28 Apr 2025 19:02:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:4df96baa1ac2bda18f81be6069e7dcaeda736896df86f5155e83afa7d19e1a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf652ae1d09b310e6e00961ce8ad4e0598f1f6444b3180090a418ab83955e6`

```dockerfile
```

-	Layers:
	-	`sha256:1ece2c5951215b5133c5441316aed8251a6853a50ffc6e34f8c34bb7dbfca006`  
		Last Modified: Mon, 28 Apr 2025 19:02:05 GMT  
		Size: 59.2 MB (59229624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e1e44e79d7c3d0a6b014d6063de0f40ad8f8239a07a9156972d4d442f47c32`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:96d2d731a8e8fdebf98976674855fcd7f5bd280620354a6e3a53b360f2195e10
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
$ docker pull odoo@sha256:2a725c03bdc69b12d46a38c3ad1a9cbc20814f4c2543e7f5fe0aeb79d38b8fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.1 MB (673054655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadffac1d71aa1239d797eecadcab98303f75492e18a5bd106bfb04f9b9e1704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c845233ace243ccd2a4da03b0061ecda5c9256c38bcc48465a6ec4f6ac9171c`  
		Last Modified: Mon, 28 Apr 2025 18:04:00 GMT  
		Size: 254.5 MB (254517502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf098f700e407d2e41787b15a9dd9cae366b5295ca9dcb30244bc8a9b26938f`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 16.7 MB (16680061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c8b45218ed6219b1fa7717e954f9baab36839ed0fc9cd6b5e5a6840f35f77`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79feab1d1ee45f6337d37a65a399d756da20815577043f50cf2dcd16161bf3`  
		Last Modified: Mon, 28 Apr 2025 18:04:04 GMT  
		Size: 371.7 MB (371658431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43114ca933f46ca1000431ed315dafdc93b2dc2ba16fa378608ff1631d8269f8`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1c45fc65af2f3a1384a1a1c97ea11be04908c8b439de2afb6f60018c779af`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c327be661111794ac12900c50b100f0af822e371f5bbb25e6b216044bdc60`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2335d426b21e2e05f33717ba71d09c305e2f027007663ce2cc234ed7bdd1daeb`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a0a2b5af6662045702f4ea28171191d91787b9c2780db0e25ab69b3ad59d0615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51532af2258230380f1ad47c1803d22c462073bcfdadae53e52db9af36b2e4cd`

```dockerfile
```

-	Layers:
	-	`sha256:8308528b0456f39b3ae6e550340444f3eab7236f07e4ad867341482470624cfa`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb3838ffb75f139752640a86b4db1a3777102381fe4bccfebb65c5fd4cca18f`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:360ff64777f51618667eb028e964cc90db23372d16ec9b8a2c5f84c72569a1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667033860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348af820ad363feb6908707e3e827d3e02f58b357a6a9e0c8606aca149a173a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3f272f7633f9719c3d96500ba992964d1c2a746e81e646b86918bf4b43f0b3`  
		Last Modified: Mon, 28 Apr 2025 19:06:00 GMT  
		Size: 371.5 MB (371515145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ec02c0254e38af78403827ce8552e20ee69e1b0dc0d820a068be5818af48e`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7521f84a6835ed9917766d147b9aaeb6047e4f4523e0035acf69c816f941159`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff73f7a4a1c4ca80e131b7476a707f59ee24df0898759013a3eb726e436524a`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b34f591547b7004a0f7f8f6fede2af03e1ba23139b4ae9ec9b2bb05960871`  
		Last Modified: Mon, 28 Apr 2025 19:05:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:41b1b7b7b351d4aa9c21472ac86bb79a5b0622111ebb9103c6cde6d1e5ea8552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf45a0f495e1b842021b0a4d8e8008ba3da96c4eb9094c2df5c052d486d1c7ef`

```dockerfile
```

-	Layers:
	-	`sha256:cbf826b7195895f1790d5837dadb7bd49534e271e5e2a4e3a3d9cd853f061b7c`  
		Last Modified: Mon, 28 Apr 2025 19:05:55 GMT  
		Size: 59.2 MB (59228768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc55296f1144abe22077b159c18c5e8f84c54daedfa18a08ac005327e1ee0869`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:6bcd29dafc2b79c6b53f65a9027fcd57339fd74d33bdca4ad5b4e00d8b847186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686886395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e5734afacddc2bcb73b56eda535e63a60ca17234d6febd4d4cea09968691b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
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
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a762243c3403cabc393781e6569590668dfac1464fca5da7da22b17593d302d5`  
		Last Modified: Mon, 28 Apr 2025 19:02:16 GMT  
		Size: 372.2 MB (372186072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3f6569319b536b62acaa2c0996a2e5127c1adb8dd13bf239756e3128a1afa6`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f6e49fd857b4426138053a10774322b8754f5f70b7d82222db21951484c91`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e2a1e9880af255b763494202520e51298981dd5cff0df2c0c473633fd0e44`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b811158bcfd5f98c9f7090ab3dbe482eaccc9b4f15fd79040b4a7fa1185e8`  
		Last Modified: Mon, 28 Apr 2025 19:02:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4df96baa1ac2bda18f81be6069e7dcaeda736896df86f5155e83afa7d19e1a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf652ae1d09b310e6e00961ce8ad4e0598f1f6444b3180090a418ab83955e6`

```dockerfile
```

-	Layers:
	-	`sha256:1ece2c5951215b5133c5441316aed8251a6853a50ffc6e34f8c34bb7dbfca006`  
		Last Modified: Mon, 28 Apr 2025 19:02:05 GMT  
		Size: 59.2 MB (59229624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e1e44e79d7c3d0a6b014d6063de0f40ad8f8239a07a9156972d4d442f47c32`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250428`

```console
$ docker pull odoo@sha256:96d2d731a8e8fdebf98976674855fcd7f5bd280620354a6e3a53b360f2195e10
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
$ docker pull odoo@sha256:2a725c03bdc69b12d46a38c3ad1a9cbc20814f4c2543e7f5fe0aeb79d38b8fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.1 MB (673054655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadffac1d71aa1239d797eecadcab98303f75492e18a5bd106bfb04f9b9e1704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c845233ace243ccd2a4da03b0061ecda5c9256c38bcc48465a6ec4f6ac9171c`  
		Last Modified: Mon, 28 Apr 2025 18:04:00 GMT  
		Size: 254.5 MB (254517502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf098f700e407d2e41787b15a9dd9cae366b5295ca9dcb30244bc8a9b26938f`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 16.7 MB (16680061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c8b45218ed6219b1fa7717e954f9baab36839ed0fc9cd6b5e5a6840f35f77`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79feab1d1ee45f6337d37a65a399d756da20815577043f50cf2dcd16161bf3`  
		Last Modified: Mon, 28 Apr 2025 18:04:04 GMT  
		Size: 371.7 MB (371658431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43114ca933f46ca1000431ed315dafdc93b2dc2ba16fa378608ff1631d8269f8`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1c45fc65af2f3a1384a1a1c97ea11be04908c8b439de2afb6f60018c779af`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c327be661111794ac12900c50b100f0af822e371f5bbb25e6b216044bdc60`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2335d426b21e2e05f33717ba71d09c305e2f027007663ce2cc234ed7bdd1daeb`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:a0a2b5af6662045702f4ea28171191d91787b9c2780db0e25ab69b3ad59d0615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51532af2258230380f1ad47c1803d22c462073bcfdadae53e52db9af36b2e4cd`

```dockerfile
```

-	Layers:
	-	`sha256:8308528b0456f39b3ae6e550340444f3eab7236f07e4ad867341482470624cfa`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb3838ffb75f139752640a86b4db1a3777102381fe4bccfebb65c5fd4cca18f`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250428` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:360ff64777f51618667eb028e964cc90db23372d16ec9b8a2c5f84c72569a1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667033860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348af820ad363feb6908707e3e827d3e02f58b357a6a9e0c8606aca149a173a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3f272f7633f9719c3d96500ba992964d1c2a746e81e646b86918bf4b43f0b3`  
		Last Modified: Mon, 28 Apr 2025 19:06:00 GMT  
		Size: 371.5 MB (371515145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ec02c0254e38af78403827ce8552e20ee69e1b0dc0d820a068be5818af48e`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7521f84a6835ed9917766d147b9aaeb6047e4f4523e0035acf69c816f941159`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff73f7a4a1c4ca80e131b7476a707f59ee24df0898759013a3eb726e436524a`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b34f591547b7004a0f7f8f6fede2af03e1ba23139b4ae9ec9b2bb05960871`  
		Last Modified: Mon, 28 Apr 2025 19:05:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:41b1b7b7b351d4aa9c21472ac86bb79a5b0622111ebb9103c6cde6d1e5ea8552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf45a0f495e1b842021b0a4d8e8008ba3da96c4eb9094c2df5c052d486d1c7ef`

```dockerfile
```

-	Layers:
	-	`sha256:cbf826b7195895f1790d5837dadb7bd49534e271e5e2a4e3a3d9cd853f061b7c`  
		Last Modified: Mon, 28 Apr 2025 19:05:55 GMT  
		Size: 59.2 MB (59228768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc55296f1144abe22077b159c18c5e8f84c54daedfa18a08ac005327e1ee0869`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250428` - linux; ppc64le

```console
$ docker pull odoo@sha256:6bcd29dafc2b79c6b53f65a9027fcd57339fd74d33bdca4ad5b4e00d8b847186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686886395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e5734afacddc2bcb73b56eda535e63a60ca17234d6febd4d4cea09968691b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
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
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a762243c3403cabc393781e6569590668dfac1464fca5da7da22b17593d302d5`  
		Last Modified: Mon, 28 Apr 2025 19:02:16 GMT  
		Size: 372.2 MB (372186072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3f6569319b536b62acaa2c0996a2e5127c1adb8dd13bf239756e3128a1afa6`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f6e49fd857b4426138053a10774322b8754f5f70b7d82222db21951484c91`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e2a1e9880af255b763494202520e51298981dd5cff0df2c0c473633fd0e44`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b811158bcfd5f98c9f7090ab3dbe482eaccc9b4f15fd79040b4a7fa1185e8`  
		Last Modified: Mon, 28 Apr 2025 19:02:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250428` - unknown; unknown

```console
$ docker pull odoo@sha256:4df96baa1ac2bda18f81be6069e7dcaeda736896df86f5155e83afa7d19e1a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf652ae1d09b310e6e00961ce8ad4e0598f1f6444b3180090a418ab83955e6`

```dockerfile
```

-	Layers:
	-	`sha256:1ece2c5951215b5133c5441316aed8251a6853a50ffc6e34f8c34bb7dbfca006`  
		Last Modified: Mon, 28 Apr 2025 19:02:05 GMT  
		Size: 59.2 MB (59229624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e1e44e79d7c3d0a6b014d6063de0f40ad8f8239a07a9156972d4d442f47c32`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:96d2d731a8e8fdebf98976674855fcd7f5bd280620354a6e3a53b360f2195e10
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
$ docker pull odoo@sha256:2a725c03bdc69b12d46a38c3ad1a9cbc20814f4c2543e7f5fe0aeb79d38b8fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.1 MB (673054655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadffac1d71aa1239d797eecadcab98303f75492e18a5bd106bfb04f9b9e1704`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c845233ace243ccd2a4da03b0061ecda5c9256c38bcc48465a6ec4f6ac9171c`  
		Last Modified: Mon, 28 Apr 2025 18:04:00 GMT  
		Size: 254.5 MB (254517502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf098f700e407d2e41787b15a9dd9cae366b5295ca9dcb30244bc8a9b26938f`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 16.7 MB (16680061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c8b45218ed6219b1fa7717e954f9baab36839ed0fc9cd6b5e5a6840f35f77`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f79feab1d1ee45f6337d37a65a399d756da20815577043f50cf2dcd16161bf3`  
		Last Modified: Mon, 28 Apr 2025 18:04:04 GMT  
		Size: 371.7 MB (371658431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43114ca933f46ca1000431ed315dafdc93b2dc2ba16fa378608ff1631d8269f8`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1c45fc65af2f3a1384a1a1c97ea11be04908c8b439de2afb6f60018c779af`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c327be661111794ac12900c50b100f0af822e371f5bbb25e6b216044bdc60`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2335d426b21e2e05f33717ba71d09c305e2f027007663ce2cc234ed7bdd1daeb`  
		Last Modified: Mon, 28 Apr 2025 18:03:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a0a2b5af6662045702f4ea28171191d91787b9c2780db0e25ab69b3ad59d0615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51532af2258230380f1ad47c1803d22c462073bcfdadae53e52db9af36b2e4cd`

```dockerfile
```

-	Layers:
	-	`sha256:8308528b0456f39b3ae6e550340444f3eab7236f07e4ad867341482470624cfa`  
		Last Modified: Mon, 28 Apr 2025 18:03:57 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb3838ffb75f139752640a86b4db1a3777102381fe4bccfebb65c5fd4cca18f`  
		Last Modified: Mon, 28 Apr 2025 18:03:56 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:360ff64777f51618667eb028e964cc90db23372d16ec9b8a2c5f84c72569a1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667033860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c348af820ad363feb6908707e3e827d3e02f58b357a6a9e0c8606aca149a173a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3f272f7633f9719c3d96500ba992964d1c2a746e81e646b86918bf4b43f0b3`  
		Last Modified: Mon, 28 Apr 2025 19:06:00 GMT  
		Size: 371.5 MB (371515145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ec02c0254e38af78403827ce8552e20ee69e1b0dc0d820a068be5818af48e`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7521f84a6835ed9917766d147b9aaeb6047e4f4523e0035acf69c816f941159`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff73f7a4a1c4ca80e131b7476a707f59ee24df0898759013a3eb726e436524a`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b34f591547b7004a0f7f8f6fede2af03e1ba23139b4ae9ec9b2bb05960871`  
		Last Modified: Mon, 28 Apr 2025 19:05:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:41b1b7b7b351d4aa9c21472ac86bb79a5b0622111ebb9103c6cde6d1e5ea8552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf45a0f495e1b842021b0a4d8e8008ba3da96c4eb9094c2df5c052d486d1c7ef`

```dockerfile
```

-	Layers:
	-	`sha256:cbf826b7195895f1790d5837dadb7bd49534e271e5e2a4e3a3d9cd853f061b7c`  
		Last Modified: Mon, 28 Apr 2025 19:05:55 GMT  
		Size: 59.2 MB (59228768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc55296f1144abe22077b159c18c5e8f84c54daedfa18a08ac005327e1ee0869`  
		Last Modified: Mon, 28 Apr 2025 19:05:52 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:6bcd29dafc2b79c6b53f65a9027fcd57339fd74d33bdca4ad5b4e00d8b847186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686886395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e5734afacddc2bcb73b56eda535e63a60ca17234d6febd4d4cea09968691b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
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
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a762243c3403cabc393781e6569590668dfac1464fca5da7da22b17593d302d5`  
		Last Modified: Mon, 28 Apr 2025 19:02:16 GMT  
		Size: 372.2 MB (372186072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3f6569319b536b62acaa2c0996a2e5127c1adb8dd13bf239756e3128a1afa6`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f6e49fd857b4426138053a10774322b8754f5f70b7d82222db21951484c91`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156e2a1e9880af255b763494202520e51298981dd5cff0df2c0c473633fd0e44`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b811158bcfd5f98c9f7090ab3dbe482eaccc9b4f15fd79040b4a7fa1185e8`  
		Last Modified: Mon, 28 Apr 2025 19:02:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:4df96baa1ac2bda18f81be6069e7dcaeda736896df86f5155e83afa7d19e1a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf652ae1d09b310e6e00961ce8ad4e0598f1f6444b3180090a418ab83955e6`

```dockerfile
```

-	Layers:
	-	`sha256:1ece2c5951215b5133c5441316aed8251a6853a50ffc6e34f8c34bb7dbfca006`  
		Last Modified: Mon, 28 Apr 2025 19:02:05 GMT  
		Size: 59.2 MB (59229624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e1e44e79d7c3d0a6b014d6063de0f40ad8f8239a07a9156972d4d442f47c32`  
		Last Modified: Mon, 28 Apr 2025 19:02:03 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
