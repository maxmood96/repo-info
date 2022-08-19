<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:latest`](#odoolatest)

## `odoo:13`

```console
$ docker pull odoo@sha256:f1a103aec7ff235cc139c566cb4a32f7478eaa5ec1bb0de6abff555051c1497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:925dd30a0003a51430da665b77c74809dbdf6047bf3bd4e67384c09fb6f70bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.4 MB (540386131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee369259ea98cc83b793c5bc2482bba47ff7bfff52e0bf5c724037173379414f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:42:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:42:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:42:50 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:42:50 GMT
ENV ODOO_VERSION=13.0
# Fri, 19 Aug 2022 19:03:06 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:03:06 GMT
ARG ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
# Fri, 19 Aug 2022 19:05:29 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:05:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:05:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:05:33 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:05:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:05:34 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:05:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:05:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:05:34 GMT
USER odoo
# Fri, 19 Aug 2022 19:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:05:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718371f43c618dd7c037dc9e6f276d3bdfb4242e47d30ede3d8e797f7e6f78a`  
		Last Modified: Tue, 02 Aug 2022 05:46:33 GMT  
		Size: 207.1 MB (207143577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b563a78258fd2c7c9ee449d16fdd0f86d7c54d1784ca7c103dd02900afc29168`  
		Last Modified: Tue, 02 Aug 2022 05:46:13 GMT  
		Size: 13.4 MB (13442945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350b162f7b9f79c7d63f4e71229b205d9070f98f801cf71ad2b9211e8ede686`  
		Last Modified: Tue, 02 Aug 2022 05:46:09 GMT  
		Size: 508.4 KB (508417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bff45994c85695095b065401cd6c1ed05643c5d9faf3a23ada691636c5432d`  
		Last Modified: Fri, 19 Aug 2022 19:07:57 GMT  
		Size: 292.1 MB (292148645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4173fe648ef49698efaf2da2ff7341776fe6c49ecffb1220060357766c732a9`  
		Last Modified: Fri, 19 Aug 2022 19:07:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd2b21b31ef35a4219f71c0446a9a3b12422a672a077fbb4930fa5a59daa073`  
		Last Modified: Fri, 19 Aug 2022 19:07:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74ba874f31801357069a481272c16bca98b939473b4edab15d0b9dcdc79be7b`  
		Last Modified: Fri, 19 Aug 2022 19:07:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42de1e9f4bbea59e4c4338a098092c92ebd1c1ebdea1a99113bf005df6c4ec88`  
		Last Modified: Fri, 19 Aug 2022 19:07:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:f1a103aec7ff235cc139c566cb4a32f7478eaa5ec1bb0de6abff555051c1497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:925dd30a0003a51430da665b77c74809dbdf6047bf3bd4e67384c09fb6f70bd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.4 MB (540386131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee369259ea98cc83b793c5bc2482bba47ff7bfff52e0bf5c724037173379414f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:42:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:42:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:42:50 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:42:50 GMT
ENV ODOO_VERSION=13.0
# Fri, 19 Aug 2022 19:03:06 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:03:06 GMT
ARG ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
# Fri, 19 Aug 2022 19:05:29 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:05:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:05:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:05:33 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=b4a67f4641a4f054287f8a38dd065b39a04a55db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:05:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:05:34 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:05:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:05:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:05:34 GMT
USER odoo
# Fri, 19 Aug 2022 19:05:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:05:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718371f43c618dd7c037dc9e6f276d3bdfb4242e47d30ede3d8e797f7e6f78a`  
		Last Modified: Tue, 02 Aug 2022 05:46:33 GMT  
		Size: 207.1 MB (207143577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b563a78258fd2c7c9ee449d16fdd0f86d7c54d1784ca7c103dd02900afc29168`  
		Last Modified: Tue, 02 Aug 2022 05:46:13 GMT  
		Size: 13.4 MB (13442945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350b162f7b9f79c7d63f4e71229b205d9070f98f801cf71ad2b9211e8ede686`  
		Last Modified: Tue, 02 Aug 2022 05:46:09 GMT  
		Size: 508.4 KB (508417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bff45994c85695095b065401cd6c1ed05643c5d9faf3a23ada691636c5432d`  
		Last Modified: Fri, 19 Aug 2022 19:07:57 GMT  
		Size: 292.1 MB (292148645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4173fe648ef49698efaf2da2ff7341776fe6c49ecffb1220060357766c732a9`  
		Last Modified: Fri, 19 Aug 2022 19:07:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd2b21b31ef35a4219f71c0446a9a3b12422a672a077fbb4930fa5a59daa073`  
		Last Modified: Fri, 19 Aug 2022 19:07:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74ba874f31801357069a481272c16bca98b939473b4edab15d0b9dcdc79be7b`  
		Last Modified: Fri, 19 Aug 2022 19:07:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42de1e9f4bbea59e4c4338a098092c92ebd1c1ebdea1a99113bf005df6c4ec88`  
		Last Modified: Fri, 19 Aug 2022 19:07:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:d2fa2c9bbb2028fe87bc7692ac970edb3ff9583a8c7c9535c2a66d31b26a2fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:f46b75fc409d2368ed2a87f6b37217ca1a7355bb3e3cda99d906b8c6cfc807d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530862801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20b422a0cbe7290deb5532d0083c076015deff82d6ab0513d34d4fa719efea3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:40:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:40:09 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:40:09 GMT
ENV ODOO_VERSION=14.0
# Fri, 19 Aug 2022 19:01:43 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:01:43 GMT
ARG ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
# Fri, 19 Aug 2022 19:02:56 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:02:59 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:03:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:03:00 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:03:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:03:00 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:03:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:03:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:03:01 GMT
USER odoo
# Fri, 19 Aug 2022 19:03:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:03:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2a9029ee3604b9372e42d87384e5e066e9148be333e0dc03e9c8f855e427b`  
		Last Modified: Tue, 02 Aug 2022 05:45:48 GMT  
		Size: 213.2 MB (213182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d65776201572904d097cfdcb3376d445b11bfc305826f497d3cafee088aeb73`  
		Last Modified: Tue, 02 Aug 2022 05:45:26 GMT  
		Size: 13.4 MB (13444602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470b77fa97db81c4c7ed1ba15b82f7fd432abb5d20e2953a06898a889d44ca6b`  
		Last Modified: Tue, 02 Aug 2022 05:45:23 GMT  
		Size: 508.2 KB (508239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9390f9db7fbe40b90df23a73d351d996a91f22e9c229ede4a09e9cb8f821610`  
		Last Modified: Fri, 19 Aug 2022 19:07:15 GMT  
		Size: 276.6 MB (276584957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677e33c3f716140660eb3c57bc83f4a3061e9620e7baed8ed619ca2d3462cc39`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7135c02fb391394d4bd4ee47809c7c88abb0875fa2920b64dc839aa97bab99`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049a9dcf3fe98d528b37ae011a9fe848255c38e17ee637f05b3dd56d05083eeb`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e353728a1000dfa01bd2abaf53b10a3779960a147fec634a9db3139a8ab42d`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:d2fa2c9bbb2028fe87bc7692ac970edb3ff9583a8c7c9535c2a66d31b26a2fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:f46b75fc409d2368ed2a87f6b37217ca1a7355bb3e3cda99d906b8c6cfc807d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530862801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20b422a0cbe7290deb5532d0083c076015deff82d6ab0513d34d4fa719efea3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:38:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:38:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:38:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:40:06 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:40:09 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:40:09 GMT
ENV ODOO_VERSION=14.0
# Fri, 19 Aug 2022 19:01:43 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:01:43 GMT
ARG ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
# Fri, 19 Aug 2022 19:02:56 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:02:59 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:03:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:03:00 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=019da831e2e16ca10c0486cf30ce7d980ea1db21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:03:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:03:00 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:03:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:03:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:03:01 GMT
USER odoo
# Fri, 19 Aug 2022 19:03:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:03:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d2a9029ee3604b9372e42d87384e5e066e9148be333e0dc03e9c8f855e427b`  
		Last Modified: Tue, 02 Aug 2022 05:45:48 GMT  
		Size: 213.2 MB (213182454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d65776201572904d097cfdcb3376d445b11bfc305826f497d3cafee088aeb73`  
		Last Modified: Tue, 02 Aug 2022 05:45:26 GMT  
		Size: 13.4 MB (13444602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470b77fa97db81c4c7ed1ba15b82f7fd432abb5d20e2953a06898a889d44ca6b`  
		Last Modified: Tue, 02 Aug 2022 05:45:23 GMT  
		Size: 508.2 KB (508239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9390f9db7fbe40b90df23a73d351d996a91f22e9c229ede4a09e9cb8f821610`  
		Last Modified: Fri, 19 Aug 2022 19:07:15 GMT  
		Size: 276.6 MB (276584957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677e33c3f716140660eb3c57bc83f4a3061e9620e7baed8ed619ca2d3462cc39`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7135c02fb391394d4bd4ee47809c7c88abb0875fa2920b64dc839aa97bab99`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049a9dcf3fe98d528b37ae011a9fe848255c38e17ee637f05b3dd56d05083eeb`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e353728a1000dfa01bd2abaf53b10a3779960a147fec634a9db3139a8ab42d`  
		Last Modified: Fri, 19 Aug 2022 19:06:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:25ab541d5e1b259fa51050aade72a06d1416aa691e7da2a0ba4e4922e417d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:b02208fb61c711c04a9a82b00579514464ac276f6b319d662d9d4f3c04f94517
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557787954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b4246285edc40a77a637d4cee285d936845472b9cb87228429f526673ba81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:36:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:36:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:36:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:37:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:37:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:37:21 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:37:21 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Aug 2022 19:00:05 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:00:05 GMT
ARG ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
# Fri, 19 Aug 2022 19:01:22 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:01:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:01:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:01:27 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:01:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:01:28 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:01:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:01:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:01:28 GMT
USER odoo
# Fri, 19 Aug 2022 19:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:01:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04a644bed3d89143e2aa316af36b00716f4554c4f513da256351fe8cce70aa`  
		Last Modified: Tue, 02 Aug 2022 05:45:00 GMT  
		Size: 220.3 MB (220296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4934bbcf7f8f118d6cb4c9dee0e952084f336902f9279646ba728e05729cb`  
		Last Modified: Tue, 02 Aug 2022 05:44:34 GMT  
		Size: 2.5 MB (2513325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77946ee2a1b368dc2efeb7362de7ab48b80331ab4549032ab68486f60bc166ba`  
		Last Modified: Tue, 02 Aug 2022 05:44:33 GMT  
		Size: 502.0 KB (501982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c765d49555b95bdb80113b6f36926c52f8fd66bbb658ac863d8e58bd0e2fd`  
		Last Modified: Fri, 19 Aug 2022 19:06:30 GMT  
		Size: 303.1 MB (303106829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36a2ebbcb4021e26b11a28e2ca3a3df45eddd9e0739db4797235c91a9372e25`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e89b4ab354360d0d2467f839db15f3c512a53dd8f059952447e925beed0913`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641110d5cdfe2edf5aa3b90d7e4bde5da79317aed872b99cef8fb6e69286e4e0`  
		Last Modified: Fri, 19 Aug 2022 19:05:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82b775aaa37fcd8daaf79ba23f5aab6d9e94c8aeac5d10d0fb334391e8b423`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:25ab541d5e1b259fa51050aade72a06d1416aa691e7da2a0ba4e4922e417d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:b02208fb61c711c04a9a82b00579514464ac276f6b319d662d9d4f3c04f94517
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557787954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b4246285edc40a77a637d4cee285d936845472b9cb87228429f526673ba81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:36:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:36:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:36:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:37:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:37:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:37:21 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:37:21 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Aug 2022 19:00:05 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:00:05 GMT
ARG ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
# Fri, 19 Aug 2022 19:01:22 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:01:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:01:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:01:27 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:01:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:01:28 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:01:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:01:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:01:28 GMT
USER odoo
# Fri, 19 Aug 2022 19:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:01:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04a644bed3d89143e2aa316af36b00716f4554c4f513da256351fe8cce70aa`  
		Last Modified: Tue, 02 Aug 2022 05:45:00 GMT  
		Size: 220.3 MB (220296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4934bbcf7f8f118d6cb4c9dee0e952084f336902f9279646ba728e05729cb`  
		Last Modified: Tue, 02 Aug 2022 05:44:34 GMT  
		Size: 2.5 MB (2513325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77946ee2a1b368dc2efeb7362de7ab48b80331ab4549032ab68486f60bc166ba`  
		Last Modified: Tue, 02 Aug 2022 05:44:33 GMT  
		Size: 502.0 KB (501982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c765d49555b95bdb80113b6f36926c52f8fd66bbb658ac863d8e58bd0e2fd`  
		Last Modified: Fri, 19 Aug 2022 19:06:30 GMT  
		Size: 303.1 MB (303106829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36a2ebbcb4021e26b11a28e2ca3a3df45eddd9e0739db4797235c91a9372e25`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e89b4ab354360d0d2467f839db15f3c512a53dd8f059952447e925beed0913`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641110d5cdfe2edf5aa3b90d7e4bde5da79317aed872b99cef8fb6e69286e4e0`  
		Last Modified: Fri, 19 Aug 2022 19:05:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82b775aaa37fcd8daaf79ba23f5aab6d9e94c8aeac5d10d0fb334391e8b423`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:25ab541d5e1b259fa51050aade72a06d1416aa691e7da2a0ba4e4922e417d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b02208fb61c711c04a9a82b00579514464ac276f6b319d662d9d4f3c04f94517
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557787954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b4246285edc40a77a637d4cee285d936845472b9cb87228429f526673ba81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:36:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 02 Aug 2022 05:36:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Aug 2022 05:36:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 05:37:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 02 Aug 2022 05:37:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:37:21 GMT
RUN npm install -g rtlcss
# Tue, 02 Aug 2022 05:37:21 GMT
ENV ODOO_VERSION=15.0
# Fri, 19 Aug 2022 19:00:05 GMT
ARG ODOO_RELEASE=20220819
# Fri, 19 Aug 2022 19:00:05 GMT
ARG ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
# Fri, 19 Aug 2022 19:01:22 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 19 Aug 2022 19:01:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 19 Aug 2022 19:01:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 19 Aug 2022 19:01:27 GMT
# ARGS: ODOO_RELEASE=20220819 ODOO_SHA=c64f22612a08f973ebe27394986dc7b6a39187d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 19 Aug 2022 19:01:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 19 Aug 2022 19:01:28 GMT
EXPOSE 8069 8071 8072
# Fri, 19 Aug 2022 19:01:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 19 Aug 2022 19:01:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 19 Aug 2022 19:01:28 GMT
USER odoo
# Fri, 19 Aug 2022 19:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Aug 2022 19:01:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc04a644bed3d89143e2aa316af36b00716f4554c4f513da256351fe8cce70aa`  
		Last Modified: Tue, 02 Aug 2022 05:45:00 GMT  
		Size: 220.3 MB (220296597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4934bbcf7f8f118d6cb4c9dee0e952084f336902f9279646ba728e05729cb`  
		Last Modified: Tue, 02 Aug 2022 05:44:34 GMT  
		Size: 2.5 MB (2513325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77946ee2a1b368dc2efeb7362de7ab48b80331ab4549032ab68486f60bc166ba`  
		Last Modified: Tue, 02 Aug 2022 05:44:33 GMT  
		Size: 502.0 KB (501982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c765d49555b95bdb80113b6f36926c52f8fd66bbb658ac863d8e58bd0e2fd`  
		Last Modified: Fri, 19 Aug 2022 19:06:30 GMT  
		Size: 303.1 MB (303106829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36a2ebbcb4021e26b11a28e2ca3a3df45eddd9e0739db4797235c91a9372e25`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e89b4ab354360d0d2467f839db15f3c512a53dd8f059952447e925beed0913`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641110d5cdfe2edf5aa3b90d7e4bde5da79317aed872b99cef8fb6e69286e4e0`  
		Last Modified: Fri, 19 Aug 2022 19:05:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82b775aaa37fcd8daaf79ba23f5aab6d9e94c8aeac5d10d0fb334391e8b423`  
		Last Modified: Fri, 19 Aug 2022 19:05:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
