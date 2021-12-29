<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:latest`](#odoolatest)

## `odoo:13`

```console
$ docker pull odoo@sha256:af9590043aff26503209366ba11bef36ff35e28c2a996a53e77aba9d768d06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:243d0058c83dbd861de2d960bff80fd34b47c03c1780cf343cc34f4393abf1d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539401955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dce716ec0447597b047d57acc0e6f9dba338da5e24dc271f86e75fc7df418fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:25:02 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:25:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:25:19 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:25:19 GMT
ENV ODOO_VERSION=13.0
# Wed, 29 Dec 2021 19:35:00 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:35:00 GMT
ARG ODOO_SHA=7824405bb0f2752a9f7f73a07661b1fcd3d09c69
# Wed, 29 Dec 2021 19:36:16 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=7824405bb0f2752a9f7f73a07661b1fcd3d09c69
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:36:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:36:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:36:20 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=7824405bb0f2752a9f7f73a07661b1fcd3d09c69
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:36:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:36:21 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:36:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:36:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:36:21 GMT
USER odoo
# Wed, 29 Dec 2021 19:36:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:36:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d7983b91605c2e8a3cac73cc85ca48790cc3efb1571d857ff46b5671b96cd2`  
		Last Modified: Tue, 21 Dec 2021 19:29:21 GMT  
		Size: 207.1 MB (207130909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0673fc42a3c3aba833b861b907d31819eef5104e4d3d00360399ea3067f7ee0`  
		Last Modified: Tue, 21 Dec 2021 19:28:56 GMT  
		Size: 13.4 MB (13434150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7739cae70db3a175f5335f33dbb8044e12cedf62c7d3f4f6fd31fef19b9d6`  
		Last Modified: Tue, 21 Dec 2021 19:28:53 GMT  
		Size: 424.5 KB (424477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689526c7b7205d1986e616dc7672f4d39ab7ea109b227988e55aee955633919d`  
		Last Modified: Wed, 29 Dec 2021 19:38:53 GMT  
		Size: 291.3 MB (291256227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5dc6b5557e9b9f9b972f0f8419a2d8b88a1798aab28f7d38fd65726100a0ed`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69234225941b3cb0742cd30000475b41f68651af686af2b4ce96a7e2fd9e700`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542092abd1545be79765c6d171610d82a20d87f9a4d30f51e34f7d72bf27464f`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1203ffeba046fca6afbde882642158c317966b8ba21f89ac87459ec39b49b01`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:af9590043aff26503209366ba11bef36ff35e28c2a996a53e77aba9d768d06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:243d0058c83dbd861de2d960bff80fd34b47c03c1780cf343cc34f4393abf1d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.4 MB (539401955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dce716ec0447597b047d57acc0e6f9dba338da5e24dc271f86e75fc7df418fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:25:02 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:25:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:25:19 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:25:19 GMT
ENV ODOO_VERSION=13.0
# Wed, 29 Dec 2021 19:35:00 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:35:00 GMT
ARG ODOO_SHA=7824405bb0f2752a9f7f73a07661b1fcd3d09c69
# Wed, 29 Dec 2021 19:36:16 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=7824405bb0f2752a9f7f73a07661b1fcd3d09c69
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:36:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:36:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:36:20 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=7824405bb0f2752a9f7f73a07661b1fcd3d09c69
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:36:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:36:21 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:36:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:36:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:36:21 GMT
USER odoo
# Wed, 29 Dec 2021 19:36:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:36:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d7983b91605c2e8a3cac73cc85ca48790cc3efb1571d857ff46b5671b96cd2`  
		Last Modified: Tue, 21 Dec 2021 19:29:21 GMT  
		Size: 207.1 MB (207130909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0673fc42a3c3aba833b861b907d31819eef5104e4d3d00360399ea3067f7ee0`  
		Last Modified: Tue, 21 Dec 2021 19:28:56 GMT  
		Size: 13.4 MB (13434150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7739cae70db3a175f5335f33dbb8044e12cedf62c7d3f4f6fd31fef19b9d6`  
		Last Modified: Tue, 21 Dec 2021 19:28:53 GMT  
		Size: 424.5 KB (424477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689526c7b7205d1986e616dc7672f4d39ab7ea109b227988e55aee955633919d`  
		Last Modified: Wed, 29 Dec 2021 19:38:53 GMT  
		Size: 291.3 MB (291256227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5dc6b5557e9b9f9b972f0f8419a2d8b88a1798aab28f7d38fd65726100a0ed`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69234225941b3cb0742cd30000475b41f68651af686af2b4ce96a7e2fd9e700`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542092abd1545be79765c6d171610d82a20d87f9a4d30f51e34f7d72bf27464f`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1203ffeba046fca6afbde882642158c317966b8ba21f89ac87459ec39b49b01`  
		Last Modified: Wed, 29 Dec 2021 19:38:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c8fcfb65eb2a0d977dd4a9c892f90d38e1f2c5737dc724bb6ed4dffc521e20e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:48924613636511df5f975463882f214c359446bd1cc8404993854d5333ebb274
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529236299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e8d6380f7060a5dc6e34e296030fae1f49a678267ddf47eee31e464bf1abe8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:21:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:21:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:21:39 GMT
ENV ODOO_VERSION=14.0
# Wed, 29 Dec 2021 19:33:22 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:33:23 GMT
ARG ODOO_SHA=8ab90c81faec34d60db5cff7a4f47276b6659a0f
# Wed, 29 Dec 2021 19:34:38 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=8ab90c81faec34d60db5cff7a4f47276b6659a0f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:34:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:34:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:34:43 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=8ab90c81faec34d60db5cff7a4f47276b6659a0f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:34:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:34:44 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:34:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:34:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:34:44 GMT
USER odoo
# Wed, 29 Dec 2021 19:34:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:34:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839734d46ac6c7d6d83c758963995a210475151f71764477376223af2bb38950`  
		Last Modified: Tue, 21 Dec 2021 19:28:29 GMT  
		Size: 213.2 MB (213174074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb501610c7e3bdc36fe243d16894877d6e4a1a7dcc18348f023e72526f9147`  
		Last Modified: Tue, 21 Dec 2021 19:28:03 GMT  
		Size: 13.4 MB (13436446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f281d2d1af4d3c80a6a1e6733c78a9432f65f60433a25b542dbe9c75226fd`  
		Last Modified: Tue, 21 Dec 2021 19:28:00 GMT  
		Size: 424.4 KB (424418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1986bd2bb0d98f341b4240e68df7f37cff230cbca079c4022be6c79c790b52`  
		Last Modified: Wed, 29 Dec 2021 19:38:11 GMT  
		Size: 275.0 MB (275045176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfef69c5909a829d483a57ad689ad97fad2ee4563d39bf8fe847e73c3b817c2`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc929bb00167e630b227b83ca7638ecefee1745e85903e8cb0cec01c4fa342`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7821a446e80c473c849ca6957314dbd0b877d39863cc899049f3c4b73f2dd9c6`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a0f9f2f6be2d7ce2be378172fed1eb9d6f9fa361750faa2540d1b157e8ab59`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c8fcfb65eb2a0d977dd4a9c892f90d38e1f2c5737dc724bb6ed4dffc521e20e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:48924613636511df5f975463882f214c359446bd1cc8404993854d5333ebb274
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529236299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e8d6380f7060a5dc6e34e296030fae1f49a678267ddf47eee31e464bf1abe8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:20:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:20:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:21:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:21:39 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:21:39 GMT
ENV ODOO_VERSION=14.0
# Wed, 29 Dec 2021 19:33:22 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:33:23 GMT
ARG ODOO_SHA=8ab90c81faec34d60db5cff7a4f47276b6659a0f
# Wed, 29 Dec 2021 19:34:38 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=8ab90c81faec34d60db5cff7a4f47276b6659a0f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:34:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:34:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:34:43 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=8ab90c81faec34d60db5cff7a4f47276b6659a0f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:34:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:34:44 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:34:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:34:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:34:44 GMT
USER odoo
# Wed, 29 Dec 2021 19:34:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:34:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839734d46ac6c7d6d83c758963995a210475151f71764477376223af2bb38950`  
		Last Modified: Tue, 21 Dec 2021 19:28:29 GMT  
		Size: 213.2 MB (213174074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfb501610c7e3bdc36fe243d16894877d6e4a1a7dcc18348f023e72526f9147`  
		Last Modified: Tue, 21 Dec 2021 19:28:03 GMT  
		Size: 13.4 MB (13436446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920f281d2d1af4d3c80a6a1e6733c78a9432f65f60433a25b542dbe9c75226fd`  
		Last Modified: Tue, 21 Dec 2021 19:28:00 GMT  
		Size: 424.4 KB (424418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1986bd2bb0d98f341b4240e68df7f37cff230cbca079c4022be6c79c790b52`  
		Last Modified: Wed, 29 Dec 2021 19:38:11 GMT  
		Size: 275.0 MB (275045176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfef69c5909a829d483a57ad689ad97fad2ee4563d39bf8fe847e73c3b817c2`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edc929bb00167e630b227b83ca7638ecefee1745e85903e8cb0cec01c4fa342`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7821a446e80c473c849ca6957314dbd0b877d39863cc899049f3c4b73f2dd9c6`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a0f9f2f6be2d7ce2be378172fed1eb9d6f9fa361750faa2540d1b157e8ab59`  
		Last Modified: Wed, 29 Dec 2021 19:37:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:700ddbfb8e02e6d5bfdaaf041b824c10ac5018966b78d4ae1467246e7b892813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:718e7ebcc4098d9c370a93c40487479fa1ab09058a5b243271138b1143ae35c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.1 MB (548053811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c0b45241f3d069c6922a89cc537606b1c71fdbcbfae3839078b28cf2434753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Wed, 29 Dec 2021 19:31:45 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:31:45 GMT
ARG ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
# Wed, 29 Dec 2021 19:33:05 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:33:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:33:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:33:10 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:33:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:33:11 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:33:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:33:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:33:12 GMT
USER odoo
# Wed, 29 Dec 2021 19:33:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:33:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bce5304190754f2715da8562f293748d41b570e1649bac91e058805a99fca7`  
		Last Modified: Wed, 29 Dec 2021 19:37:24 GMT  
		Size: 293.5 MB (293479489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dae0a0ffcf2dcff69b0a32e8928bb2ee2e222b4308eeddb09c2b9eb8acbc010`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbce0012150b2742b4f16b5e1094e5ca4607f6678a5904a5af0b1791452b4d7`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797337587b0749228dc053a7901f86c0d51955edbb5a005accf6a75a47a4a1d5`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58577c9eeeea9cad651dd869fcf91355fed6030c33a3d61f1e1b7cfe17f523ce`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:700ddbfb8e02e6d5bfdaaf041b824c10ac5018966b78d4ae1467246e7b892813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:718e7ebcc4098d9c370a93c40487479fa1ab09058a5b243271138b1143ae35c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.1 MB (548053811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c0b45241f3d069c6922a89cc537606b1c71fdbcbfae3839078b28cf2434753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Wed, 29 Dec 2021 19:31:45 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:31:45 GMT
ARG ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
# Wed, 29 Dec 2021 19:33:05 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:33:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:33:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:33:10 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:33:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:33:11 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:33:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:33:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:33:12 GMT
USER odoo
# Wed, 29 Dec 2021 19:33:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:33:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bce5304190754f2715da8562f293748d41b570e1649bac91e058805a99fca7`  
		Last Modified: Wed, 29 Dec 2021 19:37:24 GMT  
		Size: 293.5 MB (293479489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dae0a0ffcf2dcff69b0a32e8928bb2ee2e222b4308eeddb09c2b9eb8acbc010`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbce0012150b2742b4f16b5e1094e5ca4607f6678a5904a5af0b1791452b4d7`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797337587b0749228dc053a7901f86c0d51955edbb5a005accf6a75a47a4a1d5`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58577c9eeeea9cad651dd869fcf91355fed6030c33a3d61f1e1b7cfe17f523ce`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:700ddbfb8e02e6d5bfdaaf041b824c10ac5018966b78d4ae1467246e7b892813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:718e7ebcc4098d9c370a93c40487479fa1ab09058a5b243271138b1143ae35c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.1 MB (548053811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c0b45241f3d069c6922a89cc537606b1c71fdbcbfae3839078b28cf2434753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:16:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Dec 2021 19:16:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Dec 2021 19:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 19:17:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 21 Dec 2021 19:17:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:17:51 GMT
RUN npm install -g rtlcss
# Tue, 21 Dec 2021 19:17:51 GMT
ENV ODOO_VERSION=15.0
# Wed, 29 Dec 2021 19:31:45 GMT
ARG ODOO_RELEASE=20211229
# Wed, 29 Dec 2021 19:31:45 GMT
ARG ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
# Wed, 29 Dec 2021 19:33:05 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Dec 2021 19:33:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Dec 2021 19:33:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Dec 2021 19:33:10 GMT
# ARGS: ODOO_RELEASE=20211229 ODOO_SHA=9cb4888027bb55afc7dab2cef2d5ffb4f6ebce12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Dec 2021 19:33:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Dec 2021 19:33:11 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Dec 2021 19:33:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Dec 2021 19:33:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Dec 2021 19:33:12 GMT
USER odoo
# Wed, 29 Dec 2021 19:33:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Dec 2021 19:33:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18f47f481fcbd4d626a886574914b5046fe3d49070c6a0a31cd83608a315562`  
		Last Modified: Tue, 21 Dec 2021 19:27:38 GMT  
		Size: 220.3 MB (220290625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60111a5713506722102fe10c4473131ef16d2d04c11aa7f95ab5a23f3a71755e`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 2.5 MB (2506156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f9f25d81ee861429e96088735eecd4428b8c3276b2d2c397ff274383b7b27`  
		Last Modified: Tue, 21 Dec 2021 19:27:08 GMT  
		Size: 417.5 KB (417452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bce5304190754f2715da8562f293748d41b570e1649bac91e058805a99fca7`  
		Last Modified: Wed, 29 Dec 2021 19:37:24 GMT  
		Size: 293.5 MB (293479489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dae0a0ffcf2dcff69b0a32e8928bb2ee2e222b4308eeddb09c2b9eb8acbc010`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbce0012150b2742b4f16b5e1094e5ca4607f6678a5904a5af0b1791452b4d7`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797337587b0749228dc053a7901f86c0d51955edbb5a005accf6a75a47a4a1d5`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58577c9eeeea9cad651dd869fcf91355fed6030c33a3d61f1e1b7cfe17f523ce`  
		Last Modified: Wed, 29 Dec 2021 19:36:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
