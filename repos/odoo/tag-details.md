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
$ docker pull odoo@sha256:4c0a16fdadebafe15bd02b26ab33ece2dea72170243aec7334d1d5a7566e27e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:7e79321b19fa1ce136d4604ce42de383474b2287687b98ee7fb1b24c70d83caa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (539977028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1c37935d9e0f936019cade86448bbc493e6cf9264d653ba6f962e427263898`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:37:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:37:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:37:29 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:41:18 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:41:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:41:29 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:41:29 GMT
ENV ODOO_VERSION=13.0
# Wed, 11 May 2022 05:41:29 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:41:29 GMT
ARG ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
# Wed, 11 May 2022 05:42:40 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:42:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:42:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:42:44 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:42:44 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:42:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:42:45 GMT
USER odoo
# Wed, 11 May 2022 05:42:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:42:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e6252588f0e6abcf931957ac7bfc2a5e5b32db2ed14dbd6b2e8a66685a5788`  
		Last Modified: Wed, 11 May 2022 05:45:17 GMT  
		Size: 207.1 MB (207143132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0b687cc39be53c1d539fc0c580160e7d11fe3a1d308058504206f40872bf99`  
		Last Modified: Wed, 11 May 2022 05:44:56 GMT  
		Size: 13.4 MB (13438332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471fc1f5680601316e623c4c30bc1211a0b42d586e9a52fd1515c2bb3f4184d5`  
		Last Modified: Wed, 11 May 2022 05:44:53 GMT  
		Size: 468.5 KB (468467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35461c7589e5a0c8689331a843de44a66d35b8c1ffb2e79af297b6878b507d`  
		Last Modified: Wed, 11 May 2022 05:45:24 GMT  
		Size: 291.8 MB (291783907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7820df0500e343557e30b683be0ce75e4f0c987e7bfb34fc72e35e4937c45da8`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ef95c23d6ba66dd86456c2a92d252d09169dccc4d15d7e3f21f5824bb54bd9`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626552e4ca748b447cd0b7172957c931e0e105c66113eb3b9c8c28567b6aee2c`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213db5e35d09d6826c181f2e955d07e2f8acf3a73f84f8afc73cb17be3e98ab5`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:4c0a16fdadebafe15bd02b26ab33ece2dea72170243aec7334d1d5a7566e27e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:7e79321b19fa1ce136d4604ce42de383474b2287687b98ee7fb1b24c70d83caa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (539977028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1c37935d9e0f936019cade86448bbc493e6cf9264d653ba6f962e427263898`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:37:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:37:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:37:29 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:41:18 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:41:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:41:29 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:41:29 GMT
ENV ODOO_VERSION=13.0
# Wed, 11 May 2022 05:41:29 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:41:29 GMT
ARG ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
# Wed, 11 May 2022 05:42:40 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:42:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:42:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:42:44 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=3dcd6300b65a9f644a4dfc20989ae94b4a1f0b75
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:42:44 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:42:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:42:45 GMT
USER odoo
# Wed, 11 May 2022 05:42:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:42:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e6252588f0e6abcf931957ac7bfc2a5e5b32db2ed14dbd6b2e8a66685a5788`  
		Last Modified: Wed, 11 May 2022 05:45:17 GMT  
		Size: 207.1 MB (207143132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0b687cc39be53c1d539fc0c580160e7d11fe3a1d308058504206f40872bf99`  
		Last Modified: Wed, 11 May 2022 05:44:56 GMT  
		Size: 13.4 MB (13438332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471fc1f5680601316e623c4c30bc1211a0b42d586e9a52fd1515c2bb3f4184d5`  
		Last Modified: Wed, 11 May 2022 05:44:53 GMT  
		Size: 468.5 KB (468467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb35461c7589e5a0c8689331a843de44a66d35b8c1ffb2e79af297b6878b507d`  
		Last Modified: Wed, 11 May 2022 05:45:24 GMT  
		Size: 291.8 MB (291783907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7820df0500e343557e30b683be0ce75e4f0c987e7bfb34fc72e35e4937c45da8`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ef95c23d6ba66dd86456c2a92d252d09169dccc4d15d7e3f21f5824bb54bd9`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626552e4ca748b447cd0b7172957c931e0e105c66113eb3b9c8c28567b6aee2c`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213db5e35d09d6826c181f2e955d07e2f8acf3a73f84f8afc73cb17be3e98ab5`  
		Last Modified: Wed, 11 May 2022 05:44:51 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c6595ebcbf38cbbaada38fac3d8df4fbf3dc20ccbd09cc38d1bbc38390642777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:fd8d0c29c381b93ab3d97a55dbc637bb26e2d2c6bbe9e826a4ef25223ed78121
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.0 MB (530030465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4a7504469829d06f9a2c7f87414a8ac164fb8dccb9f691b90305c9b67f6c2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:37:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:37:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:37:29 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:38:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:38:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:38:49 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:38:49 GMT
ENV ODOO_VERSION=14.0
# Wed, 11 May 2022 05:38:49 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:38:49 GMT
ARG ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
# Wed, 11 May 2022 05:40:00 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:40:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:40:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:40:04 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:40:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:40:05 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:40:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:40:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:40:05 GMT
USER odoo
# Wed, 11 May 2022 05:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:40:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18be9ffd7343938551d01a3a348c625c03ca09031fcd3e96756ea392eb19866f`  
		Last Modified: Wed, 11 May 2022 05:44:28 GMT  
		Size: 213.2 MB (213181643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf10be0bcd5e9c9e8630aeb1c60b92f2abcdc6a0d1bc51a41f715cbff2b208`  
		Last Modified: Wed, 11 May 2022 05:44:05 GMT  
		Size: 13.4 MB (13440768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c667279c5c1e86e3868c1fe0d7a90481ceac438eefa2678773f2aeda7cb8153`  
		Last Modified: Wed, 11 May 2022 05:44:03 GMT  
		Size: 468.4 KB (468439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f008747eebcc24f8e33902402cf0680150404ad6a845ba997e00a670c7431a8f`  
		Last Modified: Wed, 11 May 2022 05:44:35 GMT  
		Size: 275.8 MB (275796432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e165c4d63f6dde80580023ea05c7aa74bcb4135e440a024a56ff79b05289c22e`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5a3b08afe72a12defbe290c33c833804a787ce45699f40a8b4dde6c194d006`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f26e2c9df17030a3d7b38cb020fead2cb6057bcee31899bf514e21989c23043`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb27696d89b2ac355a0fddf88b037d8fc2ab4f298a5fe3c699d99c17dfa74a33`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c6595ebcbf38cbbaada38fac3d8df4fbf3dc20ccbd09cc38d1bbc38390642777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:fd8d0c29c381b93ab3d97a55dbc637bb26e2d2c6bbe9e826a4ef25223ed78121
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.0 MB (530030465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4a7504469829d06f9a2c7f87414a8ac164fb8dccb9f691b90305c9b67f6c2c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:37:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:37:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:37:29 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:38:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:38:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:38:49 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:38:49 GMT
ENV ODOO_VERSION=14.0
# Wed, 11 May 2022 05:38:49 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:38:49 GMT
ARG ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
# Wed, 11 May 2022 05:40:00 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:40:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:40:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:40:04 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=ac816b4769fe14b9a7894790fcf7d98bcb6c3741
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:40:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:40:05 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:40:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:40:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:40:05 GMT
USER odoo
# Wed, 11 May 2022 05:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:40:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18be9ffd7343938551d01a3a348c625c03ca09031fcd3e96756ea392eb19866f`  
		Last Modified: Wed, 11 May 2022 05:44:28 GMT  
		Size: 213.2 MB (213181643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf10be0bcd5e9c9e8630aeb1c60b92f2abcdc6a0d1bc51a41f715cbff2b208`  
		Last Modified: Wed, 11 May 2022 05:44:05 GMT  
		Size: 13.4 MB (13440768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c667279c5c1e86e3868c1fe0d7a90481ceac438eefa2678773f2aeda7cb8153`  
		Last Modified: Wed, 11 May 2022 05:44:03 GMT  
		Size: 468.4 KB (468439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f008747eebcc24f8e33902402cf0680150404ad6a845ba997e00a670c7431a8f`  
		Last Modified: Wed, 11 May 2022 05:44:35 GMT  
		Size: 275.8 MB (275796432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e165c4d63f6dde80580023ea05c7aa74bcb4135e440a024a56ff79b05289c22e`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5a3b08afe72a12defbe290c33c833804a787ce45699f40a8b4dde6c194d006`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f26e2c9df17030a3d7b38cb020fead2cb6057bcee31899bf514e21989c23043`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb27696d89b2ac355a0fddf88b037d8fc2ab4f298a5fe3c699d99c17dfa74a33`  
		Last Modified: Wed, 11 May 2022 05:44:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:7fbd0d01d2e483441076ccf4461178d90a454ee080a69d466e75eba0334c6c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:485313b5cc47c3b1c1212b68b4275b1324b908df03ac6d0b3b8f833b611b7d8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552393862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a469d18da977d381c4e5a8d91f17642a5dfc682c97c5f1e1fe8688df8088e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:34:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:34:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:34:51 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:35:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:35:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:36:00 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:36:00 GMT
ENV ODOO_VERSION=15.0
# Wed, 11 May 2022 05:36:00 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:36:00 GMT
ARG ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
# Wed, 11 May 2022 05:37:14 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:37:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:37:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:37:19 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:37:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:37:19 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:37:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:37:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:37:20 GMT
USER odoo
# Wed, 11 May 2022 05:37:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:37:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26162ed3131197f6879615fefb5c8aa8bc5c0c135769db733a201cfb52c67be`  
		Last Modified: Wed, 11 May 2022 05:43:40 GMT  
		Size: 220.3 MB (220307699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486a4342c69cbaf3a5a1133c9f3eedbc817147246d4232cce876bd2843070a54`  
		Last Modified: Wed, 11 May 2022 05:43:14 GMT  
		Size: 2.5 MB (2510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978adca0c78b0c610ce566793437791b380153b4ae98d4551063a87572379869`  
		Last Modified: Wed, 11 May 2022 05:43:14 GMT  
		Size: 462.1 KB (462052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d2e850b6d4ed236390c8433256facc9048805efdafd6912cbbbf207c355286`  
		Last Modified: Wed, 11 May 2022 05:43:47 GMT  
		Size: 297.7 MB (297732069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ca4e2f3349ae31b455459b34f046d4345ea9db115f3cb340bd4b67925c01d`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca25c4537480d847b8f76870f5f15681ce92f660b976daa860cfbbda33b631`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f385cd4f804d55e59f7469a4ef45440a388eacdb0b782eebfc01fc2ad9c5dbf`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3363243f62e3063b19870591f4efde33ffc87ed69b1f7531f53628306ad7fba`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:7fbd0d01d2e483441076ccf4461178d90a454ee080a69d466e75eba0334c6c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:485313b5cc47c3b1c1212b68b4275b1324b908df03ac6d0b3b8f833b611b7d8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552393862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a469d18da977d381c4e5a8d91f17642a5dfc682c97c5f1e1fe8688df8088e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:34:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:34:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:34:51 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:35:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:35:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:36:00 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:36:00 GMT
ENV ODOO_VERSION=15.0
# Wed, 11 May 2022 05:36:00 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:36:00 GMT
ARG ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
# Wed, 11 May 2022 05:37:14 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:37:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:37:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:37:19 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:37:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:37:19 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:37:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:37:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:37:20 GMT
USER odoo
# Wed, 11 May 2022 05:37:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:37:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26162ed3131197f6879615fefb5c8aa8bc5c0c135769db733a201cfb52c67be`  
		Last Modified: Wed, 11 May 2022 05:43:40 GMT  
		Size: 220.3 MB (220307699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486a4342c69cbaf3a5a1133c9f3eedbc817147246d4232cce876bd2843070a54`  
		Last Modified: Wed, 11 May 2022 05:43:14 GMT  
		Size: 2.5 MB (2510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978adca0c78b0c610ce566793437791b380153b4ae98d4551063a87572379869`  
		Last Modified: Wed, 11 May 2022 05:43:14 GMT  
		Size: 462.1 KB (462052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d2e850b6d4ed236390c8433256facc9048805efdafd6912cbbbf207c355286`  
		Last Modified: Wed, 11 May 2022 05:43:47 GMT  
		Size: 297.7 MB (297732069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ca4e2f3349ae31b455459b34f046d4345ea9db115f3cb340bd4b67925c01d`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca25c4537480d847b8f76870f5f15681ce92f660b976daa860cfbbda33b631`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f385cd4f804d55e59f7469a4ef45440a388eacdb0b782eebfc01fc2ad9c5dbf`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3363243f62e3063b19870591f4efde33ffc87ed69b1f7531f53628306ad7fba`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7fbd0d01d2e483441076ccf4461178d90a454ee080a69d466e75eba0334c6c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:485313b5cc47c3b1c1212b68b4275b1324b908df03ac6d0b3b8f833b611b7d8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.4 MB (552393862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a469d18da977d381c4e5a8d91f17642a5dfc682c97c5f1e1fe8688df8088e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:34:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 11 May 2022 05:34:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 11 May 2022 05:34:51 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:35:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 11 May 2022 05:35:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:36:00 GMT
RUN npm install -g rtlcss
# Wed, 11 May 2022 05:36:00 GMT
ENV ODOO_VERSION=15.0
# Wed, 11 May 2022 05:36:00 GMT
ARG ODOO_RELEASE=20220506
# Wed, 11 May 2022 05:36:00 GMT
ARG ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
# Wed, 11 May 2022 05:37:14 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 11 May 2022 05:37:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 11 May 2022 05:37:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 11 May 2022 05:37:19 GMT
# ARGS: ODOO_RELEASE=20220506 ODOO_SHA=5c6b3e4f33d03472e6ee668b340984b7661de14a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 11 May 2022 05:37:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 11 May 2022 05:37:19 GMT
EXPOSE 8069 8071 8072
# Wed, 11 May 2022 05:37:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 11 May 2022 05:37:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 11 May 2022 05:37:20 GMT
USER odoo
# Wed, 11 May 2022 05:37:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 May 2022 05:37:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26162ed3131197f6879615fefb5c8aa8bc5c0c135769db733a201cfb52c67be`  
		Last Modified: Wed, 11 May 2022 05:43:40 GMT  
		Size: 220.3 MB (220307699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486a4342c69cbaf3a5a1133c9f3eedbc817147246d4232cce876bd2843070a54`  
		Last Modified: Wed, 11 May 2022 05:43:14 GMT  
		Size: 2.5 MB (2510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978adca0c78b0c610ce566793437791b380153b4ae98d4551063a87572379869`  
		Last Modified: Wed, 11 May 2022 05:43:14 GMT  
		Size: 462.1 KB (462052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d2e850b6d4ed236390c8433256facc9048805efdafd6912cbbbf207c355286`  
		Last Modified: Wed, 11 May 2022 05:43:47 GMT  
		Size: 297.7 MB (297732069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ca4e2f3349ae31b455459b34f046d4345ea9db115f3cb340bd4b67925c01d`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca25c4537480d847b8f76870f5f15681ce92f660b976daa860cfbbda33b631`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f385cd4f804d55e59f7469a4ef45440a388eacdb0b782eebfc01fc2ad9c5dbf`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3363243f62e3063b19870591f4efde33ffc87ed69b1f7531f53628306ad7fba`  
		Last Modified: Wed, 11 May 2022 05:43:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
