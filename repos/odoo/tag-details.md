<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:11`](#odoo11)
-	[`odoo:11.0`](#odoo110)
-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:latest`](#odoolatest)

## `odoo:11`

```console
$ docker pull odoo@sha256:5753d82138e5ea80a3588dbaf07b35c6a8b35b7ef08164b1413c979071072508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:2a6671e6676f77b00da5cf215f871667ffbdcea76e55c3abb9073e68f0a79a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386137104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a536b0162e4d3a7b0a315a21fcef413f36b0693b8551e8e4e730c0682d65d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:23:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:23:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:23:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:23:03 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Jun 2020 08:25:48 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:26:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:27:33 GMT
ENV ODOO_VERSION=11.0
# Mon, 29 Jun 2020 20:40:08 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:40:08 GMT
ARG ODOO_SHA=3c9c5bb32d7d878b246624a4dfc233080a2b5888
# Mon, 29 Jun 2020 20:41:11 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c9c5bb32d7d878b246624a4dfc233080a2b5888
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:41:13 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Mon, 29 Jun 2020 20:41:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:41:15 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c9c5bb32d7d878b246624a4dfc233080a2b5888
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:41:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:41:16 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:41:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:41:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:41:17 GMT
USER odoo
# Mon, 29 Jun 2020 20:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:41:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b313d67c23e06c34161f486c9e165f6ad0dc22b7473bb0ef523a4095ee563`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bf6c2ae635fbc7fb922ef42b796a0aafa997219b4bc29b3f2eaa05d3bc6d10`  
		Last Modified: Tue, 09 Jun 2020 08:30:23 GMT  
		Size: 219.6 MB (219607175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9ea7cf37cb2fda18a873ac6ecc3f4d67057330d8f827131502240b00ba57c`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 2.3 MB (2336299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0ce998423fc285d7fc84e0130f48ea28cd7a8fccc9a1495ecf419211fc99f`  
		Last Modified: Mon, 29 Jun 2020 20:43:43 GMT  
		Size: 141.7 MB (141671387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6ff1cd8f1a411f09d524892a29f376db0647fc739efc6f8cf59dba80b8ac4`  
		Last Modified: Mon, 29 Jun 2020 20:43:09 GMT  
		Size: 675.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749e62eb39fb09e6eee0bee2f6ec5766e3c394c1871d312bbcbdc3ff1092c7ee`  
		Last Modified: Mon, 29 Jun 2020 20:43:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f45a30187adae1672c09c8854a5d52721f0ebd0b2ccd44474e66b98ac525a`  
		Last Modified: Mon, 29 Jun 2020 20:43:09 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a606bd2bcf268c5650ada8c54aaaae0b2cb00ffe3d00ec8f1195ced4c25da7de`  
		Last Modified: Mon, 29 Jun 2020 20:43:09 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:5753d82138e5ea80a3588dbaf07b35c6a8b35b7ef08164b1413c979071072508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:2a6671e6676f77b00da5cf215f871667ffbdcea76e55c3abb9073e68f0a79a1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386137104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a536b0162e4d3a7b0a315a21fcef413f36b0693b8551e8e4e730c0682d65d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:23:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:23:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:23:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:23:03 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Jun 2020 08:25:48 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:26:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:27:33 GMT
ENV ODOO_VERSION=11.0
# Mon, 29 Jun 2020 20:40:08 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:40:08 GMT
ARG ODOO_SHA=3c9c5bb32d7d878b246624a4dfc233080a2b5888
# Mon, 29 Jun 2020 20:41:11 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c9c5bb32d7d878b246624a4dfc233080a2b5888
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:41:13 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Mon, 29 Jun 2020 20:41:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:41:15 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c9c5bb32d7d878b246624a4dfc233080a2b5888
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:41:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:41:16 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:41:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:41:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:41:17 GMT
USER odoo
# Mon, 29 Jun 2020 20:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:41:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b313d67c23e06c34161f486c9e165f6ad0dc22b7473bb0ef523a4095ee563`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bf6c2ae635fbc7fb922ef42b796a0aafa997219b4bc29b3f2eaa05d3bc6d10`  
		Last Modified: Tue, 09 Jun 2020 08:30:23 GMT  
		Size: 219.6 MB (219607175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9ea7cf37cb2fda18a873ac6ecc3f4d67057330d8f827131502240b00ba57c`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 2.3 MB (2336299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0ce998423fc285d7fc84e0130f48ea28cd7a8fccc9a1495ecf419211fc99f`  
		Last Modified: Mon, 29 Jun 2020 20:43:43 GMT  
		Size: 141.7 MB (141671387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6ff1cd8f1a411f09d524892a29f376db0647fc739efc6f8cf59dba80b8ac4`  
		Last Modified: Mon, 29 Jun 2020 20:43:09 GMT  
		Size: 675.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749e62eb39fb09e6eee0bee2f6ec5766e3c394c1871d312bbcbdc3ff1092c7ee`  
		Last Modified: Mon, 29 Jun 2020 20:43:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92f45a30187adae1672c09c8854a5d52721f0ebd0b2ccd44474e66b98ac525a`  
		Last Modified: Mon, 29 Jun 2020 20:43:09 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a606bd2bcf268c5650ada8c54aaaae0b2cb00ffe3d00ec8f1195ced4c25da7de`  
		Last Modified: Mon, 29 Jun 2020 20:43:09 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:a4ad3582440c114fc8aa5c06bb4c7be9541c00656ed1c8f6ebabd82e7f202178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:4f2cd56b55e3563da358218bcfeb4126236e5b619514082c478a0997c93d8b04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396131288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e62051f72f276708fadd07f911bb3f10773268bcc928d498b44a6d98c307e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:23:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:23:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:23:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:23:03 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Jun 2020 08:25:48 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:26:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:26:24 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:26:25 GMT
ENV ODOO_VERSION=12.0
# Mon, 29 Jun 2020 20:39:03 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:39:03 GMT
ARG ODOO_SHA=3c334ba4178b346839679895468ca786bcce9b5f
# Mon, 29 Jun 2020 20:39:58 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c334ba4178b346839679895468ca786bcce9b5f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:39:59 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 29 Jun 2020 20:39:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:40:00 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c334ba4178b346839679895468ca786bcce9b5f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:40:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:40:00 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:40:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:40:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:40:01 GMT
USER odoo
# Mon, 29 Jun 2020 20:40:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:40:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b313d67c23e06c34161f486c9e165f6ad0dc22b7473bb0ef523a4095ee563`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bf6c2ae635fbc7fb922ef42b796a0aafa997219b4bc29b3f2eaa05d3bc6d10`  
		Last Modified: Tue, 09 Jun 2020 08:30:23 GMT  
		Size: 219.6 MB (219607175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9ea7cf37cb2fda18a873ac6ecc3f4d67057330d8f827131502240b00ba57c`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 2.3 MB (2336299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd6a8877e66a38b39c560f90fb55be4a56f2d801001ccd5d568eb0de17c1fd`  
		Last Modified: Tue, 09 Jun 2020 08:29:33 GMT  
		Size: 22.2 MB (22234975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3904e99a0a9cce5939843118131d02085587220ab1684cf0e836233f20dea0`  
		Last Modified: Mon, 29 Jun 2020 20:43:03 GMT  
		Size: 129.4 MB (129430603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d88e89649801a7043ef1f0aa3037510ef3234e45d516ad0338df2e3fc79dc32`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cefb7b4afeb0a2121948f4f8ea954bd64200c861c240b94ceb6142d5041867a`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3b5ab5b73cfcbad22a2b4fa10e7e364fc1329cd12d79d97d05f8b05af9d98`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45820003105b5014993022c46947855eca3b72d0a0ca81ebd4df2fb0dc0fedfd`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:a4ad3582440c114fc8aa5c06bb4c7be9541c00656ed1c8f6ebabd82e7f202178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:4f2cd56b55e3563da358218bcfeb4126236e5b619514082c478a0997c93d8b04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396131288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e62051f72f276708fadd07f911bb3f10773268bcc928d498b44a6d98c307e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:23:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:23:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:23:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:23:03 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 09 Jun 2020 08:25:48 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:26:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:26:24 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:26:25 GMT
ENV ODOO_VERSION=12.0
# Mon, 29 Jun 2020 20:39:03 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:39:03 GMT
ARG ODOO_SHA=3c334ba4178b346839679895468ca786bcce9b5f
# Mon, 29 Jun 2020 20:39:58 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c334ba4178b346839679895468ca786bcce9b5f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:39:59 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 29 Jun 2020 20:39:59 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:40:00 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=3c334ba4178b346839679895468ca786bcce9b5f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:40:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:40:00 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:40:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:40:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:40:01 GMT
USER odoo
# Mon, 29 Jun 2020 20:40:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:40:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302b313d67c23e06c34161f486c9e165f6ad0dc22b7473bb0ef523a4095ee563`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bf6c2ae635fbc7fb922ef42b796a0aafa997219b4bc29b3f2eaa05d3bc6d10`  
		Last Modified: Tue, 09 Jun 2020 08:30:23 GMT  
		Size: 219.6 MB (219607175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9ea7cf37cb2fda18a873ac6ecc3f4d67057330d8f827131502240b00ba57c`  
		Last Modified: Tue, 09 Jun 2020 08:29:27 GMT  
		Size: 2.3 MB (2336299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd6a8877e66a38b39c560f90fb55be4a56f2d801001ccd5d568eb0de17c1fd`  
		Last Modified: Tue, 09 Jun 2020 08:29:33 GMT  
		Size: 22.2 MB (22234975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3904e99a0a9cce5939843118131d02085587220ab1684cf0e836233f20dea0`  
		Last Modified: Mon, 29 Jun 2020 20:43:03 GMT  
		Size: 129.4 MB (129430603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d88e89649801a7043ef1f0aa3037510ef3234e45d516ad0338df2e3fc79dc32`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cefb7b4afeb0a2121948f4f8ea954bd64200c861c240b94ceb6142d5041867a`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a3b5ab5b73cfcbad22a2b4fa10e7e364fc1329cd12d79d97d05f8b05af9d98`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45820003105b5014993022c46947855eca3b72d0a0ca81ebd4df2fb0dc0fedfd`  
		Last Modified: Mon, 29 Jun 2020 20:42:17 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:562dcfc9ec1299498ccf0fd6aa03be98ec84b83d9705712ec8edadfcaa90d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:9d455e32dad6ce70fba5611f94ed25d664584645abf1c3ed588692549142500d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381865700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f54f7d515762b3e26f16e6485ab7610f45c8f013482d0bc14a989d91557922e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:20:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:20:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:20:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:21:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:21:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:21:35 GMT
RUN npm install -g rtlcss
# Tue, 09 Jun 2020 08:21:35 GMT
ENV ODOO_VERSION=13.0
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
# Mon, 29 Jun 2020 20:38:51 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:38:53 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:38:54 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:38:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:38:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:38:54 GMT
USER odoo
# Mon, 29 Jun 2020 20:38:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:38:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c38fb221c6bbb14c929d8dc9845e790d99ab77c30f35eeda6d0271790132f8f`  
		Last Modified: Tue, 09 Jun 2020 08:29:18 GMT  
		Size: 204.1 MB (204081824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fbb07c19f556a4061c1794e095cb19bde5b5853b7bbda4820e6f15d50e720e`  
		Last Modified: Tue, 09 Jun 2020 08:28:44 GMT  
		Size: 2.3 MB (2335295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f3dc70f3be0a19e54a19846ffa5cd607a2a93c5323ffc80a908f1b4b856ad4`  
		Last Modified: Tue, 09 Jun 2020 08:28:43 GMT  
		Size: 1.1 MB (1095530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c04441f8ef8d1451f0f65a419e5ca67cae5f0350a50ceabaad40a26968552`  
		Last Modified: Mon, 29 Jun 2020 20:42:10 GMT  
		Size: 147.3 MB (147252384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ced95b7d280e6c3510b10069e39f2ddf3d1d708429f4dd85563c2c6962216`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc306e3d6e98068e9e30c6f06e3f146eeaa10ad0beeb814a57afbb5024592756`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5f1596c13e989ec960b6e44fdfe7c62f70bc01b672acf366936aee5e4b995a`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8fe6ed13672ea60237445b3cf3d9e6e69176b8042c586ce615c9088bd2281b`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:562dcfc9ec1299498ccf0fd6aa03be98ec84b83d9705712ec8edadfcaa90d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:9d455e32dad6ce70fba5611f94ed25d664584645abf1c3ed588692549142500d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381865700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f54f7d515762b3e26f16e6485ab7610f45c8f013482d0bc14a989d91557922e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:20:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:20:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:20:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:21:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:21:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:21:35 GMT
RUN npm install -g rtlcss
# Tue, 09 Jun 2020 08:21:35 GMT
ENV ODOO_VERSION=13.0
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
# Mon, 29 Jun 2020 20:38:51 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:38:53 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:38:54 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:38:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:38:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:38:54 GMT
USER odoo
# Mon, 29 Jun 2020 20:38:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:38:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c38fb221c6bbb14c929d8dc9845e790d99ab77c30f35eeda6d0271790132f8f`  
		Last Modified: Tue, 09 Jun 2020 08:29:18 GMT  
		Size: 204.1 MB (204081824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fbb07c19f556a4061c1794e095cb19bde5b5853b7bbda4820e6f15d50e720e`  
		Last Modified: Tue, 09 Jun 2020 08:28:44 GMT  
		Size: 2.3 MB (2335295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f3dc70f3be0a19e54a19846ffa5cd607a2a93c5323ffc80a908f1b4b856ad4`  
		Last Modified: Tue, 09 Jun 2020 08:28:43 GMT  
		Size: 1.1 MB (1095530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c04441f8ef8d1451f0f65a419e5ca67cae5f0350a50ceabaad40a26968552`  
		Last Modified: Mon, 29 Jun 2020 20:42:10 GMT  
		Size: 147.3 MB (147252384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ced95b7d280e6c3510b10069e39f2ddf3d1d708429f4dd85563c2c6962216`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc306e3d6e98068e9e30c6f06e3f146eeaa10ad0beeb814a57afbb5024592756`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5f1596c13e989ec960b6e44fdfe7c62f70bc01b672acf366936aee5e4b995a`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8fe6ed13672ea60237445b3cf3d9e6e69176b8042c586ce615c9088bd2281b`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:562dcfc9ec1299498ccf0fd6aa03be98ec84b83d9705712ec8edadfcaa90d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:9d455e32dad6ce70fba5611f94ed25d664584645abf1c3ed588692549142500d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381865700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f54f7d515762b3e26f16e6485ab7610f45c8f013482d0bc14a989d91557922e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:20:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:20:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:20:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:21:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:21:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:21:35 GMT
RUN npm install -g rtlcss
# Tue, 09 Jun 2020 08:21:35 GMT
ENV ODOO_VERSION=13.0
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
# Mon, 29 Jun 2020 20:38:51 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:38:53 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:38:54 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:38:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:38:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:38:54 GMT
USER odoo
# Mon, 29 Jun 2020 20:38:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:38:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c38fb221c6bbb14c929d8dc9845e790d99ab77c30f35eeda6d0271790132f8f`  
		Last Modified: Tue, 09 Jun 2020 08:29:18 GMT  
		Size: 204.1 MB (204081824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fbb07c19f556a4061c1794e095cb19bde5b5853b7bbda4820e6f15d50e720e`  
		Last Modified: Tue, 09 Jun 2020 08:28:44 GMT  
		Size: 2.3 MB (2335295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f3dc70f3be0a19e54a19846ffa5cd607a2a93c5323ffc80a908f1b4b856ad4`  
		Last Modified: Tue, 09 Jun 2020 08:28:43 GMT  
		Size: 1.1 MB (1095530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c04441f8ef8d1451f0f65a419e5ca67cae5f0350a50ceabaad40a26968552`  
		Last Modified: Mon, 29 Jun 2020 20:42:10 GMT  
		Size: 147.3 MB (147252384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ced95b7d280e6c3510b10069e39f2ddf3d1d708429f4dd85563c2c6962216`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc306e3d6e98068e9e30c6f06e3f146eeaa10ad0beeb814a57afbb5024592756`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5f1596c13e989ec960b6e44fdfe7c62f70bc01b672acf366936aee5e4b995a`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8fe6ed13672ea60237445b3cf3d9e6e69176b8042c586ce615c9088bd2281b`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
