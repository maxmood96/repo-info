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
$ docker pull odoo@sha256:38096e047a495bfc6b690c9f2df9a628fee828e48219a20eb6bbea0b3f0e5f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:0666cc06e3708a578b9b9b4f822ec99c4cc603b6c3f162454d53717653c5acbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542622520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a692474fa8d2f4f84049f08375c8677d08b3e0a2619a99a2481d8c617bb6951c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:50:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:50:48 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 12 May 2021 08:52:09 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:52:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:45 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:46 GMT
ENV ODOO_VERSION=12.0
# Tue, 18 May 2021 22:33:55 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:33:55 GMT
ARG ODOO_SHA=217c61f8644ef2dbd72c7e050075d407ffee1e3b
# Tue, 18 May 2021 22:35:00 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=217c61f8644ef2dbd72c7e050075d407ffee1e3b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:35:03 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:35:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:35:04 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=217c61f8644ef2dbd72c7e050075d407ffee1e3b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:35:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:35:05 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:35:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:35:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:35:05 GMT
USER odoo
# Tue, 18 May 2021 22:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:35:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af54249d19fe626a77f15839d273f8d043ce913784302e4e5ee6a810b158f43`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019e7996c57952fa770bb898324d340b77024067ab213469f9fefe533da19ea4`  
		Last Modified: Wed, 12 May 2021 08:57:13 GMT  
		Size: 219.6 MB (219644042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a2f907c0eef99db7b697ab129fdefdf63e755e22e9fee296c13a5179009c44`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764a9260e7d9a4e20c20fb21502f10d7ff5406fe00b088e79e0a80a0c421d5f5`  
		Last Modified: Wed, 12 May 2021 08:56:50 GMT  
		Size: 22.0 MB (22043646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f206889f897217c87c5f0ca76e0507ac27178ab8d6c34c74db0b77588903e868`  
		Last Modified: Tue, 18 May 2021 22:37:27 GMT  
		Size: 276.2 MB (276179771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e3500e4d468cfb24a3a3583ed8b631f1d87a84f60fe169a632e8a3a3879377`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef56307a08dc87063b1034d907a402e500d0d8a9629e2cf9be3b5d41e69b023`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d609b059eab26a0680495ab84777798e825bce045cb0a6a0dedd0550e8c3730`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf2375966a41cf767f1c911eff3199e5ce059e429f6d8d865c0393138ae59a8`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:38096e047a495bfc6b690c9f2df9a628fee828e48219a20eb6bbea0b3f0e5f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:0666cc06e3708a578b9b9b4f822ec99c4cc603b6c3f162454d53717653c5acbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542622520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a692474fa8d2f4f84049f08375c8677d08b3e0a2619a99a2481d8c617bb6951c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:50:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:50:48 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 12 May 2021 08:52:09 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:52:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:45 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:52:46 GMT
ENV ODOO_VERSION=12.0
# Tue, 18 May 2021 22:33:55 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:33:55 GMT
ARG ODOO_SHA=217c61f8644ef2dbd72c7e050075d407ffee1e3b
# Tue, 18 May 2021 22:35:00 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=217c61f8644ef2dbd72c7e050075d407ffee1e3b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:35:03 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:35:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:35:04 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=217c61f8644ef2dbd72c7e050075d407ffee1e3b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:35:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:35:05 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:35:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:35:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:35:05 GMT
USER odoo
# Tue, 18 May 2021 22:35:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:35:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af54249d19fe626a77f15839d273f8d043ce913784302e4e5ee6a810b158f43`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019e7996c57952fa770bb898324d340b77024067ab213469f9fefe533da19ea4`  
		Last Modified: Wed, 12 May 2021 08:57:13 GMT  
		Size: 219.6 MB (219644042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a2f907c0eef99db7b697ab129fdefdf63e755e22e9fee296c13a5179009c44`  
		Last Modified: Wed, 12 May 2021 08:56:45 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764a9260e7d9a4e20c20fb21502f10d7ff5406fe00b088e79e0a80a0c421d5f5`  
		Last Modified: Wed, 12 May 2021 08:56:50 GMT  
		Size: 22.0 MB (22043646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f206889f897217c87c5f0ca76e0507ac27178ab8d6c34c74db0b77588903e868`  
		Last Modified: Tue, 18 May 2021 22:37:27 GMT  
		Size: 276.2 MB (276179771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e3500e4d468cfb24a3a3583ed8b631f1d87a84f60fe169a632e8a3a3879377`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef56307a08dc87063b1034d907a402e500d0d8a9629e2cf9be3b5d41e69b023`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d609b059eab26a0680495ab84777798e825bce045cb0a6a0dedd0550e8c3730`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf2375966a41cf767f1c911eff3199e5ce059e429f6d8d865c0393138ae59a8`  
		Last Modified: Tue, 18 May 2021 22:36:59 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:ae9b24d175b7e4b32ba30d87db332007d55ad0a3b9d0ce870d543346292a5174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:a0915c5db1e4a743633636e59c8e662551079c49ee41a79e602c77edb1811dd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532439360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6075cf29260095226717652ae67a8eb77b6e74efcffe0c35e5384b76e25fa295`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:49:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:49:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:49:14 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:49:14 GMT
ENV ODOO_VERSION=13.0
# Tue, 18 May 2021 22:32:29 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:32:29 GMT
ARG ODOO_SHA=3f034937d378bdf761a78c1e9723a54cef302dbd
# Tue, 18 May 2021 22:33:40 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=3f034937d378bdf761a78c1e9723a54cef302dbd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:33:44 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:33:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:33:45 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=3f034937d378bdf761a78c1e9723a54cef302dbd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:33:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:33:45 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:33:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:33:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:33:46 GMT
USER odoo
# Tue, 18 May 2021 22:33:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:33:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2340d2eb35cffa9ca9e4bde49346d44e9b5256f115d1d5ef505381aa063b2`  
		Last Modified: Wed, 12 May 2021 08:56:16 GMT  
		Size: 207.1 MB (207123504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db2bf3253f515783426050c6c8a278f5d8a9d574287fae7bc3630e3586a0dc7`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 2.3 MB (2345380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37981d08650c3b2e5a5e757ba40494eb86a34a4162414076c592efa41f10e3ea`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 906.3 KB (906348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a102ffff109ae7135fb0e10eb9027127603f8cfef18156a8008dd7cc8cdcc57`  
		Last Modified: Tue, 18 May 2021 22:36:48 GMT  
		Size: 294.9 MB (294915788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ddd107ad8e60cee74d2aaf8e0d3272437a634bbe0bafefd862f9aef30b370c`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6c06c7a5818a62d2903007669eb08411f85d38d4d4cdffbe38d0e4191577b6`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c306f37fd08e66872c5413b148a963be88a8927252b845f73b8142dcbf1f9e`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c8555e07b8c40dcc83e07cbf6913ac26f695b842452bcb7d204d970ea5d206`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:ae9b24d175b7e4b32ba30d87db332007d55ad0a3b9d0ce870d543346292a5174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:a0915c5db1e4a743633636e59c8e662551079c49ee41a79e602c77edb1811dd1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532439360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6075cf29260095226717652ae67a8eb77b6e74efcffe0c35e5384b76e25fa295`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:49:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:49:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:49:14 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:49:14 GMT
ENV ODOO_VERSION=13.0
# Tue, 18 May 2021 22:32:29 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:32:29 GMT
ARG ODOO_SHA=3f034937d378bdf761a78c1e9723a54cef302dbd
# Tue, 18 May 2021 22:33:40 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=3f034937d378bdf761a78c1e9723a54cef302dbd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:33:44 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:33:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:33:45 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=3f034937d378bdf761a78c1e9723a54cef302dbd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:33:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:33:45 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:33:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:33:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:33:46 GMT
USER odoo
# Tue, 18 May 2021 22:33:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:33:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd2340d2eb35cffa9ca9e4bde49346d44e9b5256f115d1d5ef505381aa063b2`  
		Last Modified: Wed, 12 May 2021 08:56:16 GMT  
		Size: 207.1 MB (207123504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db2bf3253f515783426050c6c8a278f5d8a9d574287fae7bc3630e3586a0dc7`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 2.3 MB (2345380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37981d08650c3b2e5a5e757ba40494eb86a34a4162414076c592efa41f10e3ea`  
		Last Modified: Wed, 12 May 2021 08:55:20 GMT  
		Size: 906.3 KB (906348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a102ffff109ae7135fb0e10eb9027127603f8cfef18156a8008dd7cc8cdcc57`  
		Last Modified: Tue, 18 May 2021 22:36:48 GMT  
		Size: 294.9 MB (294915788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ddd107ad8e60cee74d2aaf8e0d3272437a634bbe0bafefd862f9aef30b370c`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6c06c7a5818a62d2903007669eb08411f85d38d4d4cdffbe38d0e4191577b6`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c306f37fd08e66872c5413b148a963be88a8927252b845f73b8142dcbf1f9e`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c8555e07b8c40dcc83e07cbf6913ac26f695b842452bcb7d204d970ea5d206`  
		Last Modified: Tue, 18 May 2021 22:36:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:4e1e147f0e6714e8f8c5806d2b484075b4076ca50490577cdf9162566086d15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:f4b2928f4fd3a58797143ac9731ec140babb70b1b4a7d2d346caba32ef3497c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.3 MB (516343549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb9bda322417dd18badc9dd700531d4921db9517a1adc00ee38238d0f2d9da3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:46:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:46:32 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:46:32 GMT
ENV ODOO_VERSION=14.0
# Tue, 18 May 2021 22:31:04 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:31:04 GMT
ARG ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
# Tue, 18 May 2021 22:32:14 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:32:18 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:32:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:32:19 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:32:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:32:20 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:32:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:32:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:32:20 GMT
USER odoo
# Tue, 18 May 2021 22:32:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:32:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4b0e38652c25af879825f24dbea2383353d341f344d6380e333c3acfe1fdaa`  
		Last Modified: Wed, 12 May 2021 08:54:57 GMT  
		Size: 213.2 MB (213170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9893a9d4028d8617a36b2cec12ad0bd2f635a565ad68099c04d5e7f25aebe81`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 2.3 MB (2348569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646c61bff1d0763d58e8409ab91365ab8469566e7f5cf9a1f9be81b21d4eeeb`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 906.3 KB (906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d68d4c70f53e5dcf24f3d3547238ea5fa01e755d67bf8baf750b9502a9792c4`  
		Last Modified: Tue, 18 May 2021 22:36:02 GMT  
		Size: 272.8 MB (272770208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d20a462844f9c5397e8320cf3ba6e825280195b373bd23f8b1e5894b2cb8e9`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc759d3c7a7ebe524df33ce5f21d299067e260a9c5ca785cccce3b69bfbe571`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715c1e54cb7bd9f3ae5f3920a7e8e0cf964b208722a04fb872ce2a7e98b232c`  
		Last Modified: Tue, 18 May 2021 22:35:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b94a4a0f705d2ee58ea6071c02218571e602cad59c13165b0a85ae3bbd21dce`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:4e1e147f0e6714e8f8c5806d2b484075b4076ca50490577cdf9162566086d15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:f4b2928f4fd3a58797143ac9731ec140babb70b1b4a7d2d346caba32ef3497c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.3 MB (516343549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb9bda322417dd18badc9dd700531d4921db9517a1adc00ee38238d0f2d9da3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:46:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:46:32 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:46:32 GMT
ENV ODOO_VERSION=14.0
# Tue, 18 May 2021 22:31:04 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:31:04 GMT
ARG ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
# Tue, 18 May 2021 22:32:14 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:32:18 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:32:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:32:19 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:32:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:32:20 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:32:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:32:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:32:20 GMT
USER odoo
# Tue, 18 May 2021 22:32:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:32:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4b0e38652c25af879825f24dbea2383353d341f344d6380e333c3acfe1fdaa`  
		Last Modified: Wed, 12 May 2021 08:54:57 GMT  
		Size: 213.2 MB (213170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9893a9d4028d8617a36b2cec12ad0bd2f635a565ad68099c04d5e7f25aebe81`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 2.3 MB (2348569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646c61bff1d0763d58e8409ab91365ab8469566e7f5cf9a1f9be81b21d4eeeb`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 906.3 KB (906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d68d4c70f53e5dcf24f3d3547238ea5fa01e755d67bf8baf750b9502a9792c4`  
		Last Modified: Tue, 18 May 2021 22:36:02 GMT  
		Size: 272.8 MB (272770208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d20a462844f9c5397e8320cf3ba6e825280195b373bd23f8b1e5894b2cb8e9`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc759d3c7a7ebe524df33ce5f21d299067e260a9c5ca785cccce3b69bfbe571`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715c1e54cb7bd9f3ae5f3920a7e8e0cf964b208722a04fb872ce2a7e98b232c`  
		Last Modified: Tue, 18 May 2021 22:35:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b94a4a0f705d2ee58ea6071c02218571e602cad59c13165b0a85ae3bbd21dce`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:4e1e147f0e6714e8f8c5806d2b484075b4076ca50490577cdf9162566086d15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f4b2928f4fd3a58797143ac9731ec140babb70b1b4a7d2d346caba32ef3497c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.3 MB (516343549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb9bda322417dd18badc9dd700531d4921db9517a1adc00ee38238d0f2d9da3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 08:44:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 12 May 2021 08:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 12 May 2021 08:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 08:46:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 12 May 2021 08:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 08:46:32 GMT
RUN npm install -g rtlcss
# Wed, 12 May 2021 08:46:32 GMT
ENV ODOO_VERSION=14.0
# Tue, 18 May 2021 22:31:04 GMT
ARG ODOO_RELEASE=20210518
# Tue, 18 May 2021 22:31:04 GMT
ARG ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
# Tue, 18 May 2021 22:32:14 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 18 May 2021 22:32:18 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 18 May 2021 22:32:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 18 May 2021 22:32:19 GMT
# ARGS: ODOO_RELEASE=20210518 ODOO_SHA=8e479ad5ac2c7374711bf5d7a1991d3d622be562
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 18 May 2021 22:32:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 May 2021 22:32:20 GMT
EXPOSE 8069 8071 8072
# Tue, 18 May 2021 22:32:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 May 2021 22:32:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 18 May 2021 22:32:20 GMT
USER odoo
# Tue, 18 May 2021 22:32:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 May 2021 22:32:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4b0e38652c25af879825f24dbea2383353d341f344d6380e333c3acfe1fdaa`  
		Last Modified: Wed, 12 May 2021 08:54:57 GMT  
		Size: 213.2 MB (213170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9893a9d4028d8617a36b2cec12ad0bd2f635a565ad68099c04d5e7f25aebe81`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 2.3 MB (2348569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646c61bff1d0763d58e8409ab91365ab8469566e7f5cf9a1f9be81b21d4eeeb`  
		Last Modified: Wed, 12 May 2021 08:54:27 GMT  
		Size: 906.3 KB (906251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d68d4c70f53e5dcf24f3d3547238ea5fa01e755d67bf8baf750b9502a9792c4`  
		Last Modified: Tue, 18 May 2021 22:36:02 GMT  
		Size: 272.8 MB (272770208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d20a462844f9c5397e8320cf3ba6e825280195b373bd23f8b1e5894b2cb8e9`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc759d3c7a7ebe524df33ce5f21d299067e260a9c5ca785cccce3b69bfbe571`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715c1e54cb7bd9f3ae5f3920a7e8e0cf964b208722a04fb872ce2a7e98b232c`  
		Last Modified: Tue, 18 May 2021 22:35:31 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b94a4a0f705d2ee58ea6071c02218571e602cad59c13165b0a85ae3bbd21dce`  
		Last Modified: Tue, 18 May 2021 22:35:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
