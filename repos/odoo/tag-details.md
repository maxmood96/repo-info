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
$ docker pull odoo@sha256:7899e1941c53009269408faa296e2d80ab511f9963e9b6e146d09f4fa6ec203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:9ea449cce3bbbb92bb8ec3568ecd501822d470ace07a264d4f68918256f4e6c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539583832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957ee8392ebad5f99fb61c45e91324286ef884be3d7ee0cacf7ab10970b65ea`
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
# Fri, 25 Feb 2022 19:15:36 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:15:36 GMT
ARG ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
# Fri, 25 Feb 2022 19:17:11 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:17:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:17:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:17:14 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:17:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:17:14 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:17:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:17:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:17:15 GMT
USER odoo
# Fri, 25 Feb 2022 19:17:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:17:15 GMT
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
	-	`sha256:6681b9c776af2285cc7d805895c54f2606d920ea2514992eb9c2d6a429601681`  
		Last Modified: Fri, 25 Feb 2022 19:19:57 GMT  
		Size: 291.4 MB (291415517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d1ee6f065738f62686b41c59c5beaa769aa8e0d4b512d36c5f3eae5d9cc109`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75400279eb241d35522f3ef4370e12c5803ed0bdc0e58e5dffefa0ddec77b24`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aec90ef978964471f123107836571284fc05f1fd76e8d778f17f4c59e809b`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7691318e4e059b92314ab4fc71d2a30e5a236f4e026a40ce48f9cb913c669`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:7899e1941c53009269408faa296e2d80ab511f9963e9b6e146d09f4fa6ec203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:9ea449cce3bbbb92bb8ec3568ecd501822d470ace07a264d4f68918256f4e6c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.6 MB (539583832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a957ee8392ebad5f99fb61c45e91324286ef884be3d7ee0cacf7ab10970b65ea`
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
# Fri, 25 Feb 2022 19:15:36 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:15:36 GMT
ARG ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
# Fri, 25 Feb 2022 19:17:11 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:17:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:17:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:17:14 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=185dd6dd73213fac8fd042d6c408bd26f697d53e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:17:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:17:14 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:17:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:17:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:17:15 GMT
USER odoo
# Fri, 25 Feb 2022 19:17:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:17:15 GMT
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
	-	`sha256:6681b9c776af2285cc7d805895c54f2606d920ea2514992eb9c2d6a429601681`  
		Last Modified: Fri, 25 Feb 2022 19:19:57 GMT  
		Size: 291.4 MB (291415517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d1ee6f065738f62686b41c59c5beaa769aa8e0d4b512d36c5f3eae5d9cc109`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75400279eb241d35522f3ef4370e12c5803ed0bdc0e58e5dffefa0ddec77b24`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299aec90ef978964471f123107836571284fc05f1fd76e8d778f17f4c59e809b`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7691318e4e059b92314ab4fc71d2a30e5a236f4e026a40ce48f9cb913c669`  
		Last Modified: Fri, 25 Feb 2022 19:19:18 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:e23c08de17ce2a48a690d4a9548c6a5ba35e3ab44fe6758f29a4fd011afd215a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:e951732a79607cb50e26ec5ca564c04c3d8186eeee20c5f695df416192df28ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.4 MB (529424856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066c698efc4c30748a827f462fb770b2b685d021014d80776c42ccdaf8465f71`
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
# Fri, 25 Feb 2022 19:13:42 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:13:42 GMT
ARG ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
# Fri, 25 Feb 2022 19:15:23 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:15:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:15:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:15:29 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:15:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:15:30 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:15:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:15:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:15:30 GMT
USER odoo
# Fri, 25 Feb 2022 19:15:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:15:31 GMT
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
	-	`sha256:cce383721eacbb2286b290fd030dd46d8d63fdcca86f95835faae9ecabf330db`  
		Last Modified: Fri, 25 Feb 2022 19:19:08 GMT  
		Size: 275.2 MB (275212016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b684eb724813294883484e33f0d3ec9d710b356abf1b58bf1112c16308317`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68917eed514e749420a34eafa9b4177aea9fe39dcddab89ca9cb56bbe9f9322d`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c04198c9436079c5fd78e3103392bce70ff9e742d2b5b34740a6ba26a17250`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a1d07441aef278fa4cde45ff315ac6fd2f663bf0aca9f2230366908e38ff73`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:e23c08de17ce2a48a690d4a9548c6a5ba35e3ab44fe6758f29a4fd011afd215a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:e951732a79607cb50e26ec5ca564c04c3d8186eeee20c5f695df416192df28ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.4 MB (529424856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066c698efc4c30748a827f462fb770b2b685d021014d80776c42ccdaf8465f71`
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
# Fri, 25 Feb 2022 19:13:42 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:13:42 GMT
ARG ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
# Fri, 25 Feb 2022 19:15:23 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:15:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:15:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:15:29 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=43391a3049b84ee35d58815ad1052c777a113e60
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:15:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:15:30 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:15:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:15:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:15:30 GMT
USER odoo
# Fri, 25 Feb 2022 19:15:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:15:31 GMT
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
	-	`sha256:cce383721eacbb2286b290fd030dd46d8d63fdcca86f95835faae9ecabf330db`  
		Last Modified: Fri, 25 Feb 2022 19:19:08 GMT  
		Size: 275.2 MB (275212016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b684eb724813294883484e33f0d3ec9d710b356abf1b58bf1112c16308317`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68917eed514e749420a34eafa9b4177aea9fe39dcddab89ca9cb56bbe9f9322d`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c04198c9436079c5fd78e3103392bce70ff9e742d2b5b34740a6ba26a17250`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a1d07441aef278fa4cde45ff315ac6fd2f663bf0aca9f2230366908e38ff73`  
		Last Modified: Fri, 25 Feb 2022 19:18:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:378de7b9cc75e9de2f5c10ada0e0950110a9a31efdd278fc043297abdb5e679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:a245f41cece0c7118e3016decc569316a928b13d7a13bb0470caf3937e12a460
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548928265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28775e04f869591ceeb617d6f542376dbb072a9b715f7e041d79c862e7f90a3`
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
# Fri, 25 Feb 2022 19:11:32 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:11:33 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Fri, 25 Feb 2022 19:13:30 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:13:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:13:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:13:36 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:13:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:13:36 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:13:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:13:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:13:37 GMT
USER odoo
# Fri, 25 Feb 2022 19:13:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:13:38 GMT
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
	-	`sha256:fe612bff0abd7042b08bb35f553922ce2084684f1ed1be9640f0cb848415380c`  
		Last Modified: Fri, 25 Feb 2022 19:18:20 GMT  
		Size: 294.3 MB (294322114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bea4d789563cd6537732d4dec566706d4d625084fc5950b43b8e4a2405f29`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0be39161b45aaedb3810d1fea16d48ecdfdef4a9fbf44930d4fccf77a2b236`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acae5b4ece5d09c16c28c8d53dc73fdc6bbf752ce91f5ebfdf16a3d86f940d`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6eee278cd3c147cda4d18ee243730ad0c24fed1d398f2348f63ecfc0807b9`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:378de7b9cc75e9de2f5c10ada0e0950110a9a31efdd278fc043297abdb5e679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:a245f41cece0c7118e3016decc569316a928b13d7a13bb0470caf3937e12a460
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548928265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28775e04f869591ceeb617d6f542376dbb072a9b715f7e041d79c862e7f90a3`
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
# Fri, 25 Feb 2022 19:11:32 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:11:33 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Fri, 25 Feb 2022 19:13:30 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:13:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:13:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:13:36 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:13:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:13:36 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:13:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:13:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:13:37 GMT
USER odoo
# Fri, 25 Feb 2022 19:13:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:13:38 GMT
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
	-	`sha256:fe612bff0abd7042b08bb35f553922ce2084684f1ed1be9640f0cb848415380c`  
		Last Modified: Fri, 25 Feb 2022 19:18:20 GMT  
		Size: 294.3 MB (294322114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bea4d789563cd6537732d4dec566706d4d625084fc5950b43b8e4a2405f29`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0be39161b45aaedb3810d1fea16d48ecdfdef4a9fbf44930d4fccf77a2b236`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acae5b4ece5d09c16c28c8d53dc73fdc6bbf752ce91f5ebfdf16a3d86f940d`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6eee278cd3c147cda4d18ee243730ad0c24fed1d398f2348f63ecfc0807b9`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:378de7b9cc75e9de2f5c10ada0e0950110a9a31efdd278fc043297abdb5e679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:a245f41cece0c7118e3016decc569316a928b13d7a13bb0470caf3937e12a460
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548928265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28775e04f869591ceeb617d6f542376dbb072a9b715f7e041d79c862e7f90a3`
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
# Fri, 25 Feb 2022 19:11:32 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:11:33 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Fri, 25 Feb 2022 19:13:30 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:13:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:13:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:13:36 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:13:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:13:36 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:13:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:13:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:13:37 GMT
USER odoo
# Fri, 25 Feb 2022 19:13:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:13:38 GMT
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
	-	`sha256:fe612bff0abd7042b08bb35f553922ce2084684f1ed1be9640f0cb848415380c`  
		Last Modified: Fri, 25 Feb 2022 19:18:20 GMT  
		Size: 294.3 MB (294322114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bea4d789563cd6537732d4dec566706d4d625084fc5950b43b8e4a2405f29`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0be39161b45aaedb3810d1fea16d48ecdfdef4a9fbf44930d4fccf77a2b236`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acae5b4ece5d09c16c28c8d53dc73fdc6bbf752ce91f5ebfdf16a3d86f940d`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6eee278cd3c147cda4d18ee243730ad0c24fed1d398f2348f63ecfc0807b9`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
