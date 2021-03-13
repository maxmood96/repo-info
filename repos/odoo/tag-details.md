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
$ docker pull odoo@sha256:8688096843498dfee3de7de10330d1d524e5eb5aeb842388066aed1bbf6538f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:3d3352f1d53fbcd836fa16f716a3ba0943921e280a0239954b001dca419a9021
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542523745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab63158b01ceb4d60ed0596d5a03a29898ecc9c8f8ef655ff98ccaaaf4a1b670`
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
# Fri, 12 Mar 2021 21:59:38 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:59:38 GMT
ARG ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
# Fri, 12 Mar 2021 22:01:11 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 22:01:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 22:01:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 22:01:17 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 22:01:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 22:01:18 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 22:01:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 22:01:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 22:01:20 GMT
USER odoo
# Fri, 12 Mar 2021 22:01:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:01:20 GMT
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
	-	`sha256:9e8c2779ed77168dbe221b18af423cef815dcb36139047bf03f0f5e25cc95b61`  
		Last Modified: Fri, 12 Mar 2021 22:05:01 GMT  
		Size: 276.1 MB (276089400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da68a6a7d652d13a384c526496b7947a912136e1f0a03e1c51883d0bc7c56cc`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2272d7ce67052d1035427fe359d06bdcb4da808f52067d1699ed03e5b53158e`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312d3403265c4f4b6523e7fbcb44ea5782a88a90142f36cbbf4cce83f5383965`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034eb8f9c08685ffedc8bc93d1084a27fccef8cd8d31c0bdd31d5f8ec070dca`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:8688096843498dfee3de7de10330d1d524e5eb5aeb842388066aed1bbf6538f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:3d3352f1d53fbcd836fa16f716a3ba0943921e280a0239954b001dca419a9021
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.5 MB (542523745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab63158b01ceb4d60ed0596d5a03a29898ecc9c8f8ef655ff98ccaaaf4a1b670`
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
# Fri, 12 Mar 2021 21:59:38 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:59:38 GMT
ARG ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
# Fri, 12 Mar 2021 22:01:11 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 22:01:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 22:01:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 22:01:17 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=e77a7a50c71c71722e6a012da2d7aa8b41dee3f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 22:01:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 22:01:18 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 22:01:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 22:01:19 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 22:01:20 GMT
USER odoo
# Fri, 12 Mar 2021 22:01:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 22:01:20 GMT
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
	-	`sha256:9e8c2779ed77168dbe221b18af423cef815dcb36139047bf03f0f5e25cc95b61`  
		Last Modified: Fri, 12 Mar 2021 22:05:01 GMT  
		Size: 276.1 MB (276089400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da68a6a7d652d13a384c526496b7947a912136e1f0a03e1c51883d0bc7c56cc`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2272d7ce67052d1035427fe359d06bdcb4da808f52067d1699ed03e5b53158e`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312d3403265c4f4b6523e7fbcb44ea5782a88a90142f36cbbf4cce83f5383965`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b034eb8f9c08685ffedc8bc93d1084a27fccef8cd8d31c0bdd31d5f8ec070dca`  
		Last Modified: Fri, 12 Mar 2021 22:03:58 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:0d04ceb872ac42eb64aff8f6cbf8acb1a8aa77003e85ad64f1a85cedbae97151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:564fd8f3c20350b3df488f0689d7e20d2e5646afcd368c4acbbda62f9c33b6f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532164599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53276582fdc145eda33435d4b26a4729bd3396b2844309fd2577e503a1dead83`
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
# Fri, 12 Mar 2021 21:55:00 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:55:01 GMT
ARG ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
# Fri, 12 Mar 2021 21:56:44 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 21:56:48 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 21:56:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 21:56:50 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 21:56:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 21:56:50 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 21:56:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 21:56:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 21:56:51 GMT
USER odoo
# Fri, 12 Mar 2021 21:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 21:56:51 GMT
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
	-	`sha256:89b4546f1f9953f5d33eda92a05179d0dc4f1a1c0178be0a6547716daed032d4`  
		Last Modified: Fri, 12 Mar 2021 22:03:40 GMT  
		Size: 294.7 MB (294687940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638ececa887ddd2fcc182238d722a7b69ea46b7314a2a067e7d669aedf7b075e`  
		Last Modified: Fri, 12 Mar 2021 22:02:43 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94938fa2f68303f98ce468a8beb90c57260400209c356c54bc9985f446040366`  
		Last Modified: Fri, 12 Mar 2021 22:02:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0424d50f712a1ece6258f30897c6e5245fa80d37bbc2305d8b4b2dd37e654f78`  
		Last Modified: Fri, 12 Mar 2021 22:02:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d528e503d5437abb534e0ace723b8c5d3b2c08e103d4c1bf89cabbe842e3bd0a`  
		Last Modified: Fri, 12 Mar 2021 22:02:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:0d04ceb872ac42eb64aff8f6cbf8acb1a8aa77003e85ad64f1a85cedbae97151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:564fd8f3c20350b3df488f0689d7e20d2e5646afcd368c4acbbda62f9c33b6f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532164599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53276582fdc145eda33435d4b26a4729bd3396b2844309fd2577e503a1dead83`
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
# Fri, 12 Mar 2021 21:55:00 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:55:01 GMT
ARG ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
# Fri, 12 Mar 2021 21:56:44 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 21:56:48 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 21:56:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 21:56:50 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=68400af8c3710a16fd94e6c64f99c532abb575ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 21:56:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 21:56:50 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 21:56:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 21:56:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 21:56:51 GMT
USER odoo
# Fri, 12 Mar 2021 21:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 21:56:51 GMT
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
	-	`sha256:89b4546f1f9953f5d33eda92a05179d0dc4f1a1c0178be0a6547716daed032d4`  
		Last Modified: Fri, 12 Mar 2021 22:03:40 GMT  
		Size: 294.7 MB (294687940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638ececa887ddd2fcc182238d722a7b69ea46b7314a2a067e7d669aedf7b075e`  
		Last Modified: Fri, 12 Mar 2021 22:02:43 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94938fa2f68303f98ce468a8beb90c57260400209c356c54bc9985f446040366`  
		Last Modified: Fri, 12 Mar 2021 22:02:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0424d50f712a1ece6258f30897c6e5245fa80d37bbc2305d8b4b2dd37e654f78`  
		Last Modified: Fri, 12 Mar 2021 22:02:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d528e503d5437abb534e0ace723b8c5d3b2c08e103d4c1bf89cabbe842e3bd0a`  
		Last Modified: Fri, 12 Mar 2021 22:02:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:d42577ec9a6edeac4522937e6036d109906d40530d08a984115f459ec6db9560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:c199660782ac73af05dd46132d4f229d62efee87bccc42097045227fb3c68c7a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515260456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9759efaf228eccae204c00c4d7d974b743b1d8eef461fbfd20fc2ae711a016`
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
# Fri, 12 Mar 2021 21:51:43 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:51:43 GMT
ARG ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
# Fri, 12 Mar 2021 21:53:02 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 21:53:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 21:53:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 21:53:05 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 21:53:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 21:53:05 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 21:53:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 21:53:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 21:53:06 GMT
USER odoo
# Fri, 12 Mar 2021 21:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 21:53:07 GMT
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
	-	`sha256:7d0a372afee959b90317f501236239a3b34403ebe571e3d73bcd2139bb2ddfb8`  
		Last Modified: Fri, 12 Mar 2021 22:02:29 GMT  
		Size: 271.7 MB (271742056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81102107ecd346c1ec31d927697b22100d167ed5244060ee64637bf575814e8c`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369b7fcfb5a7fbdaa4c84e3eb67701447879356452ba236ec6799dd8500e6fd0`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2917e2c668b5d2bc85bb9e0b8afc4f948564aa9e07ae184e1bf7a3c4335a38`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753e72f8134c2036cf4d6f4ae32ae5308f39808bd7b3f1a8959e36cfc57b29e2`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:d42577ec9a6edeac4522937e6036d109906d40530d08a984115f459ec6db9560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:c199660782ac73af05dd46132d4f229d62efee87bccc42097045227fb3c68c7a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515260456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9759efaf228eccae204c00c4d7d974b743b1d8eef461fbfd20fc2ae711a016`
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
# Fri, 12 Mar 2021 21:51:43 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:51:43 GMT
ARG ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
# Fri, 12 Mar 2021 21:53:02 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 21:53:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 21:53:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 21:53:05 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 21:53:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 21:53:05 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 21:53:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 21:53:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 21:53:06 GMT
USER odoo
# Fri, 12 Mar 2021 21:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 21:53:07 GMT
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
	-	`sha256:7d0a372afee959b90317f501236239a3b34403ebe571e3d73bcd2139bb2ddfb8`  
		Last Modified: Fri, 12 Mar 2021 22:02:29 GMT  
		Size: 271.7 MB (271742056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81102107ecd346c1ec31d927697b22100d167ed5244060ee64637bf575814e8c`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369b7fcfb5a7fbdaa4c84e3eb67701447879356452ba236ec6799dd8500e6fd0`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2917e2c668b5d2bc85bb9e0b8afc4f948564aa9e07ae184e1bf7a3c4335a38`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753e72f8134c2036cf4d6f4ae32ae5308f39808bd7b3f1a8959e36cfc57b29e2`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:d42577ec9a6edeac4522937e6036d109906d40530d08a984115f459ec6db9560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:c199660782ac73af05dd46132d4f229d62efee87bccc42097045227fb3c68c7a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515260456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9759efaf228eccae204c00c4d7d974b743b1d8eef461fbfd20fc2ae711a016`
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
# Fri, 12 Mar 2021 21:51:43 GMT
ARG ODOO_RELEASE=20210308
# Fri, 12 Mar 2021 21:51:43 GMT
ARG ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
# Fri, 12 Mar 2021 21:53:02 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 12 Mar 2021 21:53:04 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 12 Mar 2021 21:53:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 12 Mar 2021 21:53:05 GMT
# ARGS: ODOO_RELEASE=20210308 ODOO_SHA=4daeebd19613ae7d0cf53f23c2f47a2b39b29163
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 12 Mar 2021 21:53:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 12 Mar 2021 21:53:05 GMT
EXPOSE 8069 8071 8072
# Fri, 12 Mar 2021 21:53:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 12 Mar 2021 21:53:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 12 Mar 2021 21:53:06 GMT
USER odoo
# Fri, 12 Mar 2021 21:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 21:53:07 GMT
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
	-	`sha256:7d0a372afee959b90317f501236239a3b34403ebe571e3d73bcd2139bb2ddfb8`  
		Last Modified: Fri, 12 Mar 2021 22:02:29 GMT  
		Size: 271.7 MB (271742056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81102107ecd346c1ec31d927697b22100d167ed5244060ee64637bf575814e8c`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369b7fcfb5a7fbdaa4c84e3eb67701447879356452ba236ec6799dd8500e6fd0`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2917e2c668b5d2bc85bb9e0b8afc4f948564aa9e07ae184e1bf7a3c4335a38`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753e72f8134c2036cf4d6f4ae32ae5308f39808bd7b3f1a8959e36cfc57b29e2`  
		Last Modified: Fri, 12 Mar 2021 22:01:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
