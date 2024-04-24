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
$ docker pull odoo@sha256:5861361f58ec7e6882ce99e9e47386588b42b1623bdb2dfec6925aec41d6b349
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
$ docker pull odoo@sha256:8c7bb204c403953d06a319d296dd745bbc2bf383fa66b8846a15e44595447e9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578754105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37eaac62a52a5d1206328db426a9ae0bbb0a5c7172904cc380aa9a2080d838fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 04:46:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 04:46:24 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 04:46:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 04:46:24 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 04:46:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 04:46:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 04:46:24 GMT
USER odoo
# Wed, 24 Apr 2024 04:46:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:46:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4073a3095218233668eba607b98269dee24e5708986a15a4578d4c0acf3f399`  
		Last Modified: Wed, 24 Apr 2024 04:47:11 GMT  
		Size: 328.7 MB (328666473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3248f2359c1295611f5b21b00cce27337e8bc1cf9a525cbf8f71b6cd7596a367`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc71ceeba51f1fa58b766c0b6809582b6031cd578cf0b01cbe5863007d23d9c5`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840c86734b8dfeb2d3c7e4bc8d630b9c1055715b61d7d38a3732863e2ca1285`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37dafa948f61840b414363a4ea8caf26ee532fd9035340ae1b99e2dfacc4db`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:837e940bdce4a7b00f544aa877f1a16beb67e73a12c0c0d12dc3ef71f2fa6ef3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597695567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f21a028cc88fb439f4a66c9389a8518acc0fccbe3bef5343cac42939f58173`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 05:54:44 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 05:54:45 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 05:57:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 05:57:30 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 05:57:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 05:57:31 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 05:57:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 05:57:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 05:57:33 GMT
USER odoo
# Wed, 24 Apr 2024 05:57:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 05:57:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0de980b91e84a4461dde7734420d53311f24d6aaf8c89549c0f373bf9cee55`  
		Last Modified: Wed, 24 Apr 2024 05:58:35 GMT  
		Size: 330.4 MB (330443848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c213a9417b8b46f03d0be61294c06f5d6353b161c13854dd2e42a937cf18ed86`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc02886836a694ff5dad283cc31b5da6fd20a05d2c3907e2882e01eded51bcf4`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0905b66303a77077715efc929f584f536be3cc7c35d36964eafc01f4b5515d`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e11db646b83c30707b2c35571719516f9d274e6f871b8a4fc46a73ecb5897bc`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:5861361f58ec7e6882ce99e9e47386588b42b1623bdb2dfec6925aec41d6b349
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
$ docker pull odoo@sha256:8c7bb204c403953d06a319d296dd745bbc2bf383fa66b8846a15e44595447e9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578754105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37eaac62a52a5d1206328db426a9ae0bbb0a5c7172904cc380aa9a2080d838fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 04:46:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 04:46:24 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 04:46:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 04:46:24 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 04:46:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 04:46:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 04:46:24 GMT
USER odoo
# Wed, 24 Apr 2024 04:46:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:46:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4073a3095218233668eba607b98269dee24e5708986a15a4578d4c0acf3f399`  
		Last Modified: Wed, 24 Apr 2024 04:47:11 GMT  
		Size: 328.7 MB (328666473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3248f2359c1295611f5b21b00cce27337e8bc1cf9a525cbf8f71b6cd7596a367`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc71ceeba51f1fa58b766c0b6809582b6031cd578cf0b01cbe5863007d23d9c5`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840c86734b8dfeb2d3c7e4bc8d630b9c1055715b61d7d38a3732863e2ca1285`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37dafa948f61840b414363a4ea8caf26ee532fd9035340ae1b99e2dfacc4db`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:837e940bdce4a7b00f544aa877f1a16beb67e73a12c0c0d12dc3ef71f2fa6ef3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597695567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f21a028cc88fb439f4a66c9389a8518acc0fccbe3bef5343cac42939f58173`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 05:54:44 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 05:54:45 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 05:57:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 05:57:30 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 05:57:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 05:57:31 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 05:57:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 05:57:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 05:57:33 GMT
USER odoo
# Wed, 24 Apr 2024 05:57:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 05:57:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0de980b91e84a4461dde7734420d53311f24d6aaf8c89549c0f373bf9cee55`  
		Last Modified: Wed, 24 Apr 2024 05:58:35 GMT  
		Size: 330.4 MB (330443848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c213a9417b8b46f03d0be61294c06f5d6353b161c13854dd2e42a937cf18ed86`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc02886836a694ff5dad283cc31b5da6fd20a05d2c3907e2882e01eded51bcf4`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0905b66303a77077715efc929f584f536be3cc7c35d36964eafc01f4b5515d`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e11db646b83c30707b2c35571719516f9d274e6f871b8a4fc46a73ecb5897bc`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:874573f6ea07fb2b2abcf188c6562f0d0a2d4ae3ff5dc35c9e4ec60a97b46a45
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
$ docker pull odoo@sha256:5a4581819812482c0b47684711acd4738921e450691c1ab1504a23cdffea9ee4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409c8fb6e654df10a40b348cef12dcfba4d5acf0a0e36d444c1a1ea275fb35ec`
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
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:20:21 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:20:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:20:36 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:20:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:20:37 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:20:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:20:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:20:39 GMT
USER odoo
# Tue, 16 Apr 2024 22:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:20:40 GMT
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
	-	`sha256:472bba33d86762aeeb53906f1904a3e5c6bf0de11239c11802419f3ad72c1369`  
		Last Modified: Tue, 16 Apr 2024 22:24:58 GMT  
		Size: 336.5 MB (336532414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6c78c91f4cb9a5d56d431bb0bd8d491f83631e63e39ce583a990683626015d`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e7285a0d23794ef8f5ad1731a14ab1d5c1ff039209a5a2b9645740047f90`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b5c1a609c962eb44957b4e4e3c18b01edebc3376121556fbdd16508a1f101`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7b5ef5c8c02170ef3c880ab565ad8b03f28e5d753f1aefd72a9d9f83b98a9`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:874573f6ea07fb2b2abcf188c6562f0d0a2d4ae3ff5dc35c9e4ec60a97b46a45
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
$ docker pull odoo@sha256:5a4581819812482c0b47684711acd4738921e450691c1ab1504a23cdffea9ee4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409c8fb6e654df10a40b348cef12dcfba4d5acf0a0e36d444c1a1ea275fb35ec`
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
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:20:21 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:20:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:20:36 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:20:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:20:37 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:20:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:20:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:20:39 GMT
USER odoo
# Tue, 16 Apr 2024 22:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:20:40 GMT
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
	-	`sha256:472bba33d86762aeeb53906f1904a3e5c6bf0de11239c11802419f3ad72c1369`  
		Last Modified: Tue, 16 Apr 2024 22:24:58 GMT  
		Size: 336.5 MB (336532414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6c78c91f4cb9a5d56d431bb0bd8d491f83631e63e39ce583a990683626015d`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e7285a0d23794ef8f5ad1731a14ab1d5c1ff039209a5a2b9645740047f90`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b5c1a609c962eb44957b4e4e3c18b01edebc3376121556fbdd16508a1f101`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7b5ef5c8c02170ef3c880ab565ad8b03f28e5d753f1aefd72a9d9f83b98a9`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:874573f6ea07fb2b2abcf188c6562f0d0a2d4ae3ff5dc35c9e4ec60a97b46a45
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
$ docker pull odoo@sha256:5a4581819812482c0b47684711acd4738921e450691c1ab1504a23cdffea9ee4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409c8fb6e654df10a40b348cef12dcfba4d5acf0a0e36d444c1a1ea275fb35ec`
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
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:20:21 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:20:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:20:36 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:20:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:20:37 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:20:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:20:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:20:39 GMT
USER odoo
# Tue, 16 Apr 2024 22:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:20:40 GMT
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
	-	`sha256:472bba33d86762aeeb53906f1904a3e5c6bf0de11239c11802419f3ad72c1369`  
		Last Modified: Tue, 16 Apr 2024 22:24:58 GMT  
		Size: 336.5 MB (336532414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6c78c91f4cb9a5d56d431bb0bd8d491f83631e63e39ce583a990683626015d`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e7285a0d23794ef8f5ad1731a14ab1d5c1ff039209a5a2b9645740047f90`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b5c1a609c962eb44957b4e4e3c18b01edebc3376121556fbdd16508a1f101`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7b5ef5c8c02170ef3c880ab565ad8b03f28e5d753f1aefd72a9d9f83b98a9`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
