<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:latest`](#odoolatest)

## `odoo:14`

```console
$ docker pull odoo@sha256:8a62ccf4e2772a337f47c73b928c99b65b50ff9848395f56baf7890547fd5d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:7e8c20d9922e33689c1a5991bfd7891af9dec9eba8e38ae0bbda215a4be7453e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533060849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f795c1b55369e6361525b3fb30c0725f8ae4ea52892f3e96ec0bd683aae7f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:51:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:51:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:51:23 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:52:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:52:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:52:56 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:52:56 GMT
ENV ODOO_VERSION=14.0
# Mon, 07 Aug 2023 19:30:33 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:30:33 GMT
ARG ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
# Mon, 07 Aug 2023 19:31:49 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:31:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:31:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:31:53 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:31:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:31:53 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:31:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:31:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:31:54 GMT
USER odoo
# Mon, 07 Aug 2023 19:31:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:31:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bc9f9e834edba83c3efb2a57e3ac227a4d4479b19e3c12ee4c1f14d981b2f2`  
		Last Modified: Fri, 28 Jul 2023 02:56:35 GMT  
		Size: 213.2 MB (213181107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2e8d88c2846a4112310b3ca173f85e7dc9a6eb98f04b84206e7dca8e87d213`  
		Last Modified: Fri, 28 Jul 2023 02:56:14 GMT  
		Size: 13.5 MB (13521513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98658aa7823fad0615f4c54034ccaa06788d883b88e776d4574b696d7546036`  
		Last Modified: Fri, 28 Jul 2023 02:56:12 GMT  
		Size: 460.6 KB (460569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1b94e634e1c92d0066fa3e3f228f1fcc4115fb4d8c392b5ca5b73faa2691c4`  
		Last Modified: Mon, 07 Aug 2023 19:34:04 GMT  
		Size: 278.7 MB (278707771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807597a062e11d69e8653670261807cd743fd1343da4b65ce95c57d451af60b`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f55bc8c4c3ff88dbd04eeef379750b7d82e16da7be80586ad0515436c5763f`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4a1deb082b8a352338ef568d0d09bbaeebe6a4d7da0e23a5f946664412f0d`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d6adc1da8df6ae435c6c9bcf1cb8a289067e3782904b8c6e3a74a0fa88d6a7`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:8a62ccf4e2772a337f47c73b928c99b65b50ff9848395f56baf7890547fd5d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:7e8c20d9922e33689c1a5991bfd7891af9dec9eba8e38ae0bbda215a4be7453e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533060849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f795c1b55369e6361525b3fb30c0725f8ae4ea52892f3e96ec0bd683aae7f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:29 GMT
ADD file:20e7ad6bec617357895302b08431eb3430cce3113bdf0a8ff9827115f858d313 in / 
# Thu, 27 Jul 2023 23:25:30 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:51:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:51:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:51:23 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:52:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:52:53 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:52:56 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:52:56 GMT
ENV ODOO_VERSION=14.0
# Mon, 07 Aug 2023 19:30:33 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:30:33 GMT
ARG ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
# Mon, 07 Aug 2023 19:31:49 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:31:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:31:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:31:53 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:31:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:31:53 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:31:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:31:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:31:54 GMT
USER odoo
# Mon, 07 Aug 2023 19:31:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:31:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3240fe174df9a5a4923c4b52f1d887dd1ad1a9ee69245c1fb867f399167584dd`  
		Last Modified: Thu, 27 Jul 2023 23:30:49 GMT  
		Size: 27.2 MB (27187431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bc9f9e834edba83c3efb2a57e3ac227a4d4479b19e3c12ee4c1f14d981b2f2`  
		Last Modified: Fri, 28 Jul 2023 02:56:35 GMT  
		Size: 213.2 MB (213181107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2e8d88c2846a4112310b3ca173f85e7dc9a6eb98f04b84206e7dca8e87d213`  
		Last Modified: Fri, 28 Jul 2023 02:56:14 GMT  
		Size: 13.5 MB (13521513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98658aa7823fad0615f4c54034ccaa06788d883b88e776d4574b696d7546036`  
		Last Modified: Fri, 28 Jul 2023 02:56:12 GMT  
		Size: 460.6 KB (460569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1b94e634e1c92d0066fa3e3f228f1fcc4115fb4d8c392b5ca5b73faa2691c4`  
		Last Modified: Mon, 07 Aug 2023 19:34:04 GMT  
		Size: 278.7 MB (278707771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807597a062e11d69e8653670261807cd743fd1343da4b65ce95c57d451af60b`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f55bc8c4c3ff88dbd04eeef379750b7d82e16da7be80586ad0515436c5763f`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4a1deb082b8a352338ef568d0d09bbaeebe6a4d7da0e23a5f946664412f0d`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d6adc1da8df6ae435c6c9bcf1cb8a289067e3782904b8c6e3a74a0fa88d6a7`  
		Last Modified: Mon, 07 Aug 2023 19:33:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:96fed9b88ece1a196a529b0f88ab176d20e4b0bd8b2e90672af6eb83a9df7d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:8cc11a77a88b481b6ea6cd695e685474afd42bd1950beddac1484d962c1777b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562073416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c133c11972831989a1be4b9121a1830ae12e5b7e29622823661d8804ccdac91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:46:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:46:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:46:05 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:49:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:49:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:49:57 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:49:57 GMT
ENV ODOO_VERSION=15.0
# Mon, 07 Aug 2023 19:29:09 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:29:10 GMT
ARG ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
# Mon, 07 Aug 2023 19:30:23 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:30:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:30:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:30:28 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:30:28 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:30:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:30:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:30:28 GMT
USER odoo
# Mon, 07 Aug 2023 19:30:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:30:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47067e05d070a99da5ec9eb79e9becd9ac18c60d660cc43c3ef4d7444f17f49`  
		Last Modified: Fri, 28 Jul 2023 02:55:52 GMT  
		Size: 220.3 MB (220303225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3326948523e83535b774a028943ca28802b42e3ea0ddcc108faf74c94b5cf938`  
		Last Modified: Fri, 28 Jul 2023 02:55:29 GMT  
		Size: 2.6 MB (2576165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af659eb7245d7acf8035642725b2796364b5c4f24404ce31e998cf97aec6d5e`  
		Last Modified: Fri, 28 Jul 2023 02:55:28 GMT  
		Size: 456.0 KB (455986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8db8c0fa800ea067aac94483b6bd2b83139343fbce91fcbeb4fbe63b1fce04`  
		Last Modified: Mon, 07 Aug 2023 19:33:24 GMT  
		Size: 307.3 MB (307317972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb91452dde07b744214b2d06a707afad85c8a061a2bcda206609d01ce7c74b`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4042df591a84470ef7068fef670394e7f15a277561cf81e165322be0c7b81`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64fb1a00b7710bfcbc61be930acbc01b4f50101167befe4bc6e68167527f590`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d08d1d5d1167f7345c1dc64c3b07aa8af4fef9752902bd5a2f025f6e38fe51`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:96fed9b88ece1a196a529b0f88ab176d20e4b0bd8b2e90672af6eb83a9df7d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:8cc11a77a88b481b6ea6cd695e685474afd42bd1950beddac1484d962c1777b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562073416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c133c11972831989a1be4b9121a1830ae12e5b7e29622823661d8804ccdac91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:46:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:46:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:46:05 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:49:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:49:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:49:57 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:49:57 GMT
ENV ODOO_VERSION=15.0
# Mon, 07 Aug 2023 19:29:09 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:29:10 GMT
ARG ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
# Mon, 07 Aug 2023 19:30:23 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:30:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:30:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:30:28 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:30:28 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:30:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:30:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:30:28 GMT
USER odoo
# Mon, 07 Aug 2023 19:30:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:30:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47067e05d070a99da5ec9eb79e9becd9ac18c60d660cc43c3ef4d7444f17f49`  
		Last Modified: Fri, 28 Jul 2023 02:55:52 GMT  
		Size: 220.3 MB (220303225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3326948523e83535b774a028943ca28802b42e3ea0ddcc108faf74c94b5cf938`  
		Last Modified: Fri, 28 Jul 2023 02:55:29 GMT  
		Size: 2.6 MB (2576165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af659eb7245d7acf8035642725b2796364b5c4f24404ce31e998cf97aec6d5e`  
		Last Modified: Fri, 28 Jul 2023 02:55:28 GMT  
		Size: 456.0 KB (455986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8db8c0fa800ea067aac94483b6bd2b83139343fbce91fcbeb4fbe63b1fce04`  
		Last Modified: Mon, 07 Aug 2023 19:33:24 GMT  
		Size: 307.3 MB (307317972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbb91452dde07b744214b2d06a707afad85c8a061a2bcda206609d01ce7c74b`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4042df591a84470ef7068fef670394e7f15a277561cf81e165322be0c7b81`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64fb1a00b7710bfcbc61be930acbc01b4f50101167befe4bc6e68167527f590`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d08d1d5d1167f7345c1dc64c3b07aa8af4fef9752902bd5a2f025f6e38fe51`  
		Last Modified: Mon, 07 Aug 2023 19:32:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:1453fb147a4dab741f58105e1fffa7986522355fe243ca29cb6ae87a5f9ea48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:980d969e8ba8e2d5aa86b99b744c1257aba0fdaa7c41002fe7c8226b625acaf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575981050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6e60447c01c9b2fde724f63001f97f5a40528f33eb10c0f2e125e11a749f77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:46:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:46:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:46:05 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:47:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:47:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:47:25 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:47:25 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Aug 2023 19:27:31 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:27:31 GMT
ARG ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
# Mon, 07 Aug 2023 19:28:52 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:28:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:28:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:28:57 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:28:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:28:57 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:28:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:28:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:28:57 GMT
USER odoo
# Mon, 07 Aug 2023 19:28:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:28:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7b18b314a0274e5c5d25a9561602103d967aed864ca15eb24fe4a0a73eb1fc`  
		Last Modified: Fri, 28 Jul 2023 02:55:05 GMT  
		Size: 221.0 MB (220993013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d76564217e9cee3abd36ed087a60c3ff8a1b61f35844b48b76d3400a79dd9f`  
		Last Modified: Fri, 28 Jul 2023 02:54:41 GMT  
		Size: 2.6 MB (2579573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72631704fea3dd9fdabd1a84cf63254d1c3a49d0128d3aa9fbb122be8df2b3`  
		Last Modified: Fri, 28 Jul 2023 02:54:41 GMT  
		Size: 456.0 KB (455992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4474becaf3579b8b5212eea9b86365ea0049f31511db552ce306ad9a8f86aa8`  
		Last Modified: Mon, 07 Aug 2023 19:32:39 GMT  
		Size: 320.5 MB (320532403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3a3a5e0cbe4c4275a731ae854769db0f2287d6de8e7099e366c7cecafa236`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c098f7af8f65be4da2acccd821b370313a2ead2525443db8a8eb4b8777dd632a`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5d0014159b39ca058a9eed1f7535c0e5cf2a6b0ebb840b9f7c6bd7c92e644b`  
		Last Modified: Mon, 07 Aug 2023 19:32:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8ac233fd60b245fe842ab99e60b30dc13dc5a7902e7885c230775efed8eb6d`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:1453fb147a4dab741f58105e1fffa7986522355fe243ca29cb6ae87a5f9ea48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:980d969e8ba8e2d5aa86b99b744c1257aba0fdaa7c41002fe7c8226b625acaf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575981050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6e60447c01c9b2fde724f63001f97f5a40528f33eb10c0f2e125e11a749f77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:46:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:46:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:46:05 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:47:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:47:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:47:25 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:47:25 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Aug 2023 19:27:31 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:27:31 GMT
ARG ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
# Mon, 07 Aug 2023 19:28:52 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:28:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:28:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:28:57 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:28:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:28:57 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:28:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:28:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:28:57 GMT
USER odoo
# Mon, 07 Aug 2023 19:28:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:28:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7b18b314a0274e5c5d25a9561602103d967aed864ca15eb24fe4a0a73eb1fc`  
		Last Modified: Fri, 28 Jul 2023 02:55:05 GMT  
		Size: 221.0 MB (220993013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d76564217e9cee3abd36ed087a60c3ff8a1b61f35844b48b76d3400a79dd9f`  
		Last Modified: Fri, 28 Jul 2023 02:54:41 GMT  
		Size: 2.6 MB (2579573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72631704fea3dd9fdabd1a84cf63254d1c3a49d0128d3aa9fbb122be8df2b3`  
		Last Modified: Fri, 28 Jul 2023 02:54:41 GMT  
		Size: 456.0 KB (455992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4474becaf3579b8b5212eea9b86365ea0049f31511db552ce306ad9a8f86aa8`  
		Last Modified: Mon, 07 Aug 2023 19:32:39 GMT  
		Size: 320.5 MB (320532403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3a3a5e0cbe4c4275a731ae854769db0f2287d6de8e7099e366c7cecafa236`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c098f7af8f65be4da2acccd821b370313a2ead2525443db8a8eb4b8777dd632a`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5d0014159b39ca058a9eed1f7535c0e5cf2a6b0ebb840b9f7c6bd7c92e644b`  
		Last Modified: Mon, 07 Aug 2023 19:32:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8ac233fd60b245fe842ab99e60b30dc13dc5a7902e7885c230775efed8eb6d`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:1453fb147a4dab741f58105e1fffa7986522355fe243ca29cb6ae87a5f9ea48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:980d969e8ba8e2d5aa86b99b744c1257aba0fdaa7c41002fe7c8226b625acaf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575981050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6e60447c01c9b2fde724f63001f97f5a40528f33eb10c0f2e125e11a749f77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:46:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 28 Jul 2023 02:46:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 28 Jul 2023 02:46:05 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:47:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 28 Jul 2023 02:47:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:47:25 GMT
RUN npm install -g rtlcss
# Fri, 28 Jul 2023 02:47:25 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Aug 2023 19:27:31 GMT
ARG ODOO_RELEASE=20230807
# Mon, 07 Aug 2023 19:27:31 GMT
ARG ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
# Mon, 07 Aug 2023 19:28:52 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 07 Aug 2023 19:28:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 07 Aug 2023 19:28:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 07 Aug 2023 19:28:57 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 07 Aug 2023 19:28:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Aug 2023 19:28:57 GMT
EXPOSE 8069 8071 8072
# Mon, 07 Aug 2023 19:28:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Aug 2023 19:28:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 07 Aug 2023 19:28:57 GMT
USER odoo
# Mon, 07 Aug 2023 19:28:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Aug 2023 19:28:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7b18b314a0274e5c5d25a9561602103d967aed864ca15eb24fe4a0a73eb1fc`  
		Last Modified: Fri, 28 Jul 2023 02:55:05 GMT  
		Size: 221.0 MB (220993013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d76564217e9cee3abd36ed087a60c3ff8a1b61f35844b48b76d3400a79dd9f`  
		Last Modified: Fri, 28 Jul 2023 02:54:41 GMT  
		Size: 2.6 MB (2579573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72631704fea3dd9fdabd1a84cf63254d1c3a49d0128d3aa9fbb122be8df2b3`  
		Last Modified: Fri, 28 Jul 2023 02:54:41 GMT  
		Size: 456.0 KB (455992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4474becaf3579b8b5212eea9b86365ea0049f31511db552ce306ad9a8f86aa8`  
		Last Modified: Mon, 07 Aug 2023 19:32:39 GMT  
		Size: 320.5 MB (320532403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e3a3a5e0cbe4c4275a731ae854769db0f2287d6de8e7099e366c7cecafa236`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c098f7af8f65be4da2acccd821b370313a2ead2525443db8a8eb4b8777dd632a`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5d0014159b39ca058a9eed1f7535c0e5cf2a6b0ebb840b9f7c6bd7c92e644b`  
		Last Modified: Mon, 07 Aug 2023 19:32:05 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8ac233fd60b245fe842ab99e60b30dc13dc5a7902e7885c230775efed8eb6d`  
		Last Modified: Mon, 07 Aug 2023 19:32:04 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
