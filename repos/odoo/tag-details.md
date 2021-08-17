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
$ docker pull odoo@sha256:be41fc37c754da2f23bbd1a07738952679c61c526ae03543f11ab2aeb10bf686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:fa9d5ffa5c991ca5b37e216bf0160c9a8f3ecf3d45450479e0d605a320335198
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538412898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fffaa116eba6dfae08de6208f72544153a48f43e725634be24852b7efaf73f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:57:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:57:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:57:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:57:06 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 17 Aug 2021 11:59:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:59:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:59:41 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:59:42 GMT
ENV ODOO_VERSION=12.0
# Tue, 17 Aug 2021 11:59:42 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:59:42 GMT
ARG ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
# Tue, 17 Aug 2021 12:01:08 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 12:01:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 12:01:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 12:01:12 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 12:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 12:01:13 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 12:01:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 12:01:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 12:01:13 GMT
USER odoo
# Tue, 17 Aug 2021 12:01:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 12:01:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2923c7c0d54308fafd7a88052c0b53a0b4215480b42f07b90c1ccc8c5426969c`  
		Last Modified: Tue, 17 Aug 2021 12:03:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d83174e8c27b24896a1504596d30e7d96b40c2fa7fa04bd9a70326057ced19`  
		Last Modified: Tue, 17 Aug 2021 12:03:50 GMT  
		Size: 219.7 MB (219657412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d1db96ed8020ea9c24554f838cbba6fcf73f9a7b887a061bfcb21366c75f68`  
		Last Modified: Tue, 17 Aug 2021 12:03:25 GMT  
		Size: 2.2 MB (2227274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102d45792821fbda173bb15a77775b454e6dd61ecbe64487c9d36dce127cfe4`  
		Last Modified: Tue, 17 Aug 2021 12:03:30 GMT  
		Size: 22.0 MB (22029863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803c5d2e2aafaa7ce0afeed4377405701e42087bc6e311216bb09e85199bd46`  
		Last Modified: Tue, 17 Aug 2021 12:03:54 GMT  
		Size: 272.0 MB (271967908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4607257f443e80f32c20e9121740d148d1961d3d7bfc8d461c22c4fad4279`  
		Last Modified: Tue, 17 Aug 2021 12:03:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2e8c3415af25f52701297d9858a916fe5002d8a149a2f6060975cdeee16f38`  
		Last Modified: Tue, 17 Aug 2021 12:03:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cdfa53565e50cc08187b1e3703b1fea0ad5219c579413152435a8da864135f`  
		Last Modified: Tue, 17 Aug 2021 12:03:21 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8987419c2d1cadca79008e65c6eb788df2bc29caa3b1bf648676ddffd067bc`  
		Last Modified: Tue, 17 Aug 2021 12:03:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:be41fc37c754da2f23bbd1a07738952679c61c526ae03543f11ab2aeb10bf686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:fa9d5ffa5c991ca5b37e216bf0160c9a8f3ecf3d45450479e0d605a320335198
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538412898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fffaa116eba6dfae08de6208f72544153a48f43e725634be24852b7efaf73f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:57:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:57:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:57:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:57:06 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 17 Aug 2021 11:59:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:59:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:59:41 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:59:42 GMT
ENV ODOO_VERSION=12.0
# Tue, 17 Aug 2021 11:59:42 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:59:42 GMT
ARG ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
# Tue, 17 Aug 2021 12:01:08 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 12:01:11 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 12:01:11 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 12:01:12 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 12:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 12:01:13 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 12:01:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 12:01:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 12:01:13 GMT
USER odoo
# Tue, 17 Aug 2021 12:01:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 12:01:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2923c7c0d54308fafd7a88052c0b53a0b4215480b42f07b90c1ccc8c5426969c`  
		Last Modified: Tue, 17 Aug 2021 12:03:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d83174e8c27b24896a1504596d30e7d96b40c2fa7fa04bd9a70326057ced19`  
		Last Modified: Tue, 17 Aug 2021 12:03:50 GMT  
		Size: 219.7 MB (219657412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d1db96ed8020ea9c24554f838cbba6fcf73f9a7b887a061bfcb21366c75f68`  
		Last Modified: Tue, 17 Aug 2021 12:03:25 GMT  
		Size: 2.2 MB (2227274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102d45792821fbda173bb15a77775b454e6dd61ecbe64487c9d36dce127cfe4`  
		Last Modified: Tue, 17 Aug 2021 12:03:30 GMT  
		Size: 22.0 MB (22029863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803c5d2e2aafaa7ce0afeed4377405701e42087bc6e311216bb09e85199bd46`  
		Last Modified: Tue, 17 Aug 2021 12:03:54 GMT  
		Size: 272.0 MB (271967908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea4607257f443e80f32c20e9121740d148d1961d3d7bfc8d461c22c4fad4279`  
		Last Modified: Tue, 17 Aug 2021 12:03:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2e8c3415af25f52701297d9858a916fe5002d8a149a2f6060975cdeee16f38`  
		Last Modified: Tue, 17 Aug 2021 12:03:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cdfa53565e50cc08187b1e3703b1fea0ad5219c579413152435a8da864135f`  
		Last Modified: Tue, 17 Aug 2021 12:03:21 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8987419c2d1cadca79008e65c6eb788df2bc29caa3b1bf648676ddffd067bc`  
		Last Modified: Tue, 17 Aug 2021 12:03:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:f31ddfae57d43109cb743d20710644addcec9e75d675b155dd102d1eedaee08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:0c1ddeab3aadd06bb46bd163b98bd8d341358942d46945ce1e6d32bac09f4351
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528402753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236790d747464025c1c4e841a49afef753f26c0984f68cc605d31672f2dda33f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:50:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:50:57 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:54:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:54:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:55:03 GMT
RUN npm install -g rtlcss
# Tue, 17 Aug 2021 11:55:03 GMT
ENV ODOO_VERSION=13.0
# Tue, 17 Aug 2021 11:55:04 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:55:04 GMT
ARG ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
# Tue, 17 Aug 2021 11:56:43 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 11:56:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 11:56:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 11:56:49 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 11:56:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 11:56:50 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 11:56:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 11:56:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 11:56:51 GMT
USER odoo
# Tue, 17 Aug 2021 11:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 11:56:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef4019d32115e719e7849daceebfc495d4a29215e099498b175740017348f4`  
		Last Modified: Tue, 17 Aug 2021 12:03:05 GMT  
		Size: 207.1 MB (207123736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c018bc7b3d24278ed65a8773e4be24bccdaf939b2aacf69cd0210a8c103ceba`  
		Last Modified: Tue, 17 Aug 2021 12:02:38 GMT  
		Size: 2.3 MB (2347774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc887660e2c04abb2cc72fa325dfda7b313142e3893665e721feb7eb17a2e8`  
		Last Modified: Tue, 17 Aug 2021 12:02:38 GMT  
		Size: 893.4 KB (893428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b621b667dcc28a66046e67083de66316049aa1c1c73d8ff624164c11fae9328d`  
		Last Modified: Tue, 17 Aug 2021 12:03:11 GMT  
		Size: 290.9 MB (290889370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ff19e34b80f045b117700cf00736b4c9b838ecfddd9e30c7c5b1e9012bf28`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f3942af6ca7d174588be8836fdd3fe1647dba5f61a73134d1d2aa3b4457f10`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c811ad6845589e927dabcf338c282bc71188e667df88af9bc0e37d58b238b8`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2032246131dd92e2c47bcce9d2a8472d855196dd284ba23e1cfa4f68fd14c210`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:f31ddfae57d43109cb743d20710644addcec9e75d675b155dd102d1eedaee08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:0c1ddeab3aadd06bb46bd163b98bd8d341358942d46945ce1e6d32bac09f4351
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528402753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236790d747464025c1c4e841a49afef753f26c0984f68cc605d31672f2dda33f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:50:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:50:57 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:54:51 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:54:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:55:03 GMT
RUN npm install -g rtlcss
# Tue, 17 Aug 2021 11:55:03 GMT
ENV ODOO_VERSION=13.0
# Tue, 17 Aug 2021 11:55:04 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:55:04 GMT
ARG ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
# Tue, 17 Aug 2021 11:56:43 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 11:56:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 11:56:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 11:56:49 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 11:56:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 11:56:50 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 11:56:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 11:56:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 11:56:51 GMT
USER odoo
# Tue, 17 Aug 2021 11:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 11:56:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ef4019d32115e719e7849daceebfc495d4a29215e099498b175740017348f4`  
		Last Modified: Tue, 17 Aug 2021 12:03:05 GMT  
		Size: 207.1 MB (207123736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c018bc7b3d24278ed65a8773e4be24bccdaf939b2aacf69cd0210a8c103ceba`  
		Last Modified: Tue, 17 Aug 2021 12:02:38 GMT  
		Size: 2.3 MB (2347774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc887660e2c04abb2cc72fa325dfda7b313142e3893665e721feb7eb17a2e8`  
		Last Modified: Tue, 17 Aug 2021 12:02:38 GMT  
		Size: 893.4 KB (893428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b621b667dcc28a66046e67083de66316049aa1c1c73d8ff624164c11fae9328d`  
		Last Modified: Tue, 17 Aug 2021 12:03:11 GMT  
		Size: 290.9 MB (290889370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6ff19e34b80f045b117700cf00736b4c9b838ecfddd9e30c7c5b1e9012bf28`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f3942af6ca7d174588be8836fdd3fe1647dba5f61a73134d1d2aa3b4457f10`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c811ad6845589e927dabcf338c282bc71188e667df88af9bc0e37d58b238b8`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2032246131dd92e2c47bcce9d2a8472d855196dd284ba23e1cfa4f68fd14c210`  
		Last Modified: Tue, 17 Aug 2021 12:02:35 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:a595234d4ce0f3a5ad86f1daeb2b7f2f8d62595d8fc5702ccababe15f3b97c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:3533f9075153f8c31d716eb79ac291a20bd6ba612ee90a7511a994c618c7e70e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516755980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423b0096eeddea9ff160724e6ce13b31824179c49d4ea4e87066467486dbc2fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:50:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:50:57 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:52:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:52:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:52:33 GMT
RUN npm install -g rtlcss
# Tue, 17 Aug 2021 11:52:33 GMT
ENV ODOO_VERSION=14.0
# Tue, 17 Aug 2021 11:52:33 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:52:33 GMT
ARG ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
# Tue, 17 Aug 2021 11:53:42 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 11:53:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 11:53:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 11:53:46 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 11:53:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 11:53:46 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 11:53:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 11:53:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 11:53:47 GMT
USER odoo
# Tue, 17 Aug 2021 11:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 11:53:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290ecd875bf60f5c0e80a18fd5b45a0b779f65cc38290d9bb278f3654ef490f3`  
		Last Modified: Tue, 17 Aug 2021 12:02:12 GMT  
		Size: 213.2 MB (213171840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8c5deea1aaa9a2e822aff03b88acbec5d6748e713ed8360689dd3b60591384`  
		Last Modified: Tue, 17 Aug 2021 12:01:45 GMT  
		Size: 2.4 MB (2350511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d71bc7341b1c017c73c54c2df560cba3e0d2573fb00225cc7e0dc44d42914`  
		Last Modified: Tue, 17 Aug 2021 12:01:44 GMT  
		Size: 893.4 KB (893418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e16e77f4aec3846d779a42c68e80d16e2e18a0c9b9909b86ec50b57acb336a`  
		Last Modified: Tue, 17 Aug 2021 12:02:19 GMT  
		Size: 273.2 MB (273191764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fc3dfa8f69d5b8b20bbb3c4dc8f72e72268bd5f50c1730bac0874fee1d86bb`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e1f22a6808f970a12d2dfc3433720fa69dfb4e567517dd8061fc003ed5aad4`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8271607ecf5e1fef0245ae7f9a8d0909c41208ed6e21329e56dc532cfdd1d9`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53963699e3c38db6e3147ba37495bf9719c26e25fa12e5e2eb83483ac7c750f`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a595234d4ce0f3a5ad86f1daeb2b7f2f8d62595d8fc5702ccababe15f3b97c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:3533f9075153f8c31d716eb79ac291a20bd6ba612ee90a7511a994c618c7e70e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516755980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423b0096eeddea9ff160724e6ce13b31824179c49d4ea4e87066467486dbc2fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:50:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:50:57 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:52:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:52:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:52:33 GMT
RUN npm install -g rtlcss
# Tue, 17 Aug 2021 11:52:33 GMT
ENV ODOO_VERSION=14.0
# Tue, 17 Aug 2021 11:52:33 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:52:33 GMT
ARG ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
# Tue, 17 Aug 2021 11:53:42 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 11:53:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 11:53:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 11:53:46 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 11:53:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 11:53:46 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 11:53:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 11:53:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 11:53:47 GMT
USER odoo
# Tue, 17 Aug 2021 11:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 11:53:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290ecd875bf60f5c0e80a18fd5b45a0b779f65cc38290d9bb278f3654ef490f3`  
		Last Modified: Tue, 17 Aug 2021 12:02:12 GMT  
		Size: 213.2 MB (213171840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8c5deea1aaa9a2e822aff03b88acbec5d6748e713ed8360689dd3b60591384`  
		Last Modified: Tue, 17 Aug 2021 12:01:45 GMT  
		Size: 2.4 MB (2350511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d71bc7341b1c017c73c54c2df560cba3e0d2573fb00225cc7e0dc44d42914`  
		Last Modified: Tue, 17 Aug 2021 12:01:44 GMT  
		Size: 893.4 KB (893418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e16e77f4aec3846d779a42c68e80d16e2e18a0c9b9909b86ec50b57acb336a`  
		Last Modified: Tue, 17 Aug 2021 12:02:19 GMT  
		Size: 273.2 MB (273191764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fc3dfa8f69d5b8b20bbb3c4dc8f72e72268bd5f50c1730bac0874fee1d86bb`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e1f22a6808f970a12d2dfc3433720fa69dfb4e567517dd8061fc003ed5aad4`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8271607ecf5e1fef0245ae7f9a8d0909c41208ed6e21329e56dc532cfdd1d9`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53963699e3c38db6e3147ba37495bf9719c26e25fa12e5e2eb83483ac7c750f`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:a595234d4ce0f3a5ad86f1daeb2b7f2f8d62595d8fc5702ccababe15f3b97c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:3533f9075153f8c31d716eb79ac291a20bd6ba612ee90a7511a994c618c7e70e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516755980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423b0096eeddea9ff160724e6ce13b31824179c49d4ea4e87066467486dbc2fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Aug 2021 11:50:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Aug 2021 11:50:57 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:52:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 17 Aug 2021 11:52:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:52:33 GMT
RUN npm install -g rtlcss
# Tue, 17 Aug 2021 11:52:33 GMT
ENV ODOO_VERSION=14.0
# Tue, 17 Aug 2021 11:52:33 GMT
ARG ODOO_RELEASE=20210809
# Tue, 17 Aug 2021 11:52:33 GMT
ARG ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
# Tue, 17 Aug 2021 11:53:42 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 17 Aug 2021 11:53:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 17 Aug 2021 11:53:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 17 Aug 2021 11:53:46 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 17 Aug 2021 11:53:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Aug 2021 11:53:46 GMT
EXPOSE 8069 8071 8072
# Tue, 17 Aug 2021 11:53:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Aug 2021 11:53:47 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 17 Aug 2021 11:53:47 GMT
USER odoo
# Tue, 17 Aug 2021 11:53:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 11:53:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290ecd875bf60f5c0e80a18fd5b45a0b779f65cc38290d9bb278f3654ef490f3`  
		Last Modified: Tue, 17 Aug 2021 12:02:12 GMT  
		Size: 213.2 MB (213171840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8c5deea1aaa9a2e822aff03b88acbec5d6748e713ed8360689dd3b60591384`  
		Last Modified: Tue, 17 Aug 2021 12:01:45 GMT  
		Size: 2.4 MB (2350511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6d71bc7341b1c017c73c54c2df560cba3e0d2573fb00225cc7e0dc44d42914`  
		Last Modified: Tue, 17 Aug 2021 12:01:44 GMT  
		Size: 893.4 KB (893418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e16e77f4aec3846d779a42c68e80d16e2e18a0c9b9909b86ec50b57acb336a`  
		Last Modified: Tue, 17 Aug 2021 12:02:19 GMT  
		Size: 273.2 MB (273191764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fc3dfa8f69d5b8b20bbb3c4dc8f72e72268bd5f50c1730bac0874fee1d86bb`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e1f22a6808f970a12d2dfc3433720fa69dfb4e567517dd8061fc003ed5aad4`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8271607ecf5e1fef0245ae7f9a8d0909c41208ed6e21329e56dc532cfdd1d9`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53963699e3c38db6e3147ba37495bf9719c26e25fa12e5e2eb83483ac7c750f`  
		Last Modified: Tue, 17 Aug 2021 12:01:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
