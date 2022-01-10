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
$ docker pull odoo@sha256:4f634a386f755ccc1876f868754f8c15ec5c5c17a1f167d6548da0e0f343e27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:996a88cf4fa12e241f3383d949c020df3212d3392f7f8d70929d42c35f32177e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.5 MB (539458269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffaab8969de7352ad6e42d46ca1501c2bfeb6d71cf2a4514ff89f5454bce5db`
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
# Mon, 10 Jan 2022 21:40:59 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:40:59 GMT
ARG ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
# Mon, 10 Jan 2022 21:42:13 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:42:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:42:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:42:17 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:42:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:42:18 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:42:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:42:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:42:19 GMT
USER odoo
# Mon, 10 Jan 2022 21:42:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:42:19 GMT
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
	-	`sha256:ad43c78c8d0e115b572b9ddb7e8f620f00407937fc54ceaba4bd9cd5d0a20c08`  
		Last Modified: Mon, 10 Jan 2022 21:44:33 GMT  
		Size: 291.3 MB (291312546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ea9583ec15681f4636fe5609395be3cf892237a9e311730efa53c637cb12c8`  
		Last Modified: Mon, 10 Jan 2022 21:44:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1b3e725316b07acd368265f1b8112aa96ffaf112f7051c2fbab524f1a7a570`  
		Last Modified: Mon, 10 Jan 2022 21:44:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f92c672775fc897c0b08c2b4ab735ee4521e1abbda1de5dccea4c00a0cef`  
		Last Modified: Mon, 10 Jan 2022 21:44:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace8f1113f06421932b0114d371dd79436b1d6efb4e22b136e42d3a1adfde7e`  
		Last Modified: Mon, 10 Jan 2022 21:44:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:4f634a386f755ccc1876f868754f8c15ec5c5c17a1f167d6548da0e0f343e27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:996a88cf4fa12e241f3383d949c020df3212d3392f7f8d70929d42c35f32177e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.5 MB (539458269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffaab8969de7352ad6e42d46ca1501c2bfeb6d71cf2a4514ff89f5454bce5db`
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
# Mon, 10 Jan 2022 21:40:59 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:40:59 GMT
ARG ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
# Mon, 10 Jan 2022 21:42:13 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:42:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:42:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:42:17 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:42:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:42:18 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:42:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:42:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:42:19 GMT
USER odoo
# Mon, 10 Jan 2022 21:42:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:42:19 GMT
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
	-	`sha256:ad43c78c8d0e115b572b9ddb7e8f620f00407937fc54ceaba4bd9cd5d0a20c08`  
		Last Modified: Mon, 10 Jan 2022 21:44:33 GMT  
		Size: 291.3 MB (291312546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ea9583ec15681f4636fe5609395be3cf892237a9e311730efa53c637cb12c8`  
		Last Modified: Mon, 10 Jan 2022 21:44:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1b3e725316b07acd368265f1b8112aa96ffaf112f7051c2fbab524f1a7a570`  
		Last Modified: Mon, 10 Jan 2022 21:44:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f92c672775fc897c0b08c2b4ab735ee4521e1abbda1de5dccea4c00a0cef`  
		Last Modified: Mon, 10 Jan 2022 21:44:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace8f1113f06421932b0114d371dd79436b1d6efb4e22b136e42d3a1adfde7e`  
		Last Modified: Mon, 10 Jan 2022 21:44:03 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:3e993ec93a47942c5739dffff4e37f9ac85ee8b8e96d2426c0f008b3bced7634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:d576569741c92cadceeac55631fb1c0d5809eb12c7b9e45753c40916270ce91d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529226652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89152df6e5b42b3a79823bbb8af597cbd8322a5ea2b1a90ceb82f1eaba060bdc`
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
# Mon, 10 Jan 2022 21:39:07 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:39:07 GMT
ARG ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
# Mon, 10 Jan 2022 21:40:38 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:40:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:40:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:40:44 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:40:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:40:44 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:40:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:40:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:40:45 GMT
USER odoo
# Mon, 10 Jan 2022 21:40:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:40:45 GMT
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
	-	`sha256:1d0f1614d8840e14e65e31f01b216908711ac14848a8233d73c47cfedd244a0c`  
		Last Modified: Mon, 10 Jan 2022 21:43:50 GMT  
		Size: 275.0 MB (275035524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1fba85d7e724930fc2a971057588229797c0e8fdc9cb7b162ee645599579a8`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c105da56ccedfe7274041127cb729b0664a5e919c7bf0060b88c2841bdd144`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c33149cfe7d38adc1bed251b1bbd8d0278baf937ffd86e8484743a749f23258`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23179b26adc88d92cbea26028b0c6d6ad2f9b277d10d5d44e8d7ff4a27fbfba5`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:3e993ec93a47942c5739dffff4e37f9ac85ee8b8e96d2426c0f008b3bced7634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:d576569741c92cadceeac55631fb1c0d5809eb12c7b9e45753c40916270ce91d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529226652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89152df6e5b42b3a79823bbb8af597cbd8322a5ea2b1a90ceb82f1eaba060bdc`
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
# Mon, 10 Jan 2022 21:39:07 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:39:07 GMT
ARG ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
# Mon, 10 Jan 2022 21:40:38 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:40:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:40:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:40:44 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:40:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:40:44 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:40:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:40:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:40:45 GMT
USER odoo
# Mon, 10 Jan 2022 21:40:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:40:45 GMT
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
	-	`sha256:1d0f1614d8840e14e65e31f01b216908711ac14848a8233d73c47cfedd244a0c`  
		Last Modified: Mon, 10 Jan 2022 21:43:50 GMT  
		Size: 275.0 MB (275035524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1fba85d7e724930fc2a971057588229797c0e8fdc9cb7b162ee645599579a8`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c105da56ccedfe7274041127cb729b0664a5e919c7bf0060b88c2841bdd144`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c33149cfe7d38adc1bed251b1bbd8d0278baf937ffd86e8484743a749f23258`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23179b26adc88d92cbea26028b0c6d6ad2f9b277d10d5d44e8d7ff4a27fbfba5`  
		Last Modified: Mon, 10 Jan 2022 21:43:18 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:0a01cdf793c71e6d02b8f4898bd05d3a08ad643641f56abded84040748acdd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ea29569e7dff76ab50c3aadac4e55add66f4705c409f9d1a449b2ac6658df2e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548461841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec44b6ece60c08e0a59ae846e2fea8cf254407cd5a9fbff85a10751d729cd9a`
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
# Mon, 10 Jan 2022 21:37:28 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:37:28 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Mon, 10 Jan 2022 21:38:57 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:38:59 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:38:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:39:00 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:39:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:39:00 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:39:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:39:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:39:01 GMT
USER odoo
# Mon, 10 Jan 2022 21:39:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:39:01 GMT
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
	-	`sha256:2b0592d1dd22fa82886ae4a5433d66b5530030b6992db01d40b523f74f037e6a`  
		Last Modified: Mon, 10 Jan 2022 21:43:05 GMT  
		Size: 293.9 MB (293887520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8748db5a0de1593523ee68f2e1f0ee16afe8518060f90b3c700c7cc6bbafd5`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032e67583c8156ac7dc1552b99541192b44ad66bcfff6bef13258e8f7fe9f3c7`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3835c59c4bdc369f06990c744de48dab94185dbfb2a7386da675e0dac7f0c`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216b105a8b102f9cb85873ccd47c9fb2ebe1dfc09b091e605154cc0808355de1`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:0a01cdf793c71e6d02b8f4898bd05d3a08ad643641f56abded84040748acdd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ea29569e7dff76ab50c3aadac4e55add66f4705c409f9d1a449b2ac6658df2e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548461841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec44b6ece60c08e0a59ae846e2fea8cf254407cd5a9fbff85a10751d729cd9a`
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
# Mon, 10 Jan 2022 21:37:28 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:37:28 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Mon, 10 Jan 2022 21:38:57 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:38:59 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:38:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:39:00 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:39:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:39:00 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:39:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:39:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:39:01 GMT
USER odoo
# Mon, 10 Jan 2022 21:39:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:39:01 GMT
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
	-	`sha256:2b0592d1dd22fa82886ae4a5433d66b5530030b6992db01d40b523f74f037e6a`  
		Last Modified: Mon, 10 Jan 2022 21:43:05 GMT  
		Size: 293.9 MB (293887520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8748db5a0de1593523ee68f2e1f0ee16afe8518060f90b3c700c7cc6bbafd5`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032e67583c8156ac7dc1552b99541192b44ad66bcfff6bef13258e8f7fe9f3c7`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3835c59c4bdc369f06990c744de48dab94185dbfb2a7386da675e0dac7f0c`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216b105a8b102f9cb85873ccd47c9fb2ebe1dfc09b091e605154cc0808355de1`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:0a01cdf793c71e6d02b8f4898bd05d3a08ad643641f56abded84040748acdd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ea29569e7dff76ab50c3aadac4e55add66f4705c409f9d1a449b2ac6658df2e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548461841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec44b6ece60c08e0a59ae846e2fea8cf254407cd5a9fbff85a10751d729cd9a`
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
# Mon, 10 Jan 2022 21:37:28 GMT
ARG ODOO_RELEASE=20220110
# Mon, 10 Jan 2022 21:37:28 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Mon, 10 Jan 2022 21:38:57 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 10 Jan 2022 21:38:59 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 10 Jan 2022 21:38:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 10 Jan 2022 21:39:00 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 10 Jan 2022 21:39:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 10 Jan 2022 21:39:00 GMT
EXPOSE 8069 8071 8072
# Mon, 10 Jan 2022 21:39:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 10 Jan 2022 21:39:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 10 Jan 2022 21:39:01 GMT
USER odoo
# Mon, 10 Jan 2022 21:39:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jan 2022 21:39:01 GMT
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
	-	`sha256:2b0592d1dd22fa82886ae4a5433d66b5530030b6992db01d40b523f74f037e6a`  
		Last Modified: Mon, 10 Jan 2022 21:43:05 GMT  
		Size: 293.9 MB (293887520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8748db5a0de1593523ee68f2e1f0ee16afe8518060f90b3c700c7cc6bbafd5`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032e67583c8156ac7dc1552b99541192b44ad66bcfff6bef13258e8f7fe9f3c7`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b3835c59c4bdc369f06990c744de48dab94185dbfb2a7386da675e0dac7f0c`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216b105a8b102f9cb85873ccd47c9fb2ebe1dfc09b091e605154cc0808355de1`  
		Last Modified: Mon, 10 Jan 2022 21:42:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
