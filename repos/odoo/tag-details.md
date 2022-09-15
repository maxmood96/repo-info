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
$ docker pull odoo@sha256:e29e84ca93d492c5ba3a4a8e0608e17c435d6181642efb437a780fff6df3833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:996afbe05044113afaa8744bc0b0356cf1b5a84abd017080adb536f8610957a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.4 MB (540351067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476a14c67a7a835c5b5320f8bd519d729025c6475c7747299fe83b4f2d53bca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:56:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:56:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:57:02 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:57:02 GMT
ENV ODOO_VERSION=13.0
# Thu, 15 Sep 2022 17:24:50 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:24:50 GMT
ARG ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
# Thu, 15 Sep 2022 17:26:03 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:26:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:26:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:26:07 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:26:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:26:07 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:26:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:26:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:26:07 GMT
USER odoo
# Thu, 15 Sep 2022 17:26:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:26:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5fc672d49e136ecb8725a1f4d4d42c67c27dbb0cde157b5c53ae2b79e69aa`  
		Last Modified: Tue, 13 Sep 2022 07:00:46 GMT  
		Size: 207.1 MB (207143846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eba5ac56590f61c1bbc1a6ae4c2a367215fcc0f8681fa113bc534175eefac3`  
		Last Modified: Tue, 13 Sep 2022 07:00:25 GMT  
		Size: 13.4 MB (13442347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79773cdec162998e8fc6cfb2a99a8d2b8ae9db406f671c4f41cfdfca0af9b9d4`  
		Last Modified: Tue, 13 Sep 2022 07:00:22 GMT  
		Size: 454.2 KB (454225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ba9d1abacb0756d8542876998debe8c8bc5087ca06cd1e6df24a01133560de`  
		Last Modified: Thu, 15 Sep 2022 17:28:28 GMT  
		Size: 292.2 MB (292177628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7190e31195200881edb4ed6d166768bc67277c5d6c382a0bcc0e00a8a7beb0f3`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8baec6afcc573a11e35fbc08321e96dff0f0341906d772b1d721c78d39bfc2ac`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60565a66cf4df97cbb71914f41f36c140a169077449663fd82de0b6f307de750`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ca3c0f6ef20d9e0e4e6da6934bdea7ea852368b8a686618a6cced92a15848f`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:e29e84ca93d492c5ba3a4a8e0608e17c435d6181642efb437a780fff6df3833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:996afbe05044113afaa8744bc0b0356cf1b5a84abd017080adb536f8610957a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.4 MB (540351067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476a14c67a7a835c5b5320f8bd519d729025c6475c7747299fe83b4f2d53bca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:56:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:56:59 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:57:02 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:57:02 GMT
ENV ODOO_VERSION=13.0
# Thu, 15 Sep 2022 17:24:50 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:24:50 GMT
ARG ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
# Thu, 15 Sep 2022 17:26:03 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:26:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:26:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:26:07 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=c2e9376f0bda9bb11bc102e038594da452b38198
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:26:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:26:07 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:26:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:26:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:26:07 GMT
USER odoo
# Thu, 15 Sep 2022 17:26:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:26:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5fc672d49e136ecb8725a1f4d4d42c67c27dbb0cde157b5c53ae2b79e69aa`  
		Last Modified: Tue, 13 Sep 2022 07:00:46 GMT  
		Size: 207.1 MB (207143846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eba5ac56590f61c1bbc1a6ae4c2a367215fcc0f8681fa113bc534175eefac3`  
		Last Modified: Tue, 13 Sep 2022 07:00:25 GMT  
		Size: 13.4 MB (13442347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79773cdec162998e8fc6cfb2a99a8d2b8ae9db406f671c4f41cfdfca0af9b9d4`  
		Last Modified: Tue, 13 Sep 2022 07:00:22 GMT  
		Size: 454.2 KB (454225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ba9d1abacb0756d8542876998debe8c8bc5087ca06cd1e6df24a01133560de`  
		Last Modified: Thu, 15 Sep 2022 17:28:28 GMT  
		Size: 292.2 MB (292177628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7190e31195200881edb4ed6d166768bc67277c5d6c382a0bcc0e00a8a7beb0f3`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8baec6afcc573a11e35fbc08321e96dff0f0341906d772b1d721c78d39bfc2ac`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60565a66cf4df97cbb71914f41f36c140a169077449663fd82de0b6f307de750`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ca3c0f6ef20d9e0e4e6da6934bdea7ea852368b8a686618a6cced92a15848f`  
		Last Modified: Thu, 15 Sep 2022 17:27:56 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:a8674161ec18d0972a5b2a3bbdd375c5089c8f3b4f9d2972c94b65481991e7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:32e5ce2fce6f7d956733c2009bac044ecb8f8c4beb3c548da482a930a5fed25e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530879719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b3ef89255a0873dd6510129aa9d9f7d32206797209794807db615c63d6cf16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:54:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:54:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:54:16 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:54:16 GMT
ENV ODOO_VERSION=14.0
# Thu, 15 Sep 2022 17:23:27 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:23:27 GMT
ARG ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
# Thu, 15 Sep 2022 17:24:39 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:24:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:24:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:24:44 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:24:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:24:44 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:24:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:24:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:24:44 GMT
USER odoo
# Thu, 15 Sep 2022 17:24:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:24:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db956de1ff39a9971927e9b97aed9378d75cda5bc3767047513019ca339ecc`  
		Last Modified: Tue, 13 Sep 2022 07:00:04 GMT  
		Size: 213.2 MB (213182384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a30d3af868cc7a2fe2ce4051e6598baec42acba7528ce4cc01707daefc19`  
		Last Modified: Tue, 13 Sep 2022 06:59:40 GMT  
		Size: 13.4 MB (13443898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae60c9aa41d0da30fc7580b68a75025f6ce13ed515f6f4e535a1730b013df8`  
		Last Modified: Tue, 13 Sep 2022 06:59:38 GMT  
		Size: 454.2 KB (454250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72da34051230d17597e66401f3e0a4ca64e62a6a65e647838cdfb04b4275769`  
		Last Modified: Thu, 15 Sep 2022 17:27:46 GMT  
		Size: 276.7 MB (276666172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70fc37f84b27a6bc3a22b2bc1e411b2891212d489e30936976c798e3f1a6bf`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f00cd81dd67be5ffd37589f1d4b4a48fc0b2d18e1d6c0fe7b0199ae3b9f7d5`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902e7638590af7f9a5f0d4b821cee7481080f49ebe5a75b7225efbb934f8b25`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d537d60613f08f957c8659ae5a662e1cbbeb6ef7da20bcec5c95c400382c1`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a8674161ec18d0972a5b2a3bbdd375c5089c8f3b4f9d2972c94b65481991e7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:32e5ce2fce6f7d956733c2009bac044ecb8f8c4beb3c548da482a930a5fed25e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530879719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b3ef89255a0873dd6510129aa9d9f7d32206797209794807db615c63d6cf16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:52:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:52:46 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:54:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:54:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:54:16 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:54:16 GMT
ENV ODOO_VERSION=14.0
# Thu, 15 Sep 2022 17:23:27 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:23:27 GMT
ARG ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
# Thu, 15 Sep 2022 17:24:39 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:24:43 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:24:43 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:24:44 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=263af0514d9354069c62bbe9d552c3fea01e918f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:24:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:24:44 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:24:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:24:44 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:24:44 GMT
USER odoo
# Thu, 15 Sep 2022 17:24:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:24:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db956de1ff39a9971927e9b97aed9378d75cda5bc3767047513019ca339ecc`  
		Last Modified: Tue, 13 Sep 2022 07:00:04 GMT  
		Size: 213.2 MB (213182384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999a30d3af868cc7a2fe2ce4051e6598baec42acba7528ce4cc01707daefc19`  
		Last Modified: Tue, 13 Sep 2022 06:59:40 GMT  
		Size: 13.4 MB (13443898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae60c9aa41d0da30fc7580b68a75025f6ce13ed515f6f4e535a1730b013df8`  
		Last Modified: Tue, 13 Sep 2022 06:59:38 GMT  
		Size: 454.2 KB (454250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72da34051230d17597e66401f3e0a4ca64e62a6a65e647838cdfb04b4275769`  
		Last Modified: Thu, 15 Sep 2022 17:27:46 GMT  
		Size: 276.7 MB (276666172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70fc37f84b27a6bc3a22b2bc1e411b2891212d489e30936976c798e3f1a6bf`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f00cd81dd67be5ffd37589f1d4b4a48fc0b2d18e1d6c0fe7b0199ae3b9f7d5`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902e7638590af7f9a5f0d4b821cee7481080f49ebe5a75b7225efbb934f8b25`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400d537d60613f08f957c8659ae5a662e1cbbeb6ef7da20bcec5c95c400382c1`  
		Last Modified: Thu, 15 Sep 2022 17:27:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:b8d25bc0cbc1574da55a63538b70864a5e5226bfec9ddc17b353768869834dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:9ac7b681779358bf0db023137d79d6339be15fae772c18ebb27abbd57b8ba9ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557881799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1aad3d422f4610525b5def0a32efa02656c73b2bd654594fa20e9f8eb7f676`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 15 Sep 2022 17:21:48 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:21:49 GMT
ARG ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
# Thu, 15 Sep 2022 17:23:06 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:23:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:23:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:23:11 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:23:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:23:11 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:23:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:23:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:23:11 GMT
USER odoo
# Thu, 15 Sep 2022 17:23:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:23:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26aae6777e73e7a5c99846092934166a5dd08b0453a5bde885b8ac9a230b450`  
		Last Modified: Thu, 15 Sep 2022 17:27:00 GMT  
		Size: 303.2 MB (303215804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d728d07516fcc30dce422a91c56f7b2414919af3c32e3841bf1230f6787df8`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2158075ae0271ad48b26d8e1a671233808d351f698b4f851e8fec399ceb40ecb`  
		Last Modified: Thu, 15 Sep 2022 17:26:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c42aa217804700de58c273bbe04d43276a985e8ba9ddc524235e57cf3860f68`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5dd988d78229a54ac8517c1c380ad472d4964a6cc3bdf525dd75a9a435568d`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:b8d25bc0cbc1574da55a63538b70864a5e5226bfec9ddc17b353768869834dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:9ac7b681779358bf0db023137d79d6339be15fae772c18ebb27abbd57b8ba9ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557881799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1aad3d422f4610525b5def0a32efa02656c73b2bd654594fa20e9f8eb7f676`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 15 Sep 2022 17:21:48 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:21:49 GMT
ARG ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
# Thu, 15 Sep 2022 17:23:06 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:23:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:23:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:23:11 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:23:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:23:11 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:23:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:23:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:23:11 GMT
USER odoo
# Thu, 15 Sep 2022 17:23:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:23:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26aae6777e73e7a5c99846092934166a5dd08b0453a5bde885b8ac9a230b450`  
		Last Modified: Thu, 15 Sep 2022 17:27:00 GMT  
		Size: 303.2 MB (303215804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d728d07516fcc30dce422a91c56f7b2414919af3c32e3841bf1230f6787df8`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2158075ae0271ad48b26d8e1a671233808d351f698b4f851e8fec399ceb40ecb`  
		Last Modified: Thu, 15 Sep 2022 17:26:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c42aa217804700de58c273bbe04d43276a985e8ba9ddc524235e57cf3860f68`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5dd988d78229a54ac8517c1c380ad472d4964a6cc3bdf525dd75a9a435568d`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:b8d25bc0cbc1574da55a63538b70864a5e5226bfec9ddc17b353768869834dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:9ac7b681779358bf0db023137d79d6339be15fae772c18ebb27abbd57b8ba9ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557881799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1aad3d422f4610525b5def0a32efa02656c73b2bd654594fa20e9f8eb7f676`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:49:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Sep 2022 06:49:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Sep 2022 06:49:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 06:50:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Sep 2022 06:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:51:11 GMT
RUN npm install -g rtlcss
# Tue, 13 Sep 2022 06:51:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 15 Sep 2022 17:21:48 GMT
ARG ODOO_RELEASE=20220915
# Thu, 15 Sep 2022 17:21:49 GMT
ARG ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
# Thu, 15 Sep 2022 17:23:06 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 15 Sep 2022 17:23:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 15 Sep 2022 17:23:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 15 Sep 2022 17:23:11 GMT
# ARGS: ODOO_RELEASE=20220915 ODOO_SHA=77cb3593717a0b272c5c65a8b493ebb1d96c954c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 15 Sep 2022 17:23:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Sep 2022 17:23:11 GMT
EXPOSE 8069 8071 8072
# Thu, 15 Sep 2022 17:23:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Sep 2022 17:23:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 15 Sep 2022 17:23:11 GMT
USER odoo
# Thu, 15 Sep 2022 17:23:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Sep 2022 17:23:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b73f80e874fc2998c5758d4c8d65d96b8f9ff5544bf075b31ed62614eb1071b`  
		Last Modified: Tue, 13 Sep 2022 06:59:13 GMT  
		Size: 220.3 MB (220296011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fc15e3be86616ca7da0dcee3866c41e512cc3db88484000d55cc15b194c5b4`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 2.5 MB (2513532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c69e7aa750a4c8478c7e63dba1a777a14a00d608706683711ced35910615545`  
		Last Modified: Tue, 13 Sep 2022 06:58:46 GMT  
		Size: 449.9 KB (449869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26aae6777e73e7a5c99846092934166a5dd08b0453a5bde885b8ac9a230b450`  
		Last Modified: Thu, 15 Sep 2022 17:27:00 GMT  
		Size: 303.2 MB (303215804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d728d07516fcc30dce422a91c56f7b2414919af3c32e3841bf1230f6787df8`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2158075ae0271ad48b26d8e1a671233808d351f698b4f851e8fec399ceb40ecb`  
		Last Modified: Thu, 15 Sep 2022 17:26:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c42aa217804700de58c273bbe04d43276a985e8ba9ddc524235e57cf3860f68`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5dd988d78229a54ac8517c1c380ad472d4964a6cc3bdf525dd75a9a435568d`  
		Last Modified: Thu, 15 Sep 2022 17:26:25 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
