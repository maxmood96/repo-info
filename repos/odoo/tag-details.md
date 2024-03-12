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
$ docker pull odoo@sha256:9a9686d3b432620476147f962b204f235933df399c8126d2d201c282a95be3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:97c73ddcebe0e5403e4f610b092a262f31dafd4faf6366120466aebd18b4d302
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563852452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eafa33aa5f66244f281f7430ce35174d18dd05d6ca397463129f755ddba0a87`
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
# Tue, 12 Mar 2024 10:08:17 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 10:08:18 GMT
ARG ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
# Tue, 12 Mar 2024 10:09:26 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 10:09:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 10:09:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 10:09:31 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 10:09:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 10:09:31 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 10:09:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 10:09:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 10:09:31 GMT
USER odoo
# Tue, 12 Mar 2024 10:09:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 10:09:31 GMT
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
	-	`sha256:833536bd80958e9ad89cb8c36afc281ceea07b59843e5a6021212d39d133b304`  
		Last Modified: Tue, 12 Mar 2024 10:11:13 GMT  
		Size: 309.0 MB (309047636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c03e4a3944de88b4b1ebb51d988b2f6c81916acdd155ecaa8bc4b73bbdeb7f2`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d5d6841aeadcb9b99b39c741fb34758dfd4869af0928a3185ebb0d8f51cf`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49250a5f8a5fc67d9d240f9c6adb6f78ea663815c149f3db7931fb60165e58e`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a378848a8e19e7c6f2a84ce6ba042b92109cd008630f23cfdbc202bb8d253c45`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:9a9686d3b432620476147f962b204f235933df399c8126d2d201c282a95be3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:97c73ddcebe0e5403e4f610b092a262f31dafd4faf6366120466aebd18b4d302
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563852452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eafa33aa5f66244f281f7430ce35174d18dd05d6ca397463129f755ddba0a87`
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
# Tue, 12 Mar 2024 10:08:17 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 10:08:18 GMT
ARG ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
# Tue, 12 Mar 2024 10:09:26 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 10:09:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 10:09:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 10:09:31 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 10:09:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 10:09:31 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 10:09:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 10:09:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 10:09:31 GMT
USER odoo
# Tue, 12 Mar 2024 10:09:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 10:09:31 GMT
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
	-	`sha256:833536bd80958e9ad89cb8c36afc281ceea07b59843e5a6021212d39d133b304`  
		Last Modified: Tue, 12 Mar 2024 10:11:13 GMT  
		Size: 309.0 MB (309047636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c03e4a3944de88b4b1ebb51d988b2f6c81916acdd155ecaa8bc4b73bbdeb7f2`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c200d5d6841aeadcb9b99b39c741fb34758dfd4869af0928a3185ebb0d8f51cf`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49250a5f8a5fc67d9d240f9c6adb6f78ea663815c149f3db7931fb60165e58e`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a378848a8e19e7c6f2a84ce6ba042b92109cd008630f23cfdbc202bb8d253c45`  
		Last Modified: Tue, 12 Mar 2024 10:10:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:1ac47834ad36144bdbeeab0ca66f097f813255c1b6a07673b8d4baeccde66bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:dde05e777001f00ccb7bfe228ac8198f4ccb2082029a41fdff829876e9543e9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.6 MB (582629781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123e66f848b67516f2a6b07bd655eac87ab7ff59ca937584a241844f76afa66`
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
# Tue, 12 Mar 2024 10:05:44 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 10:05:44 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 10:07:04 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 10:07:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 10:07:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 10:07:09 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 10:07:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 10:07:09 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 10:07:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 10:07:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 10:07:09 GMT
USER odoo
# Tue, 12 Mar 2024 10:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 10:07:09 GMT
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
	-	`sha256:6a5f9d79b90053e457a1325674057275b5f4469db19e4b3ec20d684a8f10e21b`  
		Last Modified: Tue, 12 Mar 2024 10:10:28 GMT  
		Size: 328.5 MB (328509331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b512603dcc2085f57fcd4496b3a26223c516bb7af975ca4610392518344363`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b16499fcd8aea95e2b1695c0693e957849889bdc18e46065cde39ea1b9f18`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f93c39add983db04dddfb7da1d27714a89060261245725f6396ee6e2ebf49f`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc84e82619881f1e46cdf2a66a0b90df29eac94e3d6b7bfae66ee4e37b3d49c`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4e101f7a8cf7241ca04474625675123dc507751b09291c152c8f1077cf6a35c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.3 MB (578254382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c5c13573486c70ded7fc6fc28e489553791cdc16ac5d6702f44545c3fa9a33`
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
# Tue, 12 Mar 2024 07:10:44 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 07:10:44 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 07:11:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 07:12:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 07:12:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 07:12:03 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 07:12:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 07:12:03 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 07:12:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 07:12:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 07:12:03 GMT
USER odoo
# Tue, 12 Mar 2024 07:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 07:12:03 GMT
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
	-	`sha256:d6ec1115de5c4deb063871a1c31ed50d827e364ff45dd10b3a25c4780b36bf97`  
		Last Modified: Tue, 12 Mar 2024 07:12:54 GMT  
		Size: 328.2 MB (328179603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c65a0b5bd4ad5a5274d32834013e49087d355d30d2be18099cc2791fc89d995`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef36557d80a38b6cd60be32cea20809d2b9c1c96bb6e2384215aa7dbc2f386d`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030ea484847be17a23acf25941811905301db4af564132e68bc93613af028299`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236a3a5c57cee49a2210d7fbca86ba1e6e0eea79b6f5fc3deb89474a2b37494`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac4c26796e7de62c7c37943df36da93330c52518558ff7f6348158c7ea349c40
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597188342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a85ccfe0b798aed5e6e88db8c5b377cdb1d61edea6d6a99b960b829a1db777`
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
# Tue, 12 Mar 2024 02:46:14 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 02:46:16 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 02:52:18 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 02:52:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 02:52:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 02:52:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 02:52:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 02:52:55 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 02:52:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 02:53:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 02:53:03 GMT
USER odoo
# Tue, 12 Mar 2024 02:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 02:53:09 GMT
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
	-	`sha256:07524d2b73109a74dd0a1f20a0010d75b2fc711c5b53922553f135bc0ef5efa9`  
		Last Modified: Tue, 12 Mar 2024 02:54:14 GMT  
		Size: 329.9 MB (329948666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb9dd5d6bb8e8e8204736a4e78fe836d73f315949634a50468f87045d5e537`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623aaad4280283dfcc93d0cae94a05cf79dcc89617d8c690866ac6bb5f7403f`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26758bb8f8a978e5290eda3a3fa1038fd411b3e951a21539f2e165a9d7eecb4c`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a8f884eab14d8865dc28d1fb2728caab6b0f93bc4527fd3d1eef43c413bd97`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:1ac47834ad36144bdbeeab0ca66f097f813255c1b6a07673b8d4baeccde66bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:dde05e777001f00ccb7bfe228ac8198f4ccb2082029a41fdff829876e9543e9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.6 MB (582629781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a123e66f848b67516f2a6b07bd655eac87ab7ff59ca937584a241844f76afa66`
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
# Tue, 12 Mar 2024 10:05:44 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 10:05:44 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 10:07:04 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 10:07:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 10:07:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 10:07:09 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 10:07:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 10:07:09 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 10:07:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 10:07:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 10:07:09 GMT
USER odoo
# Tue, 12 Mar 2024 10:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 10:07:09 GMT
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
	-	`sha256:6a5f9d79b90053e457a1325674057275b5f4469db19e4b3ec20d684a8f10e21b`  
		Last Modified: Tue, 12 Mar 2024 10:10:28 GMT  
		Size: 328.5 MB (328509331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b512603dcc2085f57fcd4496b3a26223c516bb7af975ca4610392518344363`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469b16499fcd8aea95e2b1695c0693e957849889bdc18e46065cde39ea1b9f18`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f93c39add983db04dddfb7da1d27714a89060261245725f6396ee6e2ebf49f`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc84e82619881f1e46cdf2a66a0b90df29eac94e3d6b7bfae66ee4e37b3d49c`  
		Last Modified: Tue, 12 Mar 2024 10:09:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4e101f7a8cf7241ca04474625675123dc507751b09291c152c8f1077cf6a35c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.3 MB (578254382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c5c13573486c70ded7fc6fc28e489553791cdc16ac5d6702f44545c3fa9a33`
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
# Tue, 12 Mar 2024 07:10:44 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 07:10:44 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 07:11:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 07:12:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 07:12:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 07:12:03 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 07:12:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 07:12:03 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 07:12:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 07:12:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 07:12:03 GMT
USER odoo
# Tue, 12 Mar 2024 07:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 07:12:03 GMT
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
	-	`sha256:d6ec1115de5c4deb063871a1c31ed50d827e364ff45dd10b3a25c4780b36bf97`  
		Last Modified: Tue, 12 Mar 2024 07:12:54 GMT  
		Size: 328.2 MB (328179603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c65a0b5bd4ad5a5274d32834013e49087d355d30d2be18099cc2791fc89d995`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef36557d80a38b6cd60be32cea20809d2b9c1c96bb6e2384215aa7dbc2f386d`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030ea484847be17a23acf25941811905301db4af564132e68bc93613af028299`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d236a3a5c57cee49a2210d7fbca86ba1e6e0eea79b6f5fc3deb89474a2b37494`  
		Last Modified: Tue, 12 Mar 2024 07:12:24 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac4c26796e7de62c7c37943df36da93330c52518558ff7f6348158c7ea349c40
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597188342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a85ccfe0b798aed5e6e88db8c5b377cdb1d61edea6d6a99b960b829a1db777`
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
# Tue, 12 Mar 2024 02:46:14 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 02:46:16 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 02:52:18 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 02:52:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 02:52:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 02:52:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 02:52:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 02:52:55 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 02:52:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 02:53:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 02:53:03 GMT
USER odoo
# Tue, 12 Mar 2024 02:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 02:53:09 GMT
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
	-	`sha256:07524d2b73109a74dd0a1f20a0010d75b2fc711c5b53922553f135bc0ef5efa9`  
		Last Modified: Tue, 12 Mar 2024 02:54:14 GMT  
		Size: 329.9 MB (329948666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb9dd5d6bb8e8e8204736a4e78fe836d73f315949634a50468f87045d5e537`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623aaad4280283dfcc93d0cae94a05cf79dcc89617d8c690866ac6bb5f7403f`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26758bb8f8a978e5290eda3a3fa1038fd411b3e951a21539f2e165a9d7eecb4c`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a8f884eab14d8865dc28d1fb2728caab6b0f93bc4527fd3d1eef43c413bd97`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:6d7b28da1aa2ca75e10d0efff30c342f222da78148c295490c23df78fd51049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:4ec7d77268a6ddcfb57bf21d4d02809a3a59a73d663038f25b9492168644af41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599400521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643a46f2e9a90bd339ce38c1a98519a43ac5ef2d3bc16b0efea5c45bc6cc1b0`
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
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:12:17 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:12:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:12:22 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:12:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:12:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:12:22 GMT
USER odoo
# Wed, 06 Mar 2024 03:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:12:22 GMT
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
	-	`sha256:a3717329e54eff361b366c467d937defe6ca11cabe9bf154df41b26af3e0217b`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 332.2 MB (332230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90c8fa1dd7a41d4d9b1a2b6668dc5e4dbe08c783555baf1b06185df4edb089`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e7b2c45b97702bee087b74a497e56f2242989fdabd4c540a6f1fbefde1c56`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540f23430dfda96b5ace20472fe05a61c966108bec8e74f8c9d31f9ad6117b4`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fd9f4a47e84418a08805e18fef090743b51cd587988cd3989657c34bcdb68`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2f09607cc3f69cf0da21ce0768090ae0a1b20cc03ef11fd55e58a8fd8976f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594344493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210e410acf6ee10dfa11e2fd0b5183010016dfac5b66d8b3cb2aba5ae4ee280`
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
# Wed, 06 Mar 2024 04:56:24 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 04:56:25 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 04:57:58 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 04:58:07 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 04:58:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 04:58:07 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 04:58:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 04:58:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 04:58:07 GMT
USER odoo
# Wed, 06 Mar 2024 04:58:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 04:58:07 GMT
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
	-	`sha256:e119923f8f85637d1291f21089fb8f8c83b60055d0ced620ee1a5f1b0c32293b`  
		Last Modified: Wed, 06 Mar 2024 04:58:57 GMT  
		Size: 331.8 MB (331830830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752d0b20375f0106febf3111e43b12167400a8fcd198548c83579106d8bc100`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cbfbd6a8b660d3416a8d8f0668f4ed111b94e46f259dbbb2297ddd0a50800`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570037660ddca8846552de495143df700ef637408692c8a75c0f167225ca6f8`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28706c51a3064cf047be7d767cf6edb9c5515434fe36bdd1d797d5f416d1038d`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
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
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
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
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:6d7b28da1aa2ca75e10d0efff30c342f222da78148c295490c23df78fd51049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:4ec7d77268a6ddcfb57bf21d4d02809a3a59a73d663038f25b9492168644af41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599400521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643a46f2e9a90bd339ce38c1a98519a43ac5ef2d3bc16b0efea5c45bc6cc1b0`
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
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:12:17 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:12:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:12:22 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:12:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:12:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:12:22 GMT
USER odoo
# Wed, 06 Mar 2024 03:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:12:22 GMT
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
	-	`sha256:a3717329e54eff361b366c467d937defe6ca11cabe9bf154df41b26af3e0217b`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 332.2 MB (332230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90c8fa1dd7a41d4d9b1a2b6668dc5e4dbe08c783555baf1b06185df4edb089`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e7b2c45b97702bee087b74a497e56f2242989fdabd4c540a6f1fbefde1c56`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540f23430dfda96b5ace20472fe05a61c966108bec8e74f8c9d31f9ad6117b4`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fd9f4a47e84418a08805e18fef090743b51cd587988cd3989657c34bcdb68`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2f09607cc3f69cf0da21ce0768090ae0a1b20cc03ef11fd55e58a8fd8976f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594344493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210e410acf6ee10dfa11e2fd0b5183010016dfac5b66d8b3cb2aba5ae4ee280`
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
# Wed, 06 Mar 2024 04:56:24 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 04:56:25 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 04:57:58 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 04:58:07 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 04:58:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 04:58:07 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 04:58:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 04:58:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 04:58:07 GMT
USER odoo
# Wed, 06 Mar 2024 04:58:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 04:58:07 GMT
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
	-	`sha256:e119923f8f85637d1291f21089fb8f8c83b60055d0ced620ee1a5f1b0c32293b`  
		Last Modified: Wed, 06 Mar 2024 04:58:57 GMT  
		Size: 331.8 MB (331830830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752d0b20375f0106febf3111e43b12167400a8fcd198548c83579106d8bc100`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cbfbd6a8b660d3416a8d8f0668f4ed111b94e46f259dbbb2297ddd0a50800`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570037660ddca8846552de495143df700ef637408692c8a75c0f167225ca6f8`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28706c51a3064cf047be7d767cf6edb9c5515434fe36bdd1d797d5f416d1038d`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
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
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
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
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:6d7b28da1aa2ca75e10d0efff30c342f222da78148c295490c23df78fd51049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:4ec7d77268a6ddcfb57bf21d4d02809a3a59a73d663038f25b9492168644af41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599400521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643a46f2e9a90bd339ce38c1a98519a43ac5ef2d3bc16b0efea5c45bc6cc1b0`
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
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:12:17 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:12:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:12:22 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:12:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:12:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:12:22 GMT
USER odoo
# Wed, 06 Mar 2024 03:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:12:22 GMT
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
	-	`sha256:a3717329e54eff361b366c467d937defe6ca11cabe9bf154df41b26af3e0217b`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 332.2 MB (332230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90c8fa1dd7a41d4d9b1a2b6668dc5e4dbe08c783555baf1b06185df4edb089`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e7b2c45b97702bee087b74a497e56f2242989fdabd4c540a6f1fbefde1c56`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540f23430dfda96b5ace20472fe05a61c966108bec8e74f8c9d31f9ad6117b4`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fd9f4a47e84418a08805e18fef090743b51cd587988cd3989657c34bcdb68`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2f09607cc3f69cf0da21ce0768090ae0a1b20cc03ef11fd55e58a8fd8976f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594344493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210e410acf6ee10dfa11e2fd0b5183010016dfac5b66d8b3cb2aba5ae4ee280`
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
# Wed, 06 Mar 2024 04:56:24 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 04:56:25 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 04:57:58 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 04:58:07 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 04:58:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 04:58:07 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 04:58:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 04:58:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 04:58:07 GMT
USER odoo
# Wed, 06 Mar 2024 04:58:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 04:58:07 GMT
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
	-	`sha256:e119923f8f85637d1291f21089fb8f8c83b60055d0ced620ee1a5f1b0c32293b`  
		Last Modified: Wed, 06 Mar 2024 04:58:57 GMT  
		Size: 331.8 MB (331830830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752d0b20375f0106febf3111e43b12167400a8fcd198548c83579106d8bc100`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cbfbd6a8b660d3416a8d8f0668f4ed111b94e46f259dbbb2297ddd0a50800`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570037660ddca8846552de495143df700ef637408692c8a75c0f167225ca6f8`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28706c51a3064cf047be7d767cf6edb9c5515434fe36bdd1d797d5f416d1038d`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
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
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
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
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
