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
$ docker pull odoo@sha256:27f72a02f120f3f362fa84be5b6b31bf1b276b39fbaad25c22a03237eba8e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:e7fd62d81ffd6a54d84b710304e606697bbb418a49a3aee509ff0e25b254e25c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533075105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d45af71eefcc1613a5b77e6b30928774f570c00ae33f7edc9195a9ada2419b2`
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
# Fri, 25 Aug 2023 19:29:10 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:29:10 GMT
ARG ODOO_SHA=b528e0a4b9e3924a04a76a50866412e8c000b0ef
# Fri, 25 Aug 2023 19:30:24 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=b528e0a4b9e3924a04a76a50866412e8c000b0ef
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:30:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:30:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:30:28 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=b528e0a4b9e3924a04a76a50866412e8c000b0ef
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:30:28 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:30:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:30:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:30:29 GMT
USER odoo
# Fri, 25 Aug 2023 19:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:30:29 GMT
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
	-	`sha256:98c9cc67ae5381e310298a4a7adab79b2775aa874440f6d6828beea86378851b`  
		Last Modified: Fri, 25 Aug 2023 19:32:42 GMT  
		Size: 278.7 MB (278723099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cace1365c90ffde15448b1159b94408eafcfdc29ad585d9fe52632fbd47078`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eea393e0b6a6cce2f0156f843b4a44c04cf44fc00b2a0a3a4e97a9b4c4a2df`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c075c4f62aa2b0c6e598365eacb8858fec280880110003fcabf845c6e7a09472`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33117d57cb9677baa24339127755c4f6635cbe369f80b6834714c0d8085fce7c`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:27f72a02f120f3f362fa84be5b6b31bf1b276b39fbaad25c22a03237eba8e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:e7fd62d81ffd6a54d84b710304e606697bbb418a49a3aee509ff0e25b254e25c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533075105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d45af71eefcc1613a5b77e6b30928774f570c00ae33f7edc9195a9ada2419b2`
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
# Fri, 25 Aug 2023 19:29:10 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:29:10 GMT
ARG ODOO_SHA=b528e0a4b9e3924a04a76a50866412e8c000b0ef
# Fri, 25 Aug 2023 19:30:24 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=b528e0a4b9e3924a04a76a50866412e8c000b0ef
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:30:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:30:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:30:28 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=b528e0a4b9e3924a04a76a50866412e8c000b0ef
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:30:28 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:30:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:30:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:30:29 GMT
USER odoo
# Fri, 25 Aug 2023 19:30:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:30:29 GMT
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
	-	`sha256:98c9cc67ae5381e310298a4a7adab79b2775aa874440f6d6828beea86378851b`  
		Last Modified: Fri, 25 Aug 2023 19:32:42 GMT  
		Size: 278.7 MB (278723099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cace1365c90ffde15448b1159b94408eafcfdc29ad585d9fe52632fbd47078`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eea393e0b6a6cce2f0156f843b4a44c04cf44fc00b2a0a3a4e97a9b4c4a2df`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c075c4f62aa2b0c6e598365eacb8858fec280880110003fcabf845c6e7a09472`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33117d57cb9677baa24339127755c4f6635cbe369f80b6834714c0d8085fce7c`  
		Last Modified: Fri, 25 Aug 2023 19:32:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:373683c0e662628326a498e6dacf5aab3f69b689a337050f58d4de734f2960c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:1fad39f2126a127d267e138c0fb4192b30808bcd33ef1f2ebea85d7b1986e5de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562135610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb27c8577d10588ff33e4e43c54d9c5b08f3418870cfa5ffa14acae3507a32e`
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
# Fri, 25 Aug 2023 19:27:47 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:27:47 GMT
ARG ODOO_SHA=29c8f49377b264ef1e9d1e12710ec530bcceeb06
# Fri, 25 Aug 2023 19:28:58 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=29c8f49377b264ef1e9d1e12710ec530bcceeb06
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:29:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:29:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:29:03 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=29c8f49377b264ef1e9d1e12710ec530bcceeb06
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:29:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:29:03 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:29:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:29:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:29:03 GMT
USER odoo
# Fri, 25 Aug 2023 19:29:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:29:04 GMT
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
	-	`sha256:6b5e2ab788778c934f8234e38c62ad2ff8f383210f1034b2a91ef675f696e861`  
		Last Modified: Fri, 25 Aug 2023 19:32:03 GMT  
		Size: 307.4 MB (307381746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1471c5b9ebc361c6d7bded7207a03ac81953b091eb8947a41a4e0231086dbdbc`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd4e91fd31314cf999d26a6602e0052908f10919f25d1bde9c476f0b47c489f`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821a58a60c087fbf27524c174717687912f38ce9bbb8c4fe2bb3d11dc06ae3d1`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d74c00ca2f1832b8ec69a830241a752e4988b9c3623fb662b3a1096032afde`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:373683c0e662628326a498e6dacf5aab3f69b689a337050f58d4de734f2960c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:1fad39f2126a127d267e138c0fb4192b30808bcd33ef1f2ebea85d7b1986e5de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562135610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb27c8577d10588ff33e4e43c54d9c5b08f3418870cfa5ffa14acae3507a32e`
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
# Fri, 25 Aug 2023 19:27:47 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:27:47 GMT
ARG ODOO_SHA=29c8f49377b264ef1e9d1e12710ec530bcceeb06
# Fri, 25 Aug 2023 19:28:58 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=29c8f49377b264ef1e9d1e12710ec530bcceeb06
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:29:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:29:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:29:03 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=29c8f49377b264ef1e9d1e12710ec530bcceeb06
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:29:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:29:03 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:29:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:29:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:29:03 GMT
USER odoo
# Fri, 25 Aug 2023 19:29:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:29:04 GMT
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
	-	`sha256:6b5e2ab788778c934f8234e38c62ad2ff8f383210f1034b2a91ef675f696e861`  
		Last Modified: Fri, 25 Aug 2023 19:32:03 GMT  
		Size: 307.4 MB (307381746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1471c5b9ebc361c6d7bded7207a03ac81953b091eb8947a41a4e0231086dbdbc`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd4e91fd31314cf999d26a6602e0052908f10919f25d1bde9c476f0b47c489f`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821a58a60c087fbf27524c174717687912f38ce9bbb8c4fe2bb3d11dc06ae3d1`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d74c00ca2f1832b8ec69a830241a752e4988b9c3623fb662b3a1096032afde`  
		Last Modified: Fri, 25 Aug 2023 19:31:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:bd3be7f3a763f6956bd797a601af0e3ccb5127d490cbb6a3b9b3f6edf4393f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:503f66fe4215cd6613ac52d9895b582c535addfe6a932f2763d377fcdaeee0bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.2 MB (576172103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5a3999f029304799aa9da16e5b3c6191886df8c1d2efaecd81d4b71cac86bb`
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
# Fri, 25 Aug 2023 19:26:08 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:26:08 GMT
ARG ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
# Fri, 25 Aug 2023 19:27:25 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:27:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:27:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:27:31 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:27:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:27:31 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:27:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:27:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:27:31 GMT
USER odoo
# Fri, 25 Aug 2023 19:27:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:27:31 GMT
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
	-	`sha256:21f97385ef2e87681e55a8041e3495249bc6e5b17d2a1fc56900aa70b03a973d`  
		Last Modified: Fri, 25 Aug 2023 19:31:19 GMT  
		Size: 320.7 MB (320725139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c8de29b2c967b21da0a89a4a020d60e087bd124f75b0ccd64b3085869f5bbd`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6eaf4a1bcff5d4f74935eb2ec468b988d3b52993b22f5d640b1403c1861867`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19315b38705faab17e9cfb211601f14420cf84069992489e1ab2e2f0afe333b`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7df32bb1d7f59a38e0f86f5eaef08b0387558dc1a966f9ef9383629a0ffae8a`  
		Last Modified: Fri, 25 Aug 2023 19:30:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:bd3be7f3a763f6956bd797a601af0e3ccb5127d490cbb6a3b9b3f6edf4393f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:503f66fe4215cd6613ac52d9895b582c535addfe6a932f2763d377fcdaeee0bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.2 MB (576172103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5a3999f029304799aa9da16e5b3c6191886df8c1d2efaecd81d4b71cac86bb`
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
# Fri, 25 Aug 2023 19:26:08 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:26:08 GMT
ARG ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
# Fri, 25 Aug 2023 19:27:25 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:27:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:27:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:27:31 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:27:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:27:31 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:27:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:27:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:27:31 GMT
USER odoo
# Fri, 25 Aug 2023 19:27:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:27:31 GMT
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
	-	`sha256:21f97385ef2e87681e55a8041e3495249bc6e5b17d2a1fc56900aa70b03a973d`  
		Last Modified: Fri, 25 Aug 2023 19:31:19 GMT  
		Size: 320.7 MB (320725139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c8de29b2c967b21da0a89a4a020d60e087bd124f75b0ccd64b3085869f5bbd`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6eaf4a1bcff5d4f74935eb2ec468b988d3b52993b22f5d640b1403c1861867`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19315b38705faab17e9cfb211601f14420cf84069992489e1ab2e2f0afe333b`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7df32bb1d7f59a38e0f86f5eaef08b0387558dc1a966f9ef9383629a0ffae8a`  
		Last Modified: Fri, 25 Aug 2023 19:30:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:bd3be7f3a763f6956bd797a601af0e3ccb5127d490cbb6a3b9b3f6edf4393f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:503f66fe4215cd6613ac52d9895b582c535addfe6a932f2763d377fcdaeee0bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.2 MB (576172103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5a3999f029304799aa9da16e5b3c6191886df8c1d2efaecd81d4b71cac86bb`
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
# Fri, 25 Aug 2023 19:26:08 GMT
ARG ODOO_RELEASE=20230825
# Fri, 25 Aug 2023 19:26:08 GMT
ARG ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
# Fri, 25 Aug 2023 19:27:25 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Aug 2023 19:27:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Aug 2023 19:27:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Aug 2023 19:27:31 GMT
# ARGS: ODOO_RELEASE=20230825 ODOO_SHA=12ce0c5d56051d71ec3d9d474b3f4694fdcae45a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Aug 2023 19:27:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Aug 2023 19:27:31 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Aug 2023 19:27:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Aug 2023 19:27:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Aug 2023 19:27:31 GMT
USER odoo
# Fri, 25 Aug 2023 19:27:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Aug 2023 19:27:31 GMT
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
	-	`sha256:21f97385ef2e87681e55a8041e3495249bc6e5b17d2a1fc56900aa70b03a973d`  
		Last Modified: Fri, 25 Aug 2023 19:31:19 GMT  
		Size: 320.7 MB (320725139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c8de29b2c967b21da0a89a4a020d60e087bd124f75b0ccd64b3085869f5bbd`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6eaf4a1bcff5d4f74935eb2ec468b988d3b52993b22f5d640b1403c1861867`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19315b38705faab17e9cfb211601f14420cf84069992489e1ab2e2f0afe333b`  
		Last Modified: Fri, 25 Aug 2023 19:30:41 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7df32bb1d7f59a38e0f86f5eaef08b0387558dc1a966f9ef9383629a0ffae8a`  
		Last Modified: Fri, 25 Aug 2023 19:30:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
