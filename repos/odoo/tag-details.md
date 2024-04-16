<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:5d4dcfa41dd6f419bfcede7a599833e780a491897fadbdb8382cdd35d75fec82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:f119f88c7c9ec82e4a75d3438ad318c75abcfb939c5760d26571a3cc565eb7e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564110551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab393ea3a51d5a76cf85681f39e52fd992850045a80d923670ea60ceb88b941`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 13:02:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:02:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:02:38 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:02:38 GMT
ENV ODOO_VERSION=15.0
# Tue, 16 Apr 2024 21:54:57 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:54:58 GMT
ARG ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
# Tue, 16 Apr 2024 21:56:09 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:56:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:56:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:56:14 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:56:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:56:15 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:56:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:56:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:56:15 GMT
USER odoo
# Tue, 16 Apr 2024 21:56:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:56:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2045d8f0213447e0ed9c992443e5b28b28436258f31e1a7f0905c619febed4a`  
		Last Modified: Wed, 10 Apr 2024 13:05:24 GMT  
		Size: 220.3 MB (220292918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d284b698af5472e02d28e56879c21119101db7822e8d9da1cd0c8e56cfaa1`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 2.6 MB (2625949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6128ad9a05b37109de759a4d52717e2b12b67a316a0940e5722bc3062e8db6f`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 458.4 KB (458422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db39f6dc230311410ffe0fa13a48a2126d3c09bd8681631ce82732fba5a8c738`  
		Last Modified: Tue, 16 Apr 2024 21:58:39 GMT  
		Size: 309.3 MB (309303064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2374fe7e220bd4dd909e9477eee22ceac05daebe54df4c487ea797eba7e9d230`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d517a92781f9403742a01229435ae20310255f8c02f9cddb8af83bde8c922c`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7e7782fa296dcbdc262aebc94f34c3f6712bc4e5d2ad69c5d1939c234e9edc`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998c1b2fc295dc2dcea4a0513514da84ec82e06d73020538f4e6707fccea037`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:5d4dcfa41dd6f419bfcede7a599833e780a491897fadbdb8382cdd35d75fec82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:f119f88c7c9ec82e4a75d3438ad318c75abcfb939c5760d26571a3cc565eb7e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564110551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab393ea3a51d5a76cf85681f39e52fd992850045a80d923670ea60ceb88b941`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 13:02:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:02:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:02:38 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:02:38 GMT
ENV ODOO_VERSION=15.0
# Tue, 16 Apr 2024 21:54:57 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:54:58 GMT
ARG ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
# Tue, 16 Apr 2024 21:56:09 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:56:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:56:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:56:14 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:56:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:56:15 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:56:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:56:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:56:15 GMT
USER odoo
# Tue, 16 Apr 2024 21:56:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:56:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2045d8f0213447e0ed9c992443e5b28b28436258f31e1a7f0905c619febed4a`  
		Last Modified: Wed, 10 Apr 2024 13:05:24 GMT  
		Size: 220.3 MB (220292918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d284b698af5472e02d28e56879c21119101db7822e8d9da1cd0c8e56cfaa1`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 2.6 MB (2625949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6128ad9a05b37109de759a4d52717e2b12b67a316a0940e5722bc3062e8db6f`  
		Last Modified: Wed, 10 Apr 2024 13:05:00 GMT  
		Size: 458.4 KB (458422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db39f6dc230311410ffe0fa13a48a2126d3c09bd8681631ce82732fba5a8c738`  
		Last Modified: Tue, 16 Apr 2024 21:58:39 GMT  
		Size: 309.3 MB (309303064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2374fe7e220bd4dd909e9477eee22ceac05daebe54df4c487ea797eba7e9d230`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d517a92781f9403742a01229435ae20310255f8c02f9cddb8af83bde8c922c`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7e7782fa296dcbdc262aebc94f34c3f6712bc4e5d2ad69c5d1939c234e9edc`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998c1b2fc295dc2dcea4a0513514da84ec82e06d73020538f4e6707fccea037`  
		Last Modified: Tue, 16 Apr 2024 21:58:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:e8f2c01d3e470ca08e44dd2bd4620426cd941e69ab77ae5a0485d3d226bd4fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f5c87f7e9e38e3774b16737409b8eebf32becf7a3932e7deb73ab5c7a9c2d7ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.1 MB (583139362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b387113654f2d9943644cffcc2534ba7cbacaa01f60e247c340e1712b1592d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:58:42 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:59:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:00:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:00:02 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:00:02 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Apr 2024 21:53:19 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:53:19 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Tue, 16 Apr 2024 21:54:41 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:54:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:54:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:54:46 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:54:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:54:47 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:54:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:54:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:54:47 GMT
USER odoo
# Tue, 16 Apr 2024 21:54:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:54:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac79b7d43ed31e626ad7d7c9941d7c0a17c43c083711789fb83c11d9110dcfe`  
		Last Modified: Wed, 10 Apr 2024 13:04:36 GMT  
		Size: 219.6 MB (219603194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed26f48190afc427fd1165018baf6a3058a80e56d28e8e3d11097760605dbff`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 2.6 MB (2630065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308ec53827fb3d168639a63a8844a8db71a0d31b340ec755c0fd7b806e82e2f`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 458.4 KB (458435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8105fc6905658e799a06242c9236fcf25cbcfd5a97283db5aa9ad3e579a004b`  
		Last Modified: Tue, 16 Apr 2024 21:57:57 GMT  
		Size: 329.0 MB (329017469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbeea84723df059756a1d8ca820500cb4d60e448dd2eb03733409180c7c81d2`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b175ddf367740d5bbe22d944570aef1b4ee9d1ff59d1223af5482c712511e`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd19aa24a7ec97f800dcfc9715050dc4ae392226d6fead9616af636b4951182`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebee86fcf5796cc698b913dfce7a21de579af0a81b3a25930a122ade18714bd`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:49fe23046e774007811e5bbcc568295c8ee5ca24bf490c6b2f783f91eda08f73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578744920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d763e26cedc693dcbce9fefa4cefd3caf3ba3600f2263d33c45f2e4584cb378`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 06:50:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 06:50:11 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:50:11 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 06:51:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 06:51:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:26 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 06:51:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Apr 2024 22:06:26 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:06:26 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Tue, 16 Apr 2024 22:07:46 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:07:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:07:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:07:50 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:07:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:07:50 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:07:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:07:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:07:50 GMT
USER odoo
# Tue, 16 Apr 2024 22:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:07:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc553ed1e447dba5d7cd1531a7067a247647cf58771061d9030c71c8b6d14d`  
		Last Modified: Wed, 10 Apr 2024 06:53:31 GMT  
		Size: 216.9 MB (216903831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505728a268c4b89109c2cb3fd49cd9b1dcb63f30c015647bfc1823b0d6774451`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 2.6 MB (2635212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1bbf349d40bf14f17d8931d7c97e93408ecb08a25175182d63b2592b4c6eac`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4772f044af71618675f2a1692b548682b189ff4a2f6a60eb2058b7a4ef39e9c0`  
		Last Modified: Tue, 16 Apr 2024 22:09:35 GMT  
		Size: 328.7 MB (328668679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d878f99ea0f5b7c5b8203ab38e8b87756ba5ce55e6f2ee6a6c32118024889`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad72bcd74d4e0f959c31c3e1c6c196b764ef809373723f35ad550dce0e8f181a`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8361091f0fe8c959050163ce6c49c5088c1b0161a8188276c10c0d61f59dd270`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6032614ca1e75ec121f315f7ae5394bf65347842d49eab9e6663763fc5d55383`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:b000be7d56bb89a61e279293108dc3d25ebc3f1b1ae333649bcdfe39348771e3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b544ebb4a0072205ed70d0d5459c855d81e85f26e5edf838fb338d1e0687112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:11:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:11:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:11:35 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:11:36 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:15:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 12:16:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:16:14 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 12:16:15 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 12:16:16 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 12:16:17 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 12:18:59 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 12:19:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 12:19:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 12:19:15 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 12:19:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 12:19:17 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 12:19:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 12:19:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 12:19:18 GMT
USER odoo
# Wed, 10 Apr 2024 12:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 12:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e559728a938c6bae80d026fa29f2c38efa24baa26b769f31f8c84966d4e1df`  
		Last Modified: Wed, 10 Apr 2024 12:20:10 GMT  
		Size: 228.6 MB (228600553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203ec44cc6f31bfbafaf9862e879fbf8d13940d76cf12c60f413c3d4f7d2413`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 2.9 MB (2876015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe4e2bda71d3574d3ec461cc470d98dc69f9167871208766805ae0ec7e810f`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 458.4 KB (458444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bb59b6134dc895bace6ac001f367ef7df7681d8bb0e8675308b146b5f5fe0`  
		Last Modified: Wed, 10 Apr 2024 12:20:24 GMT  
		Size: 330.4 MB (330358150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9110cd77d7285e0fad9ff5e2b37e63a937f68ecd61c4aa9e602d19637a4e399`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc41657c316f5977709611ffae9798ea44ec41841054cecdfc9956512967de`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aa5a2c270579376228531eac51095da5ab0374e62d177cd7b9d06916b5e113`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2722d07f6e4f03f8bc5f976b559422fa1f74641856112a4306083f23a3784`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:e8f2c01d3e470ca08e44dd2bd4620426cd941e69ab77ae5a0485d3d226bd4fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f5c87f7e9e38e3774b16737409b8eebf32becf7a3932e7deb73ab5c7a9c2d7ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.1 MB (583139362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b387113654f2d9943644cffcc2534ba7cbacaa01f60e247c340e1712b1592d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:58:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:58:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:58:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:58:42 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:59:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 13:00:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:00:02 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 13:00:02 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Apr 2024 21:53:19 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:53:19 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Tue, 16 Apr 2024 21:54:41 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:54:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:54:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:54:46 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:54:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:54:47 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:54:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:54:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:54:47 GMT
USER odoo
# Tue, 16 Apr 2024 21:54:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:54:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac79b7d43ed31e626ad7d7c9941d7c0a17c43c083711789fb83c11d9110dcfe`  
		Last Modified: Wed, 10 Apr 2024 13:04:36 GMT  
		Size: 219.6 MB (219603194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed26f48190afc427fd1165018baf6a3058a80e56d28e8e3d11097760605dbff`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 2.6 MB (2630065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308ec53827fb3d168639a63a8844a8db71a0d31b340ec755c0fd7b806e82e2f`  
		Last Modified: Wed, 10 Apr 2024 13:04:12 GMT  
		Size: 458.4 KB (458435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8105fc6905658e799a06242c9236fcf25cbcfd5a97283db5aa9ad3e579a004b`  
		Last Modified: Tue, 16 Apr 2024 21:57:57 GMT  
		Size: 329.0 MB (329017469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbeea84723df059756a1d8ca820500cb4d60e448dd2eb03733409180c7c81d2`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15b175ddf367740d5bbe22d944570aef1b4ee9d1ff59d1223af5482c712511e`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd19aa24a7ec97f800dcfc9715050dc4ae392226d6fead9616af636b4951182`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebee86fcf5796cc698b913dfce7a21de579af0a81b3a25930a122ade18714bd`  
		Last Modified: Tue, 16 Apr 2024 21:57:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:49fe23046e774007811e5bbcc568295c8ee5ca24bf490c6b2f783f91eda08f73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578744920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d763e26cedc693dcbce9fefa4cefd3caf3ba3600f2263d33c45f2e4584cb378`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 06:50:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 06:50:11 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:50:11 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 06:51:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 06:51:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:26 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 06:51:26 GMT
ENV ODOO_VERSION=16.0
# Tue, 16 Apr 2024 22:06:26 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:06:26 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Tue, 16 Apr 2024 22:07:46 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:07:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:07:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:07:50 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:07:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:07:50 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:07:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:07:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:07:50 GMT
USER odoo
# Tue, 16 Apr 2024 22:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:07:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc553ed1e447dba5d7cd1531a7067a247647cf58771061d9030c71c8b6d14d`  
		Last Modified: Wed, 10 Apr 2024 06:53:31 GMT  
		Size: 216.9 MB (216903831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505728a268c4b89109c2cb3fd49cd9b1dcb63f30c015647bfc1823b0d6774451`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 2.6 MB (2635212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1bbf349d40bf14f17d8931d7c97e93408ecb08a25175182d63b2592b4c6eac`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4772f044af71618675f2a1692b548682b189ff4a2f6a60eb2058b7a4ef39e9c0`  
		Last Modified: Tue, 16 Apr 2024 22:09:35 GMT  
		Size: 328.7 MB (328668679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d878f99ea0f5b7c5b8203ab38e8b87756ba5ce55e6f2ee6a6c32118024889`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad72bcd74d4e0f959c31c3e1c6c196b764ef809373723f35ad550dce0e8f181a`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8361091f0fe8c959050163ce6c49c5088c1b0161a8188276c10c0d61f59dd270`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6032614ca1e75ec121f315f7ae5394bf65347842d49eab9e6663763fc5d55383`  
		Last Modified: Tue, 16 Apr 2024 22:09:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b000be7d56bb89a61e279293108dc3d25ebc3f1b1ae333649bcdfe39348771e3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b544ebb4a0072205ed70d0d5459c855d81e85f26e5edf838fb338d1e0687112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:11:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:11:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:11:35 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:11:36 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:15:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 12:16:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:16:14 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 12:16:15 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 12:16:16 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 12:16:17 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 12:18:59 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 12:19:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 12:19:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 12:19:15 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 12:19:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 12:19:17 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 12:19:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 12:19:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 12:19:18 GMT
USER odoo
# Wed, 10 Apr 2024 12:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 12:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e559728a938c6bae80d026fa29f2c38efa24baa26b769f31f8c84966d4e1df`  
		Last Modified: Wed, 10 Apr 2024 12:20:10 GMT  
		Size: 228.6 MB (228600553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203ec44cc6f31bfbafaf9862e879fbf8d13940d76cf12c60f413c3d4f7d2413`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 2.9 MB (2876015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe4e2bda71d3574d3ec461cc470d98dc69f9167871208766805ae0ec7e810f`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 458.4 KB (458444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bb59b6134dc895bace6ac001f367ef7df7681d8bb0e8675308b146b5f5fe0`  
		Last Modified: Wed, 10 Apr 2024 12:20:24 GMT  
		Size: 330.4 MB (330358150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9110cd77d7285e0fad9ff5e2b37e63a937f68ecd61c4aa9e602d19637a4e399`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc41657c316f5977709611ffae9798ea44ec41841054cecdfc9956512967de`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aa5a2c270579376228531eac51095da5ab0374e62d177cd7b9d06916b5e113`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2722d07f6e4f03f8bc5f976b559422fa1f74641856112a4306083f23a3784`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:fe17045b0ef6f5dc0f516b8749fa1f83f21127c88bfc244ab9f811eead47b874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:fe0791861eb75ceb45c7e68b3c239c7f960e6ecf3119f33320164b8f8ac4e7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.9 MB (601936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd358de70883c9f901b836fba7e30c0968fe7dc9b6f69c3a78f71b8a11e5f00b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:22:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 05:22:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 05:22:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:22:36 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 05:24:47 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 05:25:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:25:01 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 05:25:01 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 21:53:02 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:53:08 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:53:08 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:53:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:53:08 GMT
USER odoo
# Tue, 16 Apr 2024 21:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b654cdca6f84d6c42697064da4d9c97d2f2ddeec98527c983a27266adb432a`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 233.7 MB (233722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d1b850436c5dde7a24152062ed67a4c7d61249c361e63f2b17734922aaa10`  
		Last Modified: Tue, 16 Apr 2024 05:27:30 GMT  
		Size: 2.5 MB (2530416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac1b49930b0907c0df875817503ccf8aafd0e1a3d61414b4f938eca69179a`  
		Last Modified: Tue, 16 Apr 2024 05:27:29 GMT  
		Size: 459.4 KB (459352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402b412e6d22febacf7efb25f61e5d1deaa74105552d2d2d7ae27d4b05de77e6`  
		Last Modified: Tue, 16 Apr 2024 21:57:08 GMT  
		Size: 334.8 MB (334781962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ff767f8568c474ad33f147bb043af427930e6dde7135f294c3cae498e6487`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db1829567ac26e8e72330a0813fece3e091f1199941032967c83ae7d2bc1c38`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba18450f78d3869005992ea8f6255f848a6010301bc2f776c53df9fa56cdfd`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230458b6a0f97567368180519d0f8477065a176c14e972cabd6dce941570c85`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1afb61a2f2ea4969f7c1c4b94af05340c8e771b7a0582886da3e2466073882f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6603c5e3616c65462431fd2045863d051a7385613bd636193f35f685273666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:06:10 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:06:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:06:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:06:18 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:06:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:06:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:06:18 GMT
USER odoo
# Tue, 16 Apr 2024 22:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:06:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867fb137574bcce6eeb7b05beac1823d426fbafdb7533b87d7bc1320991311`  
		Last Modified: Tue, 16 Apr 2024 22:08:46 GMT  
		Size: 334.4 MB (334394960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab792be17c768d7091e22a1b08648376e901ad355178de758c34a5a28604fe`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046ac664962865859052eef31c139a4ea7821c75b735b1335c6e9f4c4c79131`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4a1ea72a4d6c32f31b265fbf3af71ae15dae3a2091e83acb278ea6dabadd0`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa77e53029620532c126dd38559036a440cf1050b88c32cbffc12beb42e448ee`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:b3242b265c88b2bcac7b7dc8568b12be7e5d5dfd2cffe0714f3efa22a4d9fb0a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618470261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dc0e91364c2d2f8197b1631e461a6291436820f54d2a217d81758a58951fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 02:27:44 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 02:27:45 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 02:32:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 02:33:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 02:33:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 02:33:21 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 02:33:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 02:33:23 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 02:33:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 02:33:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 02:33:30 GMT
USER odoo
# Tue, 16 Apr 2024 02:33:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 02:33:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac580667a28410cc8979c586c5faffe195d6894c3092f52cb35be46dd5c5c54`  
		Last Modified: Tue, 16 Apr 2024 02:34:44 GMT  
		Size: 336.3 MB (336314723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0871c91966eee2fc05bfe405aa20da9f2eaac7b331b38cae48480c5108ec1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b7e7abc278ed0cd27c5f8030fe2f1942d09b31970cc644d5a191e383b59d1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d04db108cd3503bc3080fe13bbef9199bd448fb19b952d57e8f2a39e57db10`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7a000910544187b0db486222014aa892301fda5291cc5468105a17cc23d155`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:fe17045b0ef6f5dc0f516b8749fa1f83f21127c88bfc244ab9f811eead47b874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:fe0791861eb75ceb45c7e68b3c239c7f960e6ecf3119f33320164b8f8ac4e7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.9 MB (601936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd358de70883c9f901b836fba7e30c0968fe7dc9b6f69c3a78f71b8a11e5f00b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:22:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 05:22:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 05:22:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:22:36 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 05:24:47 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 05:25:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:25:01 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 05:25:01 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 21:53:02 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:53:08 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:53:08 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:53:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:53:08 GMT
USER odoo
# Tue, 16 Apr 2024 21:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b654cdca6f84d6c42697064da4d9c97d2f2ddeec98527c983a27266adb432a`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 233.7 MB (233722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d1b850436c5dde7a24152062ed67a4c7d61249c361e63f2b17734922aaa10`  
		Last Modified: Tue, 16 Apr 2024 05:27:30 GMT  
		Size: 2.5 MB (2530416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac1b49930b0907c0df875817503ccf8aafd0e1a3d61414b4f938eca69179a`  
		Last Modified: Tue, 16 Apr 2024 05:27:29 GMT  
		Size: 459.4 KB (459352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402b412e6d22febacf7efb25f61e5d1deaa74105552d2d2d7ae27d4b05de77e6`  
		Last Modified: Tue, 16 Apr 2024 21:57:08 GMT  
		Size: 334.8 MB (334781962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ff767f8568c474ad33f147bb043af427930e6dde7135f294c3cae498e6487`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db1829567ac26e8e72330a0813fece3e091f1199941032967c83ae7d2bc1c38`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba18450f78d3869005992ea8f6255f848a6010301bc2f776c53df9fa56cdfd`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230458b6a0f97567368180519d0f8477065a176c14e972cabd6dce941570c85`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1afb61a2f2ea4969f7c1c4b94af05340c8e771b7a0582886da3e2466073882f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6603c5e3616c65462431fd2045863d051a7385613bd636193f35f685273666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:06:10 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:06:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:06:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:06:18 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:06:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:06:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:06:18 GMT
USER odoo
# Tue, 16 Apr 2024 22:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:06:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867fb137574bcce6eeb7b05beac1823d426fbafdb7533b87d7bc1320991311`  
		Last Modified: Tue, 16 Apr 2024 22:08:46 GMT  
		Size: 334.4 MB (334394960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab792be17c768d7091e22a1b08648376e901ad355178de758c34a5a28604fe`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046ac664962865859052eef31c139a4ea7821c75b735b1335c6e9f4c4c79131`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4a1ea72a4d6c32f31b265fbf3af71ae15dae3a2091e83acb278ea6dabadd0`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa77e53029620532c126dd38559036a440cf1050b88c32cbffc12beb42e448ee`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b3242b265c88b2bcac7b7dc8568b12be7e5d5dfd2cffe0714f3efa22a4d9fb0a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618470261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dc0e91364c2d2f8197b1631e461a6291436820f54d2a217d81758a58951fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 02:27:44 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 02:27:45 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 02:32:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 02:33:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 02:33:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 02:33:21 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 02:33:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 02:33:23 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 02:33:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 02:33:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 02:33:30 GMT
USER odoo
# Tue, 16 Apr 2024 02:33:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 02:33:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac580667a28410cc8979c586c5faffe195d6894c3092f52cb35be46dd5c5c54`  
		Last Modified: Tue, 16 Apr 2024 02:34:44 GMT  
		Size: 336.3 MB (336314723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0871c91966eee2fc05bfe405aa20da9f2eaac7b331b38cae48480c5108ec1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b7e7abc278ed0cd27c5f8030fe2f1942d09b31970cc644d5a191e383b59d1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d04db108cd3503bc3080fe13bbef9199bd448fb19b952d57e8f2a39e57db10`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7a000910544187b0db486222014aa892301fda5291cc5468105a17cc23d155`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:fe17045b0ef6f5dc0f516b8749fa1f83f21127c88bfc244ab9f811eead47b874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:fe0791861eb75ceb45c7e68b3c239c7f960e6ecf3119f33320164b8f8ac4e7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.9 MB (601936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd358de70883c9f901b836fba7e30c0968fe7dc9b6f69c3a78f71b8a11e5f00b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:22:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 05:22:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 05:22:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:22:36 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 05:24:47 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 05:25:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:25:01 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 05:25:01 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 21:53:02 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:53:08 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:53:08 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:53:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:53:08 GMT
USER odoo
# Tue, 16 Apr 2024 21:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b654cdca6f84d6c42697064da4d9c97d2f2ddeec98527c983a27266adb432a`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 233.7 MB (233722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d1b850436c5dde7a24152062ed67a4c7d61249c361e63f2b17734922aaa10`  
		Last Modified: Tue, 16 Apr 2024 05:27:30 GMT  
		Size: 2.5 MB (2530416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac1b49930b0907c0df875817503ccf8aafd0e1a3d61414b4f938eca69179a`  
		Last Modified: Tue, 16 Apr 2024 05:27:29 GMT  
		Size: 459.4 KB (459352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402b412e6d22febacf7efb25f61e5d1deaa74105552d2d2d7ae27d4b05de77e6`  
		Last Modified: Tue, 16 Apr 2024 21:57:08 GMT  
		Size: 334.8 MB (334781962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ff767f8568c474ad33f147bb043af427930e6dde7135f294c3cae498e6487`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db1829567ac26e8e72330a0813fece3e091f1199941032967c83ae7d2bc1c38`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba18450f78d3869005992ea8f6255f848a6010301bc2f776c53df9fa56cdfd`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230458b6a0f97567368180519d0f8477065a176c14e972cabd6dce941570c85`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1afb61a2f2ea4969f7c1c4b94af05340c8e771b7a0582886da3e2466073882f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6603c5e3616c65462431fd2045863d051a7385613bd636193f35f685273666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:06:10 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:06:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:06:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:06:18 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:06:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:06:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:06:18 GMT
USER odoo
# Tue, 16 Apr 2024 22:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:06:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867fb137574bcce6eeb7b05beac1823d426fbafdb7533b87d7bc1320991311`  
		Last Modified: Tue, 16 Apr 2024 22:08:46 GMT  
		Size: 334.4 MB (334394960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab792be17c768d7091e22a1b08648376e901ad355178de758c34a5a28604fe`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046ac664962865859052eef31c139a4ea7821c75b735b1335c6e9f4c4c79131`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4a1ea72a4d6c32f31b265fbf3af71ae15dae3a2091e83acb278ea6dabadd0`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa77e53029620532c126dd38559036a440cf1050b88c32cbffc12beb42e448ee`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:b3242b265c88b2bcac7b7dc8568b12be7e5d5dfd2cffe0714f3efa22a4d9fb0a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618470261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dc0e91364c2d2f8197b1631e461a6291436820f54d2a217d81758a58951fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 02:27:44 GMT
ARG ODOO_RELEASE=20240405
# Tue, 16 Apr 2024 02:27:45 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Tue, 16 Apr 2024 02:32:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 02:33:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 02:33:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 02:33:21 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 02:33:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 02:33:23 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 02:33:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 02:33:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 02:33:30 GMT
USER odoo
# Tue, 16 Apr 2024 02:33:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 02:33:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac580667a28410cc8979c586c5faffe195d6894c3092f52cb35be46dd5c5c54`  
		Last Modified: Tue, 16 Apr 2024 02:34:44 GMT  
		Size: 336.3 MB (336314723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb0871c91966eee2fc05bfe405aa20da9f2eaac7b331b38cae48480c5108ec1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15b7e7abc278ed0cd27c5f8030fe2f1942d09b31970cc644d5a191e383b59d1`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d04db108cd3503bc3080fe13bbef9199bd448fb19b952d57e8f2a39e57db10`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7a000910544187b0db486222014aa892301fda5291cc5468105a17cc23d155`  
		Last Modified: Tue, 16 Apr 2024 02:33:55 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
