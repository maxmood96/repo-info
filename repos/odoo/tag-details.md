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
$ docker pull odoo@sha256:ae6932016d717063790eb54630604962822eee22a119ad0c76fe9752888da44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:5889c3ea6d49f0f0888ef1d91715882800ac3e8bf35bb2b62ac661390fcdc057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540242077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3124e160b15d13756c07852fc3ece546506eaa13b73fcf5af854903fa208f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:48:46 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:48:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:48:58 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:48:58 GMT
ENV ODOO_VERSION=13.0
# Fri, 08 Jul 2022 18:42:57 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:42:57 GMT
ARG ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
# Fri, 08 Jul 2022 18:44:09 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:44:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:44:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:44:14 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:44:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:44:14 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:44:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:44:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:44:14 GMT
USER odoo
# Fri, 08 Jul 2022 18:44:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:44:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83eee462c654020a3586541aea3d6bc53550868ea56856a558c32a009ecc61f`  
		Last Modified: Thu, 23 Jun 2022 04:52:40 GMT  
		Size: 207.1 MB (207143564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccc6ace4d9383ea46d39569a7f843ffb7881fbc9c7cdab672d5e562cda66b37`  
		Last Modified: Thu, 23 Jun 2022 04:52:19 GMT  
		Size: 13.4 MB (13443244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc66057e559306ecef1d2f9dce87fdc3c8e709d9cf592428301154122ecc292`  
		Last Modified: Thu, 23 Jun 2022 04:52:16 GMT  
		Size: 491.8 KB (491847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d736c0b942251e6baba098c3f918e016259870648bdffcfbd5df57bf9ebe72a`  
		Last Modified: Fri, 08 Jul 2022 18:46:37 GMT  
		Size: 292.0 MB (292020911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf897ab4fd904085f673c53cbc03555bde7d6871f37b62cb200c00d724641b3`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13780a4c3c3e9ea2182091090d4afda691613876ebd8e182eae9969c6f28899`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeff1a17daa38fefdc0e30fb1641b8392286bd317fd40151c7d0783232a097b`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc605c9e24d929b0d2d3bb0cca28f3ba8bf5ff6844484f0703c768ea009cd91`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:ae6932016d717063790eb54630604962822eee22a119ad0c76fe9752888da44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:5889c3ea6d49f0f0888ef1d91715882800ac3e8bf35bb2b62ac661390fcdc057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540242077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3124e160b15d13756c07852fc3ece546506eaa13b73fcf5af854903fa208f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:48:46 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:48:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:48:58 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:48:58 GMT
ENV ODOO_VERSION=13.0
# Fri, 08 Jul 2022 18:42:57 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:42:57 GMT
ARG ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
# Fri, 08 Jul 2022 18:44:09 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:44:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:44:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:44:14 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=95fae6ca695e8f93d7eb6abb79b3813d1b5d926b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:44:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:44:14 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:44:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:44:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:44:14 GMT
USER odoo
# Fri, 08 Jul 2022 18:44:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:44:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83eee462c654020a3586541aea3d6bc53550868ea56856a558c32a009ecc61f`  
		Last Modified: Thu, 23 Jun 2022 04:52:40 GMT  
		Size: 207.1 MB (207143564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccc6ace4d9383ea46d39569a7f843ffb7881fbc9c7cdab672d5e562cda66b37`  
		Last Modified: Thu, 23 Jun 2022 04:52:19 GMT  
		Size: 13.4 MB (13443244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc66057e559306ecef1d2f9dce87fdc3c8e709d9cf592428301154122ecc292`  
		Last Modified: Thu, 23 Jun 2022 04:52:16 GMT  
		Size: 491.8 KB (491847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d736c0b942251e6baba098c3f918e016259870648bdffcfbd5df57bf9ebe72a`  
		Last Modified: Fri, 08 Jul 2022 18:46:37 GMT  
		Size: 292.0 MB (292020911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf897ab4fd904085f673c53cbc03555bde7d6871f37b62cb200c00d724641b3`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13780a4c3c3e9ea2182091090d4afda691613876ebd8e182eae9969c6f28899`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeff1a17daa38fefdc0e30fb1641b8392286bd317fd40151c7d0783232a097b`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc605c9e24d929b0d2d3bb0cca28f3ba8bf5ff6844484f0703c768ea009cd91`  
		Last Modified: Fri, 08 Jul 2022 18:46:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c910438a4308e0735bb48223f5a6cc5b7b77d9845a100bd588a84bf76af84a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:09c266bbf9af1a6146b89dadc166e73d1d9bc2ad629b3101de2c3e490f212bca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.6 MB (530597976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca6c65f51efb5d17ca080429c5ced3e0c274aaa5d886be5a8e67248c42097b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:46:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:46:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:46:20 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:46:20 GMT
ENV ODOO_VERSION=14.0
# Fri, 08 Jul 2022 18:41:34 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:41:34 GMT
ARG ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
# Fri, 08 Jul 2022 18:42:46 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:42:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:42:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:42:50 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:42:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:42:51 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:42:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:42:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:42:51 GMT
USER odoo
# Fri, 08 Jul 2022 18:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:42:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfddafe5e99a0c369c5c2c9011265c2b875f1b14e75d44339afebb8c4a79938`  
		Last Modified: Thu, 23 Jun 2022 04:51:57 GMT  
		Size: 213.2 MB (213182993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794ef76c633a0fd19d5aae7fa2845374d7c5a01d812c71edd98a04287e5b02c`  
		Last Modified: Thu, 23 Jun 2022 04:51:35 GMT  
		Size: 13.4 MB (13444456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1652e870c7471ca1e119944afe2e23f91b602def7422b29d3f254074c4667ee0`  
		Last Modified: Thu, 23 Jun 2022 04:51:32 GMT  
		Size: 491.8 KB (491827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6006ee8047e010b64a099edd23e20a863c6dada00965e7a968ad5358e15bc79c`  
		Last Modified: Fri, 08 Jul 2022 18:45:52 GMT  
		Size: 276.3 MB (276336192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae7c3d755c2dcbf40e981746bdf05dcdddc02e6fef7fe59333f5eadab52c311`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc34ae9305a022ae911a9de4b1bc64d47f8085b38d6e6ab0069ff0a6f769be`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1497d5565a1d566c378e9d517cf441a661ad2dcff9969d7eb8df0341ecdeb9`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a6ffa9498715e1cca3697e169c7af123c3a32647a269b483dcdaab70034814`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c910438a4308e0735bb48223f5a6cc5b7b77d9845a100bd588a84bf76af84a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:09c266bbf9af1a6146b89dadc166e73d1d9bc2ad629b3101de2c3e490f212bca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.6 MB (530597976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca6c65f51efb5d17ca080429c5ced3e0c274aaa5d886be5a8e67248c42097b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:46:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:46:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:46:20 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:46:20 GMT
ENV ODOO_VERSION=14.0
# Fri, 08 Jul 2022 18:41:34 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:41:34 GMT
ARG ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
# Fri, 08 Jul 2022 18:42:46 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:42:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:42:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:42:50 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=12774eac55ced7723f67be9e15577692162f4854
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:42:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:42:51 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:42:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:42:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:42:51 GMT
USER odoo
# Fri, 08 Jul 2022 18:42:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:42:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfddafe5e99a0c369c5c2c9011265c2b875f1b14e75d44339afebb8c4a79938`  
		Last Modified: Thu, 23 Jun 2022 04:51:57 GMT  
		Size: 213.2 MB (213182993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794ef76c633a0fd19d5aae7fa2845374d7c5a01d812c71edd98a04287e5b02c`  
		Last Modified: Thu, 23 Jun 2022 04:51:35 GMT  
		Size: 13.4 MB (13444456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1652e870c7471ca1e119944afe2e23f91b602def7422b29d3f254074c4667ee0`  
		Last Modified: Thu, 23 Jun 2022 04:51:32 GMT  
		Size: 491.8 KB (491827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6006ee8047e010b64a099edd23e20a863c6dada00965e7a968ad5358e15bc79c`  
		Last Modified: Fri, 08 Jul 2022 18:45:52 GMT  
		Size: 276.3 MB (276336192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae7c3d755c2dcbf40e981746bdf05dcdddc02e6fef7fe59333f5eadab52c311`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc34ae9305a022ae911a9de4b1bc64d47f8085b38d6e6ab0069ff0a6f769be`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1497d5565a1d566c378e9d517cf441a661ad2dcff9969d7eb8df0341ecdeb9`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a6ffa9498715e1cca3697e169c7af123c3a32647a269b483dcdaab70034814`  
		Last Modified: Fri, 08 Jul 2022 18:45:19 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:e9d693d1d5bf7667b008694135d8f6e9fa3fec40f8adc948a1af36467d5a4a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:18daa3a80af6205520c700a64cedcab3007e795c8a9de72e5e58f1354193dd10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556016372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7b0883396ecb062e2f92cae8eb93efedd2aab1c4efa543b35ab4ef942ab821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Fri, 08 Jul 2022 18:41:12 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:41:18 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:41:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:41:18 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:41:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:41:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:41:18 GMT
USER odoo
# Fri, 08 Jul 2022 18:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:41:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3910581f15fdcef2185fccd0c2a74311afe8bc687d007096fe46850f943619`  
		Last Modified: Fri, 08 Jul 2022 18:45:06 GMT  
		Size: 301.3 MB (301326761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc733f9e41f8e7ffab47edf0d95fc50e1d203f85edcfb90ba9c77194eefec8`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949ead7533e92b06806763af7ba506f58277e31403637dd8239781c1c59a048`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aea26eedacfcb6bc449a6a5aed978cc97bda1c27af44f5047dd8d924f4756c6`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02f7e0b340396eb88e897214aea454e6a35d79089a16c95e8f531fca44d9ec`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:e9d693d1d5bf7667b008694135d8f6e9fa3fec40f8adc948a1af36467d5a4a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:18daa3a80af6205520c700a64cedcab3007e795c8a9de72e5e58f1354193dd10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556016372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7b0883396ecb062e2f92cae8eb93efedd2aab1c4efa543b35ab4ef942ab821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Fri, 08 Jul 2022 18:41:12 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:41:18 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:41:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:41:18 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:41:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:41:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:41:18 GMT
USER odoo
# Fri, 08 Jul 2022 18:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:41:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3910581f15fdcef2185fccd0c2a74311afe8bc687d007096fe46850f943619`  
		Last Modified: Fri, 08 Jul 2022 18:45:06 GMT  
		Size: 301.3 MB (301326761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc733f9e41f8e7ffab47edf0d95fc50e1d203f85edcfb90ba9c77194eefec8`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949ead7533e92b06806763af7ba506f58277e31403637dd8239781c1c59a048`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aea26eedacfcb6bc449a6a5aed978cc97bda1c27af44f5047dd8d924f4756c6`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02f7e0b340396eb88e897214aea454e6a35d79089a16c95e8f531fca44d9ec`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:e9d693d1d5bf7667b008694135d8f6e9fa3fec40f8adc948a1af36467d5a4a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:18daa3a80af6205520c700a64cedcab3007e795c8a9de72e5e58f1354193dd10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556016372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7b0883396ecb062e2f92cae8eb93efedd2aab1c4efa543b35ab4ef942ab821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Fri, 08 Jul 2022 18:41:12 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:41:18 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:41:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:41:18 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:41:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:41:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:41:18 GMT
USER odoo
# Fri, 08 Jul 2022 18:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:41:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3910581f15fdcef2185fccd0c2a74311afe8bc687d007096fe46850f943619`  
		Last Modified: Fri, 08 Jul 2022 18:45:06 GMT  
		Size: 301.3 MB (301326761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc733f9e41f8e7ffab47edf0d95fc50e1d203f85edcfb90ba9c77194eefec8`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949ead7533e92b06806763af7ba506f58277e31403637dd8239781c1c59a048`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aea26eedacfcb6bc449a6a5aed978cc97bda1c27af44f5047dd8d924f4756c6`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02f7e0b340396eb88e897214aea454e6a35d79089a16c95e8f531fca44d9ec`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
