<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250311`](#odoo160-20250311)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250311`](#odoo170-20250311)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250311`](#odoo180-20250311)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:a2162d5dc0294a4929c789a5bfd8ce21a4ec00cfb71bc2191457af7377c9cc99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:2f40e0368758592be64f82b588c7a4f40eb9831983da86e3ce1794aab2ffc929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584491972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4bc69a6a7a8b1e032cd1b386a1c97977a1b75920f41f88765c41e9ae159083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 11 Mar 2025 10:28:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=16.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f750a17a03bcd6c763c06c175820e08791def8ae90fcbda8b4a9ff49aac328f5`  
		Last Modified: Mon, 17 Mar 2025 23:17:27 GMT  
		Size: 219.6 MB (219627451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1720976bdbdb834a2dacdb1c3c127bd0dc319d96d0080e7c312498678880e06`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 2.6 MB (2623303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9551dd8814a2213b15ca3cf53aad92246e80fc1a8ad5697064e6c71c9aa6dd`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 485.7 KB (485720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d352d6dd528786d12caf484cbdfc3993dafe9104348f0881d77e609af0b614c`  
		Last Modified: Mon, 17 Mar 2025 23:17:29 GMT  
		Size: 331.5 MB (331499227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb338a11e52e7d6da9035ad8aed0cbb2900b3b8ee13a934cc242f9c72086fb54`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4784340801db32054d2740c588b18b775115eaa9dd3f561f5b85e870d34903f6`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c8b402ea09ecc195074c114a1cb42c46fef7906f6b7ee1cde9a5897274ef1f`  
		Last Modified: Mon, 17 Mar 2025 23:17:26 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf81d588295b90c347e5bcb55ffab139cc910dac4ee37b0b0850dff2c3c6f6`  
		Last Modified: Mon, 17 Mar 2025 23:17:26 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:8508b4d9034b4d259b6fd9229cf629f7aa6929e80e183d8caa626becc8942984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38883013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9c429d5347a8150aabb96a4833af496e3f7a835ba5ef0bb140c1b242a9ca8`

```dockerfile
```

-	Layers:
	-	`sha256:55adf160eb7987a07dfb47f195dbc7bbb35317dba14f94c5fb4e361f9a2c308d`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 38.9 MB (38856295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e557a2d40f6dd0d73e7c29abf41d61abfce2d07dd09c33ae228433ec6b795b2`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:685efc3019ae19e7593199732ae42fd4d28e2422ed5e45e6e30c1ab776eaf844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579952810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291d699feb1b77c8a767da590c093c9ed3b580b93552760c7b4d00005a202727`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 11 Mar 2025 10:28:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=16.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4fc7951935451dce85fab3c25435cab685b6d590700f2e7721d158c84ed682`  
		Last Modified: Tue, 18 Mar 2025 03:07:08 GMT  
		Size: 216.9 MB (216927028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021ec7becfa2c26bb74b6e9057af23f27ee6fc74858576840d9827c097a95ccd`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 2.6 MB (2631446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebf2df13b124edc2e7ca6b0e5f28b9c75c925dda820af65ec296b076b88815`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 485.7 KB (485689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b2fa22a19e359a7551e81396be996f4e24ccf7626e112d5fc6faadf82981a3`  
		Last Modified: Tue, 18 Mar 2025 03:07:08 GMT  
		Size: 331.2 MB (331160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b88abfd8482cfefc5e71d754ff8eb5c8f240ce7a6ae5be17d857d214ee519`  
		Last Modified: Tue, 18 Mar 2025 03:07:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5634c583f3de8b03183f716c58a337d9cec8b643a576c2e40cafaf9115c2d5f1`  
		Last Modified: Tue, 18 Mar 2025 03:07:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a5b59c1bb9ac72a2cd7c0f9a86a3e2799b3f7f087f37ffb1d397518a684923`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7004c0c11acbe3fb1425e378172295e4593f4b3d46fc2536e6c7adc9407544ce`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:416e5047514a5069e0dda3ea2fc32bd1ff44eda4c2e4947086c9b739065fefa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38889630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f90f096dc036542ece9d3f6cf470e417472a2a4d4853704e88d14f7bb63aa54`

```dockerfile
```

-	Layers:
	-	`sha256:0df6a2e7996256c5c189269ce041809d1f7bed94132cf714064f56360fa672f8`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 38.9 MB (38862761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555788a1d1198c0084c9f6be327a114c2b11386222a9f16005a6b5a7149b1e32`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:a2162d5dc0294a4929c789a5bfd8ce21a4ec00cfb71bc2191457af7377c9cc99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:2f40e0368758592be64f82b588c7a4f40eb9831983da86e3ce1794aab2ffc929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584491972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4bc69a6a7a8b1e032cd1b386a1c97977a1b75920f41f88765c41e9ae159083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 11 Mar 2025 10:28:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=16.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f750a17a03bcd6c763c06c175820e08791def8ae90fcbda8b4a9ff49aac328f5`  
		Last Modified: Mon, 17 Mar 2025 23:17:27 GMT  
		Size: 219.6 MB (219627451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1720976bdbdb834a2dacdb1c3c127bd0dc319d96d0080e7c312498678880e06`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 2.6 MB (2623303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9551dd8814a2213b15ca3cf53aad92246e80fc1a8ad5697064e6c71c9aa6dd`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 485.7 KB (485720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d352d6dd528786d12caf484cbdfc3993dafe9104348f0881d77e609af0b614c`  
		Last Modified: Mon, 17 Mar 2025 23:17:29 GMT  
		Size: 331.5 MB (331499227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb338a11e52e7d6da9035ad8aed0cbb2900b3b8ee13a934cc242f9c72086fb54`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4784340801db32054d2740c588b18b775115eaa9dd3f561f5b85e870d34903f6`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c8b402ea09ecc195074c114a1cb42c46fef7906f6b7ee1cde9a5897274ef1f`  
		Last Modified: Mon, 17 Mar 2025 23:17:26 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf81d588295b90c347e5bcb55ffab139cc910dac4ee37b0b0850dff2c3c6f6`  
		Last Modified: Mon, 17 Mar 2025 23:17:26 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8508b4d9034b4d259b6fd9229cf629f7aa6929e80e183d8caa626becc8942984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38883013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9c429d5347a8150aabb96a4833af496e3f7a835ba5ef0bb140c1b242a9ca8`

```dockerfile
```

-	Layers:
	-	`sha256:55adf160eb7987a07dfb47f195dbc7bbb35317dba14f94c5fb4e361f9a2c308d`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 38.9 MB (38856295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e557a2d40f6dd0d73e7c29abf41d61abfce2d07dd09c33ae228433ec6b795b2`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:685efc3019ae19e7593199732ae42fd4d28e2422ed5e45e6e30c1ab776eaf844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579952810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291d699feb1b77c8a767da590c093c9ed3b580b93552760c7b4d00005a202727`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 11 Mar 2025 10:28:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=16.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4fc7951935451dce85fab3c25435cab685b6d590700f2e7721d158c84ed682`  
		Last Modified: Tue, 18 Mar 2025 03:07:08 GMT  
		Size: 216.9 MB (216927028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021ec7becfa2c26bb74b6e9057af23f27ee6fc74858576840d9827c097a95ccd`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 2.6 MB (2631446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebf2df13b124edc2e7ca6b0e5f28b9c75c925dda820af65ec296b076b88815`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 485.7 KB (485689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b2fa22a19e359a7551e81396be996f4e24ccf7626e112d5fc6faadf82981a3`  
		Last Modified: Tue, 18 Mar 2025 03:07:08 GMT  
		Size: 331.2 MB (331160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b88abfd8482cfefc5e71d754ff8eb5c8f240ce7a6ae5be17d857d214ee519`  
		Last Modified: Tue, 18 Mar 2025 03:07:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5634c583f3de8b03183f716c58a337d9cec8b643a576c2e40cafaf9115c2d5f1`  
		Last Modified: Tue, 18 Mar 2025 03:07:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a5b59c1bb9ac72a2cd7c0f9a86a3e2799b3f7f087f37ffb1d397518a684923`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7004c0c11acbe3fb1425e378172295e4593f4b3d46fc2536e6c7adc9407544ce`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:416e5047514a5069e0dda3ea2fc32bd1ff44eda4c2e4947086c9b739065fefa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38889630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f90f096dc036542ece9d3f6cf470e417472a2a4d4853704e88d14f7bb63aa54`

```dockerfile
```

-	Layers:
	-	`sha256:0df6a2e7996256c5c189269ce041809d1f7bed94132cf714064f56360fa672f8`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 38.9 MB (38862761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555788a1d1198c0084c9f6be327a114c2b11386222a9f16005a6b5a7149b1e32`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250311`

```console
$ docker pull odoo@sha256:a2162d5dc0294a4929c789a5bfd8ce21a4ec00cfb71bc2191457af7377c9cc99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250311` - linux; amd64

```console
$ docker pull odoo@sha256:2f40e0368758592be64f82b588c7a4f40eb9831983da86e3ce1794aab2ffc929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584491972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4bc69a6a7a8b1e032cd1b386a1c97977a1b75920f41f88765c41e9ae159083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 11 Mar 2025 10:28:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=16.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f750a17a03bcd6c763c06c175820e08791def8ae90fcbda8b4a9ff49aac328f5`  
		Last Modified: Mon, 17 Mar 2025 23:17:27 GMT  
		Size: 219.6 MB (219627451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1720976bdbdb834a2dacdb1c3c127bd0dc319d96d0080e7c312498678880e06`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 2.6 MB (2623303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9551dd8814a2213b15ca3cf53aad92246e80fc1a8ad5697064e6c71c9aa6dd`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 485.7 KB (485720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d352d6dd528786d12caf484cbdfc3993dafe9104348f0881d77e609af0b614c`  
		Last Modified: Mon, 17 Mar 2025 23:17:29 GMT  
		Size: 331.5 MB (331499227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb338a11e52e7d6da9035ad8aed0cbb2900b3b8ee13a934cc242f9c72086fb54`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4784340801db32054d2740c588b18b775115eaa9dd3f561f5b85e870d34903f6`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c8b402ea09ecc195074c114a1cb42c46fef7906f6b7ee1cde9a5897274ef1f`  
		Last Modified: Mon, 17 Mar 2025 23:17:26 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf81d588295b90c347e5bcb55ffab139cc910dac4ee37b0b0850dff2c3c6f6`  
		Last Modified: Mon, 17 Mar 2025 23:17:26 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:8508b4d9034b4d259b6fd9229cf629f7aa6929e80e183d8caa626becc8942984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38883013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9c429d5347a8150aabb96a4833af496e3f7a835ba5ef0bb140c1b242a9ca8`

```dockerfile
```

-	Layers:
	-	`sha256:55adf160eb7987a07dfb47f195dbc7bbb35317dba14f94c5fb4e361f9a2c308d`  
		Last Modified: Mon, 17 Mar 2025 23:17:25 GMT  
		Size: 38.9 MB (38856295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e557a2d40f6dd0d73e7c29abf41d61abfce2d07dd09c33ae228433ec6b795b2`  
		Last Modified: Mon, 17 Mar 2025 23:17:24 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250311` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:685efc3019ae19e7593199732ae42fd4d28e2422ed5e45e6e30c1ab776eaf844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579952810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291d699feb1b77c8a767da590c093c9ed3b580b93552760c7b4d00005a202727`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 11 Mar 2025 10:28:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=16.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=438bd032c85e128dacb6c17e8bfcd694edf4305b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4fc7951935451dce85fab3c25435cab685b6d590700f2e7721d158c84ed682`  
		Last Modified: Tue, 18 Mar 2025 03:07:08 GMT  
		Size: 216.9 MB (216927028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021ec7becfa2c26bb74b6e9057af23f27ee6fc74858576840d9827c097a95ccd`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 2.6 MB (2631446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cebf2df13b124edc2e7ca6b0e5f28b9c75c925dda820af65ec296b076b88815`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 485.7 KB (485689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b2fa22a19e359a7551e81396be996f4e24ccf7626e112d5fc6faadf82981a3`  
		Last Modified: Tue, 18 Mar 2025 03:07:08 GMT  
		Size: 331.2 MB (331160293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b88abfd8482cfefc5e71d754ff8eb5c8f240ce7a6ae5be17d857d214ee519`  
		Last Modified: Tue, 18 Mar 2025 03:07:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5634c583f3de8b03183f716c58a337d9cec8b643a576c2e40cafaf9115c2d5f1`  
		Last Modified: Tue, 18 Mar 2025 03:07:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a5b59c1bb9ac72a2cd7c0f9a86a3e2799b3f7f087f37ffb1d397518a684923`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7004c0c11acbe3fb1425e378172295e4593f4b3d46fc2536e6c7adc9407544ce`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:416e5047514a5069e0dda3ea2fc32bd1ff44eda4c2e4947086c9b739065fefa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38889630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f90f096dc036542ece9d3f6cf470e417472a2a4d4853704e88d14f7bb63aa54`

```dockerfile
```

-	Layers:
	-	`sha256:0df6a2e7996256c5c189269ce041809d1f7bed94132cf714064f56360fa672f8`  
		Last Modified: Tue, 18 Mar 2025 03:07:03 GMT  
		Size: 38.9 MB (38862761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555788a1d1198c0084c9f6be327a114c2b11386222a9f16005a6b5a7149b1e32`  
		Last Modified: Tue, 18 Mar 2025 03:07:01 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:ef58a43314dc76fefd6e6a5ddd66811d558b599247e9d921581a244702d746e7
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
$ docker pull odoo@sha256:aea1919f91160a911c8c10d1d469008867c6055bf4981fbf9c049d374ac9c4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602453545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95921e550b13d1a185618f9976f20e675c3e854551f6be84c430b6657b7b0c62`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7248b809b8d2107c984e769c3f8f07034c95e8a987a43e07116d8ac7c113839`  
		Last Modified: Tue, 11 Mar 2025 16:56:11 GMT  
		Size: 236.1 MB (236053394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5849ab55d708a39a159f2b56791716f7010f01e9e4a42625dc1c5ced14008`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 2.5 MB (2520314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b1964bb08955cb8892c0da5b7ffe3bdc050fa31e4caa96986f8e200fa96741`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 485.6 KB (485575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e398d9777372fb489ad3230437b7c61cea295c705ad46cdff197391c130f9`  
		Last Modified: Tue, 11 Mar 2025 16:56:12 GMT  
		Size: 333.9 MB (333855882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4043f0504ec3e2549454048e7ac576f5fcb6ed2d2c6bdbf92a8aecd2fc32aded`  
		Last Modified: Tue, 11 Mar 2025 16:55:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75b24a44894e38784b70447ec02e141ea981f8a686450e7537e5edca9ed4d41`  
		Last Modified: Tue, 11 Mar 2025 16:56:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99219559e7973a850a88e0fbc6fc34df13999ce906bbbef4d77618f70adcbd0b`  
		Last Modified: Tue, 11 Mar 2025 16:56:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff01b6c2a7c5474c36b4ef2b31897d92619bbdbe48773a7770b85775a2ea907`  
		Last Modified: Tue, 11 Mar 2025 16:56:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:8c8726a0cd2cc4298c699561d08193951b788b5ce14acfe5c258a2871cadff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39763297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4eeeef9b7b258d1eab39c6d3df143d2750de15f3e6cb73dcbdbfa79efd386d`

```dockerfile
```

-	Layers:
	-	`sha256:5e01ed543a77fa167c00a2e3c41c35d87a470cbbd29135ee3815ced5d5cd73b7`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 39.7 MB (39736462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d6804ae3ebd5bb13e3f28f7ed573ad4ad52e59ba4f5d63a10e53a3ddf97a83`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:73fc135277a69425b849c188cebd39a4b81936cdb44c652734193b9fc2c2c50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597080615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d97e0620a9f952d70dbccf8fd690c6610a58df7f4148fd78266a81b4066ba8`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31427e7e51e8fb08bf6f31ee36ce695fc2fafcdeff3133e3cd7110bf15d20a94`  
		Last Modified: Tue, 11 Mar 2025 17:38:57 GMT  
		Size: 233.3 MB (233253610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22a944ea0aa134f62776fee5c20190e3ffdaf62deaa37775965c4806575080f`  
		Last Modified: Tue, 11 Mar 2025 17:38:52 GMT  
		Size: 2.5 MB (2511614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87594f2370b29912ea1473bebcf00a87b214c3a8601097ce48012c7d58e0d93f`  
		Last Modified: Tue, 11 Mar 2025 17:38:52 GMT  
		Size: 485.6 KB (485589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df707089420afebad98f175f92acb0ffee50d6ba12322c5e18abc6d479628fce`  
		Last Modified: Tue, 11 Mar 2025 17:38:59 GMT  
		Size: 333.5 MB (333469180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07bc370da5ea377521698f04dc4d992035bac2d9ccbcf30d623d6305b339e29`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def40b76c400dd71c573a9a037e905a06c45f69a7da621db4038c6a524ff4200`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349cf4c5c4c4ce860f96bde92f76bfe9667e5965d4c1e75bbec1fe78a0a13cae`  
		Last Modified: Tue, 11 Mar 2025 17:38:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0976210955065707fa50041ac699305f91513d38f77d1365f874470be8500c0`  
		Last Modified: Tue, 11 Mar 2025 17:38:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:cccd9c860a39bc365f28ab24717c00bd59fc4ab85eadf30d42f972bc389cd9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39769956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f83b35b4afdcb4a657225c65ab9790509324e4e24bd49cb6325e5e1fad8b56`

```dockerfile
```

-	Layers:
	-	`sha256:56dbc163e52c7fe109f5722c6dd748cb847d51ab26d1af90d74486803bb15fa6`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 39.7 MB (39742969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba8e430ecdd2e66245c4e33a281bbd7f3923a584388e57ac6c616052915fa48c`  
		Last Modified: Tue, 11 Mar 2025 17:38:51 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:a2ae0bc8a3be6b1721cbde6e7092c22b4a7bd8ae2bc58b875e5eeeb6c5db7908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.3 MB (619280375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445740d7c6c3c93c1cf21a647fc3ed767a4f7ef80d49fc35ec42824509988017`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66264d2eb85271e47521d66848d5698b3814b0cb6b4bc5b56eec9e6d735c9e1`  
		Last Modified: Tue, 11 Mar 2025 17:58:54 GMT  
		Size: 245.9 MB (245909402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580dd786898c8352cb11f59f6ff36b8c1006245739e0dba4e78abce9163b40b`  
		Last Modified: Tue, 11 Mar 2025 17:58:47 GMT  
		Size: 2.8 MB (2838191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d89c6c22bdb33edaf2023b08f0feb6a93ee9e2d56ee525a24b1e9e86529229`  
		Last Modified: Tue, 11 Mar 2025 17:58:47 GMT  
		Size: 485.6 KB (485605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987ab9b8ba5045bb711ec16f9d13bb189c3610f55e036cdd2e9ae6da01f1c6c8`  
		Last Modified: Tue, 11 Mar 2025 17:59:10 GMT  
		Size: 335.6 MB (335596801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b95fc13561a50033bdc25345a3d6ec1e007297fb1d5d559b1f5fb1cc5bf811`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24bd896f66d403937400d8e618fc5126f384b2d993696f03d4fb2a9dd96774`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce21ec5ff6ffaeb3196cb00133eb693936321e290deb02204429092abe30223`  
		Last Modified: Tue, 11 Mar 2025 17:58:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406c997661cc1acec5248dd43ccae12fdf0ad61258eabc94e9f0bb027b40829b`  
		Last Modified: Tue, 11 Mar 2025 17:58:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:10220317567f1fd351a0516b99599b576d198bd510c9f10a7b6917d6a64052cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39771660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32fe939dcaddf935abefa2439d567f1a32a41add97085dbe7667e3c9cc182b`

```dockerfile
```

-	Layers:
	-	`sha256:54fd4fbb04d3b2490f5b996df1ba1fcb53fb2fb01d81c64e2a5bfc66aa96f823`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 39.7 MB (39744769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d6e46b85e3123aff44400827fe746f9746c400b721bd1b88c7defd5f042af7`  
		Last Modified: Tue, 11 Mar 2025 17:58:46 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:ef58a43314dc76fefd6e6a5ddd66811d558b599247e9d921581a244702d746e7
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
$ docker pull odoo@sha256:aea1919f91160a911c8c10d1d469008867c6055bf4981fbf9c049d374ac9c4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602453545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95921e550b13d1a185618f9976f20e675c3e854551f6be84c430b6657b7b0c62`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7248b809b8d2107c984e769c3f8f07034c95e8a987a43e07116d8ac7c113839`  
		Last Modified: Tue, 11 Mar 2025 16:56:11 GMT  
		Size: 236.1 MB (236053394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5849ab55d708a39a159f2b56791716f7010f01e9e4a42625dc1c5ced14008`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 2.5 MB (2520314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b1964bb08955cb8892c0da5b7ffe3bdc050fa31e4caa96986f8e200fa96741`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 485.6 KB (485575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e398d9777372fb489ad3230437b7c61cea295c705ad46cdff197391c130f9`  
		Last Modified: Tue, 11 Mar 2025 16:56:12 GMT  
		Size: 333.9 MB (333855882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4043f0504ec3e2549454048e7ac576f5fcb6ed2d2c6bdbf92a8aecd2fc32aded`  
		Last Modified: Tue, 11 Mar 2025 16:55:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75b24a44894e38784b70447ec02e141ea981f8a686450e7537e5edca9ed4d41`  
		Last Modified: Tue, 11 Mar 2025 16:56:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99219559e7973a850a88e0fbc6fc34df13999ce906bbbef4d77618f70adcbd0b`  
		Last Modified: Tue, 11 Mar 2025 16:56:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff01b6c2a7c5474c36b4ef2b31897d92619bbdbe48773a7770b85775a2ea907`  
		Last Modified: Tue, 11 Mar 2025 16:56:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8c8726a0cd2cc4298c699561d08193951b788b5ce14acfe5c258a2871cadff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39763297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4eeeef9b7b258d1eab39c6d3df143d2750de15f3e6cb73dcbdbfa79efd386d`

```dockerfile
```

-	Layers:
	-	`sha256:5e01ed543a77fa167c00a2e3c41c35d87a470cbbd29135ee3815ced5d5cd73b7`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 39.7 MB (39736462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d6804ae3ebd5bb13e3f28f7ed573ad4ad52e59ba4f5d63a10e53a3ddf97a83`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:73fc135277a69425b849c188cebd39a4b81936cdb44c652734193b9fc2c2c50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597080615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d97e0620a9f952d70dbccf8fd690c6610a58df7f4148fd78266a81b4066ba8`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31427e7e51e8fb08bf6f31ee36ce695fc2fafcdeff3133e3cd7110bf15d20a94`  
		Last Modified: Tue, 11 Mar 2025 17:38:57 GMT  
		Size: 233.3 MB (233253610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22a944ea0aa134f62776fee5c20190e3ffdaf62deaa37775965c4806575080f`  
		Last Modified: Tue, 11 Mar 2025 17:38:52 GMT  
		Size: 2.5 MB (2511614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87594f2370b29912ea1473bebcf00a87b214c3a8601097ce48012c7d58e0d93f`  
		Last Modified: Tue, 11 Mar 2025 17:38:52 GMT  
		Size: 485.6 KB (485589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df707089420afebad98f175f92acb0ffee50d6ba12322c5e18abc6d479628fce`  
		Last Modified: Tue, 11 Mar 2025 17:38:59 GMT  
		Size: 333.5 MB (333469180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07bc370da5ea377521698f04dc4d992035bac2d9ccbcf30d623d6305b339e29`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def40b76c400dd71c573a9a037e905a06c45f69a7da621db4038c6a524ff4200`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349cf4c5c4c4ce860f96bde92f76bfe9667e5965d4c1e75bbec1fe78a0a13cae`  
		Last Modified: Tue, 11 Mar 2025 17:38:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0976210955065707fa50041ac699305f91513d38f77d1365f874470be8500c0`  
		Last Modified: Tue, 11 Mar 2025 17:38:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cccd9c860a39bc365f28ab24717c00bd59fc4ab85eadf30d42f972bc389cd9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39769956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f83b35b4afdcb4a657225c65ab9790509324e4e24bd49cb6325e5e1fad8b56`

```dockerfile
```

-	Layers:
	-	`sha256:56dbc163e52c7fe109f5722c6dd748cb847d51ab26d1af90d74486803bb15fa6`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 39.7 MB (39742969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba8e430ecdd2e66245c4e33a281bbd7f3923a584388e57ac6c616052915fa48c`  
		Last Modified: Tue, 11 Mar 2025 17:38:51 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a2ae0bc8a3be6b1721cbde6e7092c22b4a7bd8ae2bc58b875e5eeeb6c5db7908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.3 MB (619280375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445740d7c6c3c93c1cf21a647fc3ed767a4f7ef80d49fc35ec42824509988017`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66264d2eb85271e47521d66848d5698b3814b0cb6b4bc5b56eec9e6d735c9e1`  
		Last Modified: Tue, 11 Mar 2025 17:58:54 GMT  
		Size: 245.9 MB (245909402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580dd786898c8352cb11f59f6ff36b8c1006245739e0dba4e78abce9163b40b`  
		Last Modified: Tue, 11 Mar 2025 17:58:47 GMT  
		Size: 2.8 MB (2838191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d89c6c22bdb33edaf2023b08f0feb6a93ee9e2d56ee525a24b1e9e86529229`  
		Last Modified: Tue, 11 Mar 2025 17:58:47 GMT  
		Size: 485.6 KB (485605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987ab9b8ba5045bb711ec16f9d13bb189c3610f55e036cdd2e9ae6da01f1c6c8`  
		Last Modified: Tue, 11 Mar 2025 17:59:10 GMT  
		Size: 335.6 MB (335596801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b95fc13561a50033bdc25345a3d6ec1e007297fb1d5d559b1f5fb1cc5bf811`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24bd896f66d403937400d8e618fc5126f384b2d993696f03d4fb2a9dd96774`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce21ec5ff6ffaeb3196cb00133eb693936321e290deb02204429092abe30223`  
		Last Modified: Tue, 11 Mar 2025 17:58:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406c997661cc1acec5248dd43ccae12fdf0ad61258eabc94e9f0bb027b40829b`  
		Last Modified: Tue, 11 Mar 2025 17:58:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:10220317567f1fd351a0516b99599b576d198bd510c9f10a7b6917d6a64052cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39771660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32fe939dcaddf935abefa2439d567f1a32a41add97085dbe7667e3c9cc182b`

```dockerfile
```

-	Layers:
	-	`sha256:54fd4fbb04d3b2490f5b996df1ba1fcb53fb2fb01d81c64e2a5bfc66aa96f823`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 39.7 MB (39744769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d6e46b85e3123aff44400827fe746f9746c400b721bd1b88c7defd5f042af7`  
		Last Modified: Tue, 11 Mar 2025 17:58:46 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250311`

```console
$ docker pull odoo@sha256:ef58a43314dc76fefd6e6a5ddd66811d558b599247e9d921581a244702d746e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250311` - linux; amd64

```console
$ docker pull odoo@sha256:aea1919f91160a911c8c10d1d469008867c6055bf4981fbf9c049d374ac9c4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 MB (602453545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95921e550b13d1a185618f9976f20e675c3e854551f6be84c430b6657b7b0c62`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7248b809b8d2107c984e769c3f8f07034c95e8a987a43e07116d8ac7c113839`  
		Last Modified: Tue, 11 Mar 2025 16:56:11 GMT  
		Size: 236.1 MB (236053394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5849ab55d708a39a159f2b56791716f7010f01e9e4a42625dc1c5ced14008`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 2.5 MB (2520314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b1964bb08955cb8892c0da5b7ffe3bdc050fa31e4caa96986f8e200fa96741`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 485.6 KB (485575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8e398d9777372fb489ad3230437b7c61cea295c705ad46cdff197391c130f9`  
		Last Modified: Tue, 11 Mar 2025 16:56:12 GMT  
		Size: 333.9 MB (333855882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4043f0504ec3e2549454048e7ac576f5fcb6ed2d2c6bdbf92a8aecd2fc32aded`  
		Last Modified: Tue, 11 Mar 2025 16:55:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75b24a44894e38784b70447ec02e141ea981f8a686450e7537e5edca9ed4d41`  
		Last Modified: Tue, 11 Mar 2025 16:56:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99219559e7973a850a88e0fbc6fc34df13999ce906bbbef4d77618f70adcbd0b`  
		Last Modified: Tue, 11 Mar 2025 16:56:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff01b6c2a7c5474c36b4ef2b31897d92619bbdbe48773a7770b85775a2ea907`  
		Last Modified: Tue, 11 Mar 2025 16:56:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:8c8726a0cd2cc4298c699561d08193951b788b5ce14acfe5c258a2871cadff62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39763297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4eeeef9b7b258d1eab39c6d3df143d2750de15f3e6cb73dcbdbfa79efd386d`

```dockerfile
```

-	Layers:
	-	`sha256:5e01ed543a77fa167c00a2e3c41c35d87a470cbbd29135ee3815ced5d5cd73b7`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 39.7 MB (39736462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d6804ae3ebd5bb13e3f28f7ed573ad4ad52e59ba4f5d63a10e53a3ddf97a83`  
		Last Modified: Tue, 11 Mar 2025 16:56:07 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250311` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:73fc135277a69425b849c188cebd39a4b81936cdb44c652734193b9fc2c2c50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597080615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d97e0620a9f952d70dbccf8fd690c6610a58df7f4148fd78266a81b4066ba8`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31427e7e51e8fb08bf6f31ee36ce695fc2fafcdeff3133e3cd7110bf15d20a94`  
		Last Modified: Tue, 11 Mar 2025 17:38:57 GMT  
		Size: 233.3 MB (233253610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22a944ea0aa134f62776fee5c20190e3ffdaf62deaa37775965c4806575080f`  
		Last Modified: Tue, 11 Mar 2025 17:38:52 GMT  
		Size: 2.5 MB (2511614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87594f2370b29912ea1473bebcf00a87b214c3a8601097ce48012c7d58e0d93f`  
		Last Modified: Tue, 11 Mar 2025 17:38:52 GMT  
		Size: 485.6 KB (485589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df707089420afebad98f175f92acb0ffee50d6ba12322c5e18abc6d479628fce`  
		Last Modified: Tue, 11 Mar 2025 17:38:59 GMT  
		Size: 333.5 MB (333469180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07bc370da5ea377521698f04dc4d992035bac2d9ccbcf30d623d6305b339e29`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def40b76c400dd71c573a9a037e905a06c45f69a7da621db4038c6a524ff4200`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349cf4c5c4c4ce860f96bde92f76bfe9667e5965d4c1e75bbec1fe78a0a13cae`  
		Last Modified: Tue, 11 Mar 2025 17:38:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0976210955065707fa50041ac699305f91513d38f77d1365f874470be8500c0`  
		Last Modified: Tue, 11 Mar 2025 17:38:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:cccd9c860a39bc365f28ab24717c00bd59fc4ab85eadf30d42f972bc389cd9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39769956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f83b35b4afdcb4a657225c65ab9790509324e4e24bd49cb6325e5e1fad8b56`

```dockerfile
```

-	Layers:
	-	`sha256:56dbc163e52c7fe109f5722c6dd748cb847d51ab26d1af90d74486803bb15fa6`  
		Last Modified: Tue, 11 Mar 2025 17:38:53 GMT  
		Size: 39.7 MB (39742969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba8e430ecdd2e66245c4e33a281bbd7f3923a584388e57ac6c616052915fa48c`  
		Last Modified: Tue, 11 Mar 2025 17:38:51 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250311` - linux; ppc64le

```console
$ docker pull odoo@sha256:a2ae0bc8a3be6b1721cbde6e7092c22b4a7bd8ae2bc58b875e5eeeb6c5db7908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.3 MB (619280375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445740d7c6c3c93c1cf21a647fc3ed767a4f7ef80d49fc35ec42824509988017`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=13db9f16b7047720ecb803ad8312500fb4e044d1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66264d2eb85271e47521d66848d5698b3814b0cb6b4bc5b56eec9e6d735c9e1`  
		Last Modified: Tue, 11 Mar 2025 17:58:54 GMT  
		Size: 245.9 MB (245909402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580dd786898c8352cb11f59f6ff36b8c1006245739e0dba4e78abce9163b40b`  
		Last Modified: Tue, 11 Mar 2025 17:58:47 GMT  
		Size: 2.8 MB (2838191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d89c6c22bdb33edaf2023b08f0feb6a93ee9e2d56ee525a24b1e9e86529229`  
		Last Modified: Tue, 11 Mar 2025 17:58:47 GMT  
		Size: 485.6 KB (485605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987ab9b8ba5045bb711ec16f9d13bb189c3610f55e036cdd2e9ae6da01f1c6c8`  
		Last Modified: Tue, 11 Mar 2025 17:59:10 GMT  
		Size: 335.6 MB (335596801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b95fc13561a50033bdc25345a3d6ec1e007297fb1d5d559b1f5fb1cc5bf811`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24bd896f66d403937400d8e618fc5126f384b2d993696f03d4fb2a9dd96774`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce21ec5ff6ffaeb3196cb00133eb693936321e290deb02204429092abe30223`  
		Last Modified: Tue, 11 Mar 2025 17:58:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406c997661cc1acec5248dd43ccae12fdf0ad61258eabc94e9f0bb027b40829b`  
		Last Modified: Tue, 11 Mar 2025 17:58:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:10220317567f1fd351a0516b99599b576d198bd510c9f10a7b6917d6a64052cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39771660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32fe939dcaddf935abefa2439d567f1a32a41add97085dbe7667e3c9cc182b`

```dockerfile
```

-	Layers:
	-	`sha256:54fd4fbb04d3b2490f5b996df1ba1fcb53fb2fb01d81c64e2a5bfc66aa96f823`  
		Last Modified: Tue, 11 Mar 2025 17:58:48 GMT  
		Size: 39.7 MB (39744769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d6e46b85e3123aff44400827fe746f9746c400b721bd1b88c7defd5f042af7`  
		Last Modified: Tue, 11 Mar 2025 17:58:46 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:fb9654cbc22426c03962992935ca64709f38aab9f55e5b68b55eecdeedb92e60
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
$ docker pull odoo@sha256:93d835dbdfcb57be5e0fc503515dc39594a4fbdbc63b6b3065e56ea73b0617d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.3 MB (674288189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e79d2a867f20bc41f5170371a99a68a04c888dae266316051731b79b5d32293`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa53ec96f4da5767e7f2732e777a6b541f24b30816eb3daae8f72f61508becf`  
		Last Modified: Tue, 11 Mar 2025 16:56:44 GMT  
		Size: 256.9 MB (256919349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc4b2c3ef890d9b27b3c51957c89f0ca41fbc84c2c07e74dce5eaa6a2c6bcd`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 16.7 MB (16679861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2062aa9c592dfc54d31163a7f2cf3d1e67062ace2ef3bd7d07891f65edec8382`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 485.3 KB (485325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9eb5fba9b19c935f82f236d5d10a16ab1068d4cc6ac3fb6d303f0481afb19c`  
		Last Modified: Tue, 11 Mar 2025 16:56:45 GMT  
		Size: 370.4 MB (370446928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b01ef1cdff5381e84846e3d2b61b36e44199d9180c2ffef85f595222a27d6`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836ebe08b2b620d8a3e5f6e5d70b2f37d75a31d80b6ff6f76b1ff2704e3c3de`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2b55455891b4057bd3052ea7805ea764720f264a07bd0a25551def551485a`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc9e50d3dd991661885a87d849a73f78794778d010f68f57bce79475dd527d7`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:4585fe0f6581ea788de1e491ea062be15d7438a64f9dfa01ae1ba4445bc7f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59133598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320e80c6435f7a8e42af862005c5aaf8aec6e90872f340eebb6ee1e9c7209afb`

```dockerfile
```

-	Layers:
	-	`sha256:7d87349f4b6e749b6aeb0ca15bb8e917f3187d56f92eff5a685c730daac8a104`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 59.1 MB (59106462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09f264b41f172aa7282cf94928b08a06e963ecc4e0bc5680c7525f70720f0`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:703db0b0bfe5ec80d1fe73a07085238a73e14f8c668ece5522d7b7c0a380241b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.5 MB (670462982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72acc61f0a897a43b100238a878c3e0f405e6053ff5b142b33ca7dfb0bfb24fd`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8e3368073cac4ffce1aeb0f492f74f029d2dc11e27c4ea779a66092466c925`  
		Last Modified: Tue, 11 Mar 2025 17:31:22 GMT  
		Size: 254.2 MB (254156539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3e4fd0793639bdd2743e71d6d281d4ac88971eec8ec5bb77b4f41a6884ad0`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 16.6 MB (16621804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a880ba7a884a7c64c8ae0a8cf4881f654d66150b91b02e91302fa654590ad6`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65790d9c2d3e95e74caa3722659e11eb385c1844fb4bffaddf4ce7bb0580178c`  
		Last Modified: Tue, 11 Mar 2025 17:31:25 GMT  
		Size: 370.3 MB (370303218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123532ca63d760bdaa568ecfbae07b06fa91dd26ec04c8b74eadedb805c0df0e`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fcb72d07fcff6ff878c9377873c599d28d8c80887406bd9453a88e14fc25d`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d346bd36869cc104da4ea397136c0090afc9188e30ef7c158c3f9504a10767d7`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8efc6c47e1390df072ec148e68f3659322f38fa3113fd36bd17276d39247db7`  
		Last Modified: Tue, 11 Mar 2025 17:31:20 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:63e15553f2dc4e78962201abd46e60f4cc22f6f0412645afade1d876f4272dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aede8b992e8d12ca16c7e28ce76b0de19a01a53a4c365f264872f72bd49602d6`

```dockerfile
```

-	Layers:
	-	`sha256:ec5fe4e79e0988221a045f451cb9f81c5dd6ede023c8770012001fa799f814de`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 59.1 MB (59113749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af74e1bdee0c2621e1b2b84c74d28c7a4c5b4bfa074a92c64174794c171a085`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:b28f72233c8ee5beb2583ac39c0e43b920df7bb03f178fb474b7fccca4383c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.9 MB (690926860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3e71e4dcdd1604ff320d7adec9f669907825bdabe163c2799b7e8fb16bde12`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16da6ef8fe07413cb95a3f576ed678f25863b030b28a5d45fbd9a59572184d61`  
		Last Modified: Tue, 11 Mar 2025 17:48:53 GMT  
		Size: 267.7 MB (267711163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6814aea401b619cfd0771c727c791ecc19b4d001e7486726f263957a44756f3`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 17.4 MB (17357228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8d4b899454650f6de2831ab2bd0b10936112e93afae366946f4c6a72adc2e`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 485.4 KB (485352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81af7dfe460a6b632831e3eae620dec1bd465841ad2c944c8d9bea3d5a59e9b8`  
		Last Modified: Tue, 11 Mar 2025 17:48:56 GMT  
		Size: 371.0 MB (370980851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7481f285d953f8ec53da7603f1f41e9ac769831acdbfeb7770b29d2e005ece`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134eafd19dd0a859c77b243c67125d4f98ed6ca742e71297f70fa171f9bec41`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf41f71e1ab5221b0d71874f6c14e540c3ce84b4b86657094c02dd17dafc7f`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a09d8707fa1039279ba6f860645fa686c9d8ae72fe42c2a43fec8ac9e93b71`  
		Last Modified: Tue, 11 Mar 2025 17:48:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:a3bd0566b7a48ca445b6e0ecfac8e4068604b31d979141936efb8ff4de2b2624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff64242afb6c2b8f9d9f319ae92e9c7beaa90317a40499f65dfb0240065ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:d0ec0d5c7758b859aabce4a006ce3313ade23bff7c7f00b6da94a7b03cecd581`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 59.1 MB (59114605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8f5ef1504d03b150428249a7e2b98ef5ae213ad20f74f3bef3c3e34068a681`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:fb9654cbc22426c03962992935ca64709f38aab9f55e5b68b55eecdeedb92e60
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
$ docker pull odoo@sha256:93d835dbdfcb57be5e0fc503515dc39594a4fbdbc63b6b3065e56ea73b0617d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.3 MB (674288189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e79d2a867f20bc41f5170371a99a68a04c888dae266316051731b79b5d32293`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa53ec96f4da5767e7f2732e777a6b541f24b30816eb3daae8f72f61508becf`  
		Last Modified: Tue, 11 Mar 2025 16:56:44 GMT  
		Size: 256.9 MB (256919349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc4b2c3ef890d9b27b3c51957c89f0ca41fbc84c2c07e74dce5eaa6a2c6bcd`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 16.7 MB (16679861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2062aa9c592dfc54d31163a7f2cf3d1e67062ace2ef3bd7d07891f65edec8382`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 485.3 KB (485325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9eb5fba9b19c935f82f236d5d10a16ab1068d4cc6ac3fb6d303f0481afb19c`  
		Last Modified: Tue, 11 Mar 2025 16:56:45 GMT  
		Size: 370.4 MB (370446928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b01ef1cdff5381e84846e3d2b61b36e44199d9180c2ffef85f595222a27d6`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836ebe08b2b620d8a3e5f6e5d70b2f37d75a31d80b6ff6f76b1ff2704e3c3de`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2b55455891b4057bd3052ea7805ea764720f264a07bd0a25551def551485a`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc9e50d3dd991661885a87d849a73f78794778d010f68f57bce79475dd527d7`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4585fe0f6581ea788de1e491ea062be15d7438a64f9dfa01ae1ba4445bc7f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59133598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320e80c6435f7a8e42af862005c5aaf8aec6e90872f340eebb6ee1e9c7209afb`

```dockerfile
```

-	Layers:
	-	`sha256:7d87349f4b6e749b6aeb0ca15bb8e917f3187d56f92eff5a685c730daac8a104`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 59.1 MB (59106462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09f264b41f172aa7282cf94928b08a06e963ecc4e0bc5680c7525f70720f0`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:703db0b0bfe5ec80d1fe73a07085238a73e14f8c668ece5522d7b7c0a380241b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.5 MB (670462982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72acc61f0a897a43b100238a878c3e0f405e6053ff5b142b33ca7dfb0bfb24fd`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8e3368073cac4ffce1aeb0f492f74f029d2dc11e27c4ea779a66092466c925`  
		Last Modified: Tue, 11 Mar 2025 17:31:22 GMT  
		Size: 254.2 MB (254156539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3e4fd0793639bdd2743e71d6d281d4ac88971eec8ec5bb77b4f41a6884ad0`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 16.6 MB (16621804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a880ba7a884a7c64c8ae0a8cf4881f654d66150b91b02e91302fa654590ad6`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65790d9c2d3e95e74caa3722659e11eb385c1844fb4bffaddf4ce7bb0580178c`  
		Last Modified: Tue, 11 Mar 2025 17:31:25 GMT  
		Size: 370.3 MB (370303218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123532ca63d760bdaa568ecfbae07b06fa91dd26ec04c8b74eadedb805c0df0e`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fcb72d07fcff6ff878c9377873c599d28d8c80887406bd9453a88e14fc25d`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d346bd36869cc104da4ea397136c0090afc9188e30ef7c158c3f9504a10767d7`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8efc6c47e1390df072ec148e68f3659322f38fa3113fd36bd17276d39247db7`  
		Last Modified: Tue, 11 Mar 2025 17:31:20 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:63e15553f2dc4e78962201abd46e60f4cc22f6f0412645afade1d876f4272dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aede8b992e8d12ca16c7e28ce76b0de19a01a53a4c365f264872f72bd49602d6`

```dockerfile
```

-	Layers:
	-	`sha256:ec5fe4e79e0988221a045f451cb9f81c5dd6ede023c8770012001fa799f814de`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 59.1 MB (59113749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af74e1bdee0c2621e1b2b84c74d28c7a4c5b4bfa074a92c64174794c171a085`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b28f72233c8ee5beb2583ac39c0e43b920df7bb03f178fb474b7fccca4383c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.9 MB (690926860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3e71e4dcdd1604ff320d7adec9f669907825bdabe163c2799b7e8fb16bde12`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16da6ef8fe07413cb95a3f576ed678f25863b030b28a5d45fbd9a59572184d61`  
		Last Modified: Tue, 11 Mar 2025 17:48:53 GMT  
		Size: 267.7 MB (267711163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6814aea401b619cfd0771c727c791ecc19b4d001e7486726f263957a44756f3`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 17.4 MB (17357228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8d4b899454650f6de2831ab2bd0b10936112e93afae366946f4c6a72adc2e`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 485.4 KB (485352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81af7dfe460a6b632831e3eae620dec1bd465841ad2c944c8d9bea3d5a59e9b8`  
		Last Modified: Tue, 11 Mar 2025 17:48:56 GMT  
		Size: 371.0 MB (370980851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7481f285d953f8ec53da7603f1f41e9ac769831acdbfeb7770b29d2e005ece`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134eafd19dd0a859c77b243c67125d4f98ed6ca742e71297f70fa171f9bec41`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf41f71e1ab5221b0d71874f6c14e540c3ce84b4b86657094c02dd17dafc7f`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a09d8707fa1039279ba6f860645fa686c9d8ae72fe42c2a43fec8ac9e93b71`  
		Last Modified: Tue, 11 Mar 2025 17:48:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a3bd0566b7a48ca445b6e0ecfac8e4068604b31d979141936efb8ff4de2b2624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff64242afb6c2b8f9d9f319ae92e9c7beaa90317a40499f65dfb0240065ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:d0ec0d5c7758b859aabce4a006ce3313ade23bff7c7f00b6da94a7b03cecd581`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 59.1 MB (59114605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8f5ef1504d03b150428249a7e2b98ef5ae213ad20f74f3bef3c3e34068a681`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250311`

```console
$ docker pull odoo@sha256:fb9654cbc22426c03962992935ca64709f38aab9f55e5b68b55eecdeedb92e60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250311` - linux; amd64

```console
$ docker pull odoo@sha256:93d835dbdfcb57be5e0fc503515dc39594a4fbdbc63b6b3065e56ea73b0617d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.3 MB (674288189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e79d2a867f20bc41f5170371a99a68a04c888dae266316051731b79b5d32293`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa53ec96f4da5767e7f2732e777a6b541f24b30816eb3daae8f72f61508becf`  
		Last Modified: Tue, 11 Mar 2025 16:56:44 GMT  
		Size: 256.9 MB (256919349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc4b2c3ef890d9b27b3c51957c89f0ca41fbc84c2c07e74dce5eaa6a2c6bcd`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 16.7 MB (16679861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2062aa9c592dfc54d31163a7f2cf3d1e67062ace2ef3bd7d07891f65edec8382`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 485.3 KB (485325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9eb5fba9b19c935f82f236d5d10a16ab1068d4cc6ac3fb6d303f0481afb19c`  
		Last Modified: Tue, 11 Mar 2025 16:56:45 GMT  
		Size: 370.4 MB (370446928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b01ef1cdff5381e84846e3d2b61b36e44199d9180c2ffef85f595222a27d6`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836ebe08b2b620d8a3e5f6e5d70b2f37d75a31d80b6ff6f76b1ff2704e3c3de`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2b55455891b4057bd3052ea7805ea764720f264a07bd0a25551def551485a`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc9e50d3dd991661885a87d849a73f78794778d010f68f57bce79475dd527d7`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:4585fe0f6581ea788de1e491ea062be15d7438a64f9dfa01ae1ba4445bc7f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59133598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320e80c6435f7a8e42af862005c5aaf8aec6e90872f340eebb6ee1e9c7209afb`

```dockerfile
```

-	Layers:
	-	`sha256:7d87349f4b6e749b6aeb0ca15bb8e917f3187d56f92eff5a685c730daac8a104`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 59.1 MB (59106462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09f264b41f172aa7282cf94928b08a06e963ecc4e0bc5680c7525f70720f0`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250311` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:703db0b0bfe5ec80d1fe73a07085238a73e14f8c668ece5522d7b7c0a380241b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.5 MB (670462982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72acc61f0a897a43b100238a878c3e0f405e6053ff5b142b33ca7dfb0bfb24fd`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8e3368073cac4ffce1aeb0f492f74f029d2dc11e27c4ea779a66092466c925`  
		Last Modified: Tue, 11 Mar 2025 17:31:22 GMT  
		Size: 254.2 MB (254156539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3e4fd0793639bdd2743e71d6d281d4ac88971eec8ec5bb77b4f41a6884ad0`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 16.6 MB (16621804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a880ba7a884a7c64c8ae0a8cf4881f654d66150b91b02e91302fa654590ad6`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65790d9c2d3e95e74caa3722659e11eb385c1844fb4bffaddf4ce7bb0580178c`  
		Last Modified: Tue, 11 Mar 2025 17:31:25 GMT  
		Size: 370.3 MB (370303218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123532ca63d760bdaa568ecfbae07b06fa91dd26ec04c8b74eadedb805c0df0e`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fcb72d07fcff6ff878c9377873c599d28d8c80887406bd9453a88e14fc25d`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d346bd36869cc104da4ea397136c0090afc9188e30ef7c158c3f9504a10767d7`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8efc6c47e1390df072ec148e68f3659322f38fa3113fd36bd17276d39247db7`  
		Last Modified: Tue, 11 Mar 2025 17:31:20 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:63e15553f2dc4e78962201abd46e60f4cc22f6f0412645afade1d876f4272dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aede8b992e8d12ca16c7e28ce76b0de19a01a53a4c365f264872f72bd49602d6`

```dockerfile
```

-	Layers:
	-	`sha256:ec5fe4e79e0988221a045f451cb9f81c5dd6ede023c8770012001fa799f814de`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 59.1 MB (59113749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af74e1bdee0c2621e1b2b84c74d28c7a4c5b4bfa074a92c64174794c171a085`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250311` - linux; ppc64le

```console
$ docker pull odoo@sha256:b28f72233c8ee5beb2583ac39c0e43b920df7bb03f178fb474b7fccca4383c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.9 MB (690926860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3e71e4dcdd1604ff320d7adec9f669907825bdabe163c2799b7e8fb16bde12`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16da6ef8fe07413cb95a3f576ed678f25863b030b28a5d45fbd9a59572184d61`  
		Last Modified: Tue, 11 Mar 2025 17:48:53 GMT  
		Size: 267.7 MB (267711163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6814aea401b619cfd0771c727c791ecc19b4d001e7486726f263957a44756f3`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 17.4 MB (17357228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8d4b899454650f6de2831ab2bd0b10936112e93afae366946f4c6a72adc2e`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 485.4 KB (485352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81af7dfe460a6b632831e3eae620dec1bd465841ad2c944c8d9bea3d5a59e9b8`  
		Last Modified: Tue, 11 Mar 2025 17:48:56 GMT  
		Size: 371.0 MB (370980851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7481f285d953f8ec53da7603f1f41e9ac769831acdbfeb7770b29d2e005ece`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134eafd19dd0a859c77b243c67125d4f98ed6ca742e71297f70fa171f9bec41`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf41f71e1ab5221b0d71874f6c14e540c3ce84b4b86657094c02dd17dafc7f`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a09d8707fa1039279ba6f860645fa686c9d8ae72fe42c2a43fec8ac9e93b71`  
		Last Modified: Tue, 11 Mar 2025 17:48:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250311` - unknown; unknown

```console
$ docker pull odoo@sha256:a3bd0566b7a48ca445b6e0ecfac8e4068604b31d979141936efb8ff4de2b2624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff64242afb6c2b8f9d9f319ae92e9c7beaa90317a40499f65dfb0240065ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:d0ec0d5c7758b859aabce4a006ce3313ade23bff7c7f00b6da94a7b03cecd581`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 59.1 MB (59114605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8f5ef1504d03b150428249a7e2b98ef5ae213ad20f74f3bef3c3e34068a681`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:fb9654cbc22426c03962992935ca64709f38aab9f55e5b68b55eecdeedb92e60
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
$ docker pull odoo@sha256:93d835dbdfcb57be5e0fc503515dc39594a4fbdbc63b6b3065e56ea73b0617d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.3 MB (674288189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e79d2a867f20bc41f5170371a99a68a04c888dae266316051731b79b5d32293`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=amd64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa53ec96f4da5767e7f2732e777a6b541f24b30816eb3daae8f72f61508becf`  
		Last Modified: Tue, 11 Mar 2025 16:56:44 GMT  
		Size: 256.9 MB (256919349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dc4b2c3ef890d9b27b3c51957c89f0ca41fbc84c2c07e74dce5eaa6a2c6bcd`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 16.7 MB (16679861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2062aa9c592dfc54d31163a7f2cf3d1e67062ace2ef3bd7d07891f65edec8382`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 485.3 KB (485325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9eb5fba9b19c935f82f236d5d10a16ab1068d4cc6ac3fb6d303f0481afb19c`  
		Last Modified: Tue, 11 Mar 2025 16:56:45 GMT  
		Size: 370.4 MB (370446928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b01ef1cdff5381e84846e3d2b61b36e44199d9180c2ffef85f595222a27d6`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836ebe08b2b620d8a3e5f6e5d70b2f37d75a31d80b6ff6f76b1ff2704e3c3de`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2b55455891b4057bd3052ea7805ea764720f264a07bd0a25551def551485a`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc9e50d3dd991661885a87d849a73f78794778d010f68f57bce79475dd527d7`  
		Last Modified: Tue, 11 Mar 2025 16:56:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:4585fe0f6581ea788de1e491ea062be15d7438a64f9dfa01ae1ba4445bc7f8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59133598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320e80c6435f7a8e42af862005c5aaf8aec6e90872f340eebb6ee1e9c7209afb`

```dockerfile
```

-	Layers:
	-	`sha256:7d87349f4b6e749b6aeb0ca15bb8e917f3187d56f92eff5a685c730daac8a104`  
		Last Modified: Tue, 11 Mar 2025 16:56:41 GMT  
		Size: 59.1 MB (59106462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e09f264b41f172aa7282cf94928b08a06e963ecc4e0bc5680c7525f70720f0`  
		Last Modified: Tue, 11 Mar 2025 16:56:40 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:703db0b0bfe5ec80d1fe73a07085238a73e14f8c668ece5522d7b7c0a380241b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.5 MB (670462982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72acc61f0a897a43b100238a878c3e0f405e6053ff5b142b33ca7dfb0bfb24fd`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=arm64
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8e3368073cac4ffce1aeb0f492f74f029d2dc11e27c4ea779a66092466c925`  
		Last Modified: Tue, 11 Mar 2025 17:31:22 GMT  
		Size: 254.2 MB (254156539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f3e4fd0793639bdd2743e71d6d281d4ac88971eec8ec5bb77b4f41a6884ad0`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 16.6 MB (16621804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a880ba7a884a7c64c8ae0a8cf4881f654d66150b91b02e91302fa654590ad6`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65790d9c2d3e95e74caa3722659e11eb385c1844fb4bffaddf4ce7bb0580178c`  
		Last Modified: Tue, 11 Mar 2025 17:31:25 GMT  
		Size: 370.3 MB (370303218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123532ca63d760bdaa568ecfbae07b06fa91dd26ec04c8b74eadedb805c0df0e`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fcb72d07fcff6ff878c9377873c599d28d8c80887406bd9453a88e14fc25d`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d346bd36869cc104da4ea397136c0090afc9188e30ef7c158c3f9504a10767d7`  
		Last Modified: Tue, 11 Mar 2025 17:31:19 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8efc6c47e1390df072ec148e68f3659322f38fa3113fd36bd17276d39247db7`  
		Last Modified: Tue, 11 Mar 2025 17:31:20 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:63e15553f2dc4e78962201abd46e60f4cc22f6f0412645afade1d876f4272dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aede8b992e8d12ca16c7e28ce76b0de19a01a53a4c365f264872f72bd49602d6`

```dockerfile
```

-	Layers:
	-	`sha256:ec5fe4e79e0988221a045f451cb9f81c5dd6ede023c8770012001fa799f814de`  
		Last Modified: Tue, 11 Mar 2025 17:31:18 GMT  
		Size: 59.1 MB (59113749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af74e1bdee0c2621e1b2b84c74d28c7a4c5b4bfa074a92c64174794c171a085`  
		Last Modified: Tue, 11 Mar 2025 17:31:17 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:b28f72233c8ee5beb2583ac39c0e43b920df7bb03f178fb474b7fccca4383c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.9 MB (690926860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3e71e4dcdd1604ff320d7adec9f669907825bdabe163c2799b7e8fb16bde12`
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
# Tue, 11 Mar 2025 10:28:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 11 Mar 2025 10:28:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 Mar 2025 10:28:40 GMT
ARG TARGETARCH=ppc64le
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_VERSION=18.0
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_RELEASE=20250311
# Tue, 11 Mar 2025 10:28:40 GMT
ARG ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250311 ODOO_SHA=de629e8416caca2475aa59cf73049fc89bf5ea5b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 11 Mar 2025 10:28:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 11 Mar 2025 10:28:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 11 Mar 2025 10:28:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 11 Mar 2025 10:28:40 GMT
USER odoo
# Tue, 11 Mar 2025 10:28:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Mar 2025 10:28:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16da6ef8fe07413cb95a3f576ed678f25863b030b28a5d45fbd9a59572184d61`  
		Last Modified: Tue, 11 Mar 2025 17:48:53 GMT  
		Size: 267.7 MB (267711163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6814aea401b619cfd0771c727c791ecc19b4d001e7486726f263957a44756f3`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 17.4 MB (17357228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8d4b899454650f6de2831ab2bd0b10936112e93afae366946f4c6a72adc2e`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 485.4 KB (485352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81af7dfe460a6b632831e3eae620dec1bd465841ad2c944c8d9bea3d5a59e9b8`  
		Last Modified: Tue, 11 Mar 2025 17:48:56 GMT  
		Size: 371.0 MB (370980851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7481f285d953f8ec53da7603f1f41e9ac769831acdbfeb7770b29d2e005ece`  
		Last Modified: Tue, 11 Mar 2025 17:48:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134eafd19dd0a859c77b243c67125d4f98ed6ca742e71297f70fa171f9bec41`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf41f71e1ab5221b0d71874f6c14e540c3ce84b4b86657094c02dd17dafc7f`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a09d8707fa1039279ba6f860645fa686c9d8ae72fe42c2a43fec8ac9e93b71`  
		Last Modified: Tue, 11 Mar 2025 17:48:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a3bd0566b7a48ca445b6e0ecfac8e4068604b31d979141936efb8ff4de2b2624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59141803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff64242afb6c2b8f9d9f319ae92e9c7beaa90317a40499f65dfb0240065ef2a`

```dockerfile
```

-	Layers:
	-	`sha256:d0ec0d5c7758b859aabce4a006ce3313ade23bff7c7f00b6da94a7b03cecd581`  
		Last Modified: Tue, 11 Mar 2025 17:48:48 GMT  
		Size: 59.1 MB (59114605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8f5ef1504d03b150428249a7e2b98ef5ae213ad20f74f3bef3c3e34068a681`  
		Last Modified: Tue, 11 Mar 2025 17:48:46 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
