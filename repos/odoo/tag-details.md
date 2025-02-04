<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250131`](#odoo160-20250131)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250131`](#odoo170-20250131)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250131`](#odoo180-20250131)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:12c86399924e8b48c48966fd174aa8eb24cc0f502dbdda038b24f1d4d4f7eeec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:fe6434685a3e618767de336b5909ff7b4be579ad38d088570fc00167b7736507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583947457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9188eba0b945b8e298262f211f7198f2129b6f0d9459782354642d4328634f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9dff007ca8df83cd7549d05502e4e9cbe26c7e572e0255755fc0c723b73a9`  
		Last Modified: Tue, 04 Feb 2025 04:45:57 GMT  
		Size: 219.6 MB (219628422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461f20c6470e4105ab7ea5fa31ec10f0f0598b124e47a42dcb27b090e26c199`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 2.6 MB (2575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0e6c1c0aa0c0952ce6097b0621541495cabf7a2e0a86ad19aa0c8fbe06ab9`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a837939eb8de4ca3b858ef4c3ffe9019410c44b656ff5c14e60c7d8dd70ff`  
		Last Modified: Tue, 04 Feb 2025 04:46:01 GMT  
		Size: 331.0 MB (331003170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7066f5e377f4d63caf439d58b48859d6a066321ee2afe4556fa42d594cc431`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030c50014b669d541e7859f33ee7d939f05e95f7fd00fc55163264e37bd159b`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83161e7cdaa2a92fd1a88f92fe45edf11f2d895332734d1383f32ad469ae26d`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a540d29e3e23ed474a821e7e9df3da0df1cf3561ee54e2f29e024c7e4c53a`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c6e6e9fc6fd880313ef6f509f72637e77bd39fc44e55ed08d3ba09bc1697d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38857726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cae739bab16ca246cda267aed81ba5a158e495f356ce9cd607b5194e3c7225`

```dockerfile
```

-	Layers:
	-	`sha256:b8d330cc74dd2c21ea4f6f27e02f30e3ee6e57e218025f576aaeed439dac87c3`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 38.8 MB (38831009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0d1c09a00999a605bb2c07a7ecb4094c090498afb7eaf30369ba6b687b2f2e`  
		Last Modified: Tue, 04 Feb 2025 04:45:51 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:dc484b83a844a8341b42e4cdb63b3aad608eeff6910e996cbda1f8c3e744eced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579416524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d874fd338b6637b185cceef4c5d95e71050a7140b74461a2e0b9dbd051966a92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafeaf9e54afc12dda0974bda319d5e7ab36b21b0b2442847830eccc3b2952a`  
		Last Modified: Tue, 04 Feb 2025 10:43:14 GMT  
		Size: 216.9 MB (216923560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dd15cb30094edfdb6cf94892c7d11934654eeefd5b66c786ae98ef42025a2c`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 2.6 MB (2583766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eb942daa2969f8efbdffbd56df03a28fc0ea0214978c7cad4df4c62b74e596`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 484.9 KB (484902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a43bab9ffdfb04e690f46af94e627a9a578c46ecd742003aaf2ca648a582e7`  
		Last Modified: Tue, 04 Feb 2025 10:43:16 GMT  
		Size: 330.7 MB (330677049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88cb4a36db75af25c5007fbd46ad7ba6d2a85e759e3874e7f3ea9b4d3a4066d`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb0c99164f9f0f21a83f22736722f4cc92576a7b2346831bbe3fc2aa98960c`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e85b08ecf12afe20e429a1b9a5b5e27a0973a8bcd9021856f79b8007adcec`  
		Last Modified: Tue, 04 Feb 2025 10:43:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81add11d22aa3aee7f09fadeaf873b6832268cfcc61610cf370efd6c5b1c77`  
		Last Modified: Tue, 04 Feb 2025 10:43:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:89a103f87153bd060f174b734ac69dffd023fccf0805d012c8527f0fcce3127f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38864348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6531cfb177b7d29797275c049b531f2551e7468ba30cd0e548e8badb7a90b`

```dockerfile
```

-	Layers:
	-	`sha256:923b764f2357f425fae1ab473cef549033a9bc6446a0b78d7f87a672314e7844`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 38.8 MB (38837479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0a1dc88ddf454a5759cd3d2a5bb7756b8a1b5a838a7a07731b405abd666832`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:12c86399924e8b48c48966fd174aa8eb24cc0f502dbdda038b24f1d4d4f7eeec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:fe6434685a3e618767de336b5909ff7b4be579ad38d088570fc00167b7736507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583947457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9188eba0b945b8e298262f211f7198f2129b6f0d9459782354642d4328634f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9dff007ca8df83cd7549d05502e4e9cbe26c7e572e0255755fc0c723b73a9`  
		Last Modified: Tue, 04 Feb 2025 04:45:57 GMT  
		Size: 219.6 MB (219628422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461f20c6470e4105ab7ea5fa31ec10f0f0598b124e47a42dcb27b090e26c199`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 2.6 MB (2575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0e6c1c0aa0c0952ce6097b0621541495cabf7a2e0a86ad19aa0c8fbe06ab9`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a837939eb8de4ca3b858ef4c3ffe9019410c44b656ff5c14e60c7d8dd70ff`  
		Last Modified: Tue, 04 Feb 2025 04:46:01 GMT  
		Size: 331.0 MB (331003170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7066f5e377f4d63caf439d58b48859d6a066321ee2afe4556fa42d594cc431`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030c50014b669d541e7859f33ee7d939f05e95f7fd00fc55163264e37bd159b`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83161e7cdaa2a92fd1a88f92fe45edf11f2d895332734d1383f32ad469ae26d`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a540d29e3e23ed474a821e7e9df3da0df1cf3561ee54e2f29e024c7e4c53a`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c6e6e9fc6fd880313ef6f509f72637e77bd39fc44e55ed08d3ba09bc1697d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38857726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cae739bab16ca246cda267aed81ba5a158e495f356ce9cd607b5194e3c7225`

```dockerfile
```

-	Layers:
	-	`sha256:b8d330cc74dd2c21ea4f6f27e02f30e3ee6e57e218025f576aaeed439dac87c3`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 38.8 MB (38831009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0d1c09a00999a605bb2c07a7ecb4094c090498afb7eaf30369ba6b687b2f2e`  
		Last Modified: Tue, 04 Feb 2025 04:45:51 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:dc484b83a844a8341b42e4cdb63b3aad608eeff6910e996cbda1f8c3e744eced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579416524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d874fd338b6637b185cceef4c5d95e71050a7140b74461a2e0b9dbd051966a92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafeaf9e54afc12dda0974bda319d5e7ab36b21b0b2442847830eccc3b2952a`  
		Last Modified: Tue, 04 Feb 2025 10:43:14 GMT  
		Size: 216.9 MB (216923560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dd15cb30094edfdb6cf94892c7d11934654eeefd5b66c786ae98ef42025a2c`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 2.6 MB (2583766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eb942daa2969f8efbdffbd56df03a28fc0ea0214978c7cad4df4c62b74e596`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 484.9 KB (484902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a43bab9ffdfb04e690f46af94e627a9a578c46ecd742003aaf2ca648a582e7`  
		Last Modified: Tue, 04 Feb 2025 10:43:16 GMT  
		Size: 330.7 MB (330677049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88cb4a36db75af25c5007fbd46ad7ba6d2a85e759e3874e7f3ea9b4d3a4066d`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb0c99164f9f0f21a83f22736722f4cc92576a7b2346831bbe3fc2aa98960c`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e85b08ecf12afe20e429a1b9a5b5e27a0973a8bcd9021856f79b8007adcec`  
		Last Modified: Tue, 04 Feb 2025 10:43:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81add11d22aa3aee7f09fadeaf873b6832268cfcc61610cf370efd6c5b1c77`  
		Last Modified: Tue, 04 Feb 2025 10:43:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:89a103f87153bd060f174b734ac69dffd023fccf0805d012c8527f0fcce3127f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38864348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6531cfb177b7d29797275c049b531f2551e7468ba30cd0e548e8badb7a90b`

```dockerfile
```

-	Layers:
	-	`sha256:923b764f2357f425fae1ab473cef549033a9bc6446a0b78d7f87a672314e7844`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 38.8 MB (38837479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0a1dc88ddf454a5759cd3d2a5bb7756b8a1b5a838a7a07731b405abd666832`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250131`

```console
$ docker pull odoo@sha256:12c86399924e8b48c48966fd174aa8eb24cc0f502dbdda038b24f1d4d4f7eeec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250131` - linux; amd64

```console
$ docker pull odoo@sha256:fe6434685a3e618767de336b5909ff7b4be579ad38d088570fc00167b7736507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583947457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9188eba0b945b8e298262f211f7198f2129b6f0d9459782354642d4328634f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9dff007ca8df83cd7549d05502e4e9cbe26c7e572e0255755fc0c723b73a9`  
		Last Modified: Tue, 04 Feb 2025 04:45:57 GMT  
		Size: 219.6 MB (219628422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461f20c6470e4105ab7ea5fa31ec10f0f0598b124e47a42dcb27b090e26c199`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 2.6 MB (2575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0e6c1c0aa0c0952ce6097b0621541495cabf7a2e0a86ad19aa0c8fbe06ab9`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a837939eb8de4ca3b858ef4c3ffe9019410c44b656ff5c14e60c7d8dd70ff`  
		Last Modified: Tue, 04 Feb 2025 04:46:01 GMT  
		Size: 331.0 MB (331003170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7066f5e377f4d63caf439d58b48859d6a066321ee2afe4556fa42d594cc431`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030c50014b669d541e7859f33ee7d939f05e95f7fd00fc55163264e37bd159b`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83161e7cdaa2a92fd1a88f92fe45edf11f2d895332734d1383f32ad469ae26d`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a540d29e3e23ed474a821e7e9df3da0df1cf3561ee54e2f29e024c7e4c53a`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:c6e6e9fc6fd880313ef6f509f72637e77bd39fc44e55ed08d3ba09bc1697d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38857726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cae739bab16ca246cda267aed81ba5a158e495f356ce9cd607b5194e3c7225`

```dockerfile
```

-	Layers:
	-	`sha256:b8d330cc74dd2c21ea4f6f27e02f30e3ee6e57e218025f576aaeed439dac87c3`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 38.8 MB (38831009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0d1c09a00999a605bb2c07a7ecb4094c090498afb7eaf30369ba6b687b2f2e`  
		Last Modified: Tue, 04 Feb 2025 04:45:51 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250131` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:dc484b83a844a8341b42e4cdb63b3aad608eeff6910e996cbda1f8c3e744eced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579416524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d874fd338b6637b185cceef4c5d95e71050a7140b74461a2e0b9dbd051966a92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafeaf9e54afc12dda0974bda319d5e7ab36b21b0b2442847830eccc3b2952a`  
		Last Modified: Tue, 04 Feb 2025 10:43:14 GMT  
		Size: 216.9 MB (216923560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dd15cb30094edfdb6cf94892c7d11934654eeefd5b66c786ae98ef42025a2c`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 2.6 MB (2583766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eb942daa2969f8efbdffbd56df03a28fc0ea0214978c7cad4df4c62b74e596`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 484.9 KB (484902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a43bab9ffdfb04e690f46af94e627a9a578c46ecd742003aaf2ca648a582e7`  
		Last Modified: Tue, 04 Feb 2025 10:43:16 GMT  
		Size: 330.7 MB (330677049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88cb4a36db75af25c5007fbd46ad7ba6d2a85e759e3874e7f3ea9b4d3a4066d`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb0c99164f9f0f21a83f22736722f4cc92576a7b2346831bbe3fc2aa98960c`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e85b08ecf12afe20e429a1b9a5b5e27a0973a8bcd9021856f79b8007adcec`  
		Last Modified: Tue, 04 Feb 2025 10:43:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81add11d22aa3aee7f09fadeaf873b6832268cfcc61610cf370efd6c5b1c77`  
		Last Modified: Tue, 04 Feb 2025 10:43:11 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:89a103f87153bd060f174b734ac69dffd023fccf0805d012c8527f0fcce3127f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38864348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6531cfb177b7d29797275c049b531f2551e7468ba30cd0e548e8badb7a90b`

```dockerfile
```

-	Layers:
	-	`sha256:923b764f2357f425fae1ab473cef549033a9bc6446a0b78d7f87a672314e7844`  
		Last Modified: Tue, 04 Feb 2025 10:43:10 GMT  
		Size: 38.8 MB (38837479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0a1dc88ddf454a5759cd3d2a5bb7756b8a1b5a838a7a07731b405abd666832`  
		Last Modified: Tue, 04 Feb 2025 10:43:09 GMT  
		Size: 26.9 KB (26869 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:0a34d5c1b80f2e67fc4109767800708d3165c0f185a0c5422ceaf6c64882767d
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
$ docker pull odoo@sha256:236a4c4fe28ef3c01da8af0ca7c4d385da82fa5d327e4600a1c0b7c9427920f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599537258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b514ab807f7892fd9b40dd3c2c3be930aca19ec4a18569592e449cb4cf24823`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f908ff198a15fa403ffc4bb2cdce2da98da5ff849f3212988a2a2d6f74ce9de`  
		Last Modified: Tue, 04 Feb 2025 04:45:46 GMT  
		Size: 233.8 MB (233764363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aceca15d2ebdd36e220bda2b54e8257e8451aec0c792c4c3671feff7b0440b3`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 2.5 MB (2493910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b362ca2656783ef6f8ba0e825777e2b37877bc5f4374f2d03ec39fbac22e`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 486.0 KB (486000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bb09415fdd8065d0c4560d0af94ad48cd7c7cfbaf6328e4b356f099287a183`  
		Last Modified: Tue, 04 Feb 2025 04:45:47 GMT  
		Size: 333.3 MB (333254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89299832330096893cb6121944768c85f230da3ad8d56ea350da4fa0ea9f841e`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027728759a34449b67f5bba56072c49afc8c7eb0fb59f92cf5417acaca33da61`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2028b1d6dd5724e4482a6eb54572978b452b53c1c7b3ac86c1452ffb066e4`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fb4e4bab5ad7d80435ef443bfed7eada17d454d35f6461c9354e38f064fa0`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:56ff431306f0bcaffa8b31e82a39061681b982d4de89c1a07abcf2626a1dbe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39719765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aee95bd053caf77aee3627469635d5a9a5928f45863626397ef114c9fc9ef43`

```dockerfile
```

-	Layers:
	-	`sha256:584618fe99d6945015124b4d4b438f5665e3ac36edc521b13c9a65c78bd5c9df`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 39.7 MB (39692930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f00b4b8bd19c62beb113dea9cc9c7c226cea87653713f5467e16899c0e9486`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1e4997321141467e915a77602c4504633aa034e261d114d1d1aab59649579543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594343887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbe0ee99e6ef336a778e50ac618727d86014e55847e160cc2b77b479c5516d`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6acb7c38ec579d2e5adf1913cf74e5baff30199c4bbd265576f20f2f1ba9`  
		Last Modified: Tue, 04 Feb 2025 10:39:19 GMT  
		Size: 231.2 MB (231160816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bfca387be25e6d214e5697808643409c746510f392fcdc14485fac54c6d5b6`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 2.5 MB (2485938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff35da8d1925b7c7b1432af44eb5750ac87bfd50ce4573b513fe90df65457da`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 485.9 KB (485947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55598971d6555da5b227de85247a638478825dfffad3c032878974f3673a3127`  
		Last Modified: Tue, 04 Feb 2025 10:39:22 GMT  
		Size: 332.9 MB (332850564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55eb769c5bace42f1a276a9f7e5b96796386b5497c7cba1e153cae435fbc471`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13ee5bc0ef7dbc828f6803ef794f05661f8d36d3ebf145f7cf5d40dfb6d8a0`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee5f729a198ca4fe16777d30533660040cf8a324fdedcdf569532250bc20f9`  
		Last Modified: Tue, 04 Feb 2025 10:39:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decf578b12d1e82acd4df68aa7f28ecdba85eb88fbf61b07a08cfd24789ae9bf`  
		Last Modified: Tue, 04 Feb 2025 10:39:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:63b3b5e77b909f811e9b2d7baaca0715b62822e9dbb9897447c46f5853fe988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39726428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7e1aafc8aca6d727de47a790bfc2a8351cf42a688e35eb15b66c67fbf2e05b`

```dockerfile
```

-	Layers:
	-	`sha256:e55a17944332d017c25634591ce0b0662ba73d57f836ad168c5f586774181d85`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 39.7 MB (39699441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947146ab4394be9cab12f89dd393d5c804748e39344715951fc0411cd955dcae`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:63a71a8743eef09113290edb1bb2c1065b8d1867c55db6d6f692c7bb567ed266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2703ad436900a9faba127f435def1849d9c922f0ba14d369e262b14a4e35d42`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c302ad0b1f60a7051c8ef388461d4ac84033c9c07ac7a7baeb1a775ac8419d5c`  
		Last Modified: Tue, 04 Feb 2025 09:06:28 GMT  
		Size: 243.3 MB (243286875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c24f7ecabe9e7dbdaea04240e28bf9ae973c0de95ad7097dcc04cafea139a3`  
		Last Modified: Tue, 04 Feb 2025 09:06:07 GMT  
		Size: 2.8 MB (2798274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e669e2082b4774f065092f0c1cce534836b54a639d98a23c332e84a114b22f05`  
		Last Modified: Tue, 04 Feb 2025 09:06:06 GMT  
		Size: 485.9 KB (485948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0818af47fe0a70d5932358017677daa075e44dd211b62dfd1d61e01c991d01`  
		Last Modified: Tue, 04 Feb 2025 09:06:29 GMT  
		Size: 335.0 MB (334977151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e86e0d3902b2bbb57ac1c74595b5249a31b72fc5f92ec10684906b7ed3502f`  
		Last Modified: Tue, 04 Feb 2025 09:06:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54207252a242ab8630ea8a953343b39167ddf330239ab75e9950eea0998984d0`  
		Last Modified: Tue, 04 Feb 2025 09:06:08 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0609a952868ba8498d858d7ead30d564f296134657067d4b5f9e4f209de0c8f`  
		Last Modified: Tue, 04 Feb 2025 09:06:09 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15205e25b9814a2b38883b399168374e9371bea2c9e8311352705af9d08e4d2`  
		Last Modified: Tue, 04 Feb 2025 09:06:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b0efbecdfd1fbc1364089c00adc1ade39c9ca7fb972d6cf1abbfdcc4d6b47769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f4d6f132494e6e773dedf652d3f1dc05a08d75e9cb5ce2be44065bb74412f`

```dockerfile
```

-	Layers:
	-	`sha256:5f3b5609cc035a2d137202699e07f81901fbf0ce3a9cc6a3703709fc4cd6178c`  
		Last Modified: Tue, 04 Feb 2025 09:06:08 GMT  
		Size: 39.7 MB (39701257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fd360f1839d03c26bb9881e154ed56d931fe9545c61716f2934fff7a4a7d9b`  
		Last Modified: Tue, 04 Feb 2025 09:06:06 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:0a34d5c1b80f2e67fc4109767800708d3165c0f185a0c5422ceaf6c64882767d
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
$ docker pull odoo@sha256:236a4c4fe28ef3c01da8af0ca7c4d385da82fa5d327e4600a1c0b7c9427920f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599537258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b514ab807f7892fd9b40dd3c2c3be930aca19ec4a18569592e449cb4cf24823`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f908ff198a15fa403ffc4bb2cdce2da98da5ff849f3212988a2a2d6f74ce9de`  
		Last Modified: Tue, 04 Feb 2025 04:45:46 GMT  
		Size: 233.8 MB (233764363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aceca15d2ebdd36e220bda2b54e8257e8451aec0c792c4c3671feff7b0440b3`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 2.5 MB (2493910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b362ca2656783ef6f8ba0e825777e2b37877bc5f4374f2d03ec39fbac22e`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 486.0 KB (486000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bb09415fdd8065d0c4560d0af94ad48cd7c7cfbaf6328e4b356f099287a183`  
		Last Modified: Tue, 04 Feb 2025 04:45:47 GMT  
		Size: 333.3 MB (333254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89299832330096893cb6121944768c85f230da3ad8d56ea350da4fa0ea9f841e`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027728759a34449b67f5bba56072c49afc8c7eb0fb59f92cf5417acaca33da61`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2028b1d6dd5724e4482a6eb54572978b452b53c1c7b3ac86c1452ffb066e4`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fb4e4bab5ad7d80435ef443bfed7eada17d454d35f6461c9354e38f064fa0`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:56ff431306f0bcaffa8b31e82a39061681b982d4de89c1a07abcf2626a1dbe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39719765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aee95bd053caf77aee3627469635d5a9a5928f45863626397ef114c9fc9ef43`

```dockerfile
```

-	Layers:
	-	`sha256:584618fe99d6945015124b4d4b438f5665e3ac36edc521b13c9a65c78bd5c9df`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 39.7 MB (39692930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f00b4b8bd19c62beb113dea9cc9c7c226cea87653713f5467e16899c0e9486`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1e4997321141467e915a77602c4504633aa034e261d114d1d1aab59649579543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594343887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbe0ee99e6ef336a778e50ac618727d86014e55847e160cc2b77b479c5516d`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6acb7c38ec579d2e5adf1913cf74e5baff30199c4bbd265576f20f2f1ba9`  
		Last Modified: Tue, 04 Feb 2025 10:39:19 GMT  
		Size: 231.2 MB (231160816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bfca387be25e6d214e5697808643409c746510f392fcdc14485fac54c6d5b6`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 2.5 MB (2485938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff35da8d1925b7c7b1432af44eb5750ac87bfd50ce4573b513fe90df65457da`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 485.9 KB (485947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55598971d6555da5b227de85247a638478825dfffad3c032878974f3673a3127`  
		Last Modified: Tue, 04 Feb 2025 10:39:22 GMT  
		Size: 332.9 MB (332850564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55eb769c5bace42f1a276a9f7e5b96796386b5497c7cba1e153cae435fbc471`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13ee5bc0ef7dbc828f6803ef794f05661f8d36d3ebf145f7cf5d40dfb6d8a0`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee5f729a198ca4fe16777d30533660040cf8a324fdedcdf569532250bc20f9`  
		Last Modified: Tue, 04 Feb 2025 10:39:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decf578b12d1e82acd4df68aa7f28ecdba85eb88fbf61b07a08cfd24789ae9bf`  
		Last Modified: Tue, 04 Feb 2025 10:39:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:63b3b5e77b909f811e9b2d7baaca0715b62822e9dbb9897447c46f5853fe988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39726428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7e1aafc8aca6d727de47a790bfc2a8351cf42a688e35eb15b66c67fbf2e05b`

```dockerfile
```

-	Layers:
	-	`sha256:e55a17944332d017c25634591ce0b0662ba73d57f836ad168c5f586774181d85`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 39.7 MB (39699441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947146ab4394be9cab12f89dd393d5c804748e39344715951fc0411cd955dcae`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:63a71a8743eef09113290edb1bb2c1065b8d1867c55db6d6f692c7bb567ed266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2703ad436900a9faba127f435def1849d9c922f0ba14d369e262b14a4e35d42`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c302ad0b1f60a7051c8ef388461d4ac84033c9c07ac7a7baeb1a775ac8419d5c`  
		Last Modified: Tue, 04 Feb 2025 09:06:28 GMT  
		Size: 243.3 MB (243286875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c24f7ecabe9e7dbdaea04240e28bf9ae973c0de95ad7097dcc04cafea139a3`  
		Last Modified: Tue, 04 Feb 2025 09:06:07 GMT  
		Size: 2.8 MB (2798274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e669e2082b4774f065092f0c1cce534836b54a639d98a23c332e84a114b22f05`  
		Last Modified: Tue, 04 Feb 2025 09:06:06 GMT  
		Size: 485.9 KB (485948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0818af47fe0a70d5932358017677daa075e44dd211b62dfd1d61e01c991d01`  
		Last Modified: Tue, 04 Feb 2025 09:06:29 GMT  
		Size: 335.0 MB (334977151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e86e0d3902b2bbb57ac1c74595b5249a31b72fc5f92ec10684906b7ed3502f`  
		Last Modified: Tue, 04 Feb 2025 09:06:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54207252a242ab8630ea8a953343b39167ddf330239ab75e9950eea0998984d0`  
		Last Modified: Tue, 04 Feb 2025 09:06:08 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0609a952868ba8498d858d7ead30d564f296134657067d4b5f9e4f209de0c8f`  
		Last Modified: Tue, 04 Feb 2025 09:06:09 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15205e25b9814a2b38883b399168374e9371bea2c9e8311352705af9d08e4d2`  
		Last Modified: Tue, 04 Feb 2025 09:06:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b0efbecdfd1fbc1364089c00adc1ade39c9ca7fb972d6cf1abbfdcc4d6b47769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f4d6f132494e6e773dedf652d3f1dc05a08d75e9cb5ce2be44065bb74412f`

```dockerfile
```

-	Layers:
	-	`sha256:5f3b5609cc035a2d137202699e07f81901fbf0ce3a9cc6a3703709fc4cd6178c`  
		Last Modified: Tue, 04 Feb 2025 09:06:08 GMT  
		Size: 39.7 MB (39701257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fd360f1839d03c26bb9881e154ed56d931fe9545c61716f2934fff7a4a7d9b`  
		Last Modified: Tue, 04 Feb 2025 09:06:06 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250131`

```console
$ docker pull odoo@sha256:0a34d5c1b80f2e67fc4109767800708d3165c0f185a0c5422ceaf6c64882767d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250131` - linux; amd64

```console
$ docker pull odoo@sha256:236a4c4fe28ef3c01da8af0ca7c4d385da82fa5d327e4600a1c0b7c9427920f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599537258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b514ab807f7892fd9b40dd3c2c3be930aca19ec4a18569592e449cb4cf24823`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f908ff198a15fa403ffc4bb2cdce2da98da5ff849f3212988a2a2d6f74ce9de`  
		Last Modified: Tue, 04 Feb 2025 04:45:46 GMT  
		Size: 233.8 MB (233764363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aceca15d2ebdd36e220bda2b54e8257e8451aec0c792c4c3671feff7b0440b3`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 2.5 MB (2493910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b362ca2656783ef6f8ba0e825777e2b37877bc5f4374f2d03ec39fbac22e`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 486.0 KB (486000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bb09415fdd8065d0c4560d0af94ad48cd7c7cfbaf6328e4b356f099287a183`  
		Last Modified: Tue, 04 Feb 2025 04:45:47 GMT  
		Size: 333.3 MB (333254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89299832330096893cb6121944768c85f230da3ad8d56ea350da4fa0ea9f841e`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027728759a34449b67f5bba56072c49afc8c7eb0fb59f92cf5417acaca33da61`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2028b1d6dd5724e4482a6eb54572978b452b53c1c7b3ac86c1452ffb066e4`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fb4e4bab5ad7d80435ef443bfed7eada17d454d35f6461c9354e38f064fa0`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:56ff431306f0bcaffa8b31e82a39061681b982d4de89c1a07abcf2626a1dbe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39719765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aee95bd053caf77aee3627469635d5a9a5928f45863626397ef114c9fc9ef43`

```dockerfile
```

-	Layers:
	-	`sha256:584618fe99d6945015124b4d4b438f5665e3ac36edc521b13c9a65c78bd5c9df`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 39.7 MB (39692930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f00b4b8bd19c62beb113dea9cc9c7c226cea87653713f5467e16899c0e9486`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250131` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1e4997321141467e915a77602c4504633aa034e261d114d1d1aab59649579543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594343887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbe0ee99e6ef336a778e50ac618727d86014e55847e160cc2b77b479c5516d`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6acb7c38ec579d2e5adf1913cf74e5baff30199c4bbd265576f20f2f1ba9`  
		Last Modified: Tue, 04 Feb 2025 10:39:19 GMT  
		Size: 231.2 MB (231160816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bfca387be25e6d214e5697808643409c746510f392fcdc14485fac54c6d5b6`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 2.5 MB (2485938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff35da8d1925b7c7b1432af44eb5750ac87bfd50ce4573b513fe90df65457da`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 485.9 KB (485947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55598971d6555da5b227de85247a638478825dfffad3c032878974f3673a3127`  
		Last Modified: Tue, 04 Feb 2025 10:39:22 GMT  
		Size: 332.9 MB (332850564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55eb769c5bace42f1a276a9f7e5b96796386b5497c7cba1e153cae435fbc471`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13ee5bc0ef7dbc828f6803ef794f05661f8d36d3ebf145f7cf5d40dfb6d8a0`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee5f729a198ca4fe16777d30533660040cf8a324fdedcdf569532250bc20f9`  
		Last Modified: Tue, 04 Feb 2025 10:39:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decf578b12d1e82acd4df68aa7f28ecdba85eb88fbf61b07a08cfd24789ae9bf`  
		Last Modified: Tue, 04 Feb 2025 10:39:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:63b3b5e77b909f811e9b2d7baaca0715b62822e9dbb9897447c46f5853fe988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39726428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7e1aafc8aca6d727de47a790bfc2a8351cf42a688e35eb15b66c67fbf2e05b`

```dockerfile
```

-	Layers:
	-	`sha256:e55a17944332d017c25634591ce0b0662ba73d57f836ad168c5f586774181d85`  
		Last Modified: Tue, 04 Feb 2025 10:39:16 GMT  
		Size: 39.7 MB (39699441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947146ab4394be9cab12f89dd393d5c804748e39344715951fc0411cd955dcae`  
		Last Modified: Tue, 04 Feb 2025 10:39:15 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250131` - linux; ppc64le

```console
$ docker pull odoo@sha256:63a71a8743eef09113290edb1bb2c1065b8d1867c55db6d6f692c7bb567ed266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (615998624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2703ad436900a9faba127f435def1849d9c922f0ba14d369e262b14a4e35d42`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c302ad0b1f60a7051c8ef388461d4ac84033c9c07ac7a7baeb1a775ac8419d5c`  
		Last Modified: Tue, 04 Feb 2025 09:06:28 GMT  
		Size: 243.3 MB (243286875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c24f7ecabe9e7dbdaea04240e28bf9ae973c0de95ad7097dcc04cafea139a3`  
		Last Modified: Tue, 04 Feb 2025 09:06:07 GMT  
		Size: 2.8 MB (2798274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e669e2082b4774f065092f0c1cce534836b54a639d98a23c332e84a114b22f05`  
		Last Modified: Tue, 04 Feb 2025 09:06:06 GMT  
		Size: 485.9 KB (485948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0818af47fe0a70d5932358017677daa075e44dd211b62dfd1d61e01c991d01`  
		Last Modified: Tue, 04 Feb 2025 09:06:29 GMT  
		Size: 335.0 MB (334977151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e86e0d3902b2bbb57ac1c74595b5249a31b72fc5f92ec10684906b7ed3502f`  
		Last Modified: Tue, 04 Feb 2025 09:06:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54207252a242ab8630ea8a953343b39167ddf330239ab75e9950eea0998984d0`  
		Last Modified: Tue, 04 Feb 2025 09:06:08 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0609a952868ba8498d858d7ead30d564f296134657067d4b5f9e4f209de0c8f`  
		Last Modified: Tue, 04 Feb 2025 09:06:09 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15205e25b9814a2b38883b399168374e9371bea2c9e8311352705af9d08e4d2`  
		Last Modified: Tue, 04 Feb 2025 09:06:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:b0efbecdfd1fbc1364089c00adc1ade39c9ca7fb972d6cf1abbfdcc4d6b47769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f4d6f132494e6e773dedf652d3f1dc05a08d75e9cb5ce2be44065bb74412f`

```dockerfile
```

-	Layers:
	-	`sha256:5f3b5609cc035a2d137202699e07f81901fbf0ce3a9cc6a3703709fc4cd6178c`  
		Last Modified: Tue, 04 Feb 2025 09:06:08 GMT  
		Size: 39.7 MB (39701257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fd360f1839d03c26bb9881e154ed56d931fe9545c61716f2934fff7a4a7d9b`  
		Last Modified: Tue, 04 Feb 2025 09:06:06 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:fb921bf251f2fc63d111529dec7d81488b3559f41c005302a46431df257eac29
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
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9497712ca79e025db256fcbf04799c2f04df91e07384cedddbf7f22615ad5f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 MB (664834931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11646a738238493381ceb8e0cafcc44833e4c5f33edd3dfe87da1a7fab39d6a4`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ceb7ac38df31f20728c76755b4c60dc4f0b01ddfb39cc2f7863c20f6750b7`  
		Last Modified: Tue, 04 Feb 2025 10:33:14 GMT  
		Size: 251.9 MB (251942614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f15f2dfc081e04fd9558a6f38d2419641a70b9e41db6f6b926689e9b952c20b`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 16.6 MB (16580979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baeb2cf497cf93c5dd53e99abe08c8db430f87162093d606f989096ae5a6ede`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 485.7 KB (485721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9248ded97462d729042fa5aff670dee514eef358ccfde4bc93ea850c242962`  
		Last Modified: Tue, 04 Feb 2025 10:33:16 GMT  
		Size: 366.9 MB (366929581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91bf317c0999b861aa5e6def8411913d47175722329f810c9ea012081db3b96`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cbb9baa9b48038098478d32c22b66fb8c76770f1f2b2eaeb1aae735f583700`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb60c04672fefb40d2710396a0cb4ab9c85251ea8892aacdadb485c3459a9e7`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e7ce09bdb68423aa6eb46f378fe4d4760a7da734d5867e376e531d56be5953`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:5de8a00be2199720bfc64d6d12ce9bf120dbcc6e051a6a0ea6fd80417d262581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1350b3975f40019f655d31286508a54dfdb2032d8846d3699bc80ebc093ec056`

```dockerfile
```

-	Layers:
	-	`sha256:d19c6630add72f103bff1bc4bbe11a0e4e3c638cff7034df46c1bdadaa455aec`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 58.4 MB (58417827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f7fb70a0091565476a7b91f55b8dfbda2373a6950a3a30d52d24778c5b8a39`  
		Last Modified: Tue, 04 Feb 2025 10:33:08 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:7cf8eff864dc7126f83d0e3a64c59a2f17be2e998ce63159ec840cacd84b6be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.9 MB (684860350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d813a3041b5ba28c69b8618b233969507c502c9cac1421b54a1dd211912e33`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d418c0840849483328b23e91b37906011d5428a8d33eb01d76c67643c95ed27e`  
		Last Modified: Tue, 04 Feb 2025 08:57:03 GMT  
		Size: 265.1 MB (265072565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c8deb2024dac4081ecc4eee6a89529f131b70a1967fc3e306735ec3fb400e8`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 17.3 MB (17306284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0227eac83b8514c81ecd610eb102da985ffeef75e0bfe4684cc367e98b6c8`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 485.7 KB (485731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748827fcf642dbd3233b502f85883f06a857b2e64ba727c4bf2c7d7b1c4952ba`  
		Last Modified: Tue, 04 Feb 2025 08:57:01 GMT  
		Size: 367.6 MB (367603502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af29a81682914f004a5ddcaaeceaaba08ceffc9afecfb0d162c2167f8f0f151c`  
		Last Modified: Tue, 04 Feb 2025 08:56:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c32ad48faf3b82a27f71c77d61b286c0cf2d9a7233119282b845ad0d1fe2be`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36c149aaed076cb533058cb8b92980de5b945e0ae60a9f140c7620df95a470`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbac197049fa129399df2dbc803ac53100f09d4f4015198e0d4d5fea9bd6fd`  
		Last Modified: Tue, 04 Feb 2025 08:56:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:5989e012168c7a65e5b310271837fa89db6828af0c4f012aa6849d1258ff3b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e49b414f5488674f8b1137abb232047b453d7449fd1120a6d46dd75b73a4e16`

```dockerfile
```

-	Layers:
	-	`sha256:0a0078a1416d67e2d188eb9e311c02e86191c837f2d2562b45053a548a3b0c8c`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 58.4 MB (58418699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16328d5d39e770de72c176dbb63743031ca2308fda0482b5ecd6004638ac402e`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:fb921bf251f2fc63d111529dec7d81488b3559f41c005302a46431df257eac29
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
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9497712ca79e025db256fcbf04799c2f04df91e07384cedddbf7f22615ad5f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 MB (664834931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11646a738238493381ceb8e0cafcc44833e4c5f33edd3dfe87da1a7fab39d6a4`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ceb7ac38df31f20728c76755b4c60dc4f0b01ddfb39cc2f7863c20f6750b7`  
		Last Modified: Tue, 04 Feb 2025 10:33:14 GMT  
		Size: 251.9 MB (251942614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f15f2dfc081e04fd9558a6f38d2419641a70b9e41db6f6b926689e9b952c20b`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 16.6 MB (16580979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baeb2cf497cf93c5dd53e99abe08c8db430f87162093d606f989096ae5a6ede`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 485.7 KB (485721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9248ded97462d729042fa5aff670dee514eef358ccfde4bc93ea850c242962`  
		Last Modified: Tue, 04 Feb 2025 10:33:16 GMT  
		Size: 366.9 MB (366929581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91bf317c0999b861aa5e6def8411913d47175722329f810c9ea012081db3b96`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cbb9baa9b48038098478d32c22b66fb8c76770f1f2b2eaeb1aae735f583700`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb60c04672fefb40d2710396a0cb4ab9c85251ea8892aacdadb485c3459a9e7`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e7ce09bdb68423aa6eb46f378fe4d4760a7da734d5867e376e531d56be5953`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5de8a00be2199720bfc64d6d12ce9bf120dbcc6e051a6a0ea6fd80417d262581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1350b3975f40019f655d31286508a54dfdb2032d8846d3699bc80ebc093ec056`

```dockerfile
```

-	Layers:
	-	`sha256:d19c6630add72f103bff1bc4bbe11a0e4e3c638cff7034df46c1bdadaa455aec`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 58.4 MB (58417827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f7fb70a0091565476a7b91f55b8dfbda2373a6950a3a30d52d24778c5b8a39`  
		Last Modified: Tue, 04 Feb 2025 10:33:08 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:7cf8eff864dc7126f83d0e3a64c59a2f17be2e998ce63159ec840cacd84b6be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.9 MB (684860350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d813a3041b5ba28c69b8618b233969507c502c9cac1421b54a1dd211912e33`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d418c0840849483328b23e91b37906011d5428a8d33eb01d76c67643c95ed27e`  
		Last Modified: Tue, 04 Feb 2025 08:57:03 GMT  
		Size: 265.1 MB (265072565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c8deb2024dac4081ecc4eee6a89529f131b70a1967fc3e306735ec3fb400e8`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 17.3 MB (17306284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0227eac83b8514c81ecd610eb102da985ffeef75e0bfe4684cc367e98b6c8`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 485.7 KB (485731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748827fcf642dbd3233b502f85883f06a857b2e64ba727c4bf2c7d7b1c4952ba`  
		Last Modified: Tue, 04 Feb 2025 08:57:01 GMT  
		Size: 367.6 MB (367603502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af29a81682914f004a5ddcaaeceaaba08ceffc9afecfb0d162c2167f8f0f151c`  
		Last Modified: Tue, 04 Feb 2025 08:56:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c32ad48faf3b82a27f71c77d61b286c0cf2d9a7233119282b845ad0d1fe2be`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36c149aaed076cb533058cb8b92980de5b945e0ae60a9f140c7620df95a470`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbac197049fa129399df2dbc803ac53100f09d4f4015198e0d4d5fea9bd6fd`  
		Last Modified: Tue, 04 Feb 2025 08:56:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5989e012168c7a65e5b310271837fa89db6828af0c4f012aa6849d1258ff3b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e49b414f5488674f8b1137abb232047b453d7449fd1120a6d46dd75b73a4e16`

```dockerfile
```

-	Layers:
	-	`sha256:0a0078a1416d67e2d188eb9e311c02e86191c837f2d2562b45053a548a3b0c8c`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 58.4 MB (58418699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16328d5d39e770de72c176dbb63743031ca2308fda0482b5ecd6004638ac402e`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250131`

```console
$ docker pull odoo@sha256:fb921bf251f2fc63d111529dec7d81488b3559f41c005302a46431df257eac29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250131` - linux; amd64

```console
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250131` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9497712ca79e025db256fcbf04799c2f04df91e07384cedddbf7f22615ad5f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 MB (664834931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11646a738238493381ceb8e0cafcc44833e4c5f33edd3dfe87da1a7fab39d6a4`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ceb7ac38df31f20728c76755b4c60dc4f0b01ddfb39cc2f7863c20f6750b7`  
		Last Modified: Tue, 04 Feb 2025 10:33:14 GMT  
		Size: 251.9 MB (251942614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f15f2dfc081e04fd9558a6f38d2419641a70b9e41db6f6b926689e9b952c20b`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 16.6 MB (16580979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baeb2cf497cf93c5dd53e99abe08c8db430f87162093d606f989096ae5a6ede`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 485.7 KB (485721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9248ded97462d729042fa5aff670dee514eef358ccfde4bc93ea850c242962`  
		Last Modified: Tue, 04 Feb 2025 10:33:16 GMT  
		Size: 366.9 MB (366929581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91bf317c0999b861aa5e6def8411913d47175722329f810c9ea012081db3b96`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cbb9baa9b48038098478d32c22b66fb8c76770f1f2b2eaeb1aae735f583700`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb60c04672fefb40d2710396a0cb4ab9c85251ea8892aacdadb485c3459a9e7`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e7ce09bdb68423aa6eb46f378fe4d4760a7da734d5867e376e531d56be5953`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:5de8a00be2199720bfc64d6d12ce9bf120dbcc6e051a6a0ea6fd80417d262581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1350b3975f40019f655d31286508a54dfdb2032d8846d3699bc80ebc093ec056`

```dockerfile
```

-	Layers:
	-	`sha256:d19c6630add72f103bff1bc4bbe11a0e4e3c638cff7034df46c1bdadaa455aec`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 58.4 MB (58417827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f7fb70a0091565476a7b91f55b8dfbda2373a6950a3a30d52d24778c5b8a39`  
		Last Modified: Tue, 04 Feb 2025 10:33:08 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250131` - linux; ppc64le

```console
$ docker pull odoo@sha256:7cf8eff864dc7126f83d0e3a64c59a2f17be2e998ce63159ec840cacd84b6be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.9 MB (684860350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d813a3041b5ba28c69b8618b233969507c502c9cac1421b54a1dd211912e33`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d418c0840849483328b23e91b37906011d5428a8d33eb01d76c67643c95ed27e`  
		Last Modified: Tue, 04 Feb 2025 08:57:03 GMT  
		Size: 265.1 MB (265072565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c8deb2024dac4081ecc4eee6a89529f131b70a1967fc3e306735ec3fb400e8`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 17.3 MB (17306284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0227eac83b8514c81ecd610eb102da985ffeef75e0bfe4684cc367e98b6c8`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 485.7 KB (485731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748827fcf642dbd3233b502f85883f06a857b2e64ba727c4bf2c7d7b1c4952ba`  
		Last Modified: Tue, 04 Feb 2025 08:57:01 GMT  
		Size: 367.6 MB (367603502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af29a81682914f004a5ddcaaeceaaba08ceffc9afecfb0d162c2167f8f0f151c`  
		Last Modified: Tue, 04 Feb 2025 08:56:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c32ad48faf3b82a27f71c77d61b286c0cf2d9a7233119282b845ad0d1fe2be`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36c149aaed076cb533058cb8b92980de5b945e0ae60a9f140c7620df95a470`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbac197049fa129399df2dbc803ac53100f09d4f4015198e0d4d5fea9bd6fd`  
		Last Modified: Tue, 04 Feb 2025 08:56:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:5989e012168c7a65e5b310271837fa89db6828af0c4f012aa6849d1258ff3b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e49b414f5488674f8b1137abb232047b453d7449fd1120a6d46dd75b73a4e16`

```dockerfile
```

-	Layers:
	-	`sha256:0a0078a1416d67e2d188eb9e311c02e86191c837f2d2562b45053a548a3b0c8c`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 58.4 MB (58418699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16328d5d39e770de72c176dbb63743031ca2308fda0482b5ecd6004638ac402e`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:fb921bf251f2fc63d111529dec7d81488b3559f41c005302a46431df257eac29
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
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9497712ca79e025db256fcbf04799c2f04df91e07384cedddbf7f22615ad5f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 MB (664834931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11646a738238493381ceb8e0cafcc44833e4c5f33edd3dfe87da1a7fab39d6a4`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ceb7ac38df31f20728c76755b4c60dc4f0b01ddfb39cc2f7863c20f6750b7`  
		Last Modified: Tue, 04 Feb 2025 10:33:14 GMT  
		Size: 251.9 MB (251942614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f15f2dfc081e04fd9558a6f38d2419641a70b9e41db6f6b926689e9b952c20b`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 16.6 MB (16580979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baeb2cf497cf93c5dd53e99abe08c8db430f87162093d606f989096ae5a6ede`  
		Last Modified: Tue, 04 Feb 2025 10:33:09 GMT  
		Size: 485.7 KB (485721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9248ded97462d729042fa5aff670dee514eef358ccfde4bc93ea850c242962`  
		Last Modified: Tue, 04 Feb 2025 10:33:16 GMT  
		Size: 366.9 MB (366929581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91bf317c0999b861aa5e6def8411913d47175722329f810c9ea012081db3b96`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cbb9baa9b48038098478d32c22b66fb8c76770f1f2b2eaeb1aae735f583700`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb60c04672fefb40d2710396a0cb4ab9c85251ea8892aacdadb485c3459a9e7`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e7ce09bdb68423aa6eb46f378fe4d4760a7da734d5867e376e531d56be5953`  
		Last Modified: Tue, 04 Feb 2025 10:33:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5de8a00be2199720bfc64d6d12ce9bf120dbcc6e051a6a0ea6fd80417d262581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1350b3975f40019f655d31286508a54dfdb2032d8846d3699bc80ebc093ec056`

```dockerfile
```

-	Layers:
	-	`sha256:d19c6630add72f103bff1bc4bbe11a0e4e3c638cff7034df46c1bdadaa455aec`  
		Last Modified: Tue, 04 Feb 2025 10:33:10 GMT  
		Size: 58.4 MB (58417827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f7fb70a0091565476a7b91f55b8dfbda2373a6950a3a30d52d24778c5b8a39`  
		Last Modified: Tue, 04 Feb 2025 10:33:08 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:7cf8eff864dc7126f83d0e3a64c59a2f17be2e998ce63159ec840cacd84b6be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.9 MB (684860350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d813a3041b5ba28c69b8618b233969507c502c9cac1421b54a1dd211912e33`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d418c0840849483328b23e91b37906011d5428a8d33eb01d76c67643c95ed27e`  
		Last Modified: Tue, 04 Feb 2025 08:57:03 GMT  
		Size: 265.1 MB (265072565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c8deb2024dac4081ecc4eee6a89529f131b70a1967fc3e306735ec3fb400e8`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 17.3 MB (17306284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0227eac83b8514c81ecd610eb102da985ffeef75e0bfe4684cc367e98b6c8`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 485.7 KB (485731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748827fcf642dbd3233b502f85883f06a857b2e64ba727c4bf2c7d7b1c4952ba`  
		Last Modified: Tue, 04 Feb 2025 08:57:01 GMT  
		Size: 367.6 MB (367603502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af29a81682914f004a5ddcaaeceaaba08ceffc9afecfb0d162c2167f8f0f151c`  
		Last Modified: Tue, 04 Feb 2025 08:56:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c32ad48faf3b82a27f71c77d61b286c0cf2d9a7233119282b845ad0d1fe2be`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a36c149aaed076cb533058cb8b92980de5b945e0ae60a9f140c7620df95a470`  
		Last Modified: Tue, 04 Feb 2025 08:56:37 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cbac197049fa129399df2dbc803ac53100f09d4f4015198e0d4d5fea9bd6fd`  
		Last Modified: Tue, 04 Feb 2025 08:56:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5989e012168c7a65e5b310271837fa89db6828af0c4f012aa6849d1258ff3b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58445896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e49b414f5488674f8b1137abb232047b453d7449fd1120a6d46dd75b73a4e16`

```dockerfile
```

-	Layers:
	-	`sha256:0a0078a1416d67e2d188eb9e311c02e86191c837f2d2562b45053a548a3b0c8c`  
		Last Modified: Tue, 04 Feb 2025 08:56:36 GMT  
		Size: 58.4 MB (58418699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16328d5d39e770de72c176dbb63743031ca2308fda0482b5ecd6004638ac402e`  
		Last Modified: Tue, 04 Feb 2025 08:56:34 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json
