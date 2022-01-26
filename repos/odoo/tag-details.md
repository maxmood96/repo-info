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
$ docker pull odoo@sha256:4208d49701df44ce8e17457ac79732959e168c926626a1db0c06c670d81ca079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:e5b263ecacb530e298613a20a820d2d3e34b1301e223afda2612fca6fc0c829f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.5 MB (539480984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9759606b9ca7a20f2555f436cbf16d0264d121ce1d0f2d1dd8f27a57028975ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:10:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:11:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:11:19 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:11:19 GMT
ENV ODOO_VERSION=13.0
# Wed, 26 Jan 2022 09:11:20 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:11:20 GMT
ARG ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
# Wed, 26 Jan 2022 09:13:05 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:13:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:13:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:13:11 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:13:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:13:12 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:13:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:13:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:13:13 GMT
USER odoo
# Wed, 26 Jan 2022 09:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:13:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1643683a10820c31ffd26f415c4c5a3d8da779af7f087d7c33939c40597425a`  
		Last Modified: Wed, 26 Jan 2022 09:16:15 GMT  
		Size: 207.1 MB (207131191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec2e1c27f1ac41a1fde98e797a9891f5dc8db95df82fc8e43e3717d5bcb7f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:39 GMT  
		Size: 13.4 MB (13433899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426af2fe5b1c6cfebdb4e8ec73348b9d2c5b12fc783ac4d7daa8e515c42f80f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:35 GMT  
		Size: 447.0 KB (447023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b58d8a7fb6288d202c04001a824ac0ea5e22c5c34b41489b8112f670983e13`  
		Last Modified: Wed, 26 Jan 2022 09:16:24 GMT  
		Size: 291.3 MB (291312670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c705eb7efe45b2228de4bcde24f103f6f113e3d72cc747ebf6832cbf11e857b`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1525ce0b144732b04210c55fcbc7e5c69595c5101eeb002982b0a96de9a79cbf`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95f56acd0818d2c6ca77316402040b4e854dfdfd6b6744b6aa28f621f47ad0c`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2857446879ff2dd330c0fe7ec9dd4b69014978f04b68934ff29f230adc44f`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:4208d49701df44ce8e17457ac79732959e168c926626a1db0c06c670d81ca079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:e5b263ecacb530e298613a20a820d2d3e34b1301e223afda2612fca6fc0c829f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.5 MB (539480984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9759606b9ca7a20f2555f436cbf16d0264d121ce1d0f2d1dd8f27a57028975ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:10:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:11:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:11:19 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:11:19 GMT
ENV ODOO_VERSION=13.0
# Wed, 26 Jan 2022 09:11:20 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:11:20 GMT
ARG ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
# Wed, 26 Jan 2022 09:13:05 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:13:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:13:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:13:11 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=d7b3daafb97d47551e0754a874e3c39adbb39ae3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:13:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:13:12 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:13:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:13:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:13:13 GMT
USER odoo
# Wed, 26 Jan 2022 09:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:13:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1643683a10820c31ffd26f415c4c5a3d8da779af7f087d7c33939c40597425a`  
		Last Modified: Wed, 26 Jan 2022 09:16:15 GMT  
		Size: 207.1 MB (207131191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec2e1c27f1ac41a1fde98e797a9891f5dc8db95df82fc8e43e3717d5bcb7f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:39 GMT  
		Size: 13.4 MB (13433899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426af2fe5b1c6cfebdb4e8ec73348b9d2c5b12fc783ac4d7daa8e515c42f80f8`  
		Last Modified: Wed, 26 Jan 2022 09:15:35 GMT  
		Size: 447.0 KB (447023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b58d8a7fb6288d202c04001a824ac0ea5e22c5c34b41489b8112f670983e13`  
		Last Modified: Wed, 26 Jan 2022 09:16:24 GMT  
		Size: 291.3 MB (291312670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c705eb7efe45b2228de4bcde24f103f6f113e3d72cc747ebf6832cbf11e857b`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1525ce0b144732b04210c55fcbc7e5c69595c5101eeb002982b0a96de9a79cbf`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95f56acd0818d2c6ca77316402040b4e854dfdfd6b6744b6aa28f621f47ad0c`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa2857446879ff2dd330c0fe7ec9dd4b69014978f04b68934ff29f230adc44f`  
		Last Modified: Wed, 26 Jan 2022 09:15:32 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:9226339adda708307f4d7c3de05174353745cb8594df2b614c372ecfc736cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:c40fe83bcf0f1b442d646af373efa85a3c4ac6410bf0a6c81a6c1f74439ed735
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529245563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317b1c1d2cf9e1e5335a29086a560a691dbbd61d41a47feacdf1eeba78ff54df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:07:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:07:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:07:52 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:07:52 GMT
ENV ODOO_VERSION=14.0
# Wed, 26 Jan 2022 09:07:52 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:07:52 GMT
ARG ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
# Wed, 26 Jan 2022 09:09:17 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:09:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:09:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:09:22 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:09:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:09:23 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:09:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:09:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:09:24 GMT
USER odoo
# Wed, 26 Jan 2022 09:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:09:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158787f79b5bbd45592d744836bf9bab3a8f9ffc1fc9d765e0a69828fba80f7a`  
		Last Modified: Wed, 26 Jan 2022 09:15:11 GMT  
		Size: 213.2 MB (213173094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c04dc7402806cf6edd8c86d43be59a3f35cc2abdeb069509b0b8089ff88d8c`  
		Last Modified: Wed, 26 Jan 2022 09:14:42 GMT  
		Size: 13.4 MB (13436578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b98a5866acaabb48e508494ade5b4cd13f3c3225e581cd1ea045e283d0602c`  
		Last Modified: Wed, 26 Jan 2022 09:14:38 GMT  
		Size: 447.0 KB (446976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d982b674a452e4602b09e7ea0d75634b4fc56cba0be8024f8be9f159c8fa59`  
		Last Modified: Wed, 26 Jan 2022 09:15:20 GMT  
		Size: 275.0 MB (275032717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4198c7a2c73edbab9aef11629aa22785238a0988657a024cd3df13f4c148476`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5028528aad796f0b93abf264881b798e1ff5a572196f4d254f4f74a4756108`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5979c44a3bc197224d57e5c201e2cd09897b39005810b2c9870d04912a620a`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd7c72ca13eb2164e83a9b00d1cc3f68d60b03e0cdb73890fe24c8389dbc96c`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:9226339adda708307f4d7c3de05174353745cb8594df2b614c372ecfc736cc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:c40fe83bcf0f1b442d646af373efa85a3c4ac6410bf0a6c81a6c1f74439ed735
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.2 MB (529245563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317b1c1d2cf9e1e5335a29086a560a691dbbd61d41a47feacdf1eeba78ff54df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:06:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:06:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:06:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:07:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:07:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:07:52 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:07:52 GMT
ENV ODOO_VERSION=14.0
# Wed, 26 Jan 2022 09:07:52 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:07:52 GMT
ARG ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
# Wed, 26 Jan 2022 09:09:17 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:09:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:09:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:09:22 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=a32b3d766e45320a0092b40b18728b326da1210c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:09:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:09:23 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:09:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:09:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:09:24 GMT
USER odoo
# Wed, 26 Jan 2022 09:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:09:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158787f79b5bbd45592d744836bf9bab3a8f9ffc1fc9d765e0a69828fba80f7a`  
		Last Modified: Wed, 26 Jan 2022 09:15:11 GMT  
		Size: 213.2 MB (213173094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c04dc7402806cf6edd8c86d43be59a3f35cc2abdeb069509b0b8089ff88d8c`  
		Last Modified: Wed, 26 Jan 2022 09:14:42 GMT  
		Size: 13.4 MB (13436578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b98a5866acaabb48e508494ade5b4cd13f3c3225e581cd1ea045e283d0602c`  
		Last Modified: Wed, 26 Jan 2022 09:14:38 GMT  
		Size: 447.0 KB (446976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d982b674a452e4602b09e7ea0d75634b4fc56cba0be8024f8be9f159c8fa59`  
		Last Modified: Wed, 26 Jan 2022 09:15:20 GMT  
		Size: 275.0 MB (275032717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4198c7a2c73edbab9aef11629aa22785238a0988657a024cd3df13f4c148476`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5028528aad796f0b93abf264881b798e1ff5a572196f4d254f4f74a4756108`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5979c44a3bc197224d57e5c201e2cd09897b39005810b2c9870d04912a620a`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd7c72ca13eb2164e83a9b00d1cc3f68d60b03e0cdb73890fe24c8389dbc96c`  
		Last Modified: Wed, 26 Jan 2022 09:14:35 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:2c147d75bff49e2b37ffa1e76d9b96d1eebabc9a3895aa6f49a15109c20c299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:785ae9a91ca0e74edf4301aad19f56cbc6575c3427530671e7c35c16abf8a3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548496319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e339d3503f7f9e6bba4ff7fabc3fcb03f61105904da0621d7d1cd3d0cfd21d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Wed, 26 Jan 2022 09:06:06 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:06:11 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:06:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:06:11 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:06:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:06:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:06:12 GMT
USER odoo
# Wed, 26 Jan 2022 09:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:06:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c1a1010fb85d107e9d673b43a4971e5c5186a6e588ebcb00f94b9db4fe3113`  
		Last Modified: Wed, 26 Jan 2022 09:14:21 GMT  
		Size: 293.9 MB (293890175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0905f2c0188b03b39a5709fd2e15edc5bb4786fd17a63b8cf11e3135a24c1`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f61379b5aac40a974ec8fa2a20252d2bdc6bb6e26ff6087149f19eaef624d95`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db405fdc75f98113fe1defb775a5904cfa8dab7b21adb00445b2f022605e6177`  
		Last Modified: Wed, 26 Jan 2022 09:13:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbb38d44f0fb37c54da2fbe03d1c7a9c46c395e843cb06f3a6bf7e7c204e13`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:2c147d75bff49e2b37ffa1e76d9b96d1eebabc9a3895aa6f49a15109c20c299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:785ae9a91ca0e74edf4301aad19f56cbc6575c3427530671e7c35c16abf8a3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548496319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e339d3503f7f9e6bba4ff7fabc3fcb03f61105904da0621d7d1cd3d0cfd21d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Wed, 26 Jan 2022 09:06:06 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:06:11 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:06:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:06:11 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:06:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:06:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:06:12 GMT
USER odoo
# Wed, 26 Jan 2022 09:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:06:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c1a1010fb85d107e9d673b43a4971e5c5186a6e588ebcb00f94b9db4fe3113`  
		Last Modified: Wed, 26 Jan 2022 09:14:21 GMT  
		Size: 293.9 MB (293890175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0905f2c0188b03b39a5709fd2e15edc5bb4786fd17a63b8cf11e3135a24c1`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f61379b5aac40a974ec8fa2a20252d2bdc6bb6e26ff6087149f19eaef624d95`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db405fdc75f98113fe1defb775a5904cfa8dab7b21adb00445b2f022605e6177`  
		Last Modified: Wed, 26 Jan 2022 09:13:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbb38d44f0fb37c54da2fbe03d1c7a9c46c395e843cb06f3a6bf7e7c204e13`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:2c147d75bff49e2b37ffa1e76d9b96d1eebabc9a3895aa6f49a15109c20c299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:785ae9a91ca0e74edf4301aad19f56cbc6575c3427530671e7c35c16abf8a3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548496319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e339d3503f7f9e6bba4ff7fabc3fcb03f61105904da0621d7d1cd3d0cfd21d80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Wed, 26 Jan 2022 09:06:06 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:06:11 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:06:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:06:11 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:06:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:06:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:06:12 GMT
USER odoo
# Wed, 26 Jan 2022 09:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:06:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c1a1010fb85d107e9d673b43a4971e5c5186a6e588ebcb00f94b9db4fe3113`  
		Last Modified: Wed, 26 Jan 2022 09:14:21 GMT  
		Size: 293.9 MB (293890175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0905f2c0188b03b39a5709fd2e15edc5bb4786fd17a63b8cf11e3135a24c1`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f61379b5aac40a974ec8fa2a20252d2bdc6bb6e26ff6087149f19eaef624d95`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db405fdc75f98113fe1defb775a5904cfa8dab7b21adb00445b2f022605e6177`  
		Last Modified: Wed, 26 Jan 2022 09:13:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbb38d44f0fb37c54da2fbe03d1c7a9c46c395e843cb06f3a6bf7e7c204e13`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
