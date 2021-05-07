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
$ docker pull odoo@sha256:f62d779e5a04984b586eff2513c6ac72476e61c088dc678e361b5e66adaab42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:c4ac2ba7b359a75c26265c233b5a9d829a490b3394a28cbf60a5093ae4a00f0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542601969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064e58925cb7c906595aa4b7710e9632f0e1947a6749f41d878ef737efe9d3cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:37:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:37:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:37:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:37:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 10 Apr 2021 12:39:11 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:39:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
ENV ODOO_VERSION=12.0
# Thu, 06 May 2021 21:50:51 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:50:52 GMT
ARG ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
# Thu, 06 May 2021 21:51:58 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:51:59 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:51:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:52:00 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:52:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:52:00 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:52:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:52:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:52:01 GMT
USER odoo
# Thu, 06 May 2021 21:52:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:52:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf89834cbbd2b3cee3b8a944f6b45e4a1507584664ee0a1b02259590615d59`  
		Last Modified: Sat, 10 Apr 2021 12:42:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b11cee4db50450b66bc29b47f68b86380f02d6097f24e2b69a05dab9b82788`  
		Last Modified: Sat, 10 Apr 2021 12:43:18 GMT  
		Size: 219.6 MB (219645154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98555f4c9e696b99e0a4429cafe8848f74f7baa37c2265bd07bdc5d7ca50ece3`  
		Last Modified: Sat, 10 Apr 2021 12:42:52 GMT  
		Size: 2.2 MB (2224102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd66427a8f8ee5f5e15e695a9171413d51a17fd3fa05b78c6b7b8f7f2b8a259`  
		Last Modified: Sat, 10 Apr 2021 12:42:56 GMT  
		Size: 22.0 MB (22046831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05f4b7d9a9b32316a26d50d75fb7f6f32bd2351bf5f217ea02489abcfb05bfd`  
		Last Modified: Thu, 06 May 2021 21:54:31 GMT  
		Size: 276.2 MB (276154952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d3363cb58e70d5544511af93a2bc47604a3b255fc7c1ccf7b10025b98f9374`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebef15b3b3574e6bf25ff8048aa288a92aeab312d86ca0eb2498853e00949eb5`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46a7ea149295f2f3e305a3b630593f74c82608c9591dd1dd1e22820fa333c7e`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b056eb94dd9f1c58a43add03c1102dc2da3041526d80bd75888554267cba28d4`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:f62d779e5a04984b586eff2513c6ac72476e61c088dc678e361b5e66adaab42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:c4ac2ba7b359a75c26265c233b5a9d829a490b3394a28cbf60a5093ae4a00f0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542601969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064e58925cb7c906595aa4b7710e9632f0e1947a6749f41d878ef737efe9d3cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:37:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:37:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:37:46 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:37:47 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 10 Apr 2021 12:39:11 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:39:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:39:39 GMT
ENV ODOO_VERSION=12.0
# Thu, 06 May 2021 21:50:51 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:50:52 GMT
ARG ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
# Thu, 06 May 2021 21:51:58 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:51:59 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:51:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:52:00 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:52:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:52:00 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:52:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:52:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:52:01 GMT
USER odoo
# Thu, 06 May 2021 21:52:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:52:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cf89834cbbd2b3cee3b8a944f6b45e4a1507584664ee0a1b02259590615d59`  
		Last Modified: Sat, 10 Apr 2021 12:42:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b11cee4db50450b66bc29b47f68b86380f02d6097f24e2b69a05dab9b82788`  
		Last Modified: Sat, 10 Apr 2021 12:43:18 GMT  
		Size: 219.6 MB (219645154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98555f4c9e696b99e0a4429cafe8848f74f7baa37c2265bd07bdc5d7ca50ece3`  
		Last Modified: Sat, 10 Apr 2021 12:42:52 GMT  
		Size: 2.2 MB (2224102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd66427a8f8ee5f5e15e695a9171413d51a17fd3fa05b78c6b7b8f7f2b8a259`  
		Last Modified: Sat, 10 Apr 2021 12:42:56 GMT  
		Size: 22.0 MB (22046831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05f4b7d9a9b32316a26d50d75fb7f6f32bd2351bf5f217ea02489abcfb05bfd`  
		Last Modified: Thu, 06 May 2021 21:54:31 GMT  
		Size: 276.2 MB (276154952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d3363cb58e70d5544511af93a2bc47604a3b255fc7c1ccf7b10025b98f9374`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebef15b3b3574e6bf25ff8048aa288a92aeab312d86ca0eb2498853e00949eb5`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46a7ea149295f2f3e305a3b630593f74c82608c9591dd1dd1e22820fa333c7e`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b056eb94dd9f1c58a43add03c1102dc2da3041526d80bd75888554267cba28d4`  
		Last Modified: Thu, 06 May 2021 21:54:01 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:e9ea173e4bf1bd9f5336b960ee0c63570012cfd526110d3e215d5a5d1f39ea39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:1cabc518141f81fb6748af9066804e896997829aa8357d0db4306620925e5e1e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532369542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087452fa578e667d39598e54d1d09a18ce440857d610c210da14c2cd64142982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:35:54 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:36:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:36:13 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:36:14 GMT
ENV ODOO_VERSION=13.0
# Thu, 06 May 2021 21:49:26 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:49:26 GMT
ARG ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
# Thu, 06 May 2021 21:50:40 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:50:43 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:50:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:50:45 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:50:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:50:45 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:50:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:50:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:50:46 GMT
USER odoo
# Thu, 06 May 2021 21:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:50:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f81febf0e37dd17e29257f92caf652e1fead27661526fffe25491be70915d3`  
		Last Modified: Sat, 10 Apr 2021 12:42:31 GMT  
		Size: 207.1 MB (207124621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79303e39ab88305c57546603826b66e6eb084ae3937717320b18885c8f73fb60`  
		Last Modified: Sat, 10 Apr 2021 12:42:03 GMT  
		Size: 2.3 MB (2345472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185986373d8432024fd24e5a223928c83785fd54e9527e2380262b64e621206b`  
		Last Modified: Sat, 10 Apr 2021 12:42:06 GMT  
		Size: 896.8 KB (896834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877681bc9b8e5b75aa8db6589b635f8e643917c54d922901aabf5db05de034f`  
		Last Modified: Thu, 06 May 2021 21:53:50 GMT  
		Size: 294.9 MB (294860813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7107c2effe67a96b67b158c98fd9db9e5437386d0555a8bee4430050fe1785d`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d8e689ecc6de580583f443a73a2256d71c01497880f14f2939eb73ec841ffd`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb06b9d6d46a4568b4b6cb861d77d546ac3028c122ccc0a3c269b15136c3493`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676d8787f92d6c31a3dc4004876e863d4bc62ddf339c73fb91b00ead6c8e22c`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:e9ea173e4bf1bd9f5336b960ee0c63570012cfd526110d3e215d5a5d1f39ea39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:1cabc518141f81fb6748af9066804e896997829aa8357d0db4306620925e5e1e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532369542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087452fa578e667d39598e54d1d09a18ce440857d610c210da14c2cd64142982`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:35:54 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:36:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:36:13 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:36:14 GMT
ENV ODOO_VERSION=13.0
# Thu, 06 May 2021 21:49:26 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:49:26 GMT
ARG ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
# Thu, 06 May 2021 21:50:40 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:50:43 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:50:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:50:45 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:50:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:50:45 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:50:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:50:45 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:50:46 GMT
USER odoo
# Thu, 06 May 2021 21:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:50:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f81febf0e37dd17e29257f92caf652e1fead27661526fffe25491be70915d3`  
		Last Modified: Sat, 10 Apr 2021 12:42:31 GMT  
		Size: 207.1 MB (207124621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79303e39ab88305c57546603826b66e6eb084ae3937717320b18885c8f73fb60`  
		Last Modified: Sat, 10 Apr 2021 12:42:03 GMT  
		Size: 2.3 MB (2345472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185986373d8432024fd24e5a223928c83785fd54e9527e2380262b64e621206b`  
		Last Modified: Sat, 10 Apr 2021 12:42:06 GMT  
		Size: 896.8 KB (896834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877681bc9b8e5b75aa8db6589b635f8e643917c54d922901aabf5db05de034f`  
		Last Modified: Thu, 06 May 2021 21:53:50 GMT  
		Size: 294.9 MB (294860813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7107c2effe67a96b67b158c98fd9db9e5437386d0555a8bee4430050fe1785d`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d8e689ecc6de580583f443a73a2256d71c01497880f14f2939eb73ec841ffd`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb06b9d6d46a4568b4b6cb861d77d546ac3028c122ccc0a3c269b15136c3493`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676d8787f92d6c31a3dc4004876e863d4bc62ddf339c73fb91b00ead6c8e22c`  
		Last Modified: Thu, 06 May 2021 21:53:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:a0b809d3f15aa96aa445e246a4dc2d708930a6eec8f794c0db4fae9d63cd1e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:10b2f69a988e275e9a9a9903546a910e5937957b4fab10c30eb6233e682f0d43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50ad77922e35e535b5ff1b7d41171e250bd9e379adc3124c89217038fb7a45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Thu, 06 May 2021 21:49:12 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:49:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:49:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:49:17 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:49:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:49:18 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:49:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:49:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:49:18 GMT
USER odoo
# Thu, 06 May 2021 21:49:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:49:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f192a60482e62377afe0585d6ca0537a661b6c573371c7519b3a77d45eb78`  
		Last Modified: Thu, 06 May 2021 21:53:02 GMT  
		Size: 272.7 MB (272671020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4fe1ecd40b0164874a86ecbb4caa7e26a06593c6d96983c1d89137e59092b1`  
		Last Modified: Thu, 06 May 2021 21:52:28 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cd86a8a315b356742c3d072d10d9b44ecbe24b0da947e7a0838c173ba9b92`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba2181ef8d5053b9408e6f8a5438c863bab7cadaca34a163b2fb0df804bcb61`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7361b41d2463cd55eeba366f5561088db4895b5250b5303b19dd7e23031c06`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a0b809d3f15aa96aa445e246a4dc2d708930a6eec8f794c0db4fae9d63cd1e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:10b2f69a988e275e9a9a9903546a910e5937957b4fab10c30eb6233e682f0d43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50ad77922e35e535b5ff1b7d41171e250bd9e379adc3124c89217038fb7a45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Thu, 06 May 2021 21:49:12 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:49:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:49:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:49:17 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:49:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:49:18 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:49:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:49:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:49:18 GMT
USER odoo
# Thu, 06 May 2021 21:49:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:49:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f192a60482e62377afe0585d6ca0537a661b6c573371c7519b3a77d45eb78`  
		Last Modified: Thu, 06 May 2021 21:53:02 GMT  
		Size: 272.7 MB (272671020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4fe1ecd40b0164874a86ecbb4caa7e26a06593c6d96983c1d89137e59092b1`  
		Last Modified: Thu, 06 May 2021 21:52:28 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cd86a8a315b356742c3d072d10d9b44ecbe24b0da947e7a0838c173ba9b92`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba2181ef8d5053b9408e6f8a5438c863bab7cadaca34a163b2fb0df804bcb61`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7361b41d2463cd55eeba366f5561088db4895b5250b5303b19dd7e23031c06`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:a0b809d3f15aa96aa445e246a4dc2d708930a6eec8f794c0db4fae9d63cd1e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:10b2f69a988e275e9a9a9903546a910e5937957b4fab10c30eb6233e682f0d43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50ad77922e35e535b5ff1b7d41171e250bd9e379adc3124c89217038fb7a45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Thu, 06 May 2021 21:49:12 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:49:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:49:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:49:17 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:49:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:49:18 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:49:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:49:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:49:18 GMT
USER odoo
# Thu, 06 May 2021 21:49:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:49:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f192a60482e62377afe0585d6ca0537a661b6c573371c7519b3a77d45eb78`  
		Last Modified: Thu, 06 May 2021 21:53:02 GMT  
		Size: 272.7 MB (272671020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4fe1ecd40b0164874a86ecbb4caa7e26a06593c6d96983c1d89137e59092b1`  
		Last Modified: Thu, 06 May 2021 21:52:28 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cd86a8a315b356742c3d072d10d9b44ecbe24b0da947e7a0838c173ba9b92`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba2181ef8d5053b9408e6f8a5438c863bab7cadaca34a163b2fb0df804bcb61`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7361b41d2463cd55eeba366f5561088db4895b5250b5303b19dd7e23031c06`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
