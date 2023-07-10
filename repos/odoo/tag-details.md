<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:latest`](#odoolatest)

## `odoo:14`

```console
$ docker pull odoo@sha256:e716ce39226175446173ffe3a038d13927a8d6a2660ef23d5721ca0950ea7129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:23d6f5dc965ae83d4720c0e5d953071456aeb9381ad528c0b3bc60d98c8e79d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.9 MB (532872371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d56c1a4a92b1a0334cd77e957470748f91c53c7025308883bf99c0a56c12b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:47 GMT
ADD file:ca4076bfffab8d09636384070ca253570590554cff76a132afaae5cd89b363b5 in / 
# Tue, 04 Jul 2023 01:20:48 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:54:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:54:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:54:33 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:56:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:56:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:56:37 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:56:37 GMT
ENV ODOO_VERSION=14.0
# Mon, 10 Jul 2023 20:42:32 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:42:32 GMT
ARG ODOO_SHA=d4c7092155bf60291864cc8071333cc4ef122194
# Mon, 10 Jul 2023 20:44:02 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=d4c7092155bf60291864cc8071333cc4ef122194
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:44:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:44:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:44:06 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=d4c7092155bf60291864cc8071333cc4ef122194
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:44:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:44:06 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:44:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:44:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:44:06 GMT
USER odoo
# Mon, 10 Jul 2023 20:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:44:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:90ac1ecaf92c8ae0cb37d29d8cc01b5802612c12edb933c369ad4c586ea94c6c`  
		Last Modified: Tue, 04 Jul 2023 01:26:21 GMT  
		Size: 27.1 MB (27138502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00e825012af0c5f20095b1f8902b3341da662edb2331f4bc160e8291a8d2ff8`  
		Last Modified: Tue, 04 Jul 2023 17:00:16 GMT  
		Size: 213.2 MB (213180476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab84fcf971d80a1b3e08f8415ad0ba35cbedb84cb7594ec24c79ad3dab44e84`  
		Last Modified: Tue, 04 Jul 2023 16:59:56 GMT  
		Size: 13.5 MB (13520290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc728f9cb60a83b4ab60b063840b0f84f5855805efe3fee682ef70cb18bb5`  
		Last Modified: Tue, 04 Jul 2023 16:59:54 GMT  
		Size: 458.3 KB (458274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50b2fa43e558e3fc1067ae6c098cd6b030250ed5f2efc7a2eff1e4dff5bc7e`  
		Last Modified: Mon, 10 Jul 2023 20:46:17 GMT  
		Size: 278.6 MB (278572369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebd889c5f4f8f52752674643701b2865f117c4fcddf821ad4a0f7b1e3187b50`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a48d75baf508723a6ee06f2f379b4e9566282c7204132914fedadcdc0d589b`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fa7fe5bae1e423e3a8f2c8a3e116b89196c983e93db564b4164b929662f79`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b079b7669ef9cfa4415059415822cfcd6af4e26a2ad102617f2b75dec5979824`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:e716ce39226175446173ffe3a038d13927a8d6a2660ef23d5721ca0950ea7129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:23d6f5dc965ae83d4720c0e5d953071456aeb9381ad528c0b3bc60d98c8e79d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.9 MB (532872371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d56c1a4a92b1a0334cd77e957470748f91c53c7025308883bf99c0a56c12b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:47 GMT
ADD file:ca4076bfffab8d09636384070ca253570590554cff76a132afaae5cd89b363b5 in / 
# Tue, 04 Jul 2023 01:20:48 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:54:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:54:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:54:33 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:56:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:56:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:56:37 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:56:37 GMT
ENV ODOO_VERSION=14.0
# Mon, 10 Jul 2023 20:42:32 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:42:32 GMT
ARG ODOO_SHA=d4c7092155bf60291864cc8071333cc4ef122194
# Mon, 10 Jul 2023 20:44:02 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=d4c7092155bf60291864cc8071333cc4ef122194
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:44:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:44:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:44:06 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=d4c7092155bf60291864cc8071333cc4ef122194
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:44:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:44:06 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:44:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:44:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:44:06 GMT
USER odoo
# Mon, 10 Jul 2023 20:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:44:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:90ac1ecaf92c8ae0cb37d29d8cc01b5802612c12edb933c369ad4c586ea94c6c`  
		Last Modified: Tue, 04 Jul 2023 01:26:21 GMT  
		Size: 27.1 MB (27138502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00e825012af0c5f20095b1f8902b3341da662edb2331f4bc160e8291a8d2ff8`  
		Last Modified: Tue, 04 Jul 2023 17:00:16 GMT  
		Size: 213.2 MB (213180476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab84fcf971d80a1b3e08f8415ad0ba35cbedb84cb7594ec24c79ad3dab44e84`  
		Last Modified: Tue, 04 Jul 2023 16:59:56 GMT  
		Size: 13.5 MB (13520290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc728f9cb60a83b4ab60b063840b0f84f5855805efe3fee682ef70cb18bb5`  
		Last Modified: Tue, 04 Jul 2023 16:59:54 GMT  
		Size: 458.3 KB (458274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50b2fa43e558e3fc1067ae6c098cd6b030250ed5f2efc7a2eff1e4dff5bc7e`  
		Last Modified: Mon, 10 Jul 2023 20:46:17 GMT  
		Size: 278.6 MB (278572369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebd889c5f4f8f52752674643701b2865f117c4fcddf821ad4a0f7b1e3187b50`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a48d75baf508723a6ee06f2f379b4e9566282c7204132914fedadcdc0d589b`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667fa7fe5bae1e423e3a8f2c8a3e116b89196c983e93db564b4164b929662f79`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b079b7669ef9cfa4415059415822cfcd6af4e26a2ad102617f2b75dec5979824`  
		Last Modified: Mon, 10 Jul 2023 20:45:47 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:c836d2d28c29f679b33065191419bb69affab220c7ef494de8fbdc5217de7f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:08b04ab4a91c9f257baed9c065ee8db9bf9a3d53f6804fca4070a701a8fbb5c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.8 MB (561818949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88d46cfaf10aa5c9b93e6c83531c0e446513e5627fb4e875335fe33ca5f847d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:48:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:52:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:53:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:53:06 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:53:06 GMT
ENV ODOO_VERSION=15.0
# Mon, 10 Jul 2023 20:41:08 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:41:08 GMT
ARG ODOO_SHA=e525263145212a77ae35a6f80a3f269d52547226
# Mon, 10 Jul 2023 20:42:23 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=e525263145212a77ae35a6f80a3f269d52547226
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:42:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:42:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:42:27 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=e525263145212a77ae35a6f80a3f269d52547226
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:42:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:42:27 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:42:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:42:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:42:28 GMT
USER odoo
# Mon, 10 Jul 2023 20:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:42:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecec17eceb6c3674130e046a294357d03d0a4328163573bf205d3e3313a92b3`  
		Last Modified: Tue, 04 Jul 2023 16:59:33 GMT  
		Size: 220.3 MB (220302668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3ff92d45f28abea1907822b9422b22044c4d8c3ea79cbbd890eedec7d2a2b`  
		Last Modified: Tue, 04 Jul 2023 16:59:09 GMT  
		Size: 2.6 MB (2576221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae451cd3af67981acb0b0f325d282607dfb4442750de0e5ef333d984e2ecae`  
		Last Modified: Tue, 04 Jul 2023 16:59:08 GMT  
		Size: 453.8 KB (453828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927f6314226a62b3db4bd83c2fbcd2dd5ab23b24570743a2c68defdf05bded3`  
		Last Modified: Mon, 10 Jul 2023 20:45:38 GMT  
		Size: 307.1 MB (307066386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1e74e4dc33cefe11e4d0fe527ee60dceddfeafa9177e5d23de9135b376e5`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc713c8b710d09e146a15ee77b90af766f5c4c3fba0e6d03580526659e72863a`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717135cfe2901c375f06c8188476a32f4ecca325e93c814edcd2be405e94bca2`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73215d6e65e3d201e121d89c4476ccd9c94697114a1eff68806476c0c2b36109`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:c836d2d28c29f679b33065191419bb69affab220c7ef494de8fbdc5217de7f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:08b04ab4a91c9f257baed9c065ee8db9bf9a3d53f6804fca4070a701a8fbb5c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.8 MB (561818949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88d46cfaf10aa5c9b93e6c83531c0e446513e5627fb4e875335fe33ca5f847d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:48:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:52:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:53:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:53:06 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:53:06 GMT
ENV ODOO_VERSION=15.0
# Mon, 10 Jul 2023 20:41:08 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:41:08 GMT
ARG ODOO_SHA=e525263145212a77ae35a6f80a3f269d52547226
# Mon, 10 Jul 2023 20:42:23 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=e525263145212a77ae35a6f80a3f269d52547226
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:42:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:42:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:42:27 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=e525263145212a77ae35a6f80a3f269d52547226
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:42:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:42:27 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:42:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:42:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:42:28 GMT
USER odoo
# Mon, 10 Jul 2023 20:42:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:42:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecec17eceb6c3674130e046a294357d03d0a4328163573bf205d3e3313a92b3`  
		Last Modified: Tue, 04 Jul 2023 16:59:33 GMT  
		Size: 220.3 MB (220302668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3ff92d45f28abea1907822b9422b22044c4d8c3ea79cbbd890eedec7d2a2b`  
		Last Modified: Tue, 04 Jul 2023 16:59:09 GMT  
		Size: 2.6 MB (2576221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae451cd3af67981acb0b0f325d282607dfb4442750de0e5ef333d984e2ecae`  
		Last Modified: Tue, 04 Jul 2023 16:59:08 GMT  
		Size: 453.8 KB (453828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8927f6314226a62b3db4bd83c2fbcd2dd5ab23b24570743a2c68defdf05bded3`  
		Last Modified: Mon, 10 Jul 2023 20:45:38 GMT  
		Size: 307.1 MB (307066386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea1e74e4dc33cefe11e4d0fe527ee60dceddfeafa9177e5d23de9135b376e5`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc713c8b710d09e146a15ee77b90af766f5c4c3fba0e6d03580526659e72863a`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717135cfe2901c375f06c8188476a32f4ecca325e93c814edcd2be405e94bca2`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73215d6e65e3d201e121d89c4476ccd9c94697114a1eff68806476c0c2b36109`  
		Last Modified: Mon, 10 Jul 2023 20:45:05 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:0b3d22d0c2afd895eb3a04779705fe14f5ba597ced0c9d6cfeedf9a169f4383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f4e3304c28a8e3fa3555f99635e3aecd303149a21c98cec00567504b1dfe932c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574831560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb938bd6d0628bb654e5cb256c556b45ae77f877fad7b3d17a5ca00902273b40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:48:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:50:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:50:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:50:14 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:50:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 10 Jul 2023 20:39:14 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:39:15 GMT
ARG ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
# Mon, 10 Jul 2023 20:40:49 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:40:54 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:40:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:40:55 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:40:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:40:55 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:40:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:40:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:40:55 GMT
USER odoo
# Mon, 10 Jul 2023 20:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:40:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2c7d3da2fbd2d726a8fe59c3992de7895dd89fadab551a495625fa48e8c5e7`  
		Last Modified: Tue, 04 Jul 2023 16:58:45 GMT  
		Size: 221.0 MB (220991764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd6f861e7cdc6a59484c202dc889a03e05ccea95d4463d5151d5d4d453f418b`  
		Last Modified: Tue, 04 Jul 2023 16:58:21 GMT  
		Size: 2.6 MB (2579607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9919e5999fecf8a9ca11971e06d8a9e2cd6d34b66814734d1133fa1a15c18974`  
		Last Modified: Tue, 04 Jul 2023 16:58:20 GMT  
		Size: 453.8 KB (453840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ac3d0bb1e1aa0ed0941faa8a8206a0f49c32bafb88e9d8fcf6ab7a304b588`  
		Last Modified: Mon, 10 Jul 2023 20:44:53 GMT  
		Size: 319.4 MB (319386498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de0e241b3a3ffd3cb2fbd05b8f2cf84cc57e053833cebeb9b9515c03938bd65`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b411196aa06dd24210b3feb93df1a2396ea6df672676c52c20a1f90dffefd69`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d694c4040d12f5d0f1b19d06df4edf3e832466ee01cfd70ba19705c878f60d`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa915879d7684a699a53898248c222966085823d59f011e1c9cf091629c58c`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:0b3d22d0c2afd895eb3a04779705fe14f5ba597ced0c9d6cfeedf9a169f4383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f4e3304c28a8e3fa3555f99635e3aecd303149a21c98cec00567504b1dfe932c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574831560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb938bd6d0628bb654e5cb256c556b45ae77f877fad7b3d17a5ca00902273b40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:48:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:50:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:50:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:50:14 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:50:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 10 Jul 2023 20:39:14 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:39:15 GMT
ARG ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
# Mon, 10 Jul 2023 20:40:49 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:40:54 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:40:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:40:55 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:40:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:40:55 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:40:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:40:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:40:55 GMT
USER odoo
# Mon, 10 Jul 2023 20:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:40:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2c7d3da2fbd2d726a8fe59c3992de7895dd89fadab551a495625fa48e8c5e7`  
		Last Modified: Tue, 04 Jul 2023 16:58:45 GMT  
		Size: 221.0 MB (220991764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd6f861e7cdc6a59484c202dc889a03e05ccea95d4463d5151d5d4d453f418b`  
		Last Modified: Tue, 04 Jul 2023 16:58:21 GMT  
		Size: 2.6 MB (2579607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9919e5999fecf8a9ca11971e06d8a9e2cd6d34b66814734d1133fa1a15c18974`  
		Last Modified: Tue, 04 Jul 2023 16:58:20 GMT  
		Size: 453.8 KB (453840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ac3d0bb1e1aa0ed0941faa8a8206a0f49c32bafb88e9d8fcf6ab7a304b588`  
		Last Modified: Mon, 10 Jul 2023 20:44:53 GMT  
		Size: 319.4 MB (319386498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de0e241b3a3ffd3cb2fbd05b8f2cf84cc57e053833cebeb9b9515c03938bd65`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b411196aa06dd24210b3feb93df1a2396ea6df672676c52c20a1f90dffefd69`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d694c4040d12f5d0f1b19d06df4edf3e832466ee01cfd70ba19705c878f60d`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa915879d7684a699a53898248c222966085823d59f011e1c9cf091629c58c`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:0b3d22d0c2afd895eb3a04779705fe14f5ba597ced0c9d6cfeedf9a169f4383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f4e3304c28a8e3fa3555f99635e3aecd303149a21c98cec00567504b1dfe932c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574831560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb938bd6d0628bb654e5cb256c556b45ae77f877fad7b3d17a5ca00902273b40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:48:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 04 Jul 2023 16:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 04 Jul 2023 16:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 16:50:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 04 Jul 2023 16:50:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:50:14 GMT
RUN npm install -g rtlcss
# Tue, 04 Jul 2023 16:50:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 10 Jul 2023 20:39:14 GMT
ARG ODOO_RELEASE=20230710
# Mon, 10 Jul 2023 20:39:15 GMT
ARG ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
# Mon, 10 Jul 2023 20:40:49 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jul 2023 20:40:54 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jul 2023 20:40:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jul 2023 20:40:55 GMT
# ARGS: ODOO_RELEASE=20230710 ODOO_SHA=faf46a6ddcf6a8d4d30a743c389db0e414071ce4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jul 2023 20:40:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jul 2023 20:40:55 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jul 2023 20:40:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jul 2023 20:40:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jul 2023 20:40:55 GMT
USER odoo
# Mon, 10 Jul 2023 20:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 20:40:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2c7d3da2fbd2d726a8fe59c3992de7895dd89fadab551a495625fa48e8c5e7`  
		Last Modified: Tue, 04 Jul 2023 16:58:45 GMT  
		Size: 221.0 MB (220991764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd6f861e7cdc6a59484c202dc889a03e05ccea95d4463d5151d5d4d453f418b`  
		Last Modified: Tue, 04 Jul 2023 16:58:21 GMT  
		Size: 2.6 MB (2579607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9919e5999fecf8a9ca11971e06d8a9e2cd6d34b66814734d1133fa1a15c18974`  
		Last Modified: Tue, 04 Jul 2023 16:58:20 GMT  
		Size: 453.8 KB (453840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ac3d0bb1e1aa0ed0941faa8a8206a0f49c32bafb88e9d8fcf6ab7a304b588`  
		Last Modified: Mon, 10 Jul 2023 20:44:53 GMT  
		Size: 319.4 MB (319386498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de0e241b3a3ffd3cb2fbd05b8f2cf84cc57e053833cebeb9b9515c03938bd65`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b411196aa06dd24210b3feb93df1a2396ea6df672676c52c20a1f90dffefd69`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d694c4040d12f5d0f1b19d06df4edf3e832466ee01cfd70ba19705c878f60d`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa915879d7684a699a53898248c222966085823d59f011e1c9cf091629c58c`  
		Last Modified: Mon, 10 Jul 2023 20:44:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
