<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:latest`](#odoolatest)

## `odoo:12`

```console
$ docker pull odoo@sha256:1e677e3e00bf367acf835cf2f319c894e32fbfd7227629207604ae5ca0c92ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:7d84b335803af82b7f9e030e0438d51ac0f057f48890e29bc1803941ad8246bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538382076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4908e0e5a50663d4b1d96a7ac7daa9cc3a9b65374fe4f3741cbc1f7c3a3f6fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:22:13 GMT
ADD file:a63c6cc73701d6cb7195338c446b9e92ef6b7a0f9321f6cc1bf8738e3da57c66 in / 
# Wed, 23 Jun 2021 00:22:14 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:51:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:51:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:51:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 23 Jun 2021 07:53:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:54:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:13 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:14 GMT
ENV ODOO_VERSION=12.0
# Tue, 13 Jul 2021 18:32:35 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:32:35 GMT
ARG ODOO_SHA=94460bac26be9050ac681868a5881c430e98702e
# Tue, 13 Jul 2021 18:33:40 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=94460bac26be9050ac681868a5881c430e98702e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:33:43 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:33:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:33:44 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=94460bac26be9050ac681868a5881c430e98702e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:33:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:33:45 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:33:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:33:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:33:45 GMT
USER odoo
# Tue, 13 Jul 2021 18:33:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:33:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aed007321795cdc03a0ba9b238567ffa299459e9b0322a3d835a04d06afc2500`  
		Last Modified: Wed, 23 Jun 2021 00:28:29 GMT  
		Size: 22.5 MB (22528174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f8f66a1ee8d03d029b9e9fd4fab492aae82ab75ecc939a565a9ed63bd81f8`  
		Last Modified: Wed, 23 Jun 2021 07:57:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6f54374b12d423468b84b7b20816bca30d69f0367e06c3fcc78a58990776d`  
		Last Modified: Wed, 23 Jun 2021 07:58:33 GMT  
		Size: 219.7 MB (219658352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0f9e42ea609c4a44d52d51b1be4eb6a509244b5ff23b7ce9cc26e2d31f4d9`  
		Last Modified: Wed, 23 Jun 2021 07:57:59 GMT  
		Size: 2.2 MB (2224626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47480c9939297e4d6a19caeef3f46a6554712b96da0972a4b1630a6d1a39808f`  
		Last Modified: Wed, 23 Jun 2021 07:58:05 GMT  
		Size: 22.0 MB (22023550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a510b9a2661b1a1f819c27d4f28b1a63bdbfbff2cb2260ee506b26c010550d`  
		Last Modified: Tue, 13 Jul 2021 18:36:11 GMT  
		Size: 271.9 MB (271944708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bcd1cfe3571996f94e81b763039c147ff27b54318cea86f9287acd470423e`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12767660c987a2efb9ee3cb89f38433738160e45b46c2c53200f86551caca0f`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f424e41a0745366526c1cb39c723b88abb94a284241b9664c03e1fb00f8b8771`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6018876d72c47b4eca10621a52a781e160a08751a68f77bf10d66dce0fc9add4`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:1e677e3e00bf367acf835cf2f319c894e32fbfd7227629207604ae5ca0c92ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:7d84b335803af82b7f9e030e0438d51ac0f057f48890e29bc1803941ad8246bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538382076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4908e0e5a50663d4b1d96a7ac7daa9cc3a9b65374fe4f3741cbc1f7c3a3f6fe6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:22:13 GMT
ADD file:a63c6cc73701d6cb7195338c446b9e92ef6b7a0f9321f6cc1bf8738e3da57c66 in / 
# Wed, 23 Jun 2021 00:22:14 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:51:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:51:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:51:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:51:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 23 Jun 2021 07:53:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:54:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:13 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:54:14 GMT
ENV ODOO_VERSION=12.0
# Tue, 13 Jul 2021 18:32:35 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:32:35 GMT
ARG ODOO_SHA=94460bac26be9050ac681868a5881c430e98702e
# Tue, 13 Jul 2021 18:33:40 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=94460bac26be9050ac681868a5881c430e98702e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:33:43 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:33:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:33:44 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=94460bac26be9050ac681868a5881c430e98702e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:33:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:33:45 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:33:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:33:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:33:45 GMT
USER odoo
# Tue, 13 Jul 2021 18:33:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:33:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:aed007321795cdc03a0ba9b238567ffa299459e9b0322a3d835a04d06afc2500`  
		Last Modified: Wed, 23 Jun 2021 00:28:29 GMT  
		Size: 22.5 MB (22528174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f8f66a1ee8d03d029b9e9fd4fab492aae82ab75ecc939a565a9ed63bd81f8`  
		Last Modified: Wed, 23 Jun 2021 07:57:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6f54374b12d423468b84b7b20816bca30d69f0367e06c3fcc78a58990776d`  
		Last Modified: Wed, 23 Jun 2021 07:58:33 GMT  
		Size: 219.7 MB (219658352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc0f9e42ea609c4a44d52d51b1be4eb6a509244b5ff23b7ce9cc26e2d31f4d9`  
		Last Modified: Wed, 23 Jun 2021 07:57:59 GMT  
		Size: 2.2 MB (2224626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47480c9939297e4d6a19caeef3f46a6554712b96da0972a4b1630a6d1a39808f`  
		Last Modified: Wed, 23 Jun 2021 07:58:05 GMT  
		Size: 22.0 MB (22023550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a510b9a2661b1a1f819c27d4f28b1a63bdbfbff2cb2260ee506b26c010550d`  
		Last Modified: Tue, 13 Jul 2021 18:36:11 GMT  
		Size: 271.9 MB (271944708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4bcd1cfe3571996f94e81b763039c147ff27b54318cea86f9287acd470423e`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12767660c987a2efb9ee3cb89f38433738160e45b46c2c53200f86551caca0f`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f424e41a0745366526c1cb39c723b88abb94a284241b9664c03e1fb00f8b8771`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6018876d72c47b4eca10621a52a781e160a08751a68f77bf10d66dce0fc9add4`  
		Last Modified: Tue, 13 Jul 2021 18:35:43 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:6b4a659c7da3444525ad7ecaef31807bbbf6c53e59cebb730ba379123cfe6981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:0bd8b36236775780187afe48456c6ee3f48a072ff99cc1419c181dffdd1330e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528287486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97d7131becd80e34eda08fda9411ec7a9d5968fab8c75d1b2557e1c368eaf7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:49:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:49:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:49:53 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:49:53 GMT
ENV ODOO_VERSION=13.0
# Tue, 13 Jul 2021 18:31:10 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:31:10 GMT
ARG ODOO_SHA=018e8f79ba6c2b5431eae1a5b49469a5e1b8977e
# Tue, 13 Jul 2021 18:32:20 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=018e8f79ba6c2b5431eae1a5b49469a5e1b8977e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:32:22 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:32:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:32:23 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=018e8f79ba6c2b5431eae1a5b49469a5e1b8977e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:32:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:32:24 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:32:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:32:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:32:24 GMT
USER odoo
# Tue, 13 Jul 2021 18:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760ec83e05549c1bafe40d795ed53c471a0208b2e5a5fe29f1f4575e4277ed`  
		Last Modified: Wed, 23 Jun 2021 07:57:34 GMT  
		Size: 207.1 MB (207122080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6f5407abbe57f2c624e00f8226cb3f74567fc177824c08838c437a8d05fba`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 2.3 MB (2346852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7db6376102b543b53d50ab5ed822526c9569bbee49c030740510ed71465072`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 885.8 KB (885845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6dcc1fa1a9d2a98a0761285b67e91468d86d4c84e2ed209e4e724df2f0025d`  
		Last Modified: Tue, 13 Jul 2021 18:35:31 GMT  
		Size: 290.8 MB (290784431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315d7968672090ab750f763f49eb0e87f46e9ba6b9b92fd244e8076ebb0d3e83`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a96ef2c928f6b141d3726de2ccca5cbee42003d42ed5ddb318957109a0b74cf`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790e11c5e1bddfcc3bde5b9f6ff384f809f1c843ae8b1891bf0e45c0824030d3`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503c07997e094e8ad062ade8bb5d3fb006e4946bb89c0788fbe841c66678f94a`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:6b4a659c7da3444525ad7ecaef31807bbbf6c53e59cebb730ba379123cfe6981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:0bd8b36236775780187afe48456c6ee3f48a072ff99cc1419c181dffdd1330e2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528287486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97d7131becd80e34eda08fda9411ec7a9d5968fab8c75d1b2557e1c368eaf7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:49:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:49:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:49:53 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:49:53 GMT
ENV ODOO_VERSION=13.0
# Tue, 13 Jul 2021 18:31:10 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:31:10 GMT
ARG ODOO_SHA=018e8f79ba6c2b5431eae1a5b49469a5e1b8977e
# Tue, 13 Jul 2021 18:32:20 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=018e8f79ba6c2b5431eae1a5b49469a5e1b8977e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:32:22 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:32:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:32:23 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=018e8f79ba6c2b5431eae1a5b49469a5e1b8977e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:32:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:32:24 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:32:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:32:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:32:24 GMT
USER odoo
# Tue, 13 Jul 2021 18:32:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:32:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d760ec83e05549c1bafe40d795ed53c471a0208b2e5a5fe29f1f4575e4277ed`  
		Last Modified: Wed, 23 Jun 2021 07:57:34 GMT  
		Size: 207.1 MB (207122080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6f5407abbe57f2c624e00f8226cb3f74567fc177824c08838c437a8d05fba`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 2.3 MB (2346852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7db6376102b543b53d50ab5ed822526c9569bbee49c030740510ed71465072`  
		Last Modified: Wed, 23 Jun 2021 07:57:03 GMT  
		Size: 885.8 KB (885845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6dcc1fa1a9d2a98a0761285b67e91468d86d4c84e2ed209e4e724df2f0025d`  
		Last Modified: Tue, 13 Jul 2021 18:35:31 GMT  
		Size: 290.8 MB (290784431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315d7968672090ab750f763f49eb0e87f46e9ba6b9b92fd244e8076ebb0d3e83`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a96ef2c928f6b141d3726de2ccca5cbee42003d42ed5ddb318957109a0b74cf`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790e11c5e1bddfcc3bde5b9f6ff384f809f1c843ae8b1891bf0e45c0824030d3`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503c07997e094e8ad062ade8bb5d3fb006e4946bb89c0788fbe841c66678f94a`  
		Last Modified: Tue, 13 Jul 2021 18:34:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:529d4665292b56e4a92897d1b587ab2c3d19d5ab047dc38dc4f45a8d058e43e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:4bf021269722b263c09c6b711334c56b0c0db1f6875cb94e2c56e73b726eda85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516474691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cf06ebb25be68424b6e213570d9e14be9840630dbeb5fe1e28cf6c2c06c83c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
# Tue, 13 Jul 2021 18:30:53 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:30:58 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:30:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:30:58 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:30:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:30:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:30:59 GMT
USER odoo
# Tue, 13 Jul 2021 18:30:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:30:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16506a5f3ee5de721e35b0267e025688f246d6ed0927d5ebd8c8b3ea24fc5d67`  
		Last Modified: Tue, 13 Jul 2021 18:34:46 GMT  
		Size: 272.9 MB (272919695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a490d65a662af856dd945bd11dc2c85ac9b9d15d1b06d0bca4fdc47fee1592`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f51fd15106ebf823d3cd375775e92a9ead4e8e3f176e13ea1f0bae9f1373`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac4e98c4c110c6491048b80611467618e18ed7c870e104bd7a82cf81002fc7`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6aabb5a0e9a42b03b43a58eeed96fb3890a0db14cc30478e4cd514f579580e`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:529d4665292b56e4a92897d1b587ab2c3d19d5ab047dc38dc4f45a8d058e43e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:4bf021269722b263c09c6b711334c56b0c0db1f6875cb94e2c56e73b726eda85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516474691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cf06ebb25be68424b6e213570d9e14be9840630dbeb5fe1e28cf6c2c06c83c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
# Tue, 13 Jul 2021 18:30:53 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:30:58 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:30:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:30:58 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:30:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:30:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:30:59 GMT
USER odoo
# Tue, 13 Jul 2021 18:30:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:30:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16506a5f3ee5de721e35b0267e025688f246d6ed0927d5ebd8c8b3ea24fc5d67`  
		Last Modified: Tue, 13 Jul 2021 18:34:46 GMT  
		Size: 272.9 MB (272919695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a490d65a662af856dd945bd11dc2c85ac9b9d15d1b06d0bca4fdc47fee1592`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f51fd15106ebf823d3cd375775e92a9ead4e8e3f176e13ea1f0bae9f1373`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac4e98c4c110c6491048b80611467618e18ed7c870e104bd7a82cf81002fc7`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6aabb5a0e9a42b03b43a58eeed96fb3890a0db14cc30478e4cd514f579580e`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:529d4665292b56e4a92897d1b587ab2c3d19d5ab047dc38dc4f45a8d058e43e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:4bf021269722b263c09c6b711334c56b0c0db1f6875cb94e2c56e73b726eda85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516474691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cf06ebb25be68424b6e213570d9e14be9840630dbeb5fe1e28cf6c2c06c83c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
# Tue, 13 Jul 2021 18:30:53 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:30:58 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:30:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:30:58 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:30:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:30:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:30:59 GMT
USER odoo
# Tue, 13 Jul 2021 18:30:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:30:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16506a5f3ee5de721e35b0267e025688f246d6ed0927d5ebd8c8b3ea24fc5d67`  
		Last Modified: Tue, 13 Jul 2021 18:34:46 GMT  
		Size: 272.9 MB (272919695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a490d65a662af856dd945bd11dc2c85ac9b9d15d1b06d0bca4fdc47fee1592`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f51fd15106ebf823d3cd375775e92a9ead4e8e3f176e13ea1f0bae9f1373`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac4e98c4c110c6491048b80611467618e18ed7c870e104bd7a82cf81002fc7`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6aabb5a0e9a42b03b43a58eeed96fb3890a0db14cc30478e4cd514f579580e`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
