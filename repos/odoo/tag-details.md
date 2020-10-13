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
$ docker pull odoo@sha256:789d6f71fbd36d0ea691cb1cb6255de1280ede083bd3776e7500357a786820a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:bb47dd6c3bfada2cd168dd0ff91b6f608d6ca9e4fd4514ab3d16b4163c80532e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396782808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b0fb69fa0e13af0379df76b41dfc669d65c7abc16e4c8bf7a9454041c7c378`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:55:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:55:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:55:34 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:55:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 13 Oct 2020 17:57:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:58:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
ENV ODOO_VERSION=12.0
# Tue, 13 Oct 2020 17:58:20 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:58:20 GMT
ARG ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
# Tue, 13 Oct 2020 17:59:09 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:59:10 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:59:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:59:11 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:59:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:59:11 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:59:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:59:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:59:12 GMT
USER odoo
# Tue, 13 Oct 2020 17:59:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:59:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e899471950fb23135e6e3ba4bf5e7d333956a9c8fefef201edb318f76ce8a`  
		Last Modified: Tue, 13 Oct 2020 18:03:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469473cc24d8d8f285e28db154936eb275da7e3a962ebb2fb2f6008212d92a36`  
		Last Modified: Tue, 13 Oct 2020 18:04:13 GMT  
		Size: 219.6 MB (219609741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32bdce53191bc591f6a2ef86c27ad27c001afe93d12b1b168c7a49d0c8cf79`  
		Last Modified: Tue, 13 Oct 2020 18:03:26 GMT  
		Size: 2.4 MB (2430770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd870da114a745cbea66677bec90b500570bdfbd3c22ad988b098c8fb150963f`  
		Last Modified: Tue, 13 Oct 2020 18:03:31 GMT  
		Size: 22.3 MB (22262444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee32ca80a66e312779cd536db9e321843a5383f7d726f2981dbf75239ae4201e`  
		Last Modified: Tue, 13 Oct 2020 18:04:16 GMT  
		Size: 130.0 MB (129955125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a982a903168f3376fe2f11357291f363864fe52e4259e224d468581b37753d8`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f771fd3fa06c591f0e39792eee33fc0c807c6bbe6fa80a9d170937ddeeec6b`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e238851e66f22ef53a4197e2941e4ea0c3c82584ebc376fe88e52effd5c1ace1`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec112664ae8b05684ec8d7f8e62d3b91d81cb887eadb1baceb63f3da9bc605c`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:789d6f71fbd36d0ea691cb1cb6255de1280ede083bd3776e7500357a786820a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:bb47dd6c3bfada2cd168dd0ff91b6f608d6ca9e4fd4514ab3d16b4163c80532e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.8 MB (396782808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b0fb69fa0e13af0379df76b41dfc669d65c7abc16e4c8bf7a9454041c7c378`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:55:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:55:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:55:34 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:55:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 13 Oct 2020 17:57:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:58:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:58:19 GMT
ENV ODOO_VERSION=12.0
# Tue, 13 Oct 2020 17:58:20 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:58:20 GMT
ARG ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
# Tue, 13 Oct 2020 17:59:09 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:59:10 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:59:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:59:11 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:59:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:59:11 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:59:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:59:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:59:12 GMT
USER odoo
# Tue, 13 Oct 2020 17:59:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:59:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e899471950fb23135e6e3ba4bf5e7d333956a9c8fefef201edb318f76ce8a`  
		Last Modified: Tue, 13 Oct 2020 18:03:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469473cc24d8d8f285e28db154936eb275da7e3a962ebb2fb2f6008212d92a36`  
		Last Modified: Tue, 13 Oct 2020 18:04:13 GMT  
		Size: 219.6 MB (219609741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c32bdce53191bc591f6a2ef86c27ad27c001afe93d12b1b168c7a49d0c8cf79`  
		Last Modified: Tue, 13 Oct 2020 18:03:26 GMT  
		Size: 2.4 MB (2430770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd870da114a745cbea66677bec90b500570bdfbd3c22ad988b098c8fb150963f`  
		Last Modified: Tue, 13 Oct 2020 18:03:31 GMT  
		Size: 22.3 MB (22262444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee32ca80a66e312779cd536db9e321843a5383f7d726f2981dbf75239ae4201e`  
		Last Modified: Tue, 13 Oct 2020 18:04:16 GMT  
		Size: 130.0 MB (129955125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a982a903168f3376fe2f11357291f363864fe52e4259e224d468581b37753d8`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f771fd3fa06c591f0e39792eee33fc0c807c6bbe6fa80a9d170937ddeeec6b`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e238851e66f22ef53a4197e2941e4ea0c3c82584ebc376fe88e52effd5c1ace1`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec112664ae8b05684ec8d7f8e62d3b91d81cb887eadb1baceb63f3da9bc605c`  
		Last Modified: Tue, 13 Oct 2020 18:03:23 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:e146b0da0b87a6b12f5811a23eaa4c35d4d8e29d3f234ac34bdd2fc1dd23e1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:c284ab42d6fa705a9709202f58e0c2e6d7196f55e367795785f426fe7a33bc85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382912125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50a5f0be8ec2459096f7fff7ba28419a81b24119b2577be2988e0b227651fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:53:32 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:53:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:53:43 GMT
RUN npm install -g rtlcss
# Tue, 13 Oct 2020 17:53:43 GMT
ENV ODOO_VERSION=13.0
# Tue, 13 Oct 2020 17:53:44 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:53:44 GMT
ARG ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
# Tue, 13 Oct 2020 17:55:11 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:55:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:55:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:55:15 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:55:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:55:16 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:55:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:55:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:55:17 GMT
USER odoo
# Tue, 13 Oct 2020 17:55:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:55:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080d1384a06d56bb5b6263a397eff654e4c900e5ad08744e92a9845782fabba0`  
		Last Modified: Tue, 13 Oct 2020 18:03:18 GMT  
		Size: 204.1 MB (204056565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf71f287cee4a77e3c341ff8f3b75e3bd73c08666cbcc2199409b74fdbfda6e3`  
		Last Modified: Tue, 13 Oct 2020 18:00:43 GMT  
		Size: 2.4 MB (2433032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357ff91d4cb0f31c32c8fd0394448c05adc473aadfb206eadd4c178a389fd1e1`  
		Last Modified: Tue, 13 Oct 2020 18:00:43 GMT  
		Size: 1.1 MB (1113227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a51e7fb1f691f8db95d62eb39f63691718357dde32887a9c6b44f65e21ebb55`  
		Last Modified: Tue, 13 Oct 2020 18:01:21 GMT  
		Size: 148.2 MB (148214664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d520a61bbfcb8a460710e2133afe1f92313a8fe173959f1f6c273eef60330`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2dfdd32b656af04b1bc42db74ea5224830dfa1f657a7e7088716780e04ffe2`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2052e857e1d9dcba9509020449902c13c955b7ffab2dec7ff669ab63da8c6942`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40811feb49c16dfa0b2be0f4319e8bab2f9e233a012631b41eae4f65485fed`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:e146b0da0b87a6b12f5811a23eaa4c35d4d8e29d3f234ac34bdd2fc1dd23e1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:c284ab42d6fa705a9709202f58e0c2e6d7196f55e367795785f426fe7a33bc85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382912125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50a5f0be8ec2459096f7fff7ba28419a81b24119b2577be2988e0b227651fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:53:32 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:53:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:53:43 GMT
RUN npm install -g rtlcss
# Tue, 13 Oct 2020 17:53:43 GMT
ENV ODOO_VERSION=13.0
# Tue, 13 Oct 2020 17:53:44 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:53:44 GMT
ARG ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
# Tue, 13 Oct 2020 17:55:11 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:55:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:55:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:55:15 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:55:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:55:16 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:55:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:55:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:55:17 GMT
USER odoo
# Tue, 13 Oct 2020 17:55:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:55:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080d1384a06d56bb5b6263a397eff654e4c900e5ad08744e92a9845782fabba0`  
		Last Modified: Tue, 13 Oct 2020 18:03:18 GMT  
		Size: 204.1 MB (204056565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf71f287cee4a77e3c341ff8f3b75e3bd73c08666cbcc2199409b74fdbfda6e3`  
		Last Modified: Tue, 13 Oct 2020 18:00:43 GMT  
		Size: 2.4 MB (2433032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357ff91d4cb0f31c32c8fd0394448c05adc473aadfb206eadd4c178a389fd1e1`  
		Last Modified: Tue, 13 Oct 2020 18:00:43 GMT  
		Size: 1.1 MB (1113227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a51e7fb1f691f8db95d62eb39f63691718357dde32887a9c6b44f65e21ebb55`  
		Last Modified: Tue, 13 Oct 2020 18:01:21 GMT  
		Size: 148.2 MB (148214664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d520a61bbfcb8a460710e2133afe1f92313a8fe173959f1f6c273eef60330`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2dfdd32b656af04b1bc42db74ea5224830dfa1f657a7e7088716780e04ffe2`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2052e857e1d9dcba9509020449902c13c955b7ffab2dec7ff669ab63da8c6942`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40811feb49c16dfa0b2be0f4319e8bab2f9e233a012631b41eae4f65485fed`  
		Last Modified: Tue, 13 Oct 2020 18:00:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:ed98410e34aa509a9ac15e0b3b70e72f20af71cddcf9da8b72aa27771bc3410a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:22d2f9ae3ddaeb38edde67dc1d0df250cfc63ee597ca30c75062dafe3fe12066
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389748089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6640ab6622b9810ee4918bbae3a4ad9c1c6143a45cf1bcd7932226a6366cd15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:50:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:50:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:50:29 GMT
RUN npm install -g rtlcss
# Tue, 13 Oct 2020 17:50:30 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Oct 2020 17:50:30 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:50:30 GMT
ARG ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
# Tue, 13 Oct 2020 17:51:55 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:51:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:51:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:51:59 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:51:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:52:00 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:52:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:52:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:52:01 GMT
USER odoo
# Tue, 13 Oct 2020 17:52:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:52:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045e37bf5e447ada0775fa9cbaa6602e5df56ecd2d7654731f631db378a3838`  
		Last Modified: Tue, 13 Oct 2020 18:00:36 GMT  
		Size: 210.1 MB (210103895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a9bb8bb89980a701192947a461d73828e3c073813ea3bed9bdbed2fe7c941`  
		Last Modified: Tue, 13 Oct 2020 17:59:28 GMT  
		Size: 2.4 MB (2435674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bfa3a1565153732496452a046b613d641fa51651d842e9622403d4cfa10853`  
		Last Modified: Tue, 13 Oct 2020 17:59:28 GMT  
		Size: 1.1 MB (1113111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbe45d13a50eb48c07353e514fd655a608499d6d04115fe936a91466bbebe91`  
		Last Modified: Tue, 13 Oct 2020 18:00:08 GMT  
		Size: 149.0 MB (149000775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411e9975dd88ee9d1e1b5e9e35dd564c58615940e7e25022ea7c2f784100496f`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4082931efe041f361d332e3aa3799648b505f1c085cfb16971ce3fd798de1b`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18ba2dc6bed974ec4bd3b2a8976752296fc4b4258b0b382c8bcffbe480ab712`  
		Last Modified: Tue, 13 Oct 2020 17:59:27 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b130640629b4e6b129a9ab1a793bc59e970952dd24f486fb529eee5eb72c0af`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:ed98410e34aa509a9ac15e0b3b70e72f20af71cddcf9da8b72aa27771bc3410a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:22d2f9ae3ddaeb38edde67dc1d0df250cfc63ee597ca30c75062dafe3fe12066
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389748089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6640ab6622b9810ee4918bbae3a4ad9c1c6143a45cf1bcd7932226a6366cd15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:50:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:50:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:50:29 GMT
RUN npm install -g rtlcss
# Tue, 13 Oct 2020 17:50:30 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Oct 2020 17:50:30 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:50:30 GMT
ARG ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
# Tue, 13 Oct 2020 17:51:55 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:51:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:51:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:51:59 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:51:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:52:00 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:52:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:52:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:52:01 GMT
USER odoo
# Tue, 13 Oct 2020 17:52:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:52:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045e37bf5e447ada0775fa9cbaa6602e5df56ecd2d7654731f631db378a3838`  
		Last Modified: Tue, 13 Oct 2020 18:00:36 GMT  
		Size: 210.1 MB (210103895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a9bb8bb89980a701192947a461d73828e3c073813ea3bed9bdbed2fe7c941`  
		Last Modified: Tue, 13 Oct 2020 17:59:28 GMT  
		Size: 2.4 MB (2435674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bfa3a1565153732496452a046b613d641fa51651d842e9622403d4cfa10853`  
		Last Modified: Tue, 13 Oct 2020 17:59:28 GMT  
		Size: 1.1 MB (1113111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbe45d13a50eb48c07353e514fd655a608499d6d04115fe936a91466bbebe91`  
		Last Modified: Tue, 13 Oct 2020 18:00:08 GMT  
		Size: 149.0 MB (149000775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411e9975dd88ee9d1e1b5e9e35dd564c58615940e7e25022ea7c2f784100496f`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4082931efe041f361d332e3aa3799648b505f1c085cfb16971ce3fd798de1b`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18ba2dc6bed974ec4bd3b2a8976752296fc4b4258b0b382c8bcffbe480ab712`  
		Last Modified: Tue, 13 Oct 2020 17:59:27 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b130640629b4e6b129a9ab1a793bc59e970952dd24f486fb529eee5eb72c0af`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:ed98410e34aa509a9ac15e0b3b70e72f20af71cddcf9da8b72aa27771bc3410a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:22d2f9ae3ddaeb38edde67dc1d0df250cfc63ee597ca30c75062dafe3fe12066
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389748089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6640ab6622b9810ee4918bbae3a4ad9c1c6143a45cf1bcd7932226a6366cd15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 17:49:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Oct 2020 17:49:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Oct 2020 17:49:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 17:50:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Oct 2020 17:50:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 17:50:29 GMT
RUN npm install -g rtlcss
# Tue, 13 Oct 2020 17:50:30 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Oct 2020 17:50:30 GMT
ARG ODOO_RELEASE=20201012
# Tue, 13 Oct 2020 17:50:30 GMT
ARG ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
# Tue, 13 Oct 2020 17:51:55 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Oct 2020 17:51:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Oct 2020 17:51:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Oct 2020 17:51:59 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Oct 2020 17:51:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Oct 2020 17:52:00 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Oct 2020 17:52:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Oct 2020 17:52:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Oct 2020 17:52:01 GMT
USER odoo
# Tue, 13 Oct 2020 17:52:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Oct 2020 17:52:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045e37bf5e447ada0775fa9cbaa6602e5df56ecd2d7654731f631db378a3838`  
		Last Modified: Tue, 13 Oct 2020 18:00:36 GMT  
		Size: 210.1 MB (210103895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2a9bb8bb89980a701192947a461d73828e3c073813ea3bed9bdbed2fe7c941`  
		Last Modified: Tue, 13 Oct 2020 17:59:28 GMT  
		Size: 2.4 MB (2435674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bfa3a1565153732496452a046b613d641fa51651d842e9622403d4cfa10853`  
		Last Modified: Tue, 13 Oct 2020 17:59:28 GMT  
		Size: 1.1 MB (1113111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbe45d13a50eb48c07353e514fd655a608499d6d04115fe936a91466bbebe91`  
		Last Modified: Tue, 13 Oct 2020 18:00:08 GMT  
		Size: 149.0 MB (149000775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411e9975dd88ee9d1e1b5e9e35dd564c58615940e7e25022ea7c2f784100496f`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4082931efe041f361d332e3aa3799648b505f1c085cfb16971ce3fd798de1b`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18ba2dc6bed974ec4bd3b2a8976752296fc4b4258b0b382c8bcffbe480ab712`  
		Last Modified: Tue, 13 Oct 2020 17:59:27 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b130640629b4e6b129a9ab1a793bc59e970952dd24f486fb529eee5eb72c0af`  
		Last Modified: Tue, 13 Oct 2020 17:59:26 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
