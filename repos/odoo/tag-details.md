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
$ docker pull odoo@sha256:ed873be56b8a10cf1b85477f00cdff90cd83bcdf122c527f097e4670e850ff23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:4a066f04fb4e7845d535ccec8a40e1333edc48515bc06945d54f29b443994c1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532353697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f02b4f98ec52a452f8828a4a1acdefeeb3b2795eb12f21ef1eeeb700aef883c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:15:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:15:59 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:17:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:17:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:17:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:17:55 GMT
ENV ODOO_VERSION=14.0
# Wed, 03 May 2023 22:17:55 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:17:55 GMT
ARG ODOO_SHA=06586ebb9902fa4840fb177f5e45f98d19dadf6d
# Wed, 03 May 2023 22:19:09 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=06586ebb9902fa4840fb177f5e45f98d19dadf6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:19:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:19:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:19:13 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=06586ebb9902fa4840fb177f5e45f98d19dadf6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:19:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:19:13 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:19:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:19:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:19:14 GMT
USER odoo
# Wed, 03 May 2023 22:19:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:19:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6dd9f7291fd1715775d3df086275131f79ffab649903727cf75d8bcd307f8b2`  
		Last Modified: Wed, 03 May 2023 22:21:22 GMT  
		Size: 213.2 MB (213205338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9129e7deaeb62a539efccc985e7c3e17f71b12a755cd5275ae935ca6ed83cc0f`  
		Last Modified: Wed, 03 May 2023 22:21:02 GMT  
		Size: 13.5 MB (13517741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692f23029abeb79991ccf387069946d3eb1e3aafd13a77b6d20d563a53aa75f`  
		Last Modified: Wed, 03 May 2023 22:20:59 GMT  
		Size: 456.8 KB (456827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb9734b40d3b713ca1341afcc9aa31c07bafa68b779997d70bf75dc04032afc`  
		Last Modified: Wed, 03 May 2023 22:21:29 GMT  
		Size: 278.0 MB (278032368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29d0e7a899f6ee2adaa5e10bd7aa82e12595a6b7efd9b62eb4aec5f658a630e`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f746a8e76b85311da9d7edee919881caba881fe423b61c17ea337c0e906080`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fdf6dbbc721353a1ae8cdef20ce0b3897274b206eb5503e67128a1ac3fc305`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a4f7d708108da13fae15490bfa2c93eec4ad442468f5e2759d1f4fb35d38a4`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:ed873be56b8a10cf1b85477f00cdff90cd83bcdf122c527f097e4670e850ff23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:4a066f04fb4e7845d535ccec8a40e1333edc48515bc06945d54f29b443994c1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.4 MB (532353697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f02b4f98ec52a452f8828a4a1acdefeeb3b2795eb12f21ef1eeeb700aef883c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:47:16 GMT
ADD file:00bc0eda6d2eb0f8ad4abc654f762ffb9ec7e8d1c95d0cc0e7d0cba176d33e27 in / 
# Tue, 02 May 2023 23:47:17 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:15:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:15:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:15:59 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:17:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:17:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:17:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:17:55 GMT
ENV ODOO_VERSION=14.0
# Wed, 03 May 2023 22:17:55 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:17:55 GMT
ARG ODOO_SHA=06586ebb9902fa4840fb177f5e45f98d19dadf6d
# Wed, 03 May 2023 22:19:09 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=06586ebb9902fa4840fb177f5e45f98d19dadf6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:19:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:19:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:19:13 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=06586ebb9902fa4840fb177f5e45f98d19dadf6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:19:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:19:13 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:19:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:19:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:19:14 GMT
USER odoo
# Wed, 03 May 2023 22:19:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:19:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:25ff99d195814e98b7ef4708519299d9f177def504f9b718c61eb82c7f0b34be`  
		Last Modified: Tue, 02 May 2023 23:51:01 GMT  
		Size: 27.1 MB (27138959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6dd9f7291fd1715775d3df086275131f79ffab649903727cf75d8bcd307f8b2`  
		Last Modified: Wed, 03 May 2023 22:21:22 GMT  
		Size: 213.2 MB (213205338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9129e7deaeb62a539efccc985e7c3e17f71b12a755cd5275ae935ca6ed83cc0f`  
		Last Modified: Wed, 03 May 2023 22:21:02 GMT  
		Size: 13.5 MB (13517741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a692f23029abeb79991ccf387069946d3eb1e3aafd13a77b6d20d563a53aa75f`  
		Last Modified: Wed, 03 May 2023 22:20:59 GMT  
		Size: 456.8 KB (456827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb9734b40d3b713ca1341afcc9aa31c07bafa68b779997d70bf75dc04032afc`  
		Last Modified: Wed, 03 May 2023 22:21:29 GMT  
		Size: 278.0 MB (278032368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29d0e7a899f6ee2adaa5e10bd7aa82e12595a6b7efd9b62eb4aec5f658a630e`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f746a8e76b85311da9d7edee919881caba881fe423b61c17ea337c0e906080`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fdf6dbbc721353a1ae8cdef20ce0b3897274b206eb5503e67128a1ac3fc305`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a4f7d708108da13fae15490bfa2c93eec4ad442468f5e2759d1f4fb35d38a4`  
		Last Modified: Wed, 03 May 2023 22:20:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:ff19587fb8a58cb0f823acf08a89cbbd1416448498cb818c28992c6fa336f7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:1809ba20abe186c8679e49d9ed1dc66532e3e7c588920ebf626dfc391bc9a295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560815309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bfd02716c2e16f3e1a75bd128e49cbaa02f75e9cdbe7bcc143a77c32ee86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:11:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:11:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:11:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:12:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:12:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:12:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:14:36 GMT
ENV ODOO_VERSION=15.0
# Wed, 03 May 2023 22:14:36 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:14:36 GMT
ARG ODOO_SHA=af1128e5d8126e079a968ec22696a122965a4404
# Wed, 03 May 2023 22:15:48 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=af1128e5d8126e079a968ec22696a122965a4404
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:15:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:15:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:15:52 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=af1128e5d8126e079a968ec22696a122965a4404
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:15:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:15:52 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:15:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:15:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:15:53 GMT
USER odoo
# Wed, 03 May 2023 22:15:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:15:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ba628d58ec2cec04d9a4bc73b4015a47d7707f4e4d1e9d92a40ce9c8ddcc66`  
		Last Modified: Wed, 03 May 2023 22:19:54 GMT  
		Size: 220.3 MB (220297784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc07b7d1cfb584aa1c510ede6794940b0d1e644d62606e436b92fd194198144`  
		Last Modified: Wed, 03 May 2023 22:19:30 GMT  
		Size: 2.6 MB (2575304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77a58f0a17b42f1032fbe1881c6d8711bdefa34afb5e985297f35f6c5e69b5`  
		Last Modified: Wed, 03 May 2023 22:19:29 GMT  
		Size: 452.2 KB (452241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ea0d0a168304660adc9f8f6ad6238a2c42ac8a185e761abd7f14b95621a00c`  
		Last Modified: Wed, 03 May 2023 22:20:48 GMT  
		Size: 306.1 MB (306084003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77686643c364d2c3a3995f4c81798824f9a82226ea14987d1bdae2f10b37a38d`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb80ad2d793a776ecaf615c7f5f618f03d6771cc249f2e9033199d90eb854d29`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf9bd3658dd050cc8e39a9214feb9c7b8a2d487e5eed4cf2be79b88e5126c13`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b8a78b8f68296957553b9a10a8c9e760efd387b05ad8686cde14296b903a3`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:ff19587fb8a58cb0f823acf08a89cbbd1416448498cb818c28992c6fa336f7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:1809ba20abe186c8679e49d9ed1dc66532e3e7c588920ebf626dfc391bc9a295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560815309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bfd02716c2e16f3e1a75bd128e49cbaa02f75e9cdbe7bcc143a77c32ee86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:11:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:11:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:11:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:12:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:12:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:12:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:14:36 GMT
ENV ODOO_VERSION=15.0
# Wed, 03 May 2023 22:14:36 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:14:36 GMT
ARG ODOO_SHA=af1128e5d8126e079a968ec22696a122965a4404
# Wed, 03 May 2023 22:15:48 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=af1128e5d8126e079a968ec22696a122965a4404
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:15:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:15:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:15:52 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=af1128e5d8126e079a968ec22696a122965a4404
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:15:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:15:52 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:15:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:15:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:15:53 GMT
USER odoo
# Wed, 03 May 2023 22:15:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:15:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ba628d58ec2cec04d9a4bc73b4015a47d7707f4e4d1e9d92a40ce9c8ddcc66`  
		Last Modified: Wed, 03 May 2023 22:19:54 GMT  
		Size: 220.3 MB (220297784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc07b7d1cfb584aa1c510ede6794940b0d1e644d62606e436b92fd194198144`  
		Last Modified: Wed, 03 May 2023 22:19:30 GMT  
		Size: 2.6 MB (2575304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77a58f0a17b42f1032fbe1881c6d8711bdefa34afb5e985297f35f6c5e69b5`  
		Last Modified: Wed, 03 May 2023 22:19:29 GMT  
		Size: 452.2 KB (452241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ea0d0a168304660adc9f8f6ad6238a2c42ac8a185e761abd7f14b95621a00c`  
		Last Modified: Wed, 03 May 2023 22:20:48 GMT  
		Size: 306.1 MB (306084003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77686643c364d2c3a3995f4c81798824f9a82226ea14987d1bdae2f10b37a38d`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb80ad2d793a776ecaf615c7f5f618f03d6771cc249f2e9033199d90eb854d29`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf9bd3658dd050cc8e39a9214feb9c7b8a2d487e5eed4cf2be79b88e5126c13`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2b8a78b8f68296957553b9a10a8c9e760efd387b05ad8686cde14296b903a3`  
		Last Modified: Wed, 03 May 2023 22:20:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:2e2ebbac337620116cd4000d7b8833ad1c296618a11b4e6a8f783a05a0f1215c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:d72f131d2719cdc171b7057bb47eefdaab2841dd25c45024c8254ed3d88be700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569627367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3e3639d93ff78bb635679fb408e88919d0cf8a1f14079823de89b03190a724`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:11:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:11:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:11:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:12:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:12:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:12:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:12:56 GMT
ENV ODOO_VERSION=16.0
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
# Wed, 03 May 2023 22:14:17 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:14:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:14:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:14:23 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:14:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:14:23 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:14:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:14:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:14:23 GMT
USER odoo
# Wed, 03 May 2023 22:14:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:14:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ba628d58ec2cec04d9a4bc73b4015a47d7707f4e4d1e9d92a40ce9c8ddcc66`  
		Last Modified: Wed, 03 May 2023 22:19:54 GMT  
		Size: 220.3 MB (220297784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc07b7d1cfb584aa1c510ede6794940b0d1e644d62606e436b92fd194198144`  
		Last Modified: Wed, 03 May 2023 22:19:30 GMT  
		Size: 2.6 MB (2575304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77a58f0a17b42f1032fbe1881c6d8711bdefa34afb5e985297f35f6c5e69b5`  
		Last Modified: Wed, 03 May 2023 22:19:29 GMT  
		Size: 452.2 KB (452241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91fc12cdc1288fd9654ba11e5c61b1d174f70692cc5b02bbf850127d9e20eb0`  
		Last Modified: Wed, 03 May 2023 22:20:04 GMT  
		Size: 314.9 MB (314896070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619983c05393da18859f1a59ff48254cb22a9dd04d291f1b066d922474745a7`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0c954a649b1db32a3011c78944731a7a7dc70b6fc85c657a12368d69072511`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e602314abc510f6f52e700d6d0b661bb35ae2a30e46d27bdb6205fa8e61c94`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c06d4c57624a3e3b070ae52f19b5273d9361584b8c4266f6238cf29ded33ef`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:2e2ebbac337620116cd4000d7b8833ad1c296618a11b4e6a8f783a05a0f1215c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:d72f131d2719cdc171b7057bb47eefdaab2841dd25c45024c8254ed3d88be700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569627367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3e3639d93ff78bb635679fb408e88919d0cf8a1f14079823de89b03190a724`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:11:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:11:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:11:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:12:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:12:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:12:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:12:56 GMT
ENV ODOO_VERSION=16.0
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
# Wed, 03 May 2023 22:14:17 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:14:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:14:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:14:23 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:14:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:14:23 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:14:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:14:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:14:23 GMT
USER odoo
# Wed, 03 May 2023 22:14:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:14:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ba628d58ec2cec04d9a4bc73b4015a47d7707f4e4d1e9d92a40ce9c8ddcc66`  
		Last Modified: Wed, 03 May 2023 22:19:54 GMT  
		Size: 220.3 MB (220297784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc07b7d1cfb584aa1c510ede6794940b0d1e644d62606e436b92fd194198144`  
		Last Modified: Wed, 03 May 2023 22:19:30 GMT  
		Size: 2.6 MB (2575304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77a58f0a17b42f1032fbe1881c6d8711bdefa34afb5e985297f35f6c5e69b5`  
		Last Modified: Wed, 03 May 2023 22:19:29 GMT  
		Size: 452.2 KB (452241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91fc12cdc1288fd9654ba11e5c61b1d174f70692cc5b02bbf850127d9e20eb0`  
		Last Modified: Wed, 03 May 2023 22:20:04 GMT  
		Size: 314.9 MB (314896070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619983c05393da18859f1a59ff48254cb22a9dd04d291f1b066d922474745a7`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0c954a649b1db32a3011c78944731a7a7dc70b6fc85c657a12368d69072511`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e602314abc510f6f52e700d6d0b661bb35ae2a30e46d27bdb6205fa8e61c94`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c06d4c57624a3e3b070ae52f19b5273d9361584b8c4266f6238cf29ded33ef`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:2e2ebbac337620116cd4000d7b8833ad1c296618a11b4e6a8f783a05a0f1215c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d72f131d2719cdc171b7057bb47eefdaab2841dd25c45024c8254ed3d88be700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569627367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3e3639d93ff78bb635679fb408e88919d0cf8a1f14079823de89b03190a724`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:11:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:11:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:11:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:12:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:12:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:12:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:12:56 GMT
ENV ODOO_VERSION=16.0
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
# Wed, 03 May 2023 22:14:17 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:14:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:14:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:14:23 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:14:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:14:23 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:14:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:14:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:14:23 GMT
USER odoo
# Wed, 03 May 2023 22:14:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:14:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ba628d58ec2cec04d9a4bc73b4015a47d7707f4e4d1e9d92a40ce9c8ddcc66`  
		Last Modified: Wed, 03 May 2023 22:19:54 GMT  
		Size: 220.3 MB (220297784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc07b7d1cfb584aa1c510ede6794940b0d1e644d62606e436b92fd194198144`  
		Last Modified: Wed, 03 May 2023 22:19:30 GMT  
		Size: 2.6 MB (2575304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77a58f0a17b42f1032fbe1881c6d8711bdefa34afb5e985297f35f6c5e69b5`  
		Last Modified: Wed, 03 May 2023 22:19:29 GMT  
		Size: 452.2 KB (452241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91fc12cdc1288fd9654ba11e5c61b1d174f70692cc5b02bbf850127d9e20eb0`  
		Last Modified: Wed, 03 May 2023 22:20:04 GMT  
		Size: 314.9 MB (314896070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619983c05393da18859f1a59ff48254cb22a9dd04d291f1b066d922474745a7`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0c954a649b1db32a3011c78944731a7a7dc70b6fc85c657a12368d69072511`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e602314abc510f6f52e700d6d0b661bb35ae2a30e46d27bdb6205fa8e61c94`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c06d4c57624a3e3b070ae52f19b5273d9361584b8c4266f6238cf29ded33ef`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
