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
$ docker pull odoo@sha256:ddd85e67efb97cceee9f0942f97b63bf3c34ac1c6195a7eaa8124fa40e9fab3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:de62f2fda8b9764b0926239a3637761560bead453f8170d97572e5d0874b7365
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541024316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08550fa91063466d29db2f4485341926d9ed33494cf0ad90a7dd212e4cbea794`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:33:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:33:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:33:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Feb 2021 17:35:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:36:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:16 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:17 GMT
ENV ODOO_VERSION=12.0
# Wed, 10 Feb 2021 19:28:09 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:28:09 GMT
ARG ODOO_SHA=5dbafa58ade2b5f6222bb0126bff0c31c61fe7f9
# Wed, 10 Feb 2021 19:29:12 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=5dbafa58ade2b5f6222bb0126bff0c31c61fe7f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:29:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:29:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:29:14 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=5dbafa58ade2b5f6222bb0126bff0c31c61fe7f9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:29:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:29:15 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:29:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:29:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:29:15 GMT
USER odoo
# Wed, 10 Feb 2021 19:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:29:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1cabf5609130f825def08a86940a9a06f7025505559b2c7e652b60a9e05005`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23230155ecde52cbc43dbfe8141ef3dcbfaa6a5e242654c5ff6071e727f0a9`  
		Last Modified: Tue, 09 Feb 2021 17:41:19 GMT  
		Size: 219.6 MB (219611261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ff187134bcc9d0cf0a66450af847efce4bd9dc973a88ae485acff4a4b3df1`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 2.2 MB (2222432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5ca9709c7ca8d1819e6f5e6a2a15591eb75f5cf82ba48c2825cde329116c8`  
		Last Modified: Tue, 09 Feb 2021 17:41:01 GMT  
		Size: 22.1 MB (22055467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742a59abefa99d85b58742e4857b05e2e680539a412330540c0922e363c20afc`  
		Last Modified: Wed, 10 Feb 2021 19:31:33 GMT  
		Size: 274.6 MB (274603927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994fc28ff8295006d52267af6429ed43f72f10b1ac455bc45e3cf289a9f2bfe`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bcf7b8d62fc0d51c7b010eedc5c6fe18a5309ee2178c13195c629ba5aee1c`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e582271cb30ddbaf99cbc31f50acd754c3e614ccc36224a8272e65eb7e7723`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c64efb0ecbcc5032509cdb9e4b7ff6478097331a6ce346c1ddcab38756301`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:ddd85e67efb97cceee9f0942f97b63bf3c34ac1c6195a7eaa8124fa40e9fab3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:de62f2fda8b9764b0926239a3637761560bead453f8170d97572e5d0874b7365
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541024316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08550fa91063466d29db2f4485341926d9ed33494cf0ad90a7dd212e4cbea794`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:33:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:33:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:33:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Feb 2021 17:35:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:36:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:16 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:36:17 GMT
ENV ODOO_VERSION=12.0
# Wed, 10 Feb 2021 19:28:09 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:28:09 GMT
ARG ODOO_SHA=5dbafa58ade2b5f6222bb0126bff0c31c61fe7f9
# Wed, 10 Feb 2021 19:29:12 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=5dbafa58ade2b5f6222bb0126bff0c31c61fe7f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:29:13 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:29:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:29:14 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=5dbafa58ade2b5f6222bb0126bff0c31c61fe7f9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:29:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:29:15 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:29:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:29:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:29:15 GMT
USER odoo
# Wed, 10 Feb 2021 19:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:29:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1cabf5609130f825def08a86940a9a06f7025505559b2c7e652b60a9e05005`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23230155ecde52cbc43dbfe8141ef3dcbfaa6a5e242654c5ff6071e727f0a9`  
		Last Modified: Tue, 09 Feb 2021 17:41:19 GMT  
		Size: 219.6 MB (219611261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ff187134bcc9d0cf0a66450af847efce4bd9dc973a88ae485acff4a4b3df1`  
		Last Modified: Tue, 09 Feb 2021 17:40:43 GMT  
		Size: 2.2 MB (2222432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5ca9709c7ca8d1819e6f5e6a2a15591eb75f5cf82ba48c2825cde329116c8`  
		Last Modified: Tue, 09 Feb 2021 17:41:01 GMT  
		Size: 22.1 MB (22055467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742a59abefa99d85b58742e4857b05e2e680539a412330540c0922e363c20afc`  
		Last Modified: Wed, 10 Feb 2021 19:31:33 GMT  
		Size: 274.6 MB (274603927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994fc28ff8295006d52267af6429ed43f72f10b1ac455bc45e3cf289a9f2bfe`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bcf7b8d62fc0d51c7b010eedc5c6fe18a5309ee2178c13195c629ba5aee1c`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e582271cb30ddbaf99cbc31f50acd754c3e614ccc36224a8272e65eb7e7723`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c64efb0ecbcc5032509cdb9e4b7ff6478097331a6ce346c1ddcab38756301`  
		Last Modified: Wed, 10 Feb 2021 19:31:01 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:efd690bc780f99decae042b28e6471ebc30013f77046e30af01d0ba9f6642b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:9d6c472cce448ce326df5cf5b8dee17354715e2ed89adef60e83dda4b468e37e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530687814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e38bf8474c7d1951e14ccc2f69fecb80ccbdb71b6abea3c003b5f082fad79ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:32:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:32:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:32:12 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:32:12 GMT
ENV ODOO_VERSION=13.0
# Wed, 10 Feb 2021 19:26:38 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:26:38 GMT
ARG ODOO_SHA=27e67879f5d193ec1af235d8450e46eec79deb5a
# Wed, 10 Feb 2021 19:27:52 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=27e67879f5d193ec1af235d8450e46eec79deb5a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:27:53 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:27:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:27:55 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=27e67879f5d193ec1af235d8450e46eec79deb5a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:27:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:27:55 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:27:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:27:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:27:56 GMT
USER odoo
# Wed, 10 Feb 2021 19:27:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:27:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df63def913e7acc2a8ee5bbdb8dac5f2449993c30e7aff862b1f01f485f5f2`  
		Last Modified: Tue, 09 Feb 2021 17:40:15 GMT  
		Size: 207.1 MB (207097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab203da2fb5d30f709e95af58f20d98a184b7fbc9e8611a5d91717a5fbe1c9`  
		Last Modified: Tue, 09 Feb 2021 17:39:37 GMT  
		Size: 2.3 MB (2343915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16975ddc87358fae6e7b7b9c3809881bdaaf4a63f75c307a3d344c92852557f5`  
		Last Modified: Tue, 09 Feb 2021 17:39:36 GMT  
		Size: 909.0 KB (909031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6dcb19be7d07f69147cd6847b1ba8a6433f40ecb35feb16466f5b900eb7c9b`  
		Last Modified: Wed, 10 Feb 2021 19:30:56 GMT  
		Size: 293.2 MB (293239753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fc1a16852b99c819d5c6f90829b5a52b5bd019688732863d66f88c88b1df58`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97459ad4f33d6bef19a4134e69809215e6c20ddb6c60529fbf7a25822ded6b31`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da135c30e9a92af5eb02b9eefa7cb2d69a22f45ec3c4ed9682fef32cdb058794`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb434de476050a933999c9f891ab79ba9dfd12dbd398df580819fd5ada8fba85`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:efd690bc780f99decae042b28e6471ebc30013f77046e30af01d0ba9f6642b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:9d6c472cce448ce326df5cf5b8dee17354715e2ed89adef60e83dda4b468e37e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530687814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e38bf8474c7d1951e14ccc2f69fecb80ccbdb71b6abea3c003b5f082fad79ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:32:01 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:32:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:32:12 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:32:12 GMT
ENV ODOO_VERSION=13.0
# Wed, 10 Feb 2021 19:26:38 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:26:38 GMT
ARG ODOO_SHA=27e67879f5d193ec1af235d8450e46eec79deb5a
# Wed, 10 Feb 2021 19:27:52 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=27e67879f5d193ec1af235d8450e46eec79deb5a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:27:53 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:27:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:27:55 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=27e67879f5d193ec1af235d8450e46eec79deb5a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:27:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:27:55 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:27:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:27:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:27:56 GMT
USER odoo
# Wed, 10 Feb 2021 19:27:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:27:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df63def913e7acc2a8ee5bbdb8dac5f2449993c30e7aff862b1f01f485f5f2`  
		Last Modified: Tue, 09 Feb 2021 17:40:15 GMT  
		Size: 207.1 MB (207097574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ab203da2fb5d30f709e95af58f20d98a184b7fbc9e8611a5d91717a5fbe1c9`  
		Last Modified: Tue, 09 Feb 2021 17:39:37 GMT  
		Size: 2.3 MB (2343915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16975ddc87358fae6e7b7b9c3809881bdaaf4a63f75c307a3d344c92852557f5`  
		Last Modified: Tue, 09 Feb 2021 17:39:36 GMT  
		Size: 909.0 KB (909031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6dcb19be7d07f69147cd6847b1ba8a6433f40ecb35feb16466f5b900eb7c9b`  
		Last Modified: Wed, 10 Feb 2021 19:30:56 GMT  
		Size: 293.2 MB (293239753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fc1a16852b99c819d5c6f90829b5a52b5bd019688732863d66f88c88b1df58`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97459ad4f33d6bef19a4134e69809215e6c20ddb6c60529fbf7a25822ded6b31`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da135c30e9a92af5eb02b9eefa7cb2d69a22f45ec3c4ed9682fef32cdb058794`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb434de476050a933999c9f891ab79ba9dfd12dbd398df580819fd5ada8fba85`  
		Last Modified: Wed, 10 Feb 2021 19:30:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:36c362a62d23c338c22175181bc9220ee4d19f3aa6cb79e1eb2285f36a593a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:e52530e2968653f0e4e94eb966d4001ae44e30285ad2003f74afd4ce7bf20808
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.1 MB (511099229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf465b413ce56cd1087ff4962e911d9686865078e959d03e3b2d757cd04f62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
# Wed, 10 Feb 2021 19:26:29 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:26:32 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:26:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:26:32 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:26:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:26:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:26:33 GMT
USER odoo
# Wed, 10 Feb 2021 19:26:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:26:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b4381da9ba123f495a5b44f705f0035ef5da695db16ba56ac3c83bdf1a430`  
		Last Modified: Wed, 10 Feb 2021 19:30:12 GMT  
		Size: 267.6 MB (267594264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc830ea2367662177974a1e451ca283013ea6ce2e0ab3cf281427c990ae60b7e`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a469ed8af951afee485d0bb2585aeb1c25e349e0ec83645f113cba3fb8f97762`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505caa5c2264d0ff68c93c505e5c5d26f0f2909860f5c6e8642976f2643f1cd9`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace15cb84631cedfe88d96f84ead474f5d9e99ba2f467b2f90ea176d8c49900`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:36c362a62d23c338c22175181bc9220ee4d19f3aa6cb79e1eb2285f36a593a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:e52530e2968653f0e4e94eb966d4001ae44e30285ad2003f74afd4ce7bf20808
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.1 MB (511099229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf465b413ce56cd1087ff4962e911d9686865078e959d03e3b2d757cd04f62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
# Wed, 10 Feb 2021 19:26:29 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:26:32 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:26:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:26:32 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:26:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:26:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:26:33 GMT
USER odoo
# Wed, 10 Feb 2021 19:26:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:26:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b4381da9ba123f495a5b44f705f0035ef5da695db16ba56ac3c83bdf1a430`  
		Last Modified: Wed, 10 Feb 2021 19:30:12 GMT  
		Size: 267.6 MB (267594264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc830ea2367662177974a1e451ca283013ea6ce2e0ab3cf281427c990ae60b7e`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a469ed8af951afee485d0bb2585aeb1c25e349e0ec83645f113cba3fb8f97762`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505caa5c2264d0ff68c93c505e5c5d26f0f2909860f5c6e8642976f2643f1cd9`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace15cb84631cedfe88d96f84ead474f5d9e99ba2f467b2f90ea176d8c49900`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:36c362a62d23c338c22175181bc9220ee4d19f3aa6cb79e1eb2285f36a593a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:e52530e2968653f0e4e94eb966d4001ae44e30285ad2003f74afd4ce7bf20808
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.1 MB (511099229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf465b413ce56cd1087ff4962e911d9686865078e959d03e3b2d757cd04f62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
# Wed, 10 Feb 2021 19:26:29 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:26:32 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:26:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:26:32 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:26:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:26:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:26:33 GMT
USER odoo
# Wed, 10 Feb 2021 19:26:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:26:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b4381da9ba123f495a5b44f705f0035ef5da695db16ba56ac3c83bdf1a430`  
		Last Modified: Wed, 10 Feb 2021 19:30:12 GMT  
		Size: 267.6 MB (267594264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc830ea2367662177974a1e451ca283013ea6ce2e0ab3cf281427c990ae60b7e`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a469ed8af951afee485d0bb2585aeb1c25e349e0ec83645f113cba3fb8f97762`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505caa5c2264d0ff68c93c505e5c5d26f0f2909860f5c6e8642976f2643f1cd9`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace15cb84631cedfe88d96f84ead474f5d9e99ba2f467b2f90ea176d8c49900`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
