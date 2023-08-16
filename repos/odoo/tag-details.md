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
$ docker pull odoo@sha256:e66b80ceef1d5198cbe7b18608eee0623dc49a2f9a55a742495ec80eee86c61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:4d3f6136e6a057f510e050784231f42fc7b67d75f646b4e9af7f7e4bdc99c7b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533059231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1394603f893de212ff23bba7816b47d5a9954cec6de1640fe80064a8ea82b120`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:21:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:21:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:21:48 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:23:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:23:15 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:23:17 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:23:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 16 Aug 2023 10:23:17 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:23:17 GMT
ARG ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
# Wed, 16 Aug 2023 10:24:35 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:24:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:24:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:24:40 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:24:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:24:40 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:24:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:24:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:24:40 GMT
USER odoo
# Wed, 16 Aug 2023 10:24:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:24:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94b5ed49a5ec953e83f40169b949808c407c931aa7085a46846902af681137`  
		Last Modified: Wed, 16 Aug 2023 10:27:04 GMT  
		Size: 213.2 MB (213180563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc841b610acfd62afebf8a7dee73883ec3020b5a503100b4b133df781a3bd04d`  
		Last Modified: Wed, 16 Aug 2023 10:26:44 GMT  
		Size: 13.5 MB (13522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497179ab34d276ead4cb01db777028bf342b2339f9089021ec71d1791a5da458`  
		Last Modified: Wed, 16 Aug 2023 10:26:42 GMT  
		Size: 458.9 KB (458875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629762765f62a57e2712dc0b2971d95262e6a755cfcdb73e4c54425a95d3462`  
		Last Modified: Wed, 16 Aug 2023 10:27:11 GMT  
		Size: 278.7 MB (278707230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b78af048060cb3d2885c1175f34a1da145c49f71b7394b44e7dab5a2d1b44da`  
		Last Modified: Wed, 16 Aug 2023 10:26:40 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5dfdf687922ba004bb872ca57349f5228c3ae0e82b860db3e0e9325fa2eab`  
		Last Modified: Wed, 16 Aug 2023 10:26:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67fcd724ef8fc73845f1bf3ffff145b1d8677f1d8fe1983723454b1f127a09`  
		Last Modified: Wed, 16 Aug 2023 10:26:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be5281bfbac37eca005b82bf848c0451308c37c81382d2e3e68aff9ef3241ae`  
		Last Modified: Wed, 16 Aug 2023 10:26:39 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:e66b80ceef1d5198cbe7b18608eee0623dc49a2f9a55a742495ec80eee86c61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:4d3f6136e6a057f510e050784231f42fc7b67d75f646b4e9af7f7e4bdc99c7b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533059231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1394603f893de212ff23bba7816b47d5a9954cec6de1640fe80064a8ea82b120`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:21:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:21:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:21:48 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:23:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:23:15 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:23:17 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:23:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 16 Aug 2023 10:23:17 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:23:17 GMT
ARG ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
# Wed, 16 Aug 2023 10:24:35 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:24:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:24:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:24:40 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=be9981c45465cdbd211406d91941d23786ec1e85
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:24:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:24:40 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:24:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:24:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:24:40 GMT
USER odoo
# Wed, 16 Aug 2023 10:24:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:24:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94b5ed49a5ec953e83f40169b949808c407c931aa7085a46846902af681137`  
		Last Modified: Wed, 16 Aug 2023 10:27:04 GMT  
		Size: 213.2 MB (213180563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc841b610acfd62afebf8a7dee73883ec3020b5a503100b4b133df781a3bd04d`  
		Last Modified: Wed, 16 Aug 2023 10:26:44 GMT  
		Size: 13.5 MB (13522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497179ab34d276ead4cb01db777028bf342b2339f9089021ec71d1791a5da458`  
		Last Modified: Wed, 16 Aug 2023 10:26:42 GMT  
		Size: 458.9 KB (458875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629762765f62a57e2712dc0b2971d95262e6a755cfcdb73e4c54425a95d3462`  
		Last Modified: Wed, 16 Aug 2023 10:27:11 GMT  
		Size: 278.7 MB (278707230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b78af048060cb3d2885c1175f34a1da145c49f71b7394b44e7dab5a2d1b44da`  
		Last Modified: Wed, 16 Aug 2023 10:26:40 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e5dfdf687922ba004bb872ca57349f5228c3ae0e82b860db3e0e9325fa2eab`  
		Last Modified: Wed, 16 Aug 2023 10:26:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67fcd724ef8fc73845f1bf3ffff145b1d8677f1d8fe1983723454b1f127a09`  
		Last Modified: Wed, 16 Aug 2023 10:26:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be5281bfbac37eca005b82bf848c0451308c37c81382d2e3e68aff9ef3241ae`  
		Last Modified: Wed, 16 Aug 2023 10:26:39 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:ce7f44c901c1dbe6327a809730371831d68cbec6ae276750d49b5fc3c8c6c9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ed34ab114a9e1aa2d53ae47b85ae7e0325627a11a2824d746fe7bfbdc39b9f28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562071143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83d7003acead3da54a196620d5c22fbf7d68e1fc5c32cda5171cc3142f0b96f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:20:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:20:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:20:23 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:20:24 GMT
ENV ODOO_VERSION=15.0
# Wed, 16 Aug 2023 10:20:24 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:20:24 GMT
ARG ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
# Wed, 16 Aug 2023 10:21:34 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:21:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:21:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:21:38 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:21:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:21:39 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:21:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:21:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:21:39 GMT
USER odoo
# Wed, 16 Aug 2023 10:21:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:21:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18e6ccd242f394f129dfb1542a55693c092efc01323daf560f2cea9f7c93f9d`  
		Last Modified: Wed, 16 Aug 2023 10:26:21 GMT  
		Size: 220.3 MB (220302753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8225239de85406993faad4ed5848d1f01aadf58ffcb88de9ba6cbee36f6eff`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 2.6 MB (2576533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf486b5a74cf8335fb645fe6c165ce01e7422386abffef6f5874c9353e969af6`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 454.4 KB (454433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a71f038d125afa4465309006c37c4b665982a8a43b08bb218fe399a702a009`  
		Last Modified: Wed, 16 Aug 2023 10:26:30 GMT  
		Size: 307.3 MB (307317284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5971b677aa9e3f0389fc37c4a16efc1ac94f1899c899126edb4d2ab880c6b51`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3cc080c327bd8e117e6d91812095d0b71f255ec663659dad60da07df3aa2a0`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d5ceb4c97bdf3bbc55d846509b1c3522f352280bfd91fe091bfce78e2a1ea2`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009f27c862dcdf0cddcbc38847451cbb52b08af63f9616897906a5e9593ec299`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:ce7f44c901c1dbe6327a809730371831d68cbec6ae276750d49b5fc3c8c6c9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ed34ab114a9e1aa2d53ae47b85ae7e0325627a11a2824d746fe7bfbdc39b9f28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562071143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83d7003acead3da54a196620d5c22fbf7d68e1fc5c32cda5171cc3142f0b96f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:20:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:20:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:20:23 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:20:24 GMT
ENV ODOO_VERSION=15.0
# Wed, 16 Aug 2023 10:20:24 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:20:24 GMT
ARG ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
# Wed, 16 Aug 2023 10:21:34 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:21:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:21:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:21:38 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=3d0566a191c0bd923846da38195d719c4779e727
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:21:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:21:39 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:21:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:21:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:21:39 GMT
USER odoo
# Wed, 16 Aug 2023 10:21:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:21:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18e6ccd242f394f129dfb1542a55693c092efc01323daf560f2cea9f7c93f9d`  
		Last Modified: Wed, 16 Aug 2023 10:26:21 GMT  
		Size: 220.3 MB (220302753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8225239de85406993faad4ed5848d1f01aadf58ffcb88de9ba6cbee36f6eff`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 2.6 MB (2576533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf486b5a74cf8335fb645fe6c165ce01e7422386abffef6f5874c9353e969af6`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 454.4 KB (454433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a71f038d125afa4465309006c37c4b665982a8a43b08bb218fe399a702a009`  
		Last Modified: Wed, 16 Aug 2023 10:26:30 GMT  
		Size: 307.3 MB (307317284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5971b677aa9e3f0389fc37c4a16efc1ac94f1899c899126edb4d2ab880c6b51`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3cc080c327bd8e117e6d91812095d0b71f255ec663659dad60da07df3aa2a0`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d5ceb4c97bdf3bbc55d846509b1c3522f352280bfd91fe091bfce78e2a1ea2`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009f27c862dcdf0cddcbc38847451cbb52b08af63f9616897906a5e9593ec299`  
		Last Modified: Wed, 16 Aug 2023 10:25:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:890817d2a3399096018cf50d37d28eb4c598634e6adc7520ae45d37f89a61813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:31e97f043fe6a1f9c5bda2339999a39a4ac04db03b57c01d32dd913b63cbaa7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575978269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9a4a7fac41506a0a2afd25a0329d04c655db96f4d0194ec1d777ae05dbb78d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 16 Aug 2023 10:17:44 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:17:45 GMT
ARG ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
# Wed, 16 Aug 2023 10:19:03 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:19:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:19:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:19:09 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:19:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:19:09 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:19:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:19:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:19:09 GMT
USER odoo
# Wed, 16 Aug 2023 10:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:19:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5456e32faf05cfb77b6e44a21ac706f83dede80c7f7589bb5814e7e524d319a4`  
		Last Modified: Wed, 16 Aug 2023 10:25:42 GMT  
		Size: 320.5 MB (320531299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb16dda58c6ea1e517fba59ac34a151652bbecb75a2b6003b29c9d9f041d8c1f`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e196af8086b55f33afa76f48327dc64fecc4476ac1f08410bd893a82d3b073a8`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd94e3fe6732d466d02b3393c2671b12c2d69a285282d588f6f20fa654ff2a20`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24fb3488eb6ac36cb3b85e1cdb8a4fd23c63dcc38dc1d0f574b8758111f629`  
		Last Modified: Wed, 16 Aug 2023 10:25:06 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:890817d2a3399096018cf50d37d28eb4c598634e6adc7520ae45d37f89a61813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:31e97f043fe6a1f9c5bda2339999a39a4ac04db03b57c01d32dd913b63cbaa7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575978269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9a4a7fac41506a0a2afd25a0329d04c655db96f4d0194ec1d777ae05dbb78d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 16 Aug 2023 10:17:44 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:17:45 GMT
ARG ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
# Wed, 16 Aug 2023 10:19:03 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:19:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:19:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:19:09 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:19:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:19:09 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:19:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:19:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:19:09 GMT
USER odoo
# Wed, 16 Aug 2023 10:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:19:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5456e32faf05cfb77b6e44a21ac706f83dede80c7f7589bb5814e7e524d319a4`  
		Last Modified: Wed, 16 Aug 2023 10:25:42 GMT  
		Size: 320.5 MB (320531299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb16dda58c6ea1e517fba59ac34a151652bbecb75a2b6003b29c9d9f041d8c1f`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e196af8086b55f33afa76f48327dc64fecc4476ac1f08410bd893a82d3b073a8`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd94e3fe6732d466d02b3393c2671b12c2d69a285282d588f6f20fa654ff2a20`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24fb3488eb6ac36cb3b85e1cdb8a4fd23c63dcc38dc1d0f574b8758111f629`  
		Last Modified: Wed, 16 Aug 2023 10:25:06 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:890817d2a3399096018cf50d37d28eb4c598634e6adc7520ae45d37f89a61813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:31e97f043fe6a1f9c5bda2339999a39a4ac04db03b57c01d32dd913b63cbaa7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575978269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9a4a7fac41506a0a2afd25a0329d04c655db96f4d0194ec1d777ae05dbb78d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 16 Aug 2023 10:17:44 GMT
ARG ODOO_RELEASE=20230807
# Wed, 16 Aug 2023 10:17:45 GMT
ARG ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
# Wed, 16 Aug 2023 10:19:03 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 16 Aug 2023 10:19:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 16 Aug 2023 10:19:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 16 Aug 2023 10:19:09 GMT
# ARGS: ODOO_RELEASE=20230807 ODOO_SHA=648042fc38a4f0021ad180e1bccbbe77a5c80c2c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 16 Aug 2023 10:19:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 16 Aug 2023 10:19:09 GMT
EXPOSE 8069 8071 8072
# Wed, 16 Aug 2023 10:19:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 16 Aug 2023 10:19:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 16 Aug 2023 10:19:09 GMT
USER odoo
# Wed, 16 Aug 2023 10:19:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 10:19:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5456e32faf05cfb77b6e44a21ac706f83dede80c7f7589bb5814e7e524d319a4`  
		Last Modified: Wed, 16 Aug 2023 10:25:42 GMT  
		Size: 320.5 MB (320531299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb16dda58c6ea1e517fba59ac34a151652bbecb75a2b6003b29c9d9f041d8c1f`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e196af8086b55f33afa76f48327dc64fecc4476ac1f08410bd893a82d3b073a8`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd94e3fe6732d466d02b3393c2671b12c2d69a285282d588f6f20fa654ff2a20`  
		Last Modified: Wed, 16 Aug 2023 10:25:05 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f24fb3488eb6ac36cb3b85e1cdb8a4fd23c63dcc38dc1d0f574b8758111f629`  
		Last Modified: Wed, 16 Aug 2023 10:25:06 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
