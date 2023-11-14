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
$ docker pull odoo@sha256:59f8897974c973ee284af1693b311886989ca50704c170842f17345ad130e1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ed3a88ca1f9bb776bfde513bfdedfbbaedc6959abb48ea489d4ff1348acbf74b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563007841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90460214e99cf5875217bd329f5fd1cb889bebd78f175d5d8faf1b2e20292bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 12:03:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Nov 2023 12:04:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:04:04 GMT
RUN npm install -g rtlcss
# Wed, 01 Nov 2023 12:04:04 GMT
ENV ODOO_VERSION=15.0
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
# Wed, 08 Nov 2023 00:43:16 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:43:21 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:43:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:43:21 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:43:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:43:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:43:21 GMT
USER odoo
# Wed, 08 Nov 2023 00:43:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:43:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4769061fca067a25d337753a857c225301a3391d70dc9c355ec401a1666f9`  
		Last Modified: Wed, 01 Nov 2023 12:09:44 GMT  
		Size: 220.3 MB (220298628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037b076bdf88bd13eb93037e412a84af9179318c033537325a2abb0e21f3437`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 2.6 MB (2624848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09c8bae1e450f33859e0454685d8e83ce199230cdf0487f7b3bca45bccd8a66`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 457.9 KB (457875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6818025799f187b915cf97bc1ac4ddb67a106c478369d5261f233135773734ff`  
		Last Modified: Wed, 08 Nov 2023 00:46:19 GMT  
		Size: 308.2 MB (308206110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9979448ed0ddebc713bddd4719b4941de3c33f6800e2c89f0bcbb7d676e0f96`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae54e00a1e53b4da2bf462000389824becf5ed078fd5667d16bf74a0140aad94`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7209289209c2a643bf58c06e90725e0364c37ec2cb5eebc700aedd075d1589`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9ea5daa95395c0a47e181fcbd6e39d7058e1e42a22122b4c4e25fccc0a5df8`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:59f8897974c973ee284af1693b311886989ca50704c170842f17345ad130e1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ed3a88ca1f9bb776bfde513bfdedfbbaedc6959abb48ea489d4ff1348acbf74b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563007841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90460214e99cf5875217bd329f5fd1cb889bebd78f175d5d8faf1b2e20292bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 12:03:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Nov 2023 12:04:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:04:04 GMT
RUN npm install -g rtlcss
# Wed, 01 Nov 2023 12:04:04 GMT
ENV ODOO_VERSION=15.0
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:42:03 GMT
ARG ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
# Wed, 08 Nov 2023 00:43:16 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:43:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:43:21 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=5d0022d3a282f11c1b92c727ce93e69e732febfe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:43:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:43:21 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:43:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:43:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:43:21 GMT
USER odoo
# Wed, 08 Nov 2023 00:43:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:43:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4769061fca067a25d337753a857c225301a3391d70dc9c355ec401a1666f9`  
		Last Modified: Wed, 01 Nov 2023 12:09:44 GMT  
		Size: 220.3 MB (220298628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037b076bdf88bd13eb93037e412a84af9179318c033537325a2abb0e21f3437`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 2.6 MB (2624848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09c8bae1e450f33859e0454685d8e83ce199230cdf0487f7b3bca45bccd8a66`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 457.9 KB (457875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6818025799f187b915cf97bc1ac4ddb67a106c478369d5261f233135773734ff`  
		Last Modified: Wed, 08 Nov 2023 00:46:19 GMT  
		Size: 308.2 MB (308206110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9979448ed0ddebc713bddd4719b4941de3c33f6800e2c89f0bcbb7d676e0f96`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae54e00a1e53b4da2bf462000389824becf5ed078fd5667d16bf74a0140aad94`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7209289209c2a643bf58c06e90725e0364c37ec2cb5eebc700aedd075d1589`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9ea5daa95395c0a47e181fcbd6e39d7058e1e42a22122b4c4e25fccc0a5df8`  
		Last Modified: Wed, 08 Nov 2023 00:45:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:614b53691c0148e26421b6a2013ee2089aa1ac30f04ba92792312a4ca6c45edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:050d6909f19797b0113b195dac076d9f9e9d48906c8a9c00b017d4a3162b2f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577148541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4063887fdfe4a2ffda6523576bbcd058e1040f9a000d336d84f9d7e0c77d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:41:41 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:41:45 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:41:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:41:45 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:41:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:41:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:41:46 GMT
USER odoo
# Wed, 08 Nov 2023 00:41:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:41:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3322fe74239122fed63bc5d7c0ad8426f1f64b70f8605a7d9bc76b24731bc`  
		Last Modified: Wed, 08 Nov 2023 00:45:34 GMT  
		Size: 323.0 MB (323033428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790686c1cd5cc1e7e382ab129cd19542d38167c0f49b12d62fc499162ba3034b`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3a6dcb28c4c6bfc8b69508a4e912cfb0d4ccfb03691c3aa654da8b0e4238f`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8d088b6082f21385081c583e38925e485c4cf273eea4611d603a9c4c5b505`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ddc13242fd0b2e64c6f399370d12edda33f930841d1d805eaf93eba5341c38`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8f6eedc129b5b3fcb29f2cd2b1a9ad32c524929b493c9d2adc2a8a87e2aa7651
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572758883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1566cee291601a50b7b337b36cde5aae59862c8f99c9feddbb63fda1144c08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 07 Nov 2023 23:49:48 GMT
ARG ODOO_RELEASE=20231106
# Tue, 07 Nov 2023 23:49:48 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Tue, 07 Nov 2023 23:51:03 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Nov 2023 23:51:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 07 Nov 2023 23:51:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 07 Nov 2023 23:51:12 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 07 Nov 2023 23:51:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Nov 2023 23:51:12 GMT
EXPOSE 8069 8071 8072
# Tue, 07 Nov 2023 23:51:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Nov 2023 23:51:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 07 Nov 2023 23:51:12 GMT
USER odoo
# Tue, 07 Nov 2023 23:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Nov 2023 23:51:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6432fc1af8295bd2885e33af1ed29b63dfedfa95bd638318ef031a3149020f65`  
		Last Modified: Tue, 07 Nov 2023 23:51:59 GMT  
		Size: 322.7 MB (322691375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe67fd3464d0eb156b296d671af3c33c269b79421cb53e285946720fad365f1`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c1da646860f489d84029b167a63ae78951477fea9b760f6395a78ccfa8e22a`  
		Last Modified: Tue, 07 Nov 2023 23:51:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c616c540ed904f9dd0938081c0e5b3b571369f2a5135756a0e732d7bffc1d`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753c5cd5597c8c95c1b91ff13d8463e6804519c8a55179b0e6dd2af3b75fa7a2`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:61b554c5908413812c039093ada2bfc56d219edb693d1d078f4100ca9ab6e226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591712906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716f237684cdfd6c1d7303481a77ed2f1b8d845479485ec22000ba725477dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:38:10 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:38:11 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:40:18 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:40:33 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:40:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:40:34 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:40:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:40:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:40:35 GMT
USER odoo
# Wed, 08 Nov 2023 00:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13500816d0a55578fb3acde8b75034d7c929fc654ccc114e9d8f1a17d45976b`  
		Last Modified: Wed, 08 Nov 2023 00:41:43 GMT  
		Size: 324.5 MB (324485311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8814df038c86cf9c05085931a40ed23bea1ce5702d854ed276944dcf6191ae`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e316c6ff6941cbe4117491ea563ecfcf91b6176f243de0c30ceacf7939b162`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254fd04082fa3cc5bf8f9ab205f103084858296096f0c626a10d5bba2a18b823`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb744a3bde4cae9e418d9711328d6957a6dea74a5e0eca8ae7e83287b9525e05`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:614b53691c0148e26421b6a2013ee2089aa1ac30f04ba92792312a4ca6c45edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:050d6909f19797b0113b195dac076d9f9e9d48906c8a9c00b017d4a3162b2f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577148541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4063887fdfe4a2ffda6523576bbcd058e1040f9a000d336d84f9d7e0c77d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:41:41 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:41:45 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:41:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:41:45 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:41:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:41:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:41:46 GMT
USER odoo
# Wed, 08 Nov 2023 00:41:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:41:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3322fe74239122fed63bc5d7c0ad8426f1f64b70f8605a7d9bc76b24731bc`  
		Last Modified: Wed, 08 Nov 2023 00:45:34 GMT  
		Size: 323.0 MB (323033428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790686c1cd5cc1e7e382ab129cd19542d38167c0f49b12d62fc499162ba3034b`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3a6dcb28c4c6bfc8b69508a4e912cfb0d4ccfb03691c3aa654da8b0e4238f`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8d088b6082f21385081c583e38925e485c4cf273eea4611d603a9c4c5b505`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ddc13242fd0b2e64c6f399370d12edda33f930841d1d805eaf93eba5341c38`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8f6eedc129b5b3fcb29f2cd2b1a9ad32c524929b493c9d2adc2a8a87e2aa7651
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572758883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1566cee291601a50b7b337b36cde5aae59862c8f99c9feddbb63fda1144c08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 07 Nov 2023 23:49:48 GMT
ARG ODOO_RELEASE=20231106
# Tue, 07 Nov 2023 23:49:48 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Tue, 07 Nov 2023 23:51:03 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Nov 2023 23:51:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 07 Nov 2023 23:51:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 07 Nov 2023 23:51:12 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 07 Nov 2023 23:51:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Nov 2023 23:51:12 GMT
EXPOSE 8069 8071 8072
# Tue, 07 Nov 2023 23:51:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Nov 2023 23:51:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 07 Nov 2023 23:51:12 GMT
USER odoo
# Tue, 07 Nov 2023 23:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Nov 2023 23:51:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6432fc1af8295bd2885e33af1ed29b63dfedfa95bd638318ef031a3149020f65`  
		Last Modified: Tue, 07 Nov 2023 23:51:59 GMT  
		Size: 322.7 MB (322691375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe67fd3464d0eb156b296d671af3c33c269b79421cb53e285946720fad365f1`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c1da646860f489d84029b167a63ae78951477fea9b760f6395a78ccfa8e22a`  
		Last Modified: Tue, 07 Nov 2023 23:51:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c616c540ed904f9dd0938081c0e5b3b571369f2a5135756a0e732d7bffc1d`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753c5cd5597c8c95c1b91ff13d8463e6804519c8a55179b0e6dd2af3b75fa7a2`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:61b554c5908413812c039093ada2bfc56d219edb693d1d078f4100ca9ab6e226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591712906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716f237684cdfd6c1d7303481a77ed2f1b8d845479485ec22000ba725477dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:38:10 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:38:11 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:40:18 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:40:33 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:40:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:40:34 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:40:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:40:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:40:35 GMT
USER odoo
# Wed, 08 Nov 2023 00:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13500816d0a55578fb3acde8b75034d7c929fc654ccc114e9d8f1a17d45976b`  
		Last Modified: Wed, 08 Nov 2023 00:41:43 GMT  
		Size: 324.5 MB (324485311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8814df038c86cf9c05085931a40ed23bea1ce5702d854ed276944dcf6191ae`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e316c6ff6941cbe4117491ea563ecfcf91b6176f243de0c30ceacf7939b162`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254fd04082fa3cc5bf8f9ab205f103084858296096f0c626a10d5bba2a18b823`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb744a3bde4cae9e418d9711328d6957a6dea74a5e0eca8ae7e83287b9525e05`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

**does not exist** (yet?)

## `odoo:17.0`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:614b53691c0148e26421b6a2013ee2089aa1ac30f04ba92792312a4ca6c45edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:050d6909f19797b0113b195dac076d9f9e9d48906c8a9c00b017d4a3162b2f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.1 MB (577148541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e4063887fdfe4a2ffda6523576bbcd058e1040f9a000d336d84f9d7e0c77d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:40:19 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:41:41 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:41:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:41:45 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:41:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:41:45 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:41:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:41:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:41:46 GMT
USER odoo
# Wed, 08 Nov 2023 00:41:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:41:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3322fe74239122fed63bc5d7c0ad8426f1f64b70f8605a7d9bc76b24731bc`  
		Last Modified: Wed, 08 Nov 2023 00:45:34 GMT  
		Size: 323.0 MB (323033428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790686c1cd5cc1e7e382ab129cd19542d38167c0f49b12d62fc499162ba3034b`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3a6dcb28c4c6bfc8b69508a4e912cfb0d4ccfb03691c3aa654da8b0e4238f`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f8d088b6082f21385081c583e38925e485c4cf273eea4611d603a9c4c5b505`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ddc13242fd0b2e64c6f399370d12edda33f930841d1d805eaf93eba5341c38`  
		Last Modified: Wed, 08 Nov 2023 00:44:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8f6eedc129b5b3fcb29f2cd2b1a9ad32c524929b493c9d2adc2a8a87e2aa7651
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572758883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1566cee291601a50b7b337b36cde5aae59862c8f99c9feddbb63fda1144c08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 07 Nov 2023 23:49:48 GMT
ARG ODOO_RELEASE=20231106
# Tue, 07 Nov 2023 23:49:48 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Tue, 07 Nov 2023 23:51:03 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 07 Nov 2023 23:51:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 07 Nov 2023 23:51:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 07 Nov 2023 23:51:12 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 07 Nov 2023 23:51:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Nov 2023 23:51:12 GMT
EXPOSE 8069 8071 8072
# Tue, 07 Nov 2023 23:51:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Nov 2023 23:51:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 07 Nov 2023 23:51:12 GMT
USER odoo
# Tue, 07 Nov 2023 23:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Nov 2023 23:51:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6432fc1af8295bd2885e33af1ed29b63dfedfa95bd638318ef031a3149020f65`  
		Last Modified: Tue, 07 Nov 2023 23:51:59 GMT  
		Size: 322.7 MB (322691375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe67fd3464d0eb156b296d671af3c33c269b79421cb53e285946720fad365f1`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c1da646860f489d84029b167a63ae78951477fea9b760f6395a78ccfa8e22a`  
		Last Modified: Tue, 07 Nov 2023 23:51:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139c616c540ed904f9dd0938081c0e5b3b571369f2a5135756a0e732d7bffc1d`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753c5cd5597c8c95c1b91ff13d8463e6804519c8a55179b0e6dd2af3b75fa7a2`  
		Last Modified: Tue, 07 Nov 2023 23:51:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:61b554c5908413812c039093ada2bfc56d219edb693d1d078f4100ca9ab6e226
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591712906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716f237684cdfd6c1d7303481a77ed2f1b8d845479485ec22000ba725477dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Wed, 08 Nov 2023 00:38:10 GMT
ARG ODOO_RELEASE=20231106
# Wed, 08 Nov 2023 00:38:11 GMT
ARG ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
# Wed, 08 Nov 2023 00:40:18 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 08 Nov 2023 00:40:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 08 Nov 2023 00:40:33 GMT
# ARGS: ODOO_RELEASE=20231106 ODOO_SHA=ef0fa4f34bbb1af69733a8df1a19d2756de7916b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 08 Nov 2023 00:40:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Nov 2023 00:40:34 GMT
EXPOSE 8069 8071 8072
# Wed, 08 Nov 2023 00:40:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Nov 2023 00:40:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 08 Nov 2023 00:40:35 GMT
USER odoo
# Wed, 08 Nov 2023 00:40:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Nov 2023 00:40:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13500816d0a55578fb3acde8b75034d7c929fc654ccc114e9d8f1a17d45976b`  
		Last Modified: Wed, 08 Nov 2023 00:41:43 GMT  
		Size: 324.5 MB (324485311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8814df038c86cf9c05085931a40ed23bea1ce5702d854ed276944dcf6191ae`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e316c6ff6941cbe4117491ea563ecfcf91b6176f243de0c30ceacf7939b162`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254fd04082fa3cc5bf8f9ab205f103084858296096f0c626a10d5bba2a18b823`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb744a3bde4cae9e418d9711328d6957a6dea74a5e0eca8ae7e83287b9525e05`  
		Last Modified: Wed, 08 Nov 2023 00:40:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
