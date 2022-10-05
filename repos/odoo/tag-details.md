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
$ docker pull odoo@sha256:327fc510d251ba2d858f39c6c478c3ca08d8c75bd3ecd84fa6598baf9fad267c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:5ef602d349928854b23ad60f0fe4f10b4034d3b6d7a54ac2c3ec9bf9c3644424
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.4 MB (540358332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec45ee09ccadad61e7f9caad41902524e1b721a94aaa5646e5645b02346016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:50:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:50:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:56:08 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:56:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:56:19 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:56:19 GMT
ENV ODOO_VERSION=13.0
# Wed, 05 Oct 2022 12:56:20 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:56:20 GMT
ARG ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
# Wed, 05 Oct 2022 12:57:32 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:57:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:57:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:57:36 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:57:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:57:36 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:57:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:57:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:57:37 GMT
USER odoo
# Wed, 05 Oct 2022 12:57:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:57:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e0856975f76bb58e407130d28eea0df88e55a11bc6a9d7bc162d04dd88e60`  
		Last Modified: Wed, 05 Oct 2022 13:00:00 GMT  
		Size: 207.1 MB (207144790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1abf53b046e1d759a453376e0b7546577865ef1e31341fe1b27d7619589da5`  
		Last Modified: Wed, 05 Oct 2022 12:59:38 GMT  
		Size: 13.4 MB (13442511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5fffb811e900b540def18663ab415a936770b612d0d52999ebd0ceeee9c3`  
		Last Modified: Wed, 05 Oct 2022 12:59:35 GMT  
		Size: 453.2 KB (453230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b958374f94c4f186ea6c24c02948eb93a8cb800c09b23ca51328243beeb36b`  
		Last Modified: Wed, 05 Oct 2022 13:00:06 GMT  
		Size: 292.2 MB (292177290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93794f0dfff6f701dfa3f8f17a4dfaf035616792c25140ca950c55b7fa0e9382`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd87251cb4cb7fca08d5e11cda5e6c088ccd632ec1ad884c6bdc11d03cc0a7`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff134618dc95ef133a6a6f6bd28f2efe114edff2dc5c11366b857c64c8f45e8d`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeccab775f29671e0308a56f17c8aa71b9fa7bb5691811dfeb33388415fee86`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:327fc510d251ba2d858f39c6c478c3ca08d8c75bd3ecd84fa6598baf9fad267c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:5ef602d349928854b23ad60f0fe4f10b4034d3b6d7a54ac2c3ec9bf9c3644424
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.4 MB (540358332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ec45ee09ccadad61e7f9caad41902524e1b721a94aaa5646e5645b02346016`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:50:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:50:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:56:08 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:56:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:56:19 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:56:19 GMT
ENV ODOO_VERSION=13.0
# Wed, 05 Oct 2022 12:56:20 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:56:20 GMT
ARG ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
# Wed, 05 Oct 2022 12:57:32 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:57:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:57:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:57:36 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:57:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:57:36 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:57:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:57:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:57:37 GMT
USER odoo
# Wed, 05 Oct 2022 12:57:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:57:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48e0856975f76bb58e407130d28eea0df88e55a11bc6a9d7bc162d04dd88e60`  
		Last Modified: Wed, 05 Oct 2022 13:00:00 GMT  
		Size: 207.1 MB (207144790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1abf53b046e1d759a453376e0b7546577865ef1e31341fe1b27d7619589da5`  
		Last Modified: Wed, 05 Oct 2022 12:59:38 GMT  
		Size: 13.4 MB (13442511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ec5fffb811e900b540def18663ab415a936770b612d0d52999ebd0ceeee9c3`  
		Last Modified: Wed, 05 Oct 2022 12:59:35 GMT  
		Size: 453.2 KB (453230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b958374f94c4f186ea6c24c02948eb93a8cb800c09b23ca51328243beeb36b`  
		Last Modified: Wed, 05 Oct 2022 13:00:06 GMT  
		Size: 292.2 MB (292177290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93794f0dfff6f701dfa3f8f17a4dfaf035616792c25140ca950c55b7fa0e9382`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd87251cb4cb7fca08d5e11cda5e6c088ccd632ec1ad884c6bdc11d03cc0a7`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff134618dc95ef133a6a6f6bd28f2efe114edff2dc5c11366b857c64c8f45e8d`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeccab775f29671e0308a56f17c8aa71b9fa7bb5691811dfeb33388415fee86`  
		Last Modified: Wed, 05 Oct 2022 12:59:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:73d74d918b9156b27d251e6c48d1ca6d21186c102b987deff6de9caf540b618f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:65e64b54e88ccc9676f81c3ac5589bc2f557550fb0bd2a8f9911d8e1a4a4531d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530884848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ce823c16e857102f92cf05e4fa658b116114334980292925fed1c4046624af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:50:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:50:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:52:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:52:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:52:35 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:52:35 GMT
ENV ODOO_VERSION=14.0
# Wed, 05 Oct 2022 12:52:35 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:52:35 GMT
ARG ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
# Wed, 05 Oct 2022 12:54:00 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:54:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:54:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:54:04 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:54:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:54:04 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:54:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:54:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:54:04 GMT
USER odoo
# Wed, 05 Oct 2022 12:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:54:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73991209e36bf89d51fca585d2b4242c0cb80cbfd84e98fe6314e9b7c0d1dde1`  
		Last Modified: Wed, 05 Oct 2022 12:59:16 GMT  
		Size: 213.2 MB (213182348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b040c0568df4c7a36beaffa7b2957e709200877eb8d18ce95049f470d8381`  
		Last Modified: Wed, 05 Oct 2022 12:58:54 GMT  
		Size: 13.4 MB (13443968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101df339f0e4711374ae94bdfc877da10ab15e76776311e1cc4ea61abed09c22`  
		Last Modified: Wed, 05 Oct 2022 12:58:51 GMT  
		Size: 453.2 KB (453236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6092b7935bd2611630db4987c7963e3f8313da7b5f064fbb3f728d4c33ada6`  
		Last Modified: Wed, 05 Oct 2022 12:59:23 GMT  
		Size: 276.7 MB (276664789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8a4165ecfd07dcdaa53c33afc4a86e5e4241be7be613258f9b267aa463e1d`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c676138c085ef9c61e5a5db9cd0c8b6f1308b5f7c97a0ace4b0d1ab99e711e6`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e1225d956674e47d6e84aaa834d643a53217d0026a56f4f33bc13897e5012`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f071aded59ab48c2d13f3a7430c807864840b830bc40aa3c26069199c1ad303`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:73d74d918b9156b27d251e6c48d1ca6d21186c102b987deff6de9caf540b618f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:65e64b54e88ccc9676f81c3ac5589bc2f557550fb0bd2a8f9911d8e1a4a4531d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530884848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ce823c16e857102f92cf05e4fa658b116114334980292925fed1c4046624af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:50:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:50:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:50:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:52:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:52:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:52:35 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:52:35 GMT
ENV ODOO_VERSION=14.0
# Wed, 05 Oct 2022 12:52:35 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:52:35 GMT
ARG ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
# Wed, 05 Oct 2022 12:54:00 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:54:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:54:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:54:04 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:54:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:54:04 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:54:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:54:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:54:04 GMT
USER odoo
# Wed, 05 Oct 2022 12:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:54:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73991209e36bf89d51fca585d2b4242c0cb80cbfd84e98fe6314e9b7c0d1dde1`  
		Last Modified: Wed, 05 Oct 2022 12:59:16 GMT  
		Size: 213.2 MB (213182348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b040c0568df4c7a36beaffa7b2957e709200877eb8d18ce95049f470d8381`  
		Last Modified: Wed, 05 Oct 2022 12:58:54 GMT  
		Size: 13.4 MB (13443968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101df339f0e4711374ae94bdfc877da10ab15e76776311e1cc4ea61abed09c22`  
		Last Modified: Wed, 05 Oct 2022 12:58:51 GMT  
		Size: 453.2 KB (453236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6092b7935bd2611630db4987c7963e3f8313da7b5f064fbb3f728d4c33ada6`  
		Last Modified: Wed, 05 Oct 2022 12:59:23 GMT  
		Size: 276.7 MB (276664789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8a4165ecfd07dcdaa53c33afc4a86e5e4241be7be613258f9b267aa463e1d`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c676138c085ef9c61e5a5db9cd0c8b6f1308b5f7c97a0ace4b0d1ab99e711e6`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e1225d956674e47d6e84aaa834d643a53217d0026a56f4f33bc13897e5012`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f071aded59ab48c2d13f3a7430c807864840b830bc40aa3c26069199c1ad303`  
		Last Modified: Wed, 05 Oct 2022 12:58:49 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:01c1aafffc6640db6d5dad0db2e065129c79f5ae0a8bbc3692da69a807aec90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:b34de06d7a6b1942c30cee3835963f07ee47629fa6a22a8edc4282dfdf8e2314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557896650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ff50455e949880df2ce71ed65a2a374f1c9202d19e8ea18060c4d1aefc1e59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:49:05 GMT
ENV ODOO_VERSION=15.0
# Wed, 05 Oct 2022 12:49:05 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:49:05 GMT
ARG ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
# Wed, 05 Oct 2022 12:50:30 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:50:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:50:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:50:34 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:50:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:50:35 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:50:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:50:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:50:35 GMT
USER odoo
# Wed, 05 Oct 2022 12:50:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:50:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9365e406c50dc6abf2ced561ec198069f2a2a125984be700fa4a05f9fc9439e`  
		Last Modified: Wed, 05 Oct 2022 12:58:37 GMT  
		Size: 303.2 MB (303214867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff9e73866d59e22cd91b6dbd46b5fd09ae6e3ba6b70c68d0b27e33f62ac74da`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b257de06a97928744fab39c0d6656072a9f8a7c397b71bdad68ff88d3a5a59ab`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b392a6e74bc429798aff63285c6767539b73d1379589670b82494df2329b0154`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aae61de0fe5960e11807ed6002a3bc2e2269b3777bd2ef3e55b3e133cde974`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:01c1aafffc6640db6d5dad0db2e065129c79f5ae0a8bbc3692da69a807aec90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:b34de06d7a6b1942c30cee3835963f07ee47629fa6a22a8edc4282dfdf8e2314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557896650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ff50455e949880df2ce71ed65a2a374f1c9202d19e8ea18060c4d1aefc1e59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:49:05 GMT
ENV ODOO_VERSION=15.0
# Wed, 05 Oct 2022 12:49:05 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:49:05 GMT
ARG ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
# Wed, 05 Oct 2022 12:50:30 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:50:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:50:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:50:34 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:50:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:50:35 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:50:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:50:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:50:35 GMT
USER odoo
# Wed, 05 Oct 2022 12:50:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:50:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9365e406c50dc6abf2ced561ec198069f2a2a125984be700fa4a05f9fc9439e`  
		Last Modified: Wed, 05 Oct 2022 12:58:37 GMT  
		Size: 303.2 MB (303214867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff9e73866d59e22cd91b6dbd46b5fd09ae6e3ba6b70c68d0b27e33f62ac74da`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b257de06a97928744fab39c0d6656072a9f8a7c397b71bdad68ff88d3a5a59ab`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b392a6e74bc429798aff63285c6767539b73d1379589670b82494df2329b0154`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aae61de0fe5960e11807ed6002a3bc2e2269b3777bd2ef3e55b3e133cde974`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:01c1aafffc6640db6d5dad0db2e065129c79f5ae0a8bbc3692da69a807aec90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b34de06d7a6b1942c30cee3835963f07ee47629fa6a22a8edc4282dfdf8e2314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557896650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ff50455e949880df2ce71ed65a2a374f1c9202d19e8ea18060c4d1aefc1e59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 12:47:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Oct 2022 12:47:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Oct 2022 12:47:42 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 12:48:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Oct 2022 12:49:04 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 12:49:05 GMT
RUN npm install -g rtlcss
# Wed, 05 Oct 2022 12:49:05 GMT
ENV ODOO_VERSION=15.0
# Wed, 05 Oct 2022 12:49:05 GMT
ARG ODOO_RELEASE=20220915
# Wed, 05 Oct 2022 12:49:05 GMT
ARG ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
# Wed, 05 Oct 2022 12:50:30 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 05 Oct 2022 12:50:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 05 Oct 2022 12:50:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 05 Oct 2022 12:50:34 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 05 Oct 2022 12:50:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 05 Oct 2022 12:50:35 GMT
EXPOSE 8069 8071 8072
# Wed, 05 Oct 2022 12:50:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 05 Oct 2022 12:50:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 05 Oct 2022 12:50:35 GMT
USER odoo
# Wed, 05 Oct 2022 12:50:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Oct 2022 12:50:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1eb84e6e02a853d9decd11a159b54a0995b7293fa476df2fec218d33b1df6d`  
		Last Modified: Wed, 05 Oct 2022 12:58:29 GMT  
		Size: 220.3 MB (220296502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e514ed12a4b7e196251756d20aa16acbeaf5a3a34f67005bd99c3faa6bf6cfba`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 2.5 MB (2513557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bec1ca6984d8b904d4439a7f235c18d3ab647da175de5faa8ba74a9c232cb8`  
		Last Modified: Wed, 05 Oct 2022 12:58:02 GMT  
		Size: 449.2 KB (449160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9365e406c50dc6abf2ced561ec198069f2a2a125984be700fa4a05f9fc9439e`  
		Last Modified: Wed, 05 Oct 2022 12:58:37 GMT  
		Size: 303.2 MB (303214867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff9e73866d59e22cd91b6dbd46b5fd09ae6e3ba6b70c68d0b27e33f62ac74da`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b257de06a97928744fab39c0d6656072a9f8a7c397b71bdad68ff88d3a5a59ab`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b392a6e74bc429798aff63285c6767539b73d1379589670b82494df2329b0154`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aae61de0fe5960e11807ed6002a3bc2e2269b3777bd2ef3e55b3e133cde974`  
		Last Modified: Wed, 05 Oct 2022 12:58:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
