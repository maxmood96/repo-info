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
$ docker pull odoo@sha256:a65fd89b0b22648aaad5f5cca83fb8b5947a869027fc3e0dd90b2d1791d5bb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:a21d37d7dfa20f6ac57f49cbabd8c2e831aeb530b90048dad3940d23cd550b91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541028816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81913516a229b87813a9ee06a8482c4a1c1c32d358345c1551e06177a8d68e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:55:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:55:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:55:53 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:55:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 12 Jan 2021 00:57:36 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:57:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
ENV ODOO_VERSION=12.0
# Fri, 05 Feb 2021 01:22:54 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:22:54 GMT
ARG ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
# Fri, 05 Feb 2021 01:23:57 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:23:58 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:23:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:23:59 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:23:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:23:59 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:23:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:24:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:24:00 GMT
USER odoo
# Fri, 05 Feb 2021 01:24:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:24:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144f7caa9bd25e2b72d1da03a44c4586ddda32d8ec266504d0d1f30dea2a258e`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f19c61dd7d315c35e54a26918c3cd5063439d4351dde65b8241346417d9f526`  
		Last Modified: Tue, 12 Jan 2021 01:01:36 GMT  
		Size: 219.6 MB (219610747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a45cdf8624c5c0646079590cea4c6a7938e46dde1b2377a4353a59614c975`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 2.2 MB (2222454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de80d7b651bc767ace9dafdb74e322d2fc4ca04b271eb8cd5f8d1b1346518171`  
		Last Modified: Tue, 12 Jan 2021 01:01:13 GMT  
		Size: 22.1 MB (22080263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbeff43299cf280c3b0b6a305be0e71f53b5cd5d4a3b7a85977502f5f958e25`  
		Last Modified: Fri, 05 Feb 2021 01:26:18 GMT  
		Size: 274.6 MB (274584115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e33337e8b9037407d9550be5fd1d7984c4a0609fe151c97c62dd46a69150f5`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96963dfa7bb762c29bf0b5e6f9dc2cf43ec02beb5a2c664f7d989b32f2b43eea`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833af8630069163c99fdf0679c3bfa9068e5e1dc83b99d9ab2b31169ca93bccf`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d81b25f20ce74969d470591184126289ac8702a0696ea063e0251af71c443`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:a65fd89b0b22648aaad5f5cca83fb8b5947a869027fc3e0dd90b2d1791d5bb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:a21d37d7dfa20f6ac57f49cbabd8c2e831aeb530b90048dad3940d23cd550b91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (541028816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81913516a229b87813a9ee06a8482c4a1c1c32d358345c1551e06177a8d68e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:55:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:55:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:55:53 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:55:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 12 Jan 2021 00:57:36 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:57:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:58:00 GMT
ENV ODOO_VERSION=12.0
# Fri, 05 Feb 2021 01:22:54 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:22:54 GMT
ARG ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
# Fri, 05 Feb 2021 01:23:57 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:23:58 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:23:58 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:23:59 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=fe07cca16f6c2045f3adbc4470098d4b54fccfc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:23:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:23:59 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:23:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:24:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:24:00 GMT
USER odoo
# Fri, 05 Feb 2021 01:24:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:24:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144f7caa9bd25e2b72d1da03a44c4586ddda32d8ec266504d0d1f30dea2a258e`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f19c61dd7d315c35e54a26918c3cd5063439d4351dde65b8241346417d9f526`  
		Last Modified: Tue, 12 Jan 2021 01:01:36 GMT  
		Size: 219.6 MB (219610747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a45cdf8624c5c0646079590cea4c6a7938e46dde1b2377a4353a59614c975`  
		Last Modified: Tue, 12 Jan 2021 01:01:05 GMT  
		Size: 2.2 MB (2222454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de80d7b651bc767ace9dafdb74e322d2fc4ca04b271eb8cd5f8d1b1346518171`  
		Last Modified: Tue, 12 Jan 2021 01:01:13 GMT  
		Size: 22.1 MB (22080263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbeff43299cf280c3b0b6a305be0e71f53b5cd5d4a3b7a85977502f5f958e25`  
		Last Modified: Fri, 05 Feb 2021 01:26:18 GMT  
		Size: 274.6 MB (274584115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e33337e8b9037407d9550be5fd1d7984c4a0609fe151c97c62dd46a69150f5`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96963dfa7bb762c29bf0b5e6f9dc2cf43ec02beb5a2c664f7d989b32f2b43eea`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833af8630069163c99fdf0679c3bfa9068e5e1dc83b99d9ab2b31169ca93bccf`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d81b25f20ce74969d470591184126289ac8702a0696ea063e0251af71c443`  
		Last Modified: Fri, 05 Feb 2021 01:25:43 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:7fd70111a748d1d93b18b1041839b58d8842c40ddfd30ab42c6348a7e4ecf375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:4ecac274354428a465c914b13246e3444cb5fa062296fdc21df92872a0e4e57a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530676076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628efdd9586b2e7e5caf35d38f959961d6d30175c63fd0e192a54540b1a02d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:54:32 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:54:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:54:43 GMT
ENV ODOO_VERSION=13.0
# Fri, 05 Feb 2021 01:21:23 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:21:23 GMT
ARG ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
# Fri, 05 Feb 2021 01:22:37 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:22:38 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:22:40 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:22:40 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:22:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:22:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:22:41 GMT
USER odoo
# Fri, 05 Feb 2021 01:22:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:22:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc8150f914f7dfd3a86c36b11e2952c897d2730354c258e267ac557063299c`  
		Last Modified: Tue, 12 Jan 2021 01:00:49 GMT  
		Size: 207.1 MB (207075553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1747c1263d10944107d89956ecb6fe0a0ae422613398fbf0a0dd89bd1d2c93`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 2.3 MB (2343766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc37aeea17bfe20046e96480e4e1f4790b31b216198d11c48ed495e8a2bf97`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 929.3 KB (929297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2df670e23627515d09b94c63f9c202dac5f884c277d5a6a40f30a9dc45092b`  
		Last Modified: Fri, 05 Feb 2021 01:25:38 GMT  
		Size: 293.2 MB (293216984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad6d2a12e469e47bd309e4b2ad171ac2679d3671448fb6e8c96d0e49b0cf5eb`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c62728af593e985e18e083cc0b9a742bd5b8ff1646ce5324e7093106ea65abd`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e57931dec02e3a7be61f00315a79e098bcd74f045a152d6e4e2d078ffb54623`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd710ebf1c4c48ef4ab012418aff98b3a407a8df4609f68745c012204d9da5`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:7fd70111a748d1d93b18b1041839b58d8842c40ddfd30ab42c6348a7e4ecf375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:4ecac274354428a465c914b13246e3444cb5fa062296fdc21df92872a0e4e57a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530676076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628efdd9586b2e7e5caf35d38f959961d6d30175c63fd0e192a54540b1a02d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:54:32 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:54:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:54:43 GMT
ENV ODOO_VERSION=13.0
# Fri, 05 Feb 2021 01:21:23 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:21:23 GMT
ARG ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
# Fri, 05 Feb 2021 01:22:37 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:22:38 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:22:40 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=6b81cdf3ed67143010cc8fd6bfce71aa70febca8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:22:40 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:22:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:22:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:22:41 GMT
USER odoo
# Fri, 05 Feb 2021 01:22:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:22:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbc8150f914f7dfd3a86c36b11e2952c897d2730354c258e267ac557063299c`  
		Last Modified: Tue, 12 Jan 2021 01:00:49 GMT  
		Size: 207.1 MB (207075553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1747c1263d10944107d89956ecb6fe0a0ae422613398fbf0a0dd89bd1d2c93`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 2.3 MB (2343766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc37aeea17bfe20046e96480e4e1f4790b31b216198d11c48ed495e8a2bf97`  
		Last Modified: Tue, 12 Jan 2021 01:00:10 GMT  
		Size: 929.3 KB (929297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2df670e23627515d09b94c63f9c202dac5f884c277d5a6a40f30a9dc45092b`  
		Last Modified: Fri, 05 Feb 2021 01:25:38 GMT  
		Size: 293.2 MB (293216984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad6d2a12e469e47bd309e4b2ad171ac2679d3671448fb6e8c96d0e49b0cf5eb`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c62728af593e985e18e083cc0b9a742bd5b8ff1646ce5324e7093106ea65abd`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e57931dec02e3a7be61f00315a79e098bcd74f045a152d6e4e2d078ffb54623`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd710ebf1c4c48ef4ab012418aff98b3a407a8df4609f68745c012204d9da5`  
		Last Modified: Fri, 05 Feb 2021 01:25:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:780f4c3c73c654de3bdd5ddb71d78b6add1057cd9bfff3419b772f90922346ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:7566c7a662dff5fb7112d3a459852dcacd8b63c14da7869af7644645b026f2b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511002077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1703bb7c258b51719bd459c85b9282cb16e9d937c1012b1be598fef6f2036731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:51:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:51:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:52:01 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:52:02 GMT
ENV ODOO_VERSION=14.0
# Fri, 05 Feb 2021 01:20:06 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:20:07 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Fri, 05 Feb 2021 01:21:14 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:21:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:21:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:21:16 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:21:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:21:16 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:21:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:21:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:21:17 GMT
USER odoo
# Fri, 05 Feb 2021 01:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:21:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3d9c87ea56d61be174c3af26ba561264a3c4a33447aa043ca3556ac5773a`  
		Last Modified: Tue, 12 Jan 2021 00:59:47 GMT  
		Size: 213.1 MB (213119359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80c09c10568e31cea43092e745e65e1ca21e5760faa0946402879a9af67c35`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 2.3 MB (2346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce3bc0bd27d17449f9993b0ee55b39ba3098120132f2723ce7cef93ca0f3a4d`  
		Last Modified: Tue, 12 Jan 2021 00:59:10 GMT  
		Size: 929.2 KB (929195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c4455780cc1de64cff82d557c83ccfeee48b05023ecf1fac04622078234f25`  
		Last Modified: Fri, 05 Feb 2021 01:24:55 GMT  
		Size: 267.5 MB (267496786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba47af4298fac502905289afcd95efda48f6271d3db8503475c25878b5834c6`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea90923a15aa0961c687781912ed53e136d46aa5c88735d7345d77c862ea6bac`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b2484bd8e41c5b37814006d313a329b98be0568a93e224d48ca9e86906a56`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98eefbb92a6c99e000609555477a81759bc3b3ea30f1f8b52ac6de561c2855ca`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:780f4c3c73c654de3bdd5ddb71d78b6add1057cd9bfff3419b772f90922346ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:7566c7a662dff5fb7112d3a459852dcacd8b63c14da7869af7644645b026f2b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511002077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1703bb7c258b51719bd459c85b9282cb16e9d937c1012b1be598fef6f2036731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:51:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:51:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:52:01 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:52:02 GMT
ENV ODOO_VERSION=14.0
# Fri, 05 Feb 2021 01:20:06 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:20:07 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Fri, 05 Feb 2021 01:21:14 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:21:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:21:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:21:16 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:21:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:21:16 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:21:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:21:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:21:17 GMT
USER odoo
# Fri, 05 Feb 2021 01:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:21:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3d9c87ea56d61be174c3af26ba561264a3c4a33447aa043ca3556ac5773a`  
		Last Modified: Tue, 12 Jan 2021 00:59:47 GMT  
		Size: 213.1 MB (213119359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80c09c10568e31cea43092e745e65e1ca21e5760faa0946402879a9af67c35`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 2.3 MB (2346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce3bc0bd27d17449f9993b0ee55b39ba3098120132f2723ce7cef93ca0f3a4d`  
		Last Modified: Tue, 12 Jan 2021 00:59:10 GMT  
		Size: 929.2 KB (929195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c4455780cc1de64cff82d557c83ccfeee48b05023ecf1fac04622078234f25`  
		Last Modified: Fri, 05 Feb 2021 01:24:55 GMT  
		Size: 267.5 MB (267496786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba47af4298fac502905289afcd95efda48f6271d3db8503475c25878b5834c6`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea90923a15aa0961c687781912ed53e136d46aa5c88735d7345d77c862ea6bac`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b2484bd8e41c5b37814006d313a329b98be0568a93e224d48ca9e86906a56`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98eefbb92a6c99e000609555477a81759bc3b3ea30f1f8b52ac6de561c2855ca`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:780f4c3c73c654de3bdd5ddb71d78b6add1057cd9bfff3419b772f90922346ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:7566c7a662dff5fb7112d3a459852dcacd8b63c14da7869af7644645b026f2b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.0 MB (511002077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1703bb7c258b51719bd459c85b9282cb16e9d937c1012b1be598fef6f2036731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:50:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Jan 2021 00:50:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Jan 2021 00:50:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 00:51:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Jan 2021 00:51:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 00:52:01 GMT
RUN npm install -g rtlcss
# Tue, 12 Jan 2021 00:52:02 GMT
ENV ODOO_VERSION=14.0
# Fri, 05 Feb 2021 01:20:06 GMT
ARG ODOO_RELEASE=20210204
# Fri, 05 Feb 2021 01:20:07 GMT
ARG ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
# Fri, 05 Feb 2021 01:21:14 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Feb 2021 01:21:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 05 Feb 2021 01:21:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Feb 2021 01:21:16 GMT
# ARGS: ODOO_RELEASE=20210204 ODOO_SHA=2483855a8323e27f623bc664afc4b4470787cfdd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Feb 2021 01:21:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Feb 2021 01:21:16 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Feb 2021 01:21:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Feb 2021 01:21:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Feb 2021 01:21:17 GMT
USER odoo
# Fri, 05 Feb 2021 01:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Feb 2021 01:21:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3d9c87ea56d61be174c3af26ba561264a3c4a33447aa043ca3556ac5773a`  
		Last Modified: Tue, 12 Jan 2021 00:59:47 GMT  
		Size: 213.1 MB (213119359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80c09c10568e31cea43092e745e65e1ca21e5760faa0946402879a9af67c35`  
		Last Modified: Tue, 12 Jan 2021 00:59:09 GMT  
		Size: 2.3 MB (2346263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce3bc0bd27d17449f9993b0ee55b39ba3098120132f2723ce7cef93ca0f3a4d`  
		Last Modified: Tue, 12 Jan 2021 00:59:10 GMT  
		Size: 929.2 KB (929195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c4455780cc1de64cff82d557c83ccfeee48b05023ecf1fac04622078234f25`  
		Last Modified: Fri, 05 Feb 2021 01:24:55 GMT  
		Size: 267.5 MB (267496786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba47af4298fac502905289afcd95efda48f6271d3db8503475c25878b5834c6`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea90923a15aa0961c687781912ed53e136d46aa5c88735d7345d77c862ea6bac`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b2484bd8e41c5b37814006d313a329b98be0568a93e224d48ca9e86906a56`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98eefbb92a6c99e000609555477a81759bc3b3ea30f1f8b52ac6de561c2855ca`  
		Last Modified: Fri, 05 Feb 2021 01:24:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
