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
$ docker pull odoo@sha256:4560803ba4274efe2714e445f857085b1dcf6842abfaeb1fd9a2d10160fe354f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:dcc5f8855296cb5b1a42868a8d644b6aac8677fc0d3dcf1757bb6b78f86501ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542598096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10814fbd3bd4e55ddc9346f921286b1fbf26ae39eb81d94a8cd70f01bdeb138a`
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
# Wed, 12 May 2021 08:52:46 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:52:46 GMT
ARG ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
# Wed, 12 May 2021 08:53:55 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:53:58 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:53:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:54:00 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:54:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:54:00 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:54:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:54:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:54:01 GMT
USER odoo
# Wed, 12 May 2021 08:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:54:01 GMT
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
	-	`sha256:70033d5e59356e84778c9e4850f4862cecff92a50b1217ec727b90de76c6889a`  
		Last Modified: Wed, 12 May 2021 08:57:18 GMT  
		Size: 276.2 MB (276155352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82feb446c6167809886117ff7dcb49a5871db0eea8bd908e7476286f3a42bde6`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45104fcfea178e0f89fa719cc1cbc7835449bdf31a115ecc3ec0b69107256c5a`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fca99c6bbe2891dfbc1f6f792c99e517f49744537e32fabad3e2dc392b8cf`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f7bc54c88c044de5fefb69185740a2690f570a4cbc8b01222c22d6b9f6bad`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:4560803ba4274efe2714e445f857085b1dcf6842abfaeb1fd9a2d10160fe354f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:dcc5f8855296cb5b1a42868a8d644b6aac8677fc0d3dcf1757bb6b78f86501ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542598096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10814fbd3bd4e55ddc9346f921286b1fbf26ae39eb81d94a8cd70f01bdeb138a`
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
# Wed, 12 May 2021 08:52:46 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:52:46 GMT
ARG ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
# Wed, 12 May 2021 08:53:55 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:53:58 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:53:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:54:00 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=9898d765f0c31031f86c011d2022f5485ad9b7b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:54:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:54:00 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:54:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:54:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:54:01 GMT
USER odoo
# Wed, 12 May 2021 08:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:54:01 GMT
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
	-	`sha256:70033d5e59356e84778c9e4850f4862cecff92a50b1217ec727b90de76c6889a`  
		Last Modified: Wed, 12 May 2021 08:57:18 GMT  
		Size: 276.2 MB (276155352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82feb446c6167809886117ff7dcb49a5871db0eea8bd908e7476286f3a42bde6`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45104fcfea178e0f89fa719cc1cbc7835449bdf31a115ecc3ec0b69107256c5a`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fca99c6bbe2891dfbc1f6f792c99e517f49744537e32fabad3e2dc392b8cf`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f7bc54c88c044de5fefb69185740a2690f570a4cbc8b01222c22d6b9f6bad`  
		Last Modified: Wed, 12 May 2021 08:56:42 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:6e647fd3697779b6e60b37ca54fe8129eccb76d003a425c53d5ab61ab54cb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:042d15de96491a703932f99fc504e734f12a42580ac4a9a4099c57f85301885e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532387079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf29933fcf61f0f0b6a38beee0cbae06ab1d6ab9b21f29205c948fba90194af`
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
# Wed, 12 May 2021 08:49:14 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:49:14 GMT
ARG ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
# Wed, 12 May 2021 08:50:26 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:50:30 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:50:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:50:31 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:50:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:50:32 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:50:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:50:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:50:32 GMT
USER odoo
# Wed, 12 May 2021 08:50:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:50:33 GMT
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
	-	`sha256:1fc89912cb71bc76ceec7019a851bc04d354a1bd12fafe61983e25934a00fe0f`  
		Last Modified: Wed, 12 May 2021 08:56:25 GMT  
		Size: 294.9 MB (294863503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c15cabb75ab0d8e22d641a83fca87ccb8817569e3e54d9725f1c77d9aa77c61`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1fe64f930f4341dc52786a37d0636e5282cb7932b224e9ac1871fddda95ba5`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06d333be0a7dff9f7e8db018d52679254069cefe08543a4ec510a0affd426ac`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bf088058af427af5f47642c694e4be7ddacc1e76a15f3f07936a216c1e007b`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:6e647fd3697779b6e60b37ca54fe8129eccb76d003a425c53d5ab61ab54cb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:042d15de96491a703932f99fc504e734f12a42580ac4a9a4099c57f85301885e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532387079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf29933fcf61f0f0b6a38beee0cbae06ab1d6ab9b21f29205c948fba90194af`
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
# Wed, 12 May 2021 08:49:14 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:49:14 GMT
ARG ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
# Wed, 12 May 2021 08:50:26 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:50:30 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:50:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:50:31 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=3de3d32b1bb5491855f49480d3d4c2985de9ef62
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:50:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:50:32 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:50:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:50:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:50:32 GMT
USER odoo
# Wed, 12 May 2021 08:50:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:50:33 GMT
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
	-	`sha256:1fc89912cb71bc76ceec7019a851bc04d354a1bd12fafe61983e25934a00fe0f`  
		Last Modified: Wed, 12 May 2021 08:56:25 GMT  
		Size: 294.9 MB (294863503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c15cabb75ab0d8e22d641a83fca87ccb8817569e3e54d9725f1c77d9aa77c61`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1fe64f930f4341dc52786a37d0636e5282cb7932b224e9ac1871fddda95ba5`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06d333be0a7dff9f7e8db018d52679254069cefe08543a4ec510a0affd426ac`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bf088058af427af5f47642c694e4be7ddacc1e76a15f3f07936a216c1e007b`  
		Last Modified: Wed, 12 May 2021 08:55:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:d52a9335ef5eb663af285cff4a47bc9c1c834131aaf130a07f8e048ad18f0268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:26479e1c9294862e5efc226b116cccab437da0b895c94a84b0165f7a6c892a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516240369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4370cddec27a3129d87ea738528d86ca08e85d0851dc1b9dd05b9d4d060c9bf`
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
# Wed, 12 May 2021 08:46:32 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:46:33 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Wed, 12 May 2021 08:47:44 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:47:46 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:47:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:47:47 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:47:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:47:47 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:47:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:47:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:47:48 GMT
USER odoo
# Wed, 12 May 2021 08:47:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:47:49 GMT
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
	-	`sha256:b98f921d4963c96662034e120550b29f1c89119b2663f19ac3d5c88cd1d27078`  
		Last Modified: Wed, 12 May 2021 08:55:03 GMT  
		Size: 272.7 MB (272667028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c772f6a0c0de260e204a15f9a5c412a8d5aa18b03b9aafd624f5cfea930c9bc9`  
		Last Modified: Wed, 12 May 2021 08:54:24 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d042635481664ea3eeee4f4067e6d0293a63b16ecdded65215ced24a72e4ebb9`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17f15517eee98246cfbb45a79a501b57040ddfded6d78777c417a0ace7dfa1a`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638955958d6df690dc2242494d6c2ac9fa941e4a3c1ce988a00b0729b7e89dd`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:d52a9335ef5eb663af285cff4a47bc9c1c834131aaf130a07f8e048ad18f0268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:26479e1c9294862e5efc226b116cccab437da0b895c94a84b0165f7a6c892a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516240369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4370cddec27a3129d87ea738528d86ca08e85d0851dc1b9dd05b9d4d060c9bf`
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
# Wed, 12 May 2021 08:46:32 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:46:33 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Wed, 12 May 2021 08:47:44 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:47:46 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:47:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:47:47 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:47:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:47:47 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:47:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:47:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:47:48 GMT
USER odoo
# Wed, 12 May 2021 08:47:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:47:49 GMT
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
	-	`sha256:b98f921d4963c96662034e120550b29f1c89119b2663f19ac3d5c88cd1d27078`  
		Last Modified: Wed, 12 May 2021 08:55:03 GMT  
		Size: 272.7 MB (272667028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c772f6a0c0de260e204a15f9a5c412a8d5aa18b03b9aafd624f5cfea930c9bc9`  
		Last Modified: Wed, 12 May 2021 08:54:24 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d042635481664ea3eeee4f4067e6d0293a63b16ecdded65215ced24a72e4ebb9`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17f15517eee98246cfbb45a79a501b57040ddfded6d78777c417a0ace7dfa1a`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638955958d6df690dc2242494d6c2ac9fa941e4a3c1ce988a00b0729b7e89dd`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:d52a9335ef5eb663af285cff4a47bc9c1c834131aaf130a07f8e048ad18f0268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:26479e1c9294862e5efc226b116cccab437da0b895c94a84b0165f7a6c892a55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516240369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4370cddec27a3129d87ea738528d86ca08e85d0851dc1b9dd05b9d4d060c9bf`
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
# Wed, 12 May 2021 08:46:32 GMT
ARG ODOO_RELEASE=20210506
# Wed, 12 May 2021 08:46:33 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Wed, 12 May 2021 08:47:44 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 12 May 2021 08:47:46 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 12 May 2021 08:47:46 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 12 May 2021 08:47:47 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 12 May 2021 08:47:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 12 May 2021 08:47:47 GMT
EXPOSE 8069 8071 8072
# Wed, 12 May 2021 08:47:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 12 May 2021 08:47:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 12 May 2021 08:47:48 GMT
USER odoo
# Wed, 12 May 2021 08:47:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 12 May 2021 08:47:49 GMT
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
	-	`sha256:b98f921d4963c96662034e120550b29f1c89119b2663f19ac3d5c88cd1d27078`  
		Last Modified: Wed, 12 May 2021 08:55:03 GMT  
		Size: 272.7 MB (272667028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c772f6a0c0de260e204a15f9a5c412a8d5aa18b03b9aafd624f5cfea930c9bc9`  
		Last Modified: Wed, 12 May 2021 08:54:24 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d042635481664ea3eeee4f4067e6d0293a63b16ecdded65215ced24a72e4ebb9`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17f15517eee98246cfbb45a79a501b57040ddfded6d78777c417a0ace7dfa1a`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1638955958d6df690dc2242494d6c2ac9fa941e4a3c1ce988a00b0729b7e89dd`  
		Last Modified: Wed, 12 May 2021 08:54:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
