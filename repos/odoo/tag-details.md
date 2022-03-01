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
$ docker pull odoo@sha256:8d79c09ed1d8748ea79c9df3071de5a351b80622f7509b48bb3b59e9a1208cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:002d96b8b8e0a8d62e019d8dc6519016bd6637bf7fa447f60015be6b80e2bdd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539595082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e787cd1c1bc8d04004046b8cd40256167ead1de90d3f86a4cd2f1940369343`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:08:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:08:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:08:35 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:13:55 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:14:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:14:32 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:14:32 GMT
ENV ODOO_VERSION=13.0
# Tue, 01 Mar 2022 14:14:32 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:14:32 GMT
ARG ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
# Tue, 01 Mar 2022 14:16:10 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:16:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:16:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:16:15 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:16:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:16:15 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:16:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:16:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:16:16 GMT
USER odoo
# Tue, 01 Mar 2022 14:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:16:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51d7a5019b187d246e9ae3da10053fb1cfc762a66834ca03e4a95d4f22f6c7c`  
		Last Modified: Tue, 01 Mar 2022 14:19:18 GMT  
		Size: 207.1 MB (207134366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f774b6ab8a9647a0abef7a9cafee8664e94673b07fc70cb6f1dc847a1a8ef6b3`  
		Last Modified: Tue, 01 Mar 2022 14:18:53 GMT  
		Size: 13.4 MB (13438497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92100f15afab684a47d277389605f2ec7c5eee252fd7f30b7d61e621e62ca89`  
		Last Modified: Tue, 01 Mar 2022 14:18:49 GMT  
		Size: 454.1 KB (454054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb385fb721049d7de4a64508464214cf48aaae58dc9450646552ccb8c567ed`  
		Last Modified: Tue, 01 Mar 2022 14:19:24 GMT  
		Size: 291.4 MB (291411961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514ae5cda9f96797ef88db9f287c7505dbf6c27e6ae34ba6349b4ef8fd5a868`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb5b7fa0b645036c64620009b5056985860c58997984db4e0c6ae01b4945624`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926c139f540a84d153254430380da9ec97d4971a4b61b9dd6940bdaeeb159ee4`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e41964727050f432478bf4ae7c7603ac9ebcc5990443de46078e3df8f4fcc9`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:8d79c09ed1d8748ea79c9df3071de5a351b80622f7509b48bb3b59e9a1208cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:002d96b8b8e0a8d62e019d8dc6519016bd6637bf7fa447f60015be6b80e2bdd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539595082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e787cd1c1bc8d04004046b8cd40256167ead1de90d3f86a4cd2f1940369343`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:08:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:08:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:08:35 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:13:55 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:14:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:14:32 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:14:32 GMT
ENV ODOO_VERSION=13.0
# Tue, 01 Mar 2022 14:14:32 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:14:32 GMT
ARG ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
# Tue, 01 Mar 2022 14:16:10 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:16:14 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:16:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:16:15 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:16:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:16:15 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:16:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:16:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:16:16 GMT
USER odoo
# Tue, 01 Mar 2022 14:16:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:16:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51d7a5019b187d246e9ae3da10053fb1cfc762a66834ca03e4a95d4f22f6c7c`  
		Last Modified: Tue, 01 Mar 2022 14:19:18 GMT  
		Size: 207.1 MB (207134366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f774b6ab8a9647a0abef7a9cafee8664e94673b07fc70cb6f1dc847a1a8ef6b3`  
		Last Modified: Tue, 01 Mar 2022 14:18:53 GMT  
		Size: 13.4 MB (13438497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92100f15afab684a47d277389605f2ec7c5eee252fd7f30b7d61e621e62ca89`  
		Last Modified: Tue, 01 Mar 2022 14:18:49 GMT  
		Size: 454.1 KB (454054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb385fb721049d7de4a64508464214cf48aaae58dc9450646552ccb8c567ed`  
		Last Modified: Tue, 01 Mar 2022 14:19:24 GMT  
		Size: 291.4 MB (291411961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514ae5cda9f96797ef88db9f287c7505dbf6c27e6ae34ba6349b4ef8fd5a868`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb5b7fa0b645036c64620009b5056985860c58997984db4e0c6ae01b4945624`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926c139f540a84d153254430380da9ec97d4971a4b61b9dd6940bdaeeb159ee4`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e41964727050f432478bf4ae7c7603ac9ebcc5990443de46078e3df8f4fcc9`  
		Last Modified: Tue, 01 Mar 2022 14:18:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:420f4603be916b185a289956e0234a0ff58ae2fd07b9ea7e5071587bebd81468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:103795709372e3e09024bb4163235b1fd308b49b55cbf732a410ccb2035cf133
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.4 MB (529434735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490c4496e970d96beea1a800cf1000b411ea9ba215c320e7eb95418eba082477`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:08:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:08:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:08:35 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:10:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:10:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:10:47 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:10:47 GMT
ENV ODOO_VERSION=14.0
# Tue, 01 Mar 2022 14:10:47 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:10:47 GMT
ARG ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
# Tue, 01 Mar 2022 14:12:26 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:12:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:12:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:12:32 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:12:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:12:32 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:12:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:12:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:12:32 GMT
USER odoo
# Tue, 01 Mar 2022 14:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:12:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f744a3eb8faa9c53b9214156a1731a3f54041ba4452fda20403c4a974d7833c5`  
		Last Modified: Tue, 01 Mar 2022 14:18:29 GMT  
		Size: 213.2 MB (213175223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e65e732c75de0a0623a3815cfbf17f73b6c4a96a58458b08bffb71d148e34f`  
		Last Modified: Tue, 01 Mar 2022 14:17:48 GMT  
		Size: 13.4 MB (13440948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c0506bf3aadc634c05ab579f7616d756a1e9542e0d9eb8d0ef50b95334dc04`  
		Last Modified: Tue, 01 Mar 2022 14:17:42 GMT  
		Size: 453.9 KB (453933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2036408a2a4519b452bf6ef1414e26c84cbae11da76398ac17af1bbd190f4a`  
		Last Modified: Tue, 01 Mar 2022 14:18:36 GMT  
		Size: 275.2 MB (275208434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2fcb787cd9bfe1a90a51eb3471e403bb55d2dcd91ff4883e236b5a5bedaf84`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9a202863ad30a92a7be5fc9d3577448810e997b2a5e173bc662a15103e72c`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce762be4b9f13cbd5e2145bfa42958619cc5d09931f594f0d9eebc4b5d9fd1`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571feb5fa4d24fc6f0ed85f5b58f93521d4e83e60096ec1c09a6024fd135901f`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:420f4603be916b185a289956e0234a0ff58ae2fd07b9ea7e5071587bebd81468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:103795709372e3e09024bb4163235b1fd308b49b55cbf732a410ccb2035cf133
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.4 MB (529434735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490c4496e970d96beea1a800cf1000b411ea9ba215c320e7eb95418eba082477`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:08:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:08:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:08:35 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:10:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:10:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:10:47 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:10:47 GMT
ENV ODOO_VERSION=14.0
# Tue, 01 Mar 2022 14:10:47 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:10:47 GMT
ARG ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
# Tue, 01 Mar 2022 14:12:26 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:12:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:12:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:12:32 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:12:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:12:32 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:12:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:12:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:12:32 GMT
USER odoo
# Tue, 01 Mar 2022 14:12:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:12:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f744a3eb8faa9c53b9214156a1731a3f54041ba4452fda20403c4a974d7833c5`  
		Last Modified: Tue, 01 Mar 2022 14:18:29 GMT  
		Size: 213.2 MB (213175223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e65e732c75de0a0623a3815cfbf17f73b6c4a96a58458b08bffb71d148e34f`  
		Last Modified: Tue, 01 Mar 2022 14:17:48 GMT  
		Size: 13.4 MB (13440948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c0506bf3aadc634c05ab579f7616d756a1e9542e0d9eb8d0ef50b95334dc04`  
		Last Modified: Tue, 01 Mar 2022 14:17:42 GMT  
		Size: 453.9 KB (453933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2036408a2a4519b452bf6ef1414e26c84cbae11da76398ac17af1bbd190f4a`  
		Last Modified: Tue, 01 Mar 2022 14:18:36 GMT  
		Size: 275.2 MB (275208434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2fcb787cd9bfe1a90a51eb3471e403bb55d2dcd91ff4883e236b5a5bedaf84`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9a202863ad30a92a7be5fc9d3577448810e997b2a5e173bc662a15103e72c`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce762be4b9f13cbd5e2145bfa42958619cc5d09931f594f0d9eebc4b5d9fd1`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571feb5fa4d24fc6f0ed85f5b58f93521d4e83e60096ec1c09a6024fd135901f`  
		Last Modified: Tue, 01 Mar 2022 14:17:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:b2678b8dde4589f998d8727d1f124734f251d9de1742fd97e387457c8224fa85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:3ba2d6eae2581474fc13e724f0cdf7a9d854aa7d550cc382de0bd340ef423115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548947760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec4bab35f46a4225855185a1a4f940eb733f41a39ad16bcdba2ab2b3d1b5567`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:04:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:04:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:04:27 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:05:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:06:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:06:30 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:06:30 GMT
ENV ODOO_VERSION=15.0
# Tue, 01 Mar 2022 14:06:31 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:06:31 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Tue, 01 Mar 2022 14:08:14 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:08:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:08:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:08:19 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:08:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:08:19 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:08:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:08:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:08:20 GMT
USER odoo
# Tue, 01 Mar 2022 14:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:08:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a163ebeb0494c6130a80754f29b68a5c07419748988cf37afb9630747c41c69`  
		Last Modified: Tue, 01 Mar 2022 14:17:16 GMT  
		Size: 220.3 MB (220298373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966b8e28ea8e47acbcca748753c937ef05bfde069cd7bfd2f70252b765fea99`  
		Last Modified: Tue, 01 Mar 2022 14:16:39 GMT  
		Size: 2.5 MB (2510056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9cf6997d2b0f369d91a2ce39d67ba3e78767956bd3cfdfc8d4287600b5389d`  
		Last Modified: Tue, 01 Mar 2022 14:16:38 GMT  
		Size: 447.3 KB (447285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebb0613c5de3d2fb2afdda7cc278be54b62fcacee6521530ee9bbc314b90ff0`  
		Last Modified: Tue, 01 Mar 2022 14:17:27 GMT  
		Size: 294.3 MB (294323188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e816f45b6efd29bdc715a572b6ddf911bb6a60774bcf4948bc8d719ff10e1`  
		Last Modified: Tue, 01 Mar 2022 14:16:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f68314eac90a64eaf6727d7216aa9d71667b84d9e2f7b8477be65937c5782dc`  
		Last Modified: Tue, 01 Mar 2022 14:16:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4112155967cce0788acc174fe2f54d99c3df47ecd32f32aa42f37eba2416b305`  
		Last Modified: Tue, 01 Mar 2022 14:16:36 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a082cee3ef0e8b1ace27c339702230a9588455f150b35409e7b74258e427d3a`  
		Last Modified: Tue, 01 Mar 2022 14:16:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:b2678b8dde4589f998d8727d1f124734f251d9de1742fd97e387457c8224fa85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:3ba2d6eae2581474fc13e724f0cdf7a9d854aa7d550cc382de0bd340ef423115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548947760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec4bab35f46a4225855185a1a4f940eb733f41a39ad16bcdba2ab2b3d1b5567`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:04:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:04:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:04:27 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:05:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:06:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:06:30 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:06:30 GMT
ENV ODOO_VERSION=15.0
# Tue, 01 Mar 2022 14:06:31 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:06:31 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Tue, 01 Mar 2022 14:08:14 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:08:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:08:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:08:19 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:08:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:08:19 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:08:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:08:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:08:20 GMT
USER odoo
# Tue, 01 Mar 2022 14:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:08:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a163ebeb0494c6130a80754f29b68a5c07419748988cf37afb9630747c41c69`  
		Last Modified: Tue, 01 Mar 2022 14:17:16 GMT  
		Size: 220.3 MB (220298373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966b8e28ea8e47acbcca748753c937ef05bfde069cd7bfd2f70252b765fea99`  
		Last Modified: Tue, 01 Mar 2022 14:16:39 GMT  
		Size: 2.5 MB (2510056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9cf6997d2b0f369d91a2ce39d67ba3e78767956bd3cfdfc8d4287600b5389d`  
		Last Modified: Tue, 01 Mar 2022 14:16:38 GMT  
		Size: 447.3 KB (447285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebb0613c5de3d2fb2afdda7cc278be54b62fcacee6521530ee9bbc314b90ff0`  
		Last Modified: Tue, 01 Mar 2022 14:17:27 GMT  
		Size: 294.3 MB (294323188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e816f45b6efd29bdc715a572b6ddf911bb6a60774bcf4948bc8d719ff10e1`  
		Last Modified: Tue, 01 Mar 2022 14:16:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f68314eac90a64eaf6727d7216aa9d71667b84d9e2f7b8477be65937c5782dc`  
		Last Modified: Tue, 01 Mar 2022 14:16:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4112155967cce0788acc174fe2f54d99c3df47ecd32f32aa42f37eba2416b305`  
		Last Modified: Tue, 01 Mar 2022 14:16:36 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a082cee3ef0e8b1ace27c339702230a9588455f150b35409e7b74258e427d3a`  
		Last Modified: Tue, 01 Mar 2022 14:16:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:b2678b8dde4589f998d8727d1f124734f251d9de1742fd97e387457c8224fa85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:3ba2d6eae2581474fc13e724f0cdf7a9d854aa7d550cc382de0bd340ef423115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548947760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec4bab35f46a4225855185a1a4f940eb733f41a39ad16bcdba2ab2b3d1b5567`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:04:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Mar 2022 14:04:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Mar 2022 14:04:27 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 14:05:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 01 Mar 2022 14:06:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:06:30 GMT
RUN npm install -g rtlcss
# Tue, 01 Mar 2022 14:06:30 GMT
ENV ODOO_VERSION=15.0
# Tue, 01 Mar 2022 14:06:31 GMT
ARG ODOO_RELEASE=20220225
# Tue, 01 Mar 2022 14:06:31 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Tue, 01 Mar 2022 14:08:14 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 01 Mar 2022 14:08:18 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 01 Mar 2022 14:08:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 01 Mar 2022 14:08:19 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 01 Mar 2022 14:08:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Mar 2022 14:08:19 GMT
EXPOSE 8069 8071 8072
# Tue, 01 Mar 2022 14:08:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Mar 2022 14:08:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 01 Mar 2022 14:08:20 GMT
USER odoo
# Tue, 01 Mar 2022 14:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Mar 2022 14:08:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a163ebeb0494c6130a80754f29b68a5c07419748988cf37afb9630747c41c69`  
		Last Modified: Tue, 01 Mar 2022 14:17:16 GMT  
		Size: 220.3 MB (220298373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2966b8e28ea8e47acbcca748753c937ef05bfde069cd7bfd2f70252b765fea99`  
		Last Modified: Tue, 01 Mar 2022 14:16:39 GMT  
		Size: 2.5 MB (2510056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9cf6997d2b0f369d91a2ce39d67ba3e78767956bd3cfdfc8d4287600b5389d`  
		Last Modified: Tue, 01 Mar 2022 14:16:38 GMT  
		Size: 447.3 KB (447285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebb0613c5de3d2fb2afdda7cc278be54b62fcacee6521530ee9bbc314b90ff0`  
		Last Modified: Tue, 01 Mar 2022 14:17:27 GMT  
		Size: 294.3 MB (294323188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e816f45b6efd29bdc715a572b6ddf911bb6a60774bcf4948bc8d719ff10e1`  
		Last Modified: Tue, 01 Mar 2022 14:16:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f68314eac90a64eaf6727d7216aa9d71667b84d9e2f7b8477be65937c5782dc`  
		Last Modified: Tue, 01 Mar 2022 14:16:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4112155967cce0788acc174fe2f54d99c3df47ecd32f32aa42f37eba2416b305`  
		Last Modified: Tue, 01 Mar 2022 14:16:36 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a082cee3ef0e8b1ace27c339702230a9588455f150b35409e7b74258e427d3a`  
		Last Modified: Tue, 01 Mar 2022 14:16:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
