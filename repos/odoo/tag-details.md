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
$ docker pull odoo@sha256:43bbe9acf3b431566e4f961a0f6be4d112cf652e23784286197de817d211e236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:47a51524cd93b07239714687bf73690a48b1ab094af0a6ce319daab29ec1ab94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542575764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abec46a0578f255c95ca9e23a461042cb1836cf741773da206536344ac9b14c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:33:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:33:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:33:51 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:33:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 31 Mar 2021 05:35:18 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:35:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:35:41 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:35:42 GMT
ENV ODOO_VERSION=12.0
# Wed, 07 Apr 2021 19:54:16 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:54:16 GMT
ARG ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
# Wed, 07 Apr 2021 19:55:18 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:55:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:55:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:55:21 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:55:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:55:21 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:55:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:55:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:55:22 GMT
USER odoo
# Wed, 07 Apr 2021 19:55:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:55:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c6915795ca8c7c8930ee76dd81824579247a9450e0bde952170b65c189cc05`  
		Last Modified: Wed, 31 Mar 2021 05:39:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d59774897a449e82a96dccda7da3a9181e64482d2a6670e5d96c91e27e83c1f`  
		Last Modified: Wed, 31 Mar 2021 05:39:30 GMT  
		Size: 219.7 MB (219658871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3f4875f05a0954aceee9441611ab9124140ed09e5366fe97dfe54fe35f8184`  
		Last Modified: Wed, 31 Mar 2021 05:39:01 GMT  
		Size: 2.2 MB (2224092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb531369e15e75947e95abf307ff62714c1f93d4f67ed947cd593d3056264ce`  
		Last Modified: Wed, 31 Mar 2021 05:39:06 GMT  
		Size: 22.0 MB (22042955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf333bf642dc74d7398e7388c58614a27391d4a50ab3d5c312ec411c95c23c5`  
		Last Modified: Wed, 07 Apr 2021 19:57:38 GMT  
		Size: 276.1 MB (276118925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5cf3a3e18b3749f4170e3c8ac304c2746186001995f046b20f1192826b82c`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22121792a80f298f0e6e1ca557633f874ecda10812a4166965ae8aae9afe982b`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c089fac9deaf09572b2762ef00a6011c9fa137da0ecc49e9b504646ac5f589c`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a4ba5e0a90f72f56d1507abc84f2e52f1d413f220b1e5af73804f20d4e9c5a`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:43bbe9acf3b431566e4f961a0f6be4d112cf652e23784286197de817d211e236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:47a51524cd93b07239714687bf73690a48b1ab094af0a6ce319daab29ec1ab94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542575764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abec46a0578f255c95ca9e23a461042cb1836cf741773da206536344ac9b14c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:33:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:33:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:33:51 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:33:52 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 31 Mar 2021 05:35:18 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:35:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:35:41 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:35:42 GMT
ENV ODOO_VERSION=12.0
# Wed, 07 Apr 2021 19:54:16 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:54:16 GMT
ARG ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
# Wed, 07 Apr 2021 19:55:18 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:55:20 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:55:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:55:21 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=c045039b78bf624cafa00b84f5b2b2b1b5fe532e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:55:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:55:21 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:55:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:55:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:55:22 GMT
USER odoo
# Wed, 07 Apr 2021 19:55:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:55:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c6915795ca8c7c8930ee76dd81824579247a9450e0bde952170b65c189cc05`  
		Last Modified: Wed, 31 Mar 2021 05:39:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d59774897a449e82a96dccda7da3a9181e64482d2a6670e5d96c91e27e83c1f`  
		Last Modified: Wed, 31 Mar 2021 05:39:30 GMT  
		Size: 219.7 MB (219658871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3f4875f05a0954aceee9441611ab9124140ed09e5366fe97dfe54fe35f8184`  
		Last Modified: Wed, 31 Mar 2021 05:39:01 GMT  
		Size: 2.2 MB (2224092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb531369e15e75947e95abf307ff62714c1f93d4f67ed947cd593d3056264ce`  
		Last Modified: Wed, 31 Mar 2021 05:39:06 GMT  
		Size: 22.0 MB (22042955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf333bf642dc74d7398e7388c58614a27391d4a50ab3d5c312ec411c95c23c5`  
		Last Modified: Wed, 07 Apr 2021 19:57:38 GMT  
		Size: 276.1 MB (276118925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5cf3a3e18b3749f4170e3c8ac304c2746186001995f046b20f1192826b82c`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22121792a80f298f0e6e1ca557633f874ecda10812a4166965ae8aae9afe982b`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c089fac9deaf09572b2762ef00a6011c9fa137da0ecc49e9b504646ac5f589c`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a4ba5e0a90f72f56d1507abc84f2e52f1d413f220b1e5af73804f20d4e9c5a`  
		Last Modified: Wed, 07 Apr 2021 19:57:09 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:a3e77b260e2e58e360cfe583723d95631f1a6f5c7678e7a99066cb5b652d863d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:b939bd4423517dcdf246fbc18c634c0c53d79cf55005cf1b476cffbb5e26eda2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532290044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf28d77e48186471ce641be1f7223efd9eaaacf74fa9edd4002de7791efd929`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:28:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:28:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:32:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:32:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:32:17 GMT
RUN npm install -g rtlcss
# Wed, 31 Mar 2021 05:32:18 GMT
ENV ODOO_VERSION=13.0
# Wed, 07 Apr 2021 19:52:50 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:52:50 GMT
ARG ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
# Wed, 07 Apr 2021 19:53:59 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:54:02 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:54:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:54:03 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:54:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:54:04 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:54:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:54:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:54:04 GMT
USER odoo
# Wed, 07 Apr 2021 19:54:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:54:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de28911af5f8767fc6fe7abf921e6faf5736251f49ad228e8cea796a6ff5981d`  
		Last Modified: Wed, 31 Mar 2021 05:38:39 GMT  
		Size: 207.1 MB (207123802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8b6f4271c30f6e5b71d1885f6089af04ebaa2754576ad658a29f17f6098a13`  
		Last Modified: Wed, 31 Mar 2021 05:38:10 GMT  
		Size: 2.3 MB (2345373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e216845aa303c372f43ecd3c7255099d37f5acb661344b8b0a764dca4dc5eb67`  
		Last Modified: Wed, 31 Mar 2021 05:38:09 GMT  
		Size: 894.0 KB (894002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9f5f5bcf8b22ae97e34137f8ec58ecafcea036c2d0897e98daae4eaf84bd4d`  
		Last Modified: Wed, 07 Apr 2021 19:56:57 GMT  
		Size: 294.8 MB (294785145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95df7b3d6a190cc803681e8d8f1eb11a6fb775a23f10c09c17ba82c5ccd665c1`  
		Last Modified: Wed, 07 Apr 2021 19:56:32 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c191ad66867c26c3096e01404e75b0bbafefa4db7fdfd5d2e5af5be12a44fd`  
		Last Modified: Wed, 07 Apr 2021 19:56:25 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbfc9a2c3f9370f45585de7b9743bd92b8f0214f70ae8eccb18adcf0fa44632`  
		Last Modified: Wed, 07 Apr 2021 19:56:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba67a0e7c6bbdcd3c789e5e93f0a4a43fc1555db7c6514ae27777548984c7d8`  
		Last Modified: Wed, 07 Apr 2021 19:56:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:a3e77b260e2e58e360cfe583723d95631f1a6f5c7678e7a99066cb5b652d863d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:b939bd4423517dcdf246fbc18c634c0c53d79cf55005cf1b476cffbb5e26eda2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.3 MB (532290044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf28d77e48186471ce641be1f7223efd9eaaacf74fa9edd4002de7791efd929`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:28:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:28:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:32:06 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:32:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:32:17 GMT
RUN npm install -g rtlcss
# Wed, 31 Mar 2021 05:32:18 GMT
ENV ODOO_VERSION=13.0
# Wed, 07 Apr 2021 19:52:50 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:52:50 GMT
ARG ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
# Wed, 07 Apr 2021 19:53:59 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:54:02 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:54:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:54:03 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=ca37f801e71721044351a6457dcdc4091a138771
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:54:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:54:04 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:54:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:54:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:54:04 GMT
USER odoo
# Wed, 07 Apr 2021 19:54:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:54:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de28911af5f8767fc6fe7abf921e6faf5736251f49ad228e8cea796a6ff5981d`  
		Last Modified: Wed, 31 Mar 2021 05:38:39 GMT  
		Size: 207.1 MB (207123802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8b6f4271c30f6e5b71d1885f6089af04ebaa2754576ad658a29f17f6098a13`  
		Last Modified: Wed, 31 Mar 2021 05:38:10 GMT  
		Size: 2.3 MB (2345373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e216845aa303c372f43ecd3c7255099d37f5acb661344b8b0a764dca4dc5eb67`  
		Last Modified: Wed, 31 Mar 2021 05:38:09 GMT  
		Size: 894.0 KB (894002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9f5f5bcf8b22ae97e34137f8ec58ecafcea036c2d0897e98daae4eaf84bd4d`  
		Last Modified: Wed, 07 Apr 2021 19:56:57 GMT  
		Size: 294.8 MB (294785145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95df7b3d6a190cc803681e8d8f1eb11a6fb775a23f10c09c17ba82c5ccd665c1`  
		Last Modified: Wed, 07 Apr 2021 19:56:32 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c191ad66867c26c3096e01404e75b0bbafefa4db7fdfd5d2e5af5be12a44fd`  
		Last Modified: Wed, 07 Apr 2021 19:56:25 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbfc9a2c3f9370f45585de7b9743bd92b8f0214f70ae8eccb18adcf0fa44632`  
		Last Modified: Wed, 07 Apr 2021 19:56:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba67a0e7c6bbdcd3c789e5e93f0a4a43fc1555db7c6514ae27777548984c7d8`  
		Last Modified: Wed, 07 Apr 2021 19:56:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:34806a615878d4045a383b57b8439391aacc361fb30763a9ba51cfbab0f6786a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:8a50954ba7f2324ad43e06afa236cda1b002b8278cb48a89d2392a5e2b7c4b87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515859704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45bcdd074f917c2fd0bde9713d55f462ee042009139d35c23bb5636298b8a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:28:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:28:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:29:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:29:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:29:47 GMT
RUN npm install -g rtlcss
# Wed, 31 Mar 2021 05:29:48 GMT
ENV ODOO_VERSION=14.0
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Wed, 07 Apr 2021 19:52:31 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:52:36 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:52:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:52:36 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:52:37 GMT
USER odoo
# Wed, 07 Apr 2021 19:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:52:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891b8c13a6557e87341fe3dae2cacc445b84d3061c83b252ca743c338d64cc83`  
		Last Modified: Wed, 31 Mar 2021 05:37:46 GMT  
		Size: 213.2 MB (213169537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acf2c1161bac7f6d917df1dab741f4f98b3d7d9bb4994d7fd1913385578875e`  
		Last Modified: Wed, 31 Mar 2021 05:37:18 GMT  
		Size: 2.3 MB (2348508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b52e489bcfae111683bd0dc94749af43d9ea55931a3c2a703c8c3ff3dfb6e`  
		Last Modified: Wed, 31 Mar 2021 05:37:16 GMT  
		Size: 894.0 KB (894018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b049e678c814ae5246118f37ec0988cc42cc96690bccdd6ea9f6cad2f57114c8`  
		Last Modified: Wed, 07 Apr 2021 19:56:11 GMT  
		Size: 272.3 MB (272305917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c78a5820c7d656599da2fef55bc7b006e517667cb059ed9544982532ec17da0`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d50c2bb3dcbef24818b454814d99221d5557698825f25243bbc6e1edb85e3`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd632fea738b974175a0a0ad439008139fb06611cdb6a351adcf67343b7476`  
		Last Modified: Wed, 07 Apr 2021 19:55:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac361ec738ee19861cf5e8d975c4b68c1efd40d281adbc234de94e94e6b5060`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:34806a615878d4045a383b57b8439391aacc361fb30763a9ba51cfbab0f6786a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:8a50954ba7f2324ad43e06afa236cda1b002b8278cb48a89d2392a5e2b7c4b87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515859704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45bcdd074f917c2fd0bde9713d55f462ee042009139d35c23bb5636298b8a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:28:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:28:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:29:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:29:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:29:47 GMT
RUN npm install -g rtlcss
# Wed, 31 Mar 2021 05:29:48 GMT
ENV ODOO_VERSION=14.0
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Wed, 07 Apr 2021 19:52:31 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:52:36 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:52:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:52:36 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:52:37 GMT
USER odoo
# Wed, 07 Apr 2021 19:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:52:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891b8c13a6557e87341fe3dae2cacc445b84d3061c83b252ca743c338d64cc83`  
		Last Modified: Wed, 31 Mar 2021 05:37:46 GMT  
		Size: 213.2 MB (213169537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acf2c1161bac7f6d917df1dab741f4f98b3d7d9bb4994d7fd1913385578875e`  
		Last Modified: Wed, 31 Mar 2021 05:37:18 GMT  
		Size: 2.3 MB (2348508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b52e489bcfae111683bd0dc94749af43d9ea55931a3c2a703c8c3ff3dfb6e`  
		Last Modified: Wed, 31 Mar 2021 05:37:16 GMT  
		Size: 894.0 KB (894018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b049e678c814ae5246118f37ec0988cc42cc96690bccdd6ea9f6cad2f57114c8`  
		Last Modified: Wed, 07 Apr 2021 19:56:11 GMT  
		Size: 272.3 MB (272305917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c78a5820c7d656599da2fef55bc7b006e517667cb059ed9544982532ec17da0`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d50c2bb3dcbef24818b454814d99221d5557698825f25243bbc6e1edb85e3`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd632fea738b974175a0a0ad439008139fb06611cdb6a351adcf67343b7476`  
		Last Modified: Wed, 07 Apr 2021 19:55:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac361ec738ee19861cf5e8d975c4b68c1efd40d281adbc234de94e94e6b5060`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:34806a615878d4045a383b57b8439391aacc361fb30763a9ba51cfbab0f6786a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8a50954ba7f2324ad43e06afa236cda1b002b8278cb48a89d2392a5e2b7c4b87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515859704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45bcdd074f917c2fd0bde9713d55f462ee042009139d35c23bb5636298b8a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:28:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:28:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:29:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:29:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:29:47 GMT
RUN npm install -g rtlcss
# Wed, 31 Mar 2021 05:29:48 GMT
ENV ODOO_VERSION=14.0
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Wed, 07 Apr 2021 19:52:31 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:52:36 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:52:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:52:36 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:52:37 GMT
USER odoo
# Wed, 07 Apr 2021 19:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:52:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891b8c13a6557e87341fe3dae2cacc445b84d3061c83b252ca743c338d64cc83`  
		Last Modified: Wed, 31 Mar 2021 05:37:46 GMT  
		Size: 213.2 MB (213169537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acf2c1161bac7f6d917df1dab741f4f98b3d7d9bb4994d7fd1913385578875e`  
		Last Modified: Wed, 31 Mar 2021 05:37:18 GMT  
		Size: 2.3 MB (2348508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b52e489bcfae111683bd0dc94749af43d9ea55931a3c2a703c8c3ff3dfb6e`  
		Last Modified: Wed, 31 Mar 2021 05:37:16 GMT  
		Size: 894.0 KB (894018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b049e678c814ae5246118f37ec0988cc42cc96690bccdd6ea9f6cad2f57114c8`  
		Last Modified: Wed, 07 Apr 2021 19:56:11 GMT  
		Size: 272.3 MB (272305917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c78a5820c7d656599da2fef55bc7b006e517667cb059ed9544982532ec17da0`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d50c2bb3dcbef24818b454814d99221d5557698825f25243bbc6e1edb85e3`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd632fea738b974175a0a0ad439008139fb06611cdb6a351adcf67343b7476`  
		Last Modified: Wed, 07 Apr 2021 19:55:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac361ec738ee19861cf5e8d975c4b68c1efd40d281adbc234de94e94e6b5060`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
