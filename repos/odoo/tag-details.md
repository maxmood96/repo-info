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
$ docker pull odoo@sha256:d692630baf5908b4c30d38477b3d2e997c77e1fe6be36877b46ff781de2ee676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:ddaf682de2722486d57f40570035a5a5899c521e9315525fe5150adc13538aaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.2 MB (531215931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00414f1c83f2b94c7ebe04df2189ad0fa19ad09f14afe1e65ac04ff6fbb8d4d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:52:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:52:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:52:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:54:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:54:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:54:22 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:54:22 GMT
ENV ODOO_VERSION=14.0
# Fri, 02 Dec 2022 18:23:33 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:23:33 GMT
ARG ODOO_SHA=41a75eecbf06b0adfc5537a476e406d28557f938
# Fri, 02 Dec 2022 18:24:58 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=41a75eecbf06b0adfc5537a476e406d28557f938
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:25:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:25:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:25:02 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=41a75eecbf06b0adfc5537a476e406d28557f938
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:25:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:25:02 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:25:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:25:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:25:03 GMT
USER odoo
# Fri, 02 Dec 2022 18:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:25:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b34b977d9e2c14944e351d9e8090d5360032ae3196bf76c9426aee15b5242`  
		Last Modified: Tue, 15 Nov 2022 14:58:04 GMT  
		Size: 213.2 MB (213185691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba36b7486e11dd53416493de75e4889858b80b3e79a5db728c39a06d005c67a`  
		Last Modified: Tue, 15 Nov 2022 14:57:42 GMT  
		Size: 13.5 MB (13515122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574226e6811aa978fe2238c06ed2681ca26ad2af45ff4a66459051ad5956fbf7`  
		Last Modified: Tue, 15 Nov 2022 14:57:40 GMT  
		Size: 454.3 KB (454333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe45bbb253b3c3507ed8d1dfa33534dd94cc6a5858364fde12a33ec41a9fc77`  
		Last Modified: Fri, 02 Dec 2022 18:27:26 GMT  
		Size: 276.9 MB (276917990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f62e338a2eec95ad51270ecc9f1c5f606365c71caaf931373c2be45fa60354`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba984c2c3951a8211ac5dbf4bc31f3f6417b05bcd4332a918f66bfae1046ea`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2bfd72c683f95bf482f5c932739c04e6bca4e7fede3db262c1cf8f578117f8`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791d5ce70ad5118915017f7784c0da34c6d8a852231d25630237660d72b5001c`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:d692630baf5908b4c30d38477b3d2e997c77e1fe6be36877b46ff781de2ee676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:ddaf682de2722486d57f40570035a5a5899c521e9315525fe5150adc13538aaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.2 MB (531215931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00414f1c83f2b94c7ebe04df2189ad0fa19ad09f14afe1e65ac04ff6fbb8d4d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:52:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:52:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:52:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:54:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:54:19 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:54:22 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:54:22 GMT
ENV ODOO_VERSION=14.0
# Fri, 02 Dec 2022 18:23:33 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:23:33 GMT
ARG ODOO_SHA=41a75eecbf06b0adfc5537a476e406d28557f938
# Fri, 02 Dec 2022 18:24:58 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=41a75eecbf06b0adfc5537a476e406d28557f938
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:25:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:25:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:25:02 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=41a75eecbf06b0adfc5537a476e406d28557f938
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:25:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:25:02 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:25:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:25:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:25:03 GMT
USER odoo
# Fri, 02 Dec 2022 18:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:25:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832b34b977d9e2c14944e351d9e8090d5360032ae3196bf76c9426aee15b5242`  
		Last Modified: Tue, 15 Nov 2022 14:58:04 GMT  
		Size: 213.2 MB (213185691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba36b7486e11dd53416493de75e4889858b80b3e79a5db728c39a06d005c67a`  
		Last Modified: Tue, 15 Nov 2022 14:57:42 GMT  
		Size: 13.5 MB (13515122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574226e6811aa978fe2238c06ed2681ca26ad2af45ff4a66459051ad5956fbf7`  
		Last Modified: Tue, 15 Nov 2022 14:57:40 GMT  
		Size: 454.3 KB (454333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe45bbb253b3c3507ed8d1dfa33534dd94cc6a5858364fde12a33ec41a9fc77`  
		Last Modified: Fri, 02 Dec 2022 18:27:26 GMT  
		Size: 276.9 MB (276917990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f62e338a2eec95ad51270ecc9f1c5f606365c71caaf931373c2be45fa60354`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba984c2c3951a8211ac5dbf4bc31f3f6417b05bcd4332a918f66bfae1046ea`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2bfd72c683f95bf482f5c932739c04e6bca4e7fede3db262c1cf8f578117f8`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791d5ce70ad5118915017f7784c0da34c6d8a852231d25630237660d72b5001c`  
		Last Modified: Fri, 02 Dec 2022 18:26:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:15cdeb01b2d20d1ad853720a10b8c28cbfb8af6bc958194d2af49c1d7905949a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:0a32dcf60de15b6e471f7bc9120d4eeedd95352bc586b52c0caade58c6daadf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.3 MB (559257696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37c5533308478a0d1c7b89f90154f68c8a5dc9b5dd841e02a4f994863d34ec1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:51:06 GMT
ENV ODOO_VERSION=15.0
# Fri, 02 Dec 2022 18:21:55 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:21:55 GMT
ARG ODOO_SHA=d0ee50281624260267085ee90302d1fe422eebbb
# Fri, 02 Dec 2022 18:23:11 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=d0ee50281624260267085ee90302d1fe422eebbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:23:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:23:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:23:16 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=d0ee50281624260267085ee90302d1fe422eebbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:23:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:23:16 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:23:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:23:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:23:16 GMT
USER odoo
# Fri, 02 Dec 2022 18:23:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:23:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503a65eaa3124df6506165627789c6b5f9c098f57233037871070bd7a71987bd`  
		Last Modified: Fri, 02 Dec 2022 18:26:45 GMT  
		Size: 304.5 MB (304517830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e1a8133734a0c0c4b670d3f4bc402bfe3d371e11156033b509e377faf038f0`  
		Last Modified: Fri, 02 Dec 2022 18:26:09 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd7540699b0aac01577bfe7b1d0c53a45043e4cb5e35c90191d5b02fc3f8e7`  
		Last Modified: Fri, 02 Dec 2022 18:26:10 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2bf449e7298ef4aadd58394d74d8705b27a3706985430935a2c072e478b001`  
		Last Modified: Fri, 02 Dec 2022 18:26:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954f2d490633656f30d5fc77f23fb3c4b1343048a2307b34357702921700d067`  
		Last Modified: Fri, 02 Dec 2022 18:26:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:15cdeb01b2d20d1ad853720a10b8c28cbfb8af6bc958194d2af49c1d7905949a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:0a32dcf60de15b6e471f7bc9120d4eeedd95352bc586b52c0caade58c6daadf4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.3 MB (559257696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37c5533308478a0d1c7b89f90154f68c8a5dc9b5dd841e02a4f994863d34ec1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:51:06 GMT
ENV ODOO_VERSION=15.0
# Fri, 02 Dec 2022 18:21:55 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:21:55 GMT
ARG ODOO_SHA=d0ee50281624260267085ee90302d1fe422eebbb
# Fri, 02 Dec 2022 18:23:11 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=d0ee50281624260267085ee90302d1fe422eebbb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:23:15 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:23:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:23:16 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=d0ee50281624260267085ee90302d1fe422eebbb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:23:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:23:16 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:23:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:23:16 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:23:16 GMT
USER odoo
# Fri, 02 Dec 2022 18:23:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:23:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503a65eaa3124df6506165627789c6b5f9c098f57233037871070bd7a71987bd`  
		Last Modified: Fri, 02 Dec 2022 18:26:45 GMT  
		Size: 304.5 MB (304517830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e1a8133734a0c0c4b670d3f4bc402bfe3d371e11156033b509e377faf038f0`  
		Last Modified: Fri, 02 Dec 2022 18:26:09 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bd7540699b0aac01577bfe7b1d0c53a45043e4cb5e35c90191d5b02fc3f8e7`  
		Last Modified: Fri, 02 Dec 2022 18:26:10 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2bf449e7298ef4aadd58394d74d8705b27a3706985430935a2c072e478b001`  
		Last Modified: Fri, 02 Dec 2022 18:26:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954f2d490633656f30d5fc77f23fb3c4b1343048a2307b34357702921700d067`  
		Last Modified: Fri, 02 Dec 2022 18:26:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:b0a97485e9abf64cfdd663ad588b74cc1a49b13b3748034abc7521e56e880d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:8483d8c83fb3e843ddda1fac2310fab1e0fffaac1fb5afba22221e46674e2860
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.9 MB (561935942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad2c8f54238cbfb9c4d680660dd9e124c2e09f2763757c4c03b0048df0ce037`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:49:31 GMT
ENV ODOO_VERSION=16.0
# Fri, 02 Dec 2022 18:20:17 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:20:17 GMT
ARG ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
# Fri, 02 Dec 2022 18:21:40 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:21:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:21:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:21:45 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:21:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:21:46 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:21:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:21:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:21:46 GMT
USER odoo
# Fri, 02 Dec 2022 18:21:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:21:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf0070c399591f237356b22256817958cb65ec6ec7f9bc3e94442c7e220ae07`  
		Last Modified: Fri, 02 Dec 2022 18:25:58 GMT  
		Size: 307.2 MB (307196075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a8ac51aa6590cb628a95b8650f9e7af295f973609d4456f163d98942db558`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c32aaa640d6a252d5506b372ff47e50b30a0802050ea6f4335448ff01e9dd8`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6c457007bda727c643fce92b52ad2bc964bfca93204f97b57fc200d35fac81`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e4e46fab8ea14c330a1dcb69c96878a1a2fcf44efae27fde4e93942de76287`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:b0a97485e9abf64cfdd663ad588b74cc1a49b13b3748034abc7521e56e880d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:8483d8c83fb3e843ddda1fac2310fab1e0fffaac1fb5afba22221e46674e2860
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.9 MB (561935942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad2c8f54238cbfb9c4d680660dd9e124c2e09f2763757c4c03b0048df0ce037`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:49:31 GMT
ENV ODOO_VERSION=16.0
# Fri, 02 Dec 2022 18:20:17 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:20:17 GMT
ARG ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
# Fri, 02 Dec 2022 18:21:40 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:21:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:21:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:21:45 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:21:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:21:46 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:21:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:21:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:21:46 GMT
USER odoo
# Fri, 02 Dec 2022 18:21:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:21:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf0070c399591f237356b22256817958cb65ec6ec7f9bc3e94442c7e220ae07`  
		Last Modified: Fri, 02 Dec 2022 18:25:58 GMT  
		Size: 307.2 MB (307196075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a8ac51aa6590cb628a95b8650f9e7af295f973609d4456f163d98942db558`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c32aaa640d6a252d5506b372ff47e50b30a0802050ea6f4335448ff01e9dd8`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6c457007bda727c643fce92b52ad2bc964bfca93204f97b57fc200d35fac81`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e4e46fab8ea14c330a1dcb69c96878a1a2fcf44efae27fde4e93942de76287`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:b0a97485e9abf64cfdd663ad588b74cc1a49b13b3748034abc7521e56e880d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8483d8c83fb3e843ddda1fac2310fab1e0fffaac1fb5afba22221e46674e2860
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.9 MB (561935942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad2c8f54238cbfb9c4d680660dd9e124c2e09f2763757c4c03b0048df0ce037`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Nov 2022 14:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Nov 2022 14:47:58 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:49:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 15 Nov 2022 14:49:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:49:31 GMT
RUN npm install -g rtlcss
# Tue, 15 Nov 2022 14:49:31 GMT
ENV ODOO_VERSION=16.0
# Fri, 02 Dec 2022 18:20:17 GMT
ARG ODOO_RELEASE=20221202
# Fri, 02 Dec 2022 18:20:17 GMT
ARG ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
# Fri, 02 Dec 2022 18:21:40 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 02 Dec 2022 18:21:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 02 Dec 2022 18:21:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 02 Dec 2022 18:21:45 GMT
# ARGS: ODOO_RELEASE=20221202 ODOO_SHA=3ffc37e18490c281cae46fc5cb52edbf7e41738a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 02 Dec 2022 18:21:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 02 Dec 2022 18:21:46 GMT
EXPOSE 8069 8071 8072
# Fri, 02 Dec 2022 18:21:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 02 Dec 2022 18:21:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 02 Dec 2022 18:21:46 GMT
USER odoo
# Fri, 02 Dec 2022 18:21:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Dec 2022 18:21:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b89c925f079bb8ba18a9f6d5c8f0894d0524b6b2ef1540d8fd8507d363b8a`  
		Last Modified: Tue, 15 Nov 2022 14:56:35 GMT  
		Size: 220.3 MB (220299738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e6839b17eaee38e74eb0dcfde7e4cbb4be23b04003070bebfdb4f4bdc8baa`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 2.6 MB (2574749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dbd3426fec007142c2f160a56383779f3735b1cdf9b37d83e9e192721eeef6`  
		Last Modified: Tue, 15 Nov 2022 14:56:08 GMT  
		Size: 450.3 KB (450290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf0070c399591f237356b22256817958cb65ec6ec7f9bc3e94442c7e220ae07`  
		Last Modified: Fri, 02 Dec 2022 18:25:58 GMT  
		Size: 307.2 MB (307196075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a8ac51aa6590cb628a95b8650f9e7af295f973609d4456f163d98942db558`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c32aaa640d6a252d5506b372ff47e50b30a0802050ea6f4335448ff01e9dd8`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6c457007bda727c643fce92b52ad2bc964bfca93204f97b57fc200d35fac81`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e4e46fab8ea14c330a1dcb69c96878a1a2fcf44efae27fde4e93942de76287`  
		Last Modified: Fri, 02 Dec 2022 18:25:23 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
