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
$ docker pull odoo@sha256:9f29412085c9a480e27374e67bcfbe7948d56b4c24d0dbc13a1ce438fa6bec63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:4c3151319999ceb9675e72909f1005ef33f37999227c15165f2615d327426bbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563948204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05045df6f599e3a30f11228e397e715519638f084fd47d6c835adce7adfa153`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:08:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:08:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:08:17 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:08:17 GMT
ENV ODOO_VERSION=15.0
# Tue, 12 Mar 2024 18:01:50 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:01:50 GMT
ARG ODOO_SHA=8508bde605e961c6c823809cc162437424a01e76
# Tue, 12 Mar 2024 18:03:01 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=8508bde605e961c6c823809cc162437424a01e76
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:03:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:03:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:03:06 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=8508bde605e961c6c823809cc162437424a01e76
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:03:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:03:06 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:03:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:03:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:03:06 GMT
USER odoo
# Tue, 12 Mar 2024 18:03:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:03:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f755211239ff95827bdf02a4263220ef29f30514bfb45e9719405f61b7eb1fe`  
		Last Modified: Tue, 12 Mar 2024 10:11:05 GMT  
		Size: 220.3 MB (220291492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e350755bf81273bed12fdf2a9b0164c28be00db54322cbca54eb5c183aa61798`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 2.6 MB (2625910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465eacd304d72395092a950bf1096c7504f0a76ef0820999e0bda4a3e4068ea`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 462.5 KB (462463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf12c94e2f24d65503e435a052c9652041591d35d14209684112fbe959e7705e`  
		Last Modified: Tue, 12 Mar 2024 18:05:30 GMT  
		Size: 309.1 MB (309143385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11518701df94d31e15dbffe304e0c30edf80c51affc7f09fbbd2cb2b0d04b893`  
		Last Modified: Tue, 12 Mar 2024 18:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b8dd13c0a340286f48d2c32ee9db1f5378ec01244773325c96dd10331db6d4`  
		Last Modified: Tue, 12 Mar 2024 18:04:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a0f8fb7168015ce640aa2ea057f819c9ab1090b361059d0eb65dcfeb2b7bb6`  
		Last Modified: Tue, 12 Mar 2024 18:04:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074926563ef81cd636d6b705038946556385c8af3b2a5d7be7ed394231261405`  
		Last Modified: Tue, 12 Mar 2024 18:04:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:9f29412085c9a480e27374e67bcfbe7948d56b4c24d0dbc13a1ce438fa6bec63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:4c3151319999ceb9675e72909f1005ef33f37999227c15165f2615d327426bbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563948204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05045df6f599e3a30f11228e397e715519638f084fd47d6c835adce7adfa153`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:08:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:08:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:08:17 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:08:17 GMT
ENV ODOO_VERSION=15.0
# Tue, 12 Mar 2024 18:01:50 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:01:50 GMT
ARG ODOO_SHA=8508bde605e961c6c823809cc162437424a01e76
# Tue, 12 Mar 2024 18:03:01 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=8508bde605e961c6c823809cc162437424a01e76
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:03:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:03:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:03:06 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=8508bde605e961c6c823809cc162437424a01e76
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:03:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:03:06 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:03:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:03:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:03:06 GMT
USER odoo
# Tue, 12 Mar 2024 18:03:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:03:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f755211239ff95827bdf02a4263220ef29f30514bfb45e9719405f61b7eb1fe`  
		Last Modified: Tue, 12 Mar 2024 10:11:05 GMT  
		Size: 220.3 MB (220291492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e350755bf81273bed12fdf2a9b0164c28be00db54322cbca54eb5c183aa61798`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 2.6 MB (2625910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465eacd304d72395092a950bf1096c7504f0a76ef0820999e0bda4a3e4068ea`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 462.5 KB (462463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf12c94e2f24d65503e435a052c9652041591d35d14209684112fbe959e7705e`  
		Last Modified: Tue, 12 Mar 2024 18:05:30 GMT  
		Size: 309.1 MB (309143385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11518701df94d31e15dbffe304e0c30edf80c51affc7f09fbbd2cb2b0d04b893`  
		Last Modified: Tue, 12 Mar 2024 18:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b8dd13c0a340286f48d2c32ee9db1f5378ec01244773325c96dd10331db6d4`  
		Last Modified: Tue, 12 Mar 2024 18:04:56 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a0f8fb7168015ce640aa2ea057f819c9ab1090b361059d0eb65dcfeb2b7bb6`  
		Last Modified: Tue, 12 Mar 2024 18:04:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074926563ef81cd636d6b705038946556385c8af3b2a5d7be7ed394231261405`  
		Last Modified: Tue, 12 Mar 2024 18:04:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:425dc09251d1193bc3e7f181a0db0679bbd5fca4e04d4570ec147e2fbe336543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:7834e6680591a68d99267ec31e610f4bb61e60aac6aab8c82a8bfe8529d9f49f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.9 MB (582856975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377d32757db1bd0feba15d07843a560b9c8d9dde6bceab0dd9af543ed96315e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:04:23 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 10:05:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:05:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:05:44 GMT
ENV ODOO_VERSION=16.0
# Tue, 12 Mar 2024 18:00:11 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:00:11 GMT
ARG ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
# Tue, 12 Mar 2024 18:01:33 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:01:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:01:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:01:37 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:01:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:01:37 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:01:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:01:38 GMT
USER odoo
# Tue, 12 Mar 2024 18:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6792aa9ce6832f860c6e1be9f969760839af537e4898318aa4f6bfb1c028b`  
		Last Modified: Tue, 12 Mar 2024 10:10:15 GMT  
		Size: 219.6 MB (219603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2315d87d3b1baf540e35d3ecccceacc3315ff5069bf3f9bfa9cfb289aeba9`  
		Last Modified: Tue, 12 Mar 2024 10:09:51 GMT  
		Size: 2.6 MB (2630018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dda5b3fd48c7f6681e64745ee86cffaf18fee97aeba54f00d6ee06b5ba526`  
		Last Modified: Tue, 12 Mar 2024 10:09:50 GMT  
		Size: 462.5 KB (462467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63224d7e2d6b20960764701f6d84e65b13e5c57134f2d69a48e03e19fbc5be5`  
		Last Modified: Tue, 12 Mar 2024 18:04:48 GMT  
		Size: 328.7 MB (328736524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2f62c5352f90351d828c2305a7b615c5650f46dc79c0c9d9440c9f86802e9`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13189d0aae84ebc89af19db74937225e97b562d2248c84c5a2f0a0874a498315`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb73234e5d972641392edef9d99144a991b1e5bc1359832e40eaedcfa2b62d7`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50df693d43818f4b21b0a52dbc90c8b723ec48449cc83c2cca54494ad690d`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c65a8bfd76725256436bd13069000a441ca2d98d40a3d137e30bad23372b2f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.5 MB (578453523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eee093cd847912641db0e3c95254cbb8905c28d5585f1f200a596b51c2abf76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:09:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 07:09:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 07:09:25 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 07:09:25 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 07:10:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 07:10:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:10:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 07:10:44 GMT
ENV ODOO_VERSION=16.0
# Tue, 12 Mar 2024 17:19:12 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:19:12 GMT
ARG ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
# Tue, 12 Mar 2024 17:20:27 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 17:20:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 17:20:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 17:20:36 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 17:20:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 17:20:36 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 17:20:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 17:20:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 17:20:36 GMT
USER odoo
# Tue, 12 Mar 2024 17:20:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:20:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550bf50c1c5bb03f8258887877b215242f2faaca6547d16135a1e15bf67c37da`  
		Last Modified: Tue, 12 Mar 2024 07:12:44 GMT  
		Size: 216.9 MB (216903519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8867a1af5f453861e2f8e8ef6fff1ed5ff0485d4380aeb1760a3ee61ddfa`  
		Last Modified: Tue, 12 Mar 2024 07:12:27 GMT  
		Size: 2.6 MB (2635199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd44908863b6493f4ab93ee84278d19411f9365e54dc4f97fd93f6e872c6df`  
		Last Modified: Tue, 12 Mar 2024 07:12:26 GMT  
		Size: 462.5 KB (462480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b1564f52f8d1cf84b98252a5d1ed5c6643cfb5e48755059ed282fc72a9a871`  
		Last Modified: Tue, 12 Mar 2024 17:22:12 GMT  
		Size: 328.4 MB (328378751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5834d2a41439f2dd5bc2c2575a59358f736c14e3b564dbab514e36c59b4eb8ed`  
		Last Modified: Tue, 12 Mar 2024 17:21:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3861fc2855e37cc54e8e8bce74307ba49ac08e8137d28853d4704e47380f36f`  
		Last Modified: Tue, 12 Mar 2024 17:21:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db2124f0d03f53bd78b4291f4d68b8c19f8453d870e65a2cd3c6cb73e941b06`  
		Last Modified: Tue, 12 Mar 2024 17:21:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b075bf6f469da77c01f544693f4352277d367a43c2fa0e21c59c51b7762f92a`  
		Last Modified: Tue, 12 Mar 2024 17:21:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:055fd43bb9eb79eed7a0bd4bfec6cded5a3e8625916d3225c424ac743aaf91a9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597418232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c764f1ae8e6cc2519f67a088e9ba4706ea7dac13158992f3f097ce08ac269e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:38:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 02:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 02:38:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 02:38:47 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 02:45:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 02:46:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:46:11 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 02:46:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 12 Mar 2024 18:45:35 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:45:35 GMT
ARG ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
# Tue, 12 Mar 2024 18:49:49 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:50:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:50:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:50:21 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:50:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:50:23 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:50:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:50:24 GMT
USER odoo
# Tue, 12 Mar 2024 18:50:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:50:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a32c556380680a1795889bca44d0f0a883f42b50860b84f480546468a7a03`  
		Last Modified: Tue, 12 Mar 2024 02:54:00 GMT  
		Size: 228.6 MB (228600421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c60f6a8d0d4afdc1ff134aae19e82a3c10cbeb5816bcab9c7cdac58ff961e6`  
		Last Modified: Tue, 12 Mar 2024 02:53:31 GMT  
		Size: 2.9 MB (2876315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec00e5fbd9079a262ec1e1c1ae57ae88ae27282c49b89f9952917db58b01f6b`  
		Last Modified: Tue, 12 Mar 2024 02:53:30 GMT  
		Size: 462.5 KB (462469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97614c4983d81c7de16a9e98fd3d9d48346e0f7d298a4f552aa8bc88a0792956`  
		Last Modified: Tue, 12 Mar 2024 18:52:20 GMT  
		Size: 330.2 MB (330178553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f500882fc16908f317fbd339275b8276f63aa3409a74018e84ea07d2a3cffe6e`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a594a0c7b642975246b42bca03ad8645cf593e242b5d0f9a249bf3a90fe9c49`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7f7a1aa5bb4b7f6f7d9dbeed4d2c9d09327b7344266f89247ef05ab3eb1557`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8bb7126bd954b54132db0903f9c277f6cf8288543b1bd7dff50f9a2518eb0`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:425dc09251d1193bc3e7f181a0db0679bbd5fca4e04d4570ec147e2fbe336543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:7834e6680591a68d99267ec31e610f4bb61e60aac6aab8c82a8bfe8529d9f49f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.9 MB (582856975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377d32757db1bd0feba15d07843a560b9c8d9dde6bceab0dd9af543ed96315e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:04:23 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 10:05:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:05:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:05:44 GMT
ENV ODOO_VERSION=16.0
# Tue, 12 Mar 2024 18:00:11 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:00:11 GMT
ARG ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
# Tue, 12 Mar 2024 18:01:33 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:01:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:01:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:01:37 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:01:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:01:37 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:01:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:01:38 GMT
USER odoo
# Tue, 12 Mar 2024 18:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6792aa9ce6832f860c6e1be9f969760839af537e4898318aa4f6bfb1c028b`  
		Last Modified: Tue, 12 Mar 2024 10:10:15 GMT  
		Size: 219.6 MB (219603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2315d87d3b1baf540e35d3ecccceacc3315ff5069bf3f9bfa9cfb289aeba9`  
		Last Modified: Tue, 12 Mar 2024 10:09:51 GMT  
		Size: 2.6 MB (2630018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dda5b3fd48c7f6681e64745ee86cffaf18fee97aeba54f00d6ee06b5ba526`  
		Last Modified: Tue, 12 Mar 2024 10:09:50 GMT  
		Size: 462.5 KB (462467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63224d7e2d6b20960764701f6d84e65b13e5c57134f2d69a48e03e19fbc5be5`  
		Last Modified: Tue, 12 Mar 2024 18:04:48 GMT  
		Size: 328.7 MB (328736524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2f62c5352f90351d828c2305a7b615c5650f46dc79c0c9d9440c9f86802e9`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13189d0aae84ebc89af19db74937225e97b562d2248c84c5a2f0a0874a498315`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb73234e5d972641392edef9d99144a991b1e5bc1359832e40eaedcfa2b62d7`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f50df693d43818f4b21b0a52dbc90c8b723ec48449cc83c2cca54494ad690d`  
		Last Modified: Tue, 12 Mar 2024 18:04:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c65a8bfd76725256436bd13069000a441ca2d98d40a3d137e30bad23372b2f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.5 MB (578453523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eee093cd847912641db0e3c95254cbb8905c28d5585f1f200a596b51c2abf76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:09:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 07:09:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 07:09:25 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 07:09:25 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 07:10:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 07:10:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:10:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 07:10:44 GMT
ENV ODOO_VERSION=16.0
# Tue, 12 Mar 2024 17:19:12 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:19:12 GMT
ARG ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
# Tue, 12 Mar 2024 17:20:27 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 17:20:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 17:20:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 17:20:36 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 17:20:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 17:20:36 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 17:20:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 17:20:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 17:20:36 GMT
USER odoo
# Tue, 12 Mar 2024 17:20:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:20:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550bf50c1c5bb03f8258887877b215242f2faaca6547d16135a1e15bf67c37da`  
		Last Modified: Tue, 12 Mar 2024 07:12:44 GMT  
		Size: 216.9 MB (216903519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8867a1af5f453861e2f8e8ef6fff1ed5ff0485d4380aeb1760a3ee61ddfa`  
		Last Modified: Tue, 12 Mar 2024 07:12:27 GMT  
		Size: 2.6 MB (2635199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd44908863b6493f4ab93ee84278d19411f9365e54dc4f97fd93f6e872c6df`  
		Last Modified: Tue, 12 Mar 2024 07:12:26 GMT  
		Size: 462.5 KB (462480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b1564f52f8d1cf84b98252a5d1ed5c6643cfb5e48755059ed282fc72a9a871`  
		Last Modified: Tue, 12 Mar 2024 17:22:12 GMT  
		Size: 328.4 MB (328378751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5834d2a41439f2dd5bc2c2575a59358f736c14e3b564dbab514e36c59b4eb8ed`  
		Last Modified: Tue, 12 Mar 2024 17:21:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3861fc2855e37cc54e8e8bce74307ba49ac08e8137d28853d4704e47380f36f`  
		Last Modified: Tue, 12 Mar 2024 17:21:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db2124f0d03f53bd78b4291f4d68b8c19f8453d870e65a2cd3c6cb73e941b06`  
		Last Modified: Tue, 12 Mar 2024 17:21:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b075bf6f469da77c01f544693f4352277d367a43c2fa0e21c59c51b7762f92a`  
		Last Modified: Tue, 12 Mar 2024 17:21:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:055fd43bb9eb79eed7a0bd4bfec6cded5a3e8625916d3225c424ac743aaf91a9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597418232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c764f1ae8e6cc2519f67a088e9ba4706ea7dac13158992f3f097ce08ac269e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:38:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 02:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 02:38:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 02:38:47 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 02:45:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 02:46:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:46:11 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 02:46:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 12 Mar 2024 18:45:35 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:45:35 GMT
ARG ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
# Tue, 12 Mar 2024 18:49:49 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:50:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:50:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:50:21 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=900d911aecd734277f511c51e041ef92964ad55b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:50:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:50:23 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:50:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:50:24 GMT
USER odoo
# Tue, 12 Mar 2024 18:50:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:50:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a32c556380680a1795889bca44d0f0a883f42b50860b84f480546468a7a03`  
		Last Modified: Tue, 12 Mar 2024 02:54:00 GMT  
		Size: 228.6 MB (228600421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c60f6a8d0d4afdc1ff134aae19e82a3c10cbeb5816bcab9c7cdac58ff961e6`  
		Last Modified: Tue, 12 Mar 2024 02:53:31 GMT  
		Size: 2.9 MB (2876315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec00e5fbd9079a262ec1e1c1ae57ae88ae27282c49b89f9952917db58b01f6b`  
		Last Modified: Tue, 12 Mar 2024 02:53:30 GMT  
		Size: 462.5 KB (462469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97614c4983d81c7de16a9e98fd3d9d48346e0f7d298a4f552aa8bc88a0792956`  
		Last Modified: Tue, 12 Mar 2024 18:52:20 GMT  
		Size: 330.2 MB (330178553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f500882fc16908f317fbd339275b8276f63aa3409a74018e84ea07d2a3cffe6e`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a594a0c7b642975246b42bca03ad8645cf593e242b5d0f9a249bf3a90fe9c49`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7f7a1aa5bb4b7f6f7d9dbeed4d2c9d09327b7344266f89247ef05ab3eb1557`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8bb7126bd954b54132db0903f9c277f6cf8288543b1bd7dff50f9a2518eb0`  
		Last Modified: Tue, 12 Mar 2024 18:51:34 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:7523a05b13d0b0addbbf79bdfbecee62ade032076ba391054c70711f3ade3a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:c097985f4243b7d057715118b98eae309d1c963ac4ba496065094a4970248d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.9 MB (600880596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a117dd3eff1275e66067c47ce92c119f6ec01a3bdbbaac307dfa31c2e4eaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:00:03 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:00:08 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:00:08 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:00:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:00:08 GMT
USER odoo
# Tue, 12 Mar 2024 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e690b7354eb75e119ec42b72ccc5128ba6233158c10fb963500f5056304efacf`  
		Last Modified: Tue, 12 Mar 2024 18:03:59 GMT  
		Size: 333.7 MB (333710535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529d45c0119d1973d1b79b9c578129f51e2262b554a502d4f1c62bbca9447a7`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a51b5089356d97fb773c804884a9a212bd14d917704ac07a03a689859ad77c`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a71476cf6d9ad48c07e4132d9d404b97c9ae3d970f08e64c16829476d9cfbee`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c83c4741a0aaa79b05350e564691153b2f2e5a0248b77651e93cc0a7871f77`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ea848e7067d43101ca6d5509a94a787962c060ab77ee2dbff2f1a0e6e3b2ec81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595845243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34df8c4e9dcc31ef75afe067b00eda22cc9cd31392853781e6733865322e88be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 17:18:55 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 17:19:04 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 17:19:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 17:19:04 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 17:19:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 17:19:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 17:19:05 GMT
USER odoo
# Tue, 12 Mar 2024 17:19:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:19:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3be5e5d50a421dd890930bfb95b1fe77d1ff92e350cd6c162187b6d675851b`  
		Last Modified: Tue, 12 Mar 2024 17:21:31 GMT  
		Size: 333.3 MB (333331582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695c01490528a61fffeb7dfc44d25d3d2ae760bae68280b595ec4eab88fadb8d`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e22e664cf1ded17a59155829cca757ea678212c7ad5e2d256ea97feea889ab4`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772bfac9ac02fd36bf0f3bcd1d231cc4f8e82f42a4d01fa44ffe59f9e88c8a18`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c93b6c4da4abc860c51a63c7e4153def0e9d396218b3fb5a7b3d9d72b1306b`  
		Last Modified: Tue, 12 Mar 2024 17:20:57 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:be9fb82d4b7d75b6db6c1d1958f253dd3da953b0da588b8c63d9b833ce5e4ae3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617652838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f05c160663686f012782be156c37773b5ab04bf48bafb38cdf95bb02a5a34ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 18:41:10 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:41:11 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:45:07 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:45:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:45:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:45:23 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:45:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:45:24 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:45:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:45:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:45:27 GMT
USER odoo
# Tue, 12 Mar 2024 18:45:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:45:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2ecb9421489d54a3104f2ff940fe8d77dd1bbd28b0da17944138bf6f6a0af0`  
		Last Modified: Tue, 12 Mar 2024 18:51:22 GMT  
		Size: 335.5 MB (335460060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae50c6a278937581f5561399e82838010f30b4b85da235221aa80aac038d473`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0c5bb949045be8efdd08af5f14aed8a85e5af0b552c06664a195b0e6e72dba`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91463c9d76f658346bc54c69797e671d95dff35b1459d901ef8ad1f635de40fa`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8413d6df2fb76a798d9ae862fb23dbe91f9bf25f34671a30bd7866d647e6e`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7523a05b13d0b0addbbf79bdfbecee62ade032076ba391054c70711f3ade3a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:c097985f4243b7d057715118b98eae309d1c963ac4ba496065094a4970248d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.9 MB (600880596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a117dd3eff1275e66067c47ce92c119f6ec01a3bdbbaac307dfa31c2e4eaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:00:03 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:00:08 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:00:08 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:00:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:00:08 GMT
USER odoo
# Tue, 12 Mar 2024 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e690b7354eb75e119ec42b72ccc5128ba6233158c10fb963500f5056304efacf`  
		Last Modified: Tue, 12 Mar 2024 18:03:59 GMT  
		Size: 333.7 MB (333710535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529d45c0119d1973d1b79b9c578129f51e2262b554a502d4f1c62bbca9447a7`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a51b5089356d97fb773c804884a9a212bd14d917704ac07a03a689859ad77c`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a71476cf6d9ad48c07e4132d9d404b97c9ae3d970f08e64c16829476d9cfbee`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c83c4741a0aaa79b05350e564691153b2f2e5a0248b77651e93cc0a7871f77`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ea848e7067d43101ca6d5509a94a787962c060ab77ee2dbff2f1a0e6e3b2ec81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595845243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34df8c4e9dcc31ef75afe067b00eda22cc9cd31392853781e6733865322e88be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 17:18:55 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 17:19:04 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 17:19:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 17:19:04 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 17:19:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 17:19:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 17:19:05 GMT
USER odoo
# Tue, 12 Mar 2024 17:19:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:19:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3be5e5d50a421dd890930bfb95b1fe77d1ff92e350cd6c162187b6d675851b`  
		Last Modified: Tue, 12 Mar 2024 17:21:31 GMT  
		Size: 333.3 MB (333331582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695c01490528a61fffeb7dfc44d25d3d2ae760bae68280b595ec4eab88fadb8d`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e22e664cf1ded17a59155829cca757ea678212c7ad5e2d256ea97feea889ab4`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772bfac9ac02fd36bf0f3bcd1d231cc4f8e82f42a4d01fa44ffe59f9e88c8a18`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c93b6c4da4abc860c51a63c7e4153def0e9d396218b3fb5a7b3d9d72b1306b`  
		Last Modified: Tue, 12 Mar 2024 17:20:57 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:be9fb82d4b7d75b6db6c1d1958f253dd3da953b0da588b8c63d9b833ce5e4ae3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617652838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f05c160663686f012782be156c37773b5ab04bf48bafb38cdf95bb02a5a34ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 18:41:10 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:41:11 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:45:07 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:45:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:45:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:45:23 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:45:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:45:24 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:45:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:45:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:45:27 GMT
USER odoo
# Tue, 12 Mar 2024 18:45:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:45:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2ecb9421489d54a3104f2ff940fe8d77dd1bbd28b0da17944138bf6f6a0af0`  
		Last Modified: Tue, 12 Mar 2024 18:51:22 GMT  
		Size: 335.5 MB (335460060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae50c6a278937581f5561399e82838010f30b4b85da235221aa80aac038d473`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0c5bb949045be8efdd08af5f14aed8a85e5af0b552c06664a195b0e6e72dba`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91463c9d76f658346bc54c69797e671d95dff35b1459d901ef8ad1f635de40fa`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8413d6df2fb76a798d9ae862fb23dbe91f9bf25f34671a30bd7866d647e6e`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7523a05b13d0b0addbbf79bdfbecee62ade032076ba391054c70711f3ade3a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:c097985f4243b7d057715118b98eae309d1c963ac4ba496065094a4970248d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.9 MB (600880596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a117dd3eff1275e66067c47ce92c119f6ec01a3bdbbaac307dfa31c2e4eaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:00:03 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:00:08 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:00:08 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:00:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:00:08 GMT
USER odoo
# Tue, 12 Mar 2024 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e690b7354eb75e119ec42b72ccc5128ba6233158c10fb963500f5056304efacf`  
		Last Modified: Tue, 12 Mar 2024 18:03:59 GMT  
		Size: 333.7 MB (333710535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529d45c0119d1973d1b79b9c578129f51e2262b554a502d4f1c62bbca9447a7`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a51b5089356d97fb773c804884a9a212bd14d917704ac07a03a689859ad77c`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a71476cf6d9ad48c07e4132d9d404b97c9ae3d970f08e64c16829476d9cfbee`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c83c4741a0aaa79b05350e564691153b2f2e5a0248b77651e93cc0a7871f77`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ea848e7067d43101ca6d5509a94a787962c060ab77ee2dbff2f1a0e6e3b2ec81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595845243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34df8c4e9dcc31ef75afe067b00eda22cc9cd31392853781e6733865322e88be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 17:18:55 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 17:19:04 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 17:19:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 17:19:04 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 17:19:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 17:19:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 17:19:05 GMT
USER odoo
# Tue, 12 Mar 2024 17:19:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:19:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3be5e5d50a421dd890930bfb95b1fe77d1ff92e350cd6c162187b6d675851b`  
		Last Modified: Tue, 12 Mar 2024 17:21:31 GMT  
		Size: 333.3 MB (333331582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695c01490528a61fffeb7dfc44d25d3d2ae760bae68280b595ec4eab88fadb8d`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e22e664cf1ded17a59155829cca757ea678212c7ad5e2d256ea97feea889ab4`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772bfac9ac02fd36bf0f3bcd1d231cc4f8e82f42a4d01fa44ffe59f9e88c8a18`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c93b6c4da4abc860c51a63c7e4153def0e9d396218b3fb5a7b3d9d72b1306b`  
		Last Modified: Tue, 12 Mar 2024 17:20:57 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:be9fb82d4b7d75b6db6c1d1958f253dd3da953b0da588b8c63d9b833ce5e4ae3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617652838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f05c160663686f012782be156c37773b5ab04bf48bafb38cdf95bb02a5a34ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 18:41:10 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 18:41:11 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:45:07 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:45:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:45:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:45:23 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:45:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:45:24 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:45:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:45:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:45:27 GMT
USER odoo
# Tue, 12 Mar 2024 18:45:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:45:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2ecb9421489d54a3104f2ff940fe8d77dd1bbd28b0da17944138bf6f6a0af0`  
		Last Modified: Tue, 12 Mar 2024 18:51:22 GMT  
		Size: 335.5 MB (335460060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae50c6a278937581f5561399e82838010f30b4b85da235221aa80aac038d473`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0c5bb949045be8efdd08af5f14aed8a85e5af0b552c06664a195b0e6e72dba`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91463c9d76f658346bc54c69797e671d95dff35b1459d901ef8ad1f635de40fa`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f8413d6df2fb76a798d9ae862fb23dbe91f9bf25f34671a30bd7866d647e6e`  
		Last Modified: Tue, 12 Mar 2024 18:50:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
