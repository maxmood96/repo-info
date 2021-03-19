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
$ docker pull odoo@sha256:6db3603ff64a2d0be0fb4db1bd74c8744b62551eda992588492acfd428d70e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:fdbccc26369fc1b2f3fa0f6edb32ade12a758beca36a8fae8e3201e20e82688b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542525600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daea8cb074d1036181c18609b34730ec4c8e176d0d0e9fe3e9ce60a9bb805df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:47 GMT
ADD file:1d706af4169332956a23f3faa02754cb503003812cc1d43ad9b2448f7c26f431 in / 
# Fri, 12 Mar 2021 02:22:48 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:57:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:57:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:57:03 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:57:04 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 12 Mar 2021 21:58:58 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:59:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:59:37 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:59:38 GMT
ENV ODOO_VERSION=12.0
# Thu, 18 Mar 2021 19:37:02 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:37:02 GMT
ARG ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
# Thu, 18 Mar 2021 19:38:06 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:38:09 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:38:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:38:11 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:38:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:38:11 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:38:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:38:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:38:12 GMT
USER odoo
# Thu, 18 Mar 2021 19:38:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:38:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a4feded82f54dd43cb68930d190cb6715378fa2aca3ecce0bcac959359f58d2f`  
		Last Modified: Fri, 12 Mar 2021 02:30:28 GMT  
		Size: 22.5 MB (22528907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4fdcd0eeea96714c68cebab45e9829bdea03b211d07012c38b794a32a2da9`  
		Last Modified: Fri, 12 Mar 2021 22:04:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4794139c6a8d4bc29e2b19577775bd0dec775c86c1f0ee85d7b880d3d7e6`  
		Last Modified: Fri, 12 Mar 2021 22:04:56 GMT  
		Size: 219.6 MB (219625164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46603f24491b1e6612ddc47c2513ba1bda59eef65cb0703b92fa3abd8383418e`  
		Last Modified: Fri, 12 Mar 2021 22:04:02 GMT  
		Size: 2.2 MB (2224012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311b17537573f0466b05333c99351ca6cce0ddee0ed6213728b6ccad9cd30f34`  
		Last Modified: Fri, 12 Mar 2021 22:04:11 GMT  
		Size: 22.1 MB (22053596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f62409976130e465e490aec09e8b872de937cd0528845aeb38bd23bfd7c521`  
		Last Modified: Thu, 18 Mar 2021 19:40:54 GMT  
		Size: 276.1 MB (276091257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed1391b0ae09927d073fd3d809ab8d7d23ae30d0986e024e524a6c39a80f40`  
		Last Modified: Thu, 18 Mar 2021 19:40:23 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d3fae23b5bbaf285a4fb567b4aa65ee28408d22648d9afa25f13f3a3674bd`  
		Last Modified: Thu, 18 Mar 2021 19:40:25 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a559361d402b5c507ec609ee82d161c103d948e24d529d8a991bd80e7c083bd`  
		Last Modified: Thu, 18 Mar 2021 19:40:23 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0dffff092de38c2c550f9cedf8798e61f9b6070a0bc5164d18379b3a09e225`  
		Last Modified: Thu, 18 Mar 2021 19:40:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:6db3603ff64a2d0be0fb4db1bd74c8744b62551eda992588492acfd428d70e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:fdbccc26369fc1b2f3fa0f6edb32ade12a758beca36a8fae8e3201e20e82688b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542525600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daea8cb074d1036181c18609b34730ec4c8e176d0d0e9fe3e9ce60a9bb805df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:22:47 GMT
ADD file:1d706af4169332956a23f3faa02754cb503003812cc1d43ad9b2448f7c26f431 in / 
# Fri, 12 Mar 2021 02:22:48 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:57:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:57:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:57:03 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:57:04 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 12 Mar 2021 21:58:58 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:59:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:59:37 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:59:38 GMT
ENV ODOO_VERSION=12.0
# Thu, 18 Mar 2021 19:37:02 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:37:02 GMT
ARG ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
# Thu, 18 Mar 2021 19:38:06 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:38:09 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:38:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:38:11 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=830878e5deb4133e7bd75360981f397943a7a433
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:38:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:38:11 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:38:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:38:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:38:12 GMT
USER odoo
# Thu, 18 Mar 2021 19:38:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:38:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a4feded82f54dd43cb68930d190cb6715378fa2aca3ecce0bcac959359f58d2f`  
		Last Modified: Fri, 12 Mar 2021 02:30:28 GMT  
		Size: 22.5 MB (22528907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d4fdcd0eeea96714c68cebab45e9829bdea03b211d07012c38b794a32a2da9`  
		Last Modified: Fri, 12 Mar 2021 22:04:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846b4794139c6a8d4bc29e2b19577775bd0dec775c86c1f0ee85d7b880d3d7e6`  
		Last Modified: Fri, 12 Mar 2021 22:04:56 GMT  
		Size: 219.6 MB (219625164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46603f24491b1e6612ddc47c2513ba1bda59eef65cb0703b92fa3abd8383418e`  
		Last Modified: Fri, 12 Mar 2021 22:04:02 GMT  
		Size: 2.2 MB (2224012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311b17537573f0466b05333c99351ca6cce0ddee0ed6213728b6ccad9cd30f34`  
		Last Modified: Fri, 12 Mar 2021 22:04:11 GMT  
		Size: 22.1 MB (22053596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f62409976130e465e490aec09e8b872de937cd0528845aeb38bd23bfd7c521`  
		Last Modified: Thu, 18 Mar 2021 19:40:54 GMT  
		Size: 276.1 MB (276091257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed1391b0ae09927d073fd3d809ab8d7d23ae30d0986e024e524a6c39a80f40`  
		Last Modified: Thu, 18 Mar 2021 19:40:23 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d3fae23b5bbaf285a4fb567b4aa65ee28408d22648d9afa25f13f3a3674bd`  
		Last Modified: Thu, 18 Mar 2021 19:40:25 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a559361d402b5c507ec609ee82d161c103d948e24d529d8a991bd80e7c083bd`  
		Last Modified: Thu, 18 Mar 2021 19:40:23 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0dffff092de38c2c550f9cedf8798e61f9b6070a0bc5164d18379b3a09e225`  
		Last Modified: Thu, 18 Mar 2021 19:40:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:78a959018c4934f112a913c90b0fb60b7eeb232b433ed5f65bf17830a4cefd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:b776fbf649d9790f2ed625cdea0df048a66357b02a5b0a6f4f50b22a1494c202
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532201411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a60117a565db65d6e994193e36a10f9b78156dafe4dbf184bd24915f68f69ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:49:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:49:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:49:40 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:54:40 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:54:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:55:00 GMT
RUN npm install -g rtlcss
# Fri, 12 Mar 2021 21:55:00 GMT
ENV ODOO_VERSION=13.0
# Thu, 18 Mar 2021 19:35:36 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:35:36 GMT
ARG ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
# Thu, 18 Mar 2021 19:36:47 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:36:49 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:36:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:36:50 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:36:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:36:50 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:36:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:36:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:36:51 GMT
USER odoo
# Thu, 18 Mar 2021 19:36:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:36:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d147e9f8313e26b9cdf526c68f98143b5b0e711dab8b2cc3206ee55802106152`  
		Last Modified: Fri, 12 Mar 2021 22:03:25 GMT  
		Size: 207.1 MB (207119290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba7d701f81e9cb5c45029fa66cf880a76fa5d1a05e85d0b67610a8d329a9164`  
		Last Modified: Fri, 12 Mar 2021 22:02:46 GMT  
		Size: 2.3 MB (2345368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e321861ae06e2ea5bb1891e5dcbcef40d462fd069958dec6a437425ca3d05`  
		Last Modified: Fri, 12 Mar 2021 22:02:46 GMT  
		Size: 908.6 KB (908574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d988d45bc75ae826fbd8ce21502ab75c2b4691d9b2deb16d0ff8f67bcf02bc`  
		Last Modified: Thu, 18 Mar 2021 19:40:11 GMT  
		Size: 294.7 MB (294724750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96a7667f4465c5a1c9c9e4d07d88a69a52765c739b8392dac7d765077c1b2e4`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ed04ba604597b51d14b143a1e3427cd46c89f237b4c2f9c5bff67b2063d146`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf9c2264fb41042aba4c62cc78f48be2c653790a065a15902b05f2eb32e7720`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891ecd49912acccbcd4e92d2938fc6c7ec7fbd0500a52387047688ec1d0c55`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:78a959018c4934f112a913c90b0fb60b7eeb232b433ed5f65bf17830a4cefd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:b776fbf649d9790f2ed625cdea0df048a66357b02a5b0a6f4f50b22a1494c202
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532201411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a60117a565db65d6e994193e36a10f9b78156dafe4dbf184bd24915f68f69ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:49:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:49:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:49:40 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:54:40 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:54:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:55:00 GMT
RUN npm install -g rtlcss
# Fri, 12 Mar 2021 21:55:00 GMT
ENV ODOO_VERSION=13.0
# Thu, 18 Mar 2021 19:35:36 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:35:36 GMT
ARG ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
# Thu, 18 Mar 2021 19:36:47 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:36:49 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:36:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:36:50 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=e72e224190d65a9679b764f085b2403fcb6ad97d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:36:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:36:50 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:36:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:36:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:36:51 GMT
USER odoo
# Thu, 18 Mar 2021 19:36:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:36:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d147e9f8313e26b9cdf526c68f98143b5b0e711dab8b2cc3206ee55802106152`  
		Last Modified: Fri, 12 Mar 2021 22:03:25 GMT  
		Size: 207.1 MB (207119290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba7d701f81e9cb5c45029fa66cf880a76fa5d1a05e85d0b67610a8d329a9164`  
		Last Modified: Fri, 12 Mar 2021 22:02:46 GMT  
		Size: 2.3 MB (2345368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161e321861ae06e2ea5bb1891e5dcbcef40d462fd069958dec6a437425ca3d05`  
		Last Modified: Fri, 12 Mar 2021 22:02:46 GMT  
		Size: 908.6 KB (908574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d988d45bc75ae826fbd8ce21502ab75c2b4691d9b2deb16d0ff8f67bcf02bc`  
		Last Modified: Thu, 18 Mar 2021 19:40:11 GMT  
		Size: 294.7 MB (294724750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96a7667f4465c5a1c9c9e4d07d88a69a52765c739b8392dac7d765077c1b2e4`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ed04ba604597b51d14b143a1e3427cd46c89f237b4c2f9c5bff67b2063d146`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf9c2264fb41042aba4c62cc78f48be2c653790a065a15902b05f2eb32e7720`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891ecd49912acccbcd4e92d2938fc6c7ec7fbd0500a52387047688ec1d0c55`  
		Last Modified: Thu, 18 Mar 2021 19:39:35 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:3556dc2519a135d48f1a60ac179a9a6b6cd65208547370a6615883c82e7e4fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:af3445627c6a235f7d4560c43b6787a810519b7098b07e8739a3587c05deddf6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515344447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a732e1e3d036468084e506c097791b128f1c2cc116f4acadf7c367b1c5174c23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:49:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:49:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:49:40 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:51:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:51:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:51:42 GMT
RUN npm install -g rtlcss
# Fri, 12 Mar 2021 21:51:43 GMT
ENV ODOO_VERSION=14.0
# Thu, 18 Mar 2021 19:34:10 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:34:11 GMT
ARG ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
# Thu, 18 Mar 2021 19:35:20 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:35:24 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:35:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:35:25 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:35:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:35:26 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:35:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:35:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:35:26 GMT
USER odoo
# Thu, 18 Mar 2021 19:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:35:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951b769785cc5d78c0e0180853756a9b169b199230862dde077cc9b7e23f039c`  
		Last Modified: Fri, 12 Mar 2021 22:02:22 GMT  
		Size: 213.2 MB (213158063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ceada3ee9708b7debe052477fe9f95795b584ebd3386bbe9e2024834256af6`  
		Last Modified: Fri, 12 Mar 2021 22:01:49 GMT  
		Size: 2.3 MB (2348603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742fc2b8cc3c337d65d7f660dfd90cc3f1d68a56a849733aa56f8a67251c3668`  
		Last Modified: Fri, 12 Mar 2021 22:01:48 GMT  
		Size: 908.3 KB (908301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c75fe3213895cffbe6bc67006a419883e9efcfcc676e40badf7d7012813031`  
		Last Modified: Thu, 18 Mar 2021 19:39:21 GMT  
		Size: 271.8 MB (271826048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad2d2a98733be09aaa469e7b5a8d37722c6afaecf5796967243afe61368615d`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc275a6574da24d180cba5306695767cacf4bbe196a525190bcf7b81771767`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c7b0e9993364d3130bea48f493e5136d4f2d8d91fd2f8de032be017b4f572`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9746083e9dc1206b341fbba60df897fd954b6a5e37f964d5445998c30cef52`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:3556dc2519a135d48f1a60ac179a9a6b6cd65208547370a6615883c82e7e4fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:af3445627c6a235f7d4560c43b6787a810519b7098b07e8739a3587c05deddf6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515344447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a732e1e3d036468084e506c097791b128f1c2cc116f4acadf7c367b1c5174c23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:49:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:49:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:49:40 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:51:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:51:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:51:42 GMT
RUN npm install -g rtlcss
# Fri, 12 Mar 2021 21:51:43 GMT
ENV ODOO_VERSION=14.0
# Thu, 18 Mar 2021 19:34:10 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:34:11 GMT
ARG ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
# Thu, 18 Mar 2021 19:35:20 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:35:24 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:35:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:35:25 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:35:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:35:26 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:35:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:35:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:35:26 GMT
USER odoo
# Thu, 18 Mar 2021 19:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:35:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951b769785cc5d78c0e0180853756a9b169b199230862dde077cc9b7e23f039c`  
		Last Modified: Fri, 12 Mar 2021 22:02:22 GMT  
		Size: 213.2 MB (213158063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ceada3ee9708b7debe052477fe9f95795b584ebd3386bbe9e2024834256af6`  
		Last Modified: Fri, 12 Mar 2021 22:01:49 GMT  
		Size: 2.3 MB (2348603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742fc2b8cc3c337d65d7f660dfd90cc3f1d68a56a849733aa56f8a67251c3668`  
		Last Modified: Fri, 12 Mar 2021 22:01:48 GMT  
		Size: 908.3 KB (908301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c75fe3213895cffbe6bc67006a419883e9efcfcc676e40badf7d7012813031`  
		Last Modified: Thu, 18 Mar 2021 19:39:21 GMT  
		Size: 271.8 MB (271826048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad2d2a98733be09aaa469e7b5a8d37722c6afaecf5796967243afe61368615d`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc275a6574da24d180cba5306695767cacf4bbe196a525190bcf7b81771767`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c7b0e9993364d3130bea48f493e5136d4f2d8d91fd2f8de032be017b4f572`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9746083e9dc1206b341fbba60df897fd954b6a5e37f964d5445998c30cef52`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:3556dc2519a135d48f1a60ac179a9a6b6cd65208547370a6615883c82e7e4fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:af3445627c6a235f7d4560c43b6787a810519b7098b07e8739a3587c05deddf6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515344447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a732e1e3d036468084e506c097791b128f1c2cc116f4acadf7c367b1c5174c23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 21:49:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 12 Mar 2021 21:49:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 12 Mar 2021 21:49:40 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 21:51:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 12 Mar 2021 21:51:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 21:51:42 GMT
RUN npm install -g rtlcss
# Fri, 12 Mar 2021 21:51:43 GMT
ENV ODOO_VERSION=14.0
# Thu, 18 Mar 2021 19:34:10 GMT
ARG ODOO_RELEASE=20210318
# Thu, 18 Mar 2021 19:34:11 GMT
ARG ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
# Thu, 18 Mar 2021 19:35:20 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 18 Mar 2021 19:35:24 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 18 Mar 2021 19:35:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 18 Mar 2021 19:35:25 GMT
# ARGS: ODOO_RELEASE=20210318 ODOO_SHA=c8b020d0a3197f02ed75d8245c8626f9f123edf2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 18 Mar 2021 19:35:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Mar 2021 19:35:26 GMT
EXPOSE 8069 8071 8072
# Thu, 18 Mar 2021 19:35:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Mar 2021 19:35:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 18 Mar 2021 19:35:26 GMT
USER odoo
# Thu, 18 Mar 2021 19:35:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Mar 2021 19:35:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951b769785cc5d78c0e0180853756a9b169b199230862dde077cc9b7e23f039c`  
		Last Modified: Fri, 12 Mar 2021 22:02:22 GMT  
		Size: 213.2 MB (213158063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ceada3ee9708b7debe052477fe9f95795b584ebd3386bbe9e2024834256af6`  
		Last Modified: Fri, 12 Mar 2021 22:01:49 GMT  
		Size: 2.3 MB (2348603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742fc2b8cc3c337d65d7f660dfd90cc3f1d68a56a849733aa56f8a67251c3668`  
		Last Modified: Fri, 12 Mar 2021 22:01:48 GMT  
		Size: 908.3 KB (908301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c75fe3213895cffbe6bc67006a419883e9efcfcc676e40badf7d7012813031`  
		Last Modified: Thu, 18 Mar 2021 19:39:21 GMT  
		Size: 271.8 MB (271826048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad2d2a98733be09aaa469e7b5a8d37722c6afaecf5796967243afe61368615d`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc275a6574da24d180cba5306695767cacf4bbe196a525190bcf7b81771767`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0c7b0e9993364d3130bea48f493e5136d4f2d8d91fd2f8de032be017b4f572`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9746083e9dc1206b341fbba60df897fd954b6a5e37f964d5445998c30cef52`  
		Last Modified: Thu, 18 Mar 2021 19:38:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
