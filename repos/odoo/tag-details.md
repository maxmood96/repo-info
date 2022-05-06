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
$ docker pull odoo@sha256:0d87974113f001c84a3ff6d14a318a391617b495487151dbaa118078e510c46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:919b0ab05cb48885fce7ce7bba7bee7c736f3f2385649097ec8ba9c38f04364e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (539971086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf53f9fda2378d4be09c4d360c3c19e6436d6e41e22af1c2cfd62933306ff44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:50:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:50:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:50:41 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:50:41 GMT
ENV ODOO_VERSION=13.0
# Fri, 06 May 2022 19:23:20 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:23:20 GMT
ARG ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
# Fri, 06 May 2022 19:24:31 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:24:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:24:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:24:35 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:24:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:24:35 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:24:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:24:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:24:36 GMT
USER odoo
# Fri, 06 May 2022 19:24:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:24:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb5c2f3aa8570028e1481e683ce676526f2f383e1d583fc8fe80151c3d75a46`  
		Last Modified: Wed, 20 Apr 2022 12:54:29 GMT  
		Size: 207.1 MB (207144149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed24c51a5113dc123abfe7c3ae5947e181a730ec5220f51852ce8b7cb296d9`  
		Last Modified: Wed, 20 Apr 2022 12:54:07 GMT  
		Size: 13.4 MB (13438172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e9a8cb5ff656fd7d11d44d86b540b5429edfa5d9d2ce063061e5f2a027b2b`  
		Last Modified: Wed, 20 Apr 2022 12:54:05 GMT  
		Size: 458.4 KB (458398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69861d0610e8be9194028b3d37b76390371784d2fb9141f168f3e343a901660c`  
		Last Modified: Fri, 06 May 2022 19:26:55 GMT  
		Size: 291.8 MB (291787235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246a22859fbf0f17c13ef319a162f0106c58af80fb12e9dc84725ab97ab093fc`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf877e14dd93e92b50631ec5e55b45a89d88daadcc76ed968f5fa878f1e6777`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40048b6d91fd845aff97be87d1329160208df846cb5c63bbc68167dabfca9a40`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1710f8e650f9cb723d6bbf80152339ff5f49c53922da3d27a5796c0ce3e66927`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:0d87974113f001c84a3ff6d14a318a391617b495487151dbaa118078e510c46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:919b0ab05cb48885fce7ce7bba7bee7c736f3f2385649097ec8ba9c38f04364e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (539971086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf53f9fda2378d4be09c4d360c3c19e6436d6e41e22af1c2cfd62933306ff44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:50:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:50:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:50:41 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:50:41 GMT
ENV ODOO_VERSION=13.0
# Fri, 06 May 2022 19:23:20 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:23:20 GMT
ARG ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
# Fri, 06 May 2022 19:24:31 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:24:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:24:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:24:35 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:24:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:24:35 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:24:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:24:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:24:36 GMT
USER odoo
# Fri, 06 May 2022 19:24:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:24:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb5c2f3aa8570028e1481e683ce676526f2f383e1d583fc8fe80151c3d75a46`  
		Last Modified: Wed, 20 Apr 2022 12:54:29 GMT  
		Size: 207.1 MB (207144149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ed24c51a5113dc123abfe7c3ae5947e181a730ec5220f51852ce8b7cb296d9`  
		Last Modified: Wed, 20 Apr 2022 12:54:07 GMT  
		Size: 13.4 MB (13438172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2e9a8cb5ff656fd7d11d44d86b540b5429edfa5d9d2ce063061e5f2a027b2b`  
		Last Modified: Wed, 20 Apr 2022 12:54:05 GMT  
		Size: 458.4 KB (458398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69861d0610e8be9194028b3d37b76390371784d2fb9141f168f3e343a901660c`  
		Last Modified: Fri, 06 May 2022 19:26:55 GMT  
		Size: 291.8 MB (291787235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246a22859fbf0f17c13ef319a162f0106c58af80fb12e9dc84725ab97ab093fc`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf877e14dd93e92b50631ec5e55b45a89d88daadcc76ed968f5fa878f1e6777`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40048b6d91fd845aff97be87d1329160208df846cb5c63bbc68167dabfca9a40`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1710f8e650f9cb723d6bbf80152339ff5f49c53922da3d27a5796c0ce3e66927`  
		Last Modified: Fri, 06 May 2022 19:26:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c21fb7d72dd80611749b271ca8ffb4ddd46d371acef8df9b30d7ddd397fe65a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:4dbcf709ba264b110b086a52d9b3b8ff5354b618f3e7d8253cab42d01786d374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.0 MB (530018117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aad4c762977ea3f77fe8fd9e2d5308df2536ca4eace90f307d56845da866d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:47:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:47:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:47:55 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:47:56 GMT
ENV ODOO_VERSION=14.0
# Fri, 06 May 2022 19:21:57 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:21:57 GMT
ARG ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
# Fri, 06 May 2022 19:23:08 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:23:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:23:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:23:12 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:23:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:23:12 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:23:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:23:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:23:13 GMT
USER odoo
# Fri, 06 May 2022 19:23:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:23:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0b3a5b3ccf6bc33961621c8b4217adc5f5ef26d7b92c47c8c39a8820fd58b`  
		Last Modified: Wed, 20 Apr 2022 12:53:38 GMT  
		Size: 213.2 MB (213177837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b2adc658049f20fffa9059922d790f2cc75e2fc5db14b3c1b77043b486b694`  
		Last Modified: Wed, 20 Apr 2022 12:53:16 GMT  
		Size: 13.4 MB (13440548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafa09d0f12a0ed57ad93fe02efadcc57e517a8c1b2abf6d42c04e6b5031e65`  
		Last Modified: Wed, 20 Apr 2022 12:53:13 GMT  
		Size: 458.5 KB (458493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241a9037e373200aab5ed7f37aa3a6546168f3218fdbcb359d3381e9156911c6`  
		Last Modified: Fri, 06 May 2022 19:26:14 GMT  
		Size: 275.8 MB (275798114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0de85052a1f4a18817e561e24bd26df65127aed305098a6a2693615a9a5166`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b505c0975458d02bc30727eed1fb5ed8e5f9fe6d64b5e63af57e68a7fe508cd`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba53fa51cd5011f3c7c3c431e3a52b44fc0cdace86d6735f367bd058cecfbbb`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6b9cf27c1a40186b897ec79cacaee106605f9fb6e55e8b69b84fdaacedeb47`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c21fb7d72dd80611749b271ca8ffb4ddd46d371acef8df9b30d7ddd397fe65a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:4dbcf709ba264b110b086a52d9b3b8ff5354b618f3e7d8253cab42d01786d374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.0 MB (530018117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aad4c762977ea3f77fe8fd9e2d5308df2536ca4eace90f307d56845da866d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:46:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:46:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:46:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:47:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:47:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:47:55 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:47:56 GMT
ENV ODOO_VERSION=14.0
# Fri, 06 May 2022 19:21:57 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:21:57 GMT
ARG ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
# Fri, 06 May 2022 19:23:08 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:23:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:23:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:23:12 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:23:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:23:12 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:23:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:23:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:23:13 GMT
USER odoo
# Fri, 06 May 2022 19:23:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:23:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef0b3a5b3ccf6bc33961621c8b4217adc5f5ef26d7b92c47c8c39a8820fd58b`  
		Last Modified: Wed, 20 Apr 2022 12:53:38 GMT  
		Size: 213.2 MB (213177837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b2adc658049f20fffa9059922d790f2cc75e2fc5db14b3c1b77043b486b694`  
		Last Modified: Wed, 20 Apr 2022 12:53:16 GMT  
		Size: 13.4 MB (13440548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dafa09d0f12a0ed57ad93fe02efadcc57e517a8c1b2abf6d42c04e6b5031e65`  
		Last Modified: Wed, 20 Apr 2022 12:53:13 GMT  
		Size: 458.5 KB (458493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241a9037e373200aab5ed7f37aa3a6546168f3218fdbcb359d3381e9156911c6`  
		Last Modified: Fri, 06 May 2022 19:26:14 GMT  
		Size: 275.8 MB (275798114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0de85052a1f4a18817e561e24bd26df65127aed305098a6a2693615a9a5166`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b505c0975458d02bc30727eed1fb5ed8e5f9fe6d64b5e63af57e68a7fe508cd`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba53fa51cd5011f3c7c3c431e3a52b44fc0cdace86d6735f367bd058cecfbbb`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6b9cf27c1a40186b897ec79cacaee106605f9fb6e55e8b69b84fdaacedeb47`  
		Last Modified: Fri, 06 May 2022 19:25:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:4ed6c23cfe09db46a0595334f412a97376eb5f7187cb84b6393e9bd5f98595b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:442c19b55dda9b1c807d472aac3afc4f27ef4a286c8303ce05b87903f6c77c01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552375098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaff58885d7c6cc355db93bcfc9ace389eec167e89d13409c3103e1e7d5dac4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:43:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:43:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:44:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:44:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:44:52 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:44:52 GMT
ENV ODOO_VERSION=15.0
# Fri, 06 May 2022 19:20:34 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:20:34 GMT
ARG ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
# Fri, 06 May 2022 19:21:49 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:21:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:21:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:21:54 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:21:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:21:54 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:21:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:21:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:21:55 GMT
USER odoo
# Fri, 06 May 2022 19:21:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:21:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f1aac8f860c1d54f3f94ccc883be166c671639bb052e7754baf4d6032ab4b3`  
		Last Modified: Wed, 20 Apr 2022 12:52:49 GMT  
		Size: 220.3 MB (220300936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875665d357afcc2f5c5593ae40db6baed8f4446ec9b8dca77d5605a49495e0cb`  
		Last Modified: Wed, 20 Apr 2022 12:52:24 GMT  
		Size: 2.5 MB (2510123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af9a5928702128a35bd3b53d8a01c591d7884eda973ecebcd3d765abeab07b8`  
		Last Modified: Wed, 20 Apr 2022 12:52:23 GMT  
		Size: 451.8 KB (451820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b94c222ba92f0c934b1b2099ff0406eadca27f51b26fae0e88356803b29cd8`  
		Last Modified: Fri, 06 May 2022 19:25:29 GMT  
		Size: 297.7 MB (297730781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b930edd98cc1d6703b4894f84016700340304408030aef8f0cef0d66c05d1b8`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b965855a9b662087a590f7f5a73f004fa36e985e7b0909c14632769d1952a0`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bf3e1c5956d31544a8e5f5e176b42ef98ae8ce97aab96135604687b273a246`  
		Last Modified: Fri, 06 May 2022 19:24:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e52893534e54c34cc9123bcb4b48914d7dc5dba76e4e7dc1f24cb25eb4a4d20`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:4ed6c23cfe09db46a0595334f412a97376eb5f7187cb84b6393e9bd5f98595b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:442c19b55dda9b1c807d472aac3afc4f27ef4a286c8303ce05b87903f6c77c01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552375098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaff58885d7c6cc355db93bcfc9ace389eec167e89d13409c3103e1e7d5dac4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:43:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:43:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:44:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:44:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:44:52 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:44:52 GMT
ENV ODOO_VERSION=15.0
# Fri, 06 May 2022 19:20:34 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:20:34 GMT
ARG ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
# Fri, 06 May 2022 19:21:49 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:21:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:21:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:21:54 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:21:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:21:54 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:21:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:21:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:21:55 GMT
USER odoo
# Fri, 06 May 2022 19:21:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:21:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f1aac8f860c1d54f3f94ccc883be166c671639bb052e7754baf4d6032ab4b3`  
		Last Modified: Wed, 20 Apr 2022 12:52:49 GMT  
		Size: 220.3 MB (220300936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875665d357afcc2f5c5593ae40db6baed8f4446ec9b8dca77d5605a49495e0cb`  
		Last Modified: Wed, 20 Apr 2022 12:52:24 GMT  
		Size: 2.5 MB (2510123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af9a5928702128a35bd3b53d8a01c591d7884eda973ecebcd3d765abeab07b8`  
		Last Modified: Wed, 20 Apr 2022 12:52:23 GMT  
		Size: 451.8 KB (451820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b94c222ba92f0c934b1b2099ff0406eadca27f51b26fae0e88356803b29cd8`  
		Last Modified: Fri, 06 May 2022 19:25:29 GMT  
		Size: 297.7 MB (297730781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b930edd98cc1d6703b4894f84016700340304408030aef8f0cef0d66c05d1b8`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b965855a9b662087a590f7f5a73f004fa36e985e7b0909c14632769d1952a0`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bf3e1c5956d31544a8e5f5e176b42ef98ae8ce97aab96135604687b273a246`  
		Last Modified: Fri, 06 May 2022 19:24:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e52893534e54c34cc9123bcb4b48914d7dc5dba76e4e7dc1f24cb25eb4a4d20`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:4ed6c23cfe09db46a0595334f412a97376eb5f7187cb84b6393e9bd5f98595b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:442c19b55dda9b1c807d472aac3afc4f27ef4a286c8303ce05b87903f6c77c01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552375098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaff58885d7c6cc355db93bcfc9ace389eec167e89d13409c3103e1e7d5dac4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:43:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Apr 2022 12:43:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Apr 2022 12:43:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:44:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Apr 2022 12:44:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:44:52 GMT
RUN npm install -g rtlcss
# Wed, 20 Apr 2022 12:44:52 GMT
ENV ODOO_VERSION=15.0
# Fri, 06 May 2022 19:20:34 GMT
ARG ODOO_RELEASE=20220506
# Fri, 06 May 2022 19:20:34 GMT
ARG ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
# Fri, 06 May 2022 19:21:49 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 06 May 2022 19:21:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 06 May 2022 19:21:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 06 May 2022 19:21:54 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 06 May 2022 19:21:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 May 2022 19:21:54 GMT
EXPOSE 8069 8071 8072
# Fri, 06 May 2022 19:21:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 May 2022 19:21:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 06 May 2022 19:21:55 GMT
USER odoo
# Fri, 06 May 2022 19:21:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 May 2022 19:21:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f1aac8f860c1d54f3f94ccc883be166c671639bb052e7754baf4d6032ab4b3`  
		Last Modified: Wed, 20 Apr 2022 12:52:49 GMT  
		Size: 220.3 MB (220300936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875665d357afcc2f5c5593ae40db6baed8f4446ec9b8dca77d5605a49495e0cb`  
		Last Modified: Wed, 20 Apr 2022 12:52:24 GMT  
		Size: 2.5 MB (2510123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af9a5928702128a35bd3b53d8a01c591d7884eda973ecebcd3d765abeab07b8`  
		Last Modified: Wed, 20 Apr 2022 12:52:23 GMT  
		Size: 451.8 KB (451820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b94c222ba92f0c934b1b2099ff0406eadca27f51b26fae0e88356803b29cd8`  
		Last Modified: Fri, 06 May 2022 19:25:29 GMT  
		Size: 297.7 MB (297730781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b930edd98cc1d6703b4894f84016700340304408030aef8f0cef0d66c05d1b8`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b965855a9b662087a590f7f5a73f004fa36e985e7b0909c14632769d1952a0`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bf3e1c5956d31544a8e5f5e176b42ef98ae8ce97aab96135604687b273a246`  
		Last Modified: Fri, 06 May 2022 19:24:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e52893534e54c34cc9123bcb4b48914d7dc5dba76e4e7dc1f24cb25eb4a4d20`  
		Last Modified: Fri, 06 May 2022 19:24:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
