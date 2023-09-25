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
$ docker pull odoo@sha256:92765e6973c10b09a6dd9aee4be235518cb8b25309d40a574726949bf7d93216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:4a27d15282aa8403e75f63cee0fc17773d25a7c1d00debf247103491c405f143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.3 MB (533292553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163c29234f5d95afe5579e7ce1f29f96cdb94ad41b1aee98f5c987ea157ea2ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:10:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:10:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:10:35 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:11:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:12:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:12:13 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:12:13 GMT
ENV ODOO_VERSION=14.0
# Mon, 25 Sep 2023 22:27:59 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:27:59 GMT
ARG ODOO_SHA=b7622d939c7135e693d498aec22a21638616bfee
# Mon, 25 Sep 2023 22:29:14 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=b7622d939c7135e693d498aec22a21638616bfee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:29:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:29:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:29:18 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=b7622d939c7135e693d498aec22a21638616bfee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:29:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:29:18 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:29:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:29:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:29:18 GMT
USER odoo
# Mon, 25 Sep 2023 22:29:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:29:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c00cc67825184a50f8ac124275cd02e1cfe225202df2b8529a89b347f17fc`  
		Last Modified: Wed, 20 Sep 2023 17:15:52 GMT  
		Size: 213.2 MB (213177221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e38b6ee0418a568b6723031ee851c0255648d189062f7a34cd082738a5a1da`  
		Last Modified: Wed, 20 Sep 2023 17:15:31 GMT  
		Size: 13.6 MB (13567689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41556b9b524d52ec328e6b0ee7c21deedf8aed8e3e61bae271a9d58162ecaa84`  
		Last Modified: Wed, 20 Sep 2023 17:15:29 GMT  
		Size: 460.0 KB (459973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bcab3789a0a2d428eaf79d0614e6689a83d23fe92e21739594dbef4ac04d76`  
		Last Modified: Mon, 25 Sep 2023 22:31:32 GMT  
		Size: 278.9 MB (278897794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a25a06f1d456434a716a1c72de010b3e9900487d5f3a9588b0ebdb38b253ea8`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5e1e8ec6e9360c01de60dab75a4f9fdb6332c4984a65ac5a949a1093316270`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5ff43b733417167eec575f27eb7cea33a13a948c6a5d104ab734dc95eda2c6`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151561246ce03ae4eaa79d4b80a9044013fb974528eca442bf95355551c026ef`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:92765e6973c10b09a6dd9aee4be235518cb8b25309d40a574726949bf7d93216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:4a27d15282aa8403e75f63cee0fc17773d25a7c1d00debf247103491c405f143
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.3 MB (533292553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163c29234f5d95afe5579e7ce1f29f96cdb94ad41b1aee98f5c987ea157ea2ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:10:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:10:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:10:35 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:11:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:12:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:12:13 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:12:13 GMT
ENV ODOO_VERSION=14.0
# Mon, 25 Sep 2023 22:27:59 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:27:59 GMT
ARG ODOO_SHA=b7622d939c7135e693d498aec22a21638616bfee
# Mon, 25 Sep 2023 22:29:14 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=b7622d939c7135e693d498aec22a21638616bfee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:29:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:29:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:29:18 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=b7622d939c7135e693d498aec22a21638616bfee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:29:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:29:18 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:29:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:29:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:29:18 GMT
USER odoo
# Mon, 25 Sep 2023 22:29:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:29:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2c00cc67825184a50f8ac124275cd02e1cfe225202df2b8529a89b347f17fc`  
		Last Modified: Wed, 20 Sep 2023 17:15:52 GMT  
		Size: 213.2 MB (213177221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e38b6ee0418a568b6723031ee851c0255648d189062f7a34cd082738a5a1da`  
		Last Modified: Wed, 20 Sep 2023 17:15:31 GMT  
		Size: 13.6 MB (13567689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41556b9b524d52ec328e6b0ee7c21deedf8aed8e3e61bae271a9d58162ecaa84`  
		Last Modified: Wed, 20 Sep 2023 17:15:29 GMT  
		Size: 460.0 KB (459973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bcab3789a0a2d428eaf79d0614e6689a83d23fe92e21739594dbef4ac04d76`  
		Last Modified: Mon, 25 Sep 2023 22:31:32 GMT  
		Size: 278.9 MB (278897794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a25a06f1d456434a716a1c72de010b3e9900487d5f3a9588b0ebdb38b253ea8`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5e1e8ec6e9360c01de60dab75a4f9fdb6332c4984a65ac5a949a1093316270`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5ff43b733417167eec575f27eb7cea33a13a948c6a5d104ab734dc95eda2c6`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151561246ce03ae4eaa79d4b80a9044013fb974528eca442bf95355551c026ef`  
		Last Modified: Mon, 25 Sep 2023 22:31:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:819cbf95d80a0b129c7c7b1f17c2277ffdc70c324fee954102a2856a3e68c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:9c98688cb17116b99aae80d7f6126b4c64f984e137e9060ddbaad66f2104a7c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.5 MB (562472073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb6798615d863524a2932f71a2e9d7610977ee0a27b0fb49e2e15d00cf2710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:05:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:05:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:05:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:09:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:09:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:09:10 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:09:10 GMT
ENV ODOO_VERSION=15.0
# Mon, 25 Sep 2023 22:26:35 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:26:35 GMT
ARG ODOO_SHA=e10abf8d0b57917d198d8185aa893fd44ce65c9c
# Mon, 25 Sep 2023 22:27:48 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=e10abf8d0b57917d198d8185aa893fd44ce65c9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:27:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:27:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:27:53 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=e10abf8d0b57917d198d8185aa893fd44ce65c9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:27:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:27:53 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:27:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:27:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:27:54 GMT
USER odoo
# Mon, 25 Sep 2023 22:27:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:27:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6575baebaed17dfc5bb5620e882ccd394a631c23a37b46b31e8f35be27a5539e`  
		Last Modified: Wed, 20 Sep 2023 17:15:07 GMT  
		Size: 220.3 MB (220302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd472c483e558655dc4a27e0fbaf86ccab2eca5b2cf1310880f2f0a268b4f0f`  
		Last Modified: Wed, 20 Sep 2023 17:14:43 GMT  
		Size: 2.6 MB (2624479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb18e6c2a98cf38295f637890a9999541712df42f606502c7be9aa8d797db06c`  
		Last Modified: Wed, 20 Sep 2023 17:14:42 GMT  
		Size: 455.5 KB (455523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3263aa158ae3641f6029659d040385954e2aa3f00c412fded0062abcf9ae0d0`  
		Last Modified: Mon, 25 Sep 2023 22:30:52 GMT  
		Size: 307.7 MB (307669724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fb57526b3386d3de4c3cb7ddc07d0cff9b14c7fff5cfc08acf6a8a102d8e5a`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb459872ee1afcd5f10eae981ff73a014a8228ce4730a89e21f5468b88db830`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e186554e54a7433c1b1af380c0fc4dc182bb848f3c1d28c7ef9028863a50d`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce6e87ee0826ab3f6061b1e164857493511b0c155b44dbceb7efac5e78d8ae`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:819cbf95d80a0b129c7c7b1f17c2277ffdc70c324fee954102a2856a3e68c667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:9c98688cb17116b99aae80d7f6126b4c64f984e137e9060ddbaad66f2104a7c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.5 MB (562472073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb6798615d863524a2932f71a2e9d7610977ee0a27b0fb49e2e15d00cf2710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:05:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:05:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:05:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:09:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:09:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:09:10 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:09:10 GMT
ENV ODOO_VERSION=15.0
# Mon, 25 Sep 2023 22:26:35 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:26:35 GMT
ARG ODOO_SHA=e10abf8d0b57917d198d8185aa893fd44ce65c9c
# Mon, 25 Sep 2023 22:27:48 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=e10abf8d0b57917d198d8185aa893fd44ce65c9c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:27:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:27:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:27:53 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=e10abf8d0b57917d198d8185aa893fd44ce65c9c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:27:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:27:53 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:27:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:27:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:27:54 GMT
USER odoo
# Mon, 25 Sep 2023 22:27:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:27:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6575baebaed17dfc5bb5620e882ccd394a631c23a37b46b31e8f35be27a5539e`  
		Last Modified: Wed, 20 Sep 2023 17:15:07 GMT  
		Size: 220.3 MB (220302175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd472c483e558655dc4a27e0fbaf86ccab2eca5b2cf1310880f2f0a268b4f0f`  
		Last Modified: Wed, 20 Sep 2023 17:14:43 GMT  
		Size: 2.6 MB (2624479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb18e6c2a98cf38295f637890a9999541712df42f606502c7be9aa8d797db06c`  
		Last Modified: Wed, 20 Sep 2023 17:14:42 GMT  
		Size: 455.5 KB (455523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3263aa158ae3641f6029659d040385954e2aa3f00c412fded0062abcf9ae0d0`  
		Last Modified: Mon, 25 Sep 2023 22:30:52 GMT  
		Size: 307.7 MB (307669724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fb57526b3386d3de4c3cb7ddc07d0cff9b14c7fff5cfc08acf6a8a102d8e5a`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb459872ee1afcd5f10eae981ff73a014a8228ce4730a89e21f5468b88db830`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e186554e54a7433c1b1af380c0fc4dc182bb848f3c1d28c7ef9028863a50d`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce6e87ee0826ab3f6061b1e164857493511b0c155b44dbceb7efac5e78d8ae`  
		Last Modified: Mon, 25 Sep 2023 22:30:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:9a622d6bf544aa44eb653227e282b9b090aa527ff4d67f7c49a0717fbda07f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:4c3452274217d93106a440a673914c34ef9392a734b78c3710bf9a53d6d8f76f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576802498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10abb3cd9e9a827db22e802885dc06dfcfc1444b08ed87a6ebd282badf76924c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:05:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:05:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:05:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:06:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:06:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:06:34 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:06:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Sep 2023 22:24:56 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:24:57 GMT
ARG ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
# Mon, 25 Sep 2023 22:26:18 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:26:23 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:26:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:26:24 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:26:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:26:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:26:24 GMT
USER odoo
# Mon, 25 Sep 2023 22:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:26:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11206b2f0b0742a04b2e5aa673cf9bc01605b066d9fb144ce3973545531f57`  
		Last Modified: Wed, 20 Sep 2023 17:14:18 GMT  
		Size: 221.0 MB (220991931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e852d5c710cf3b695ca69683a47c0c02019debf9d920cb9cf770b83b5b466e3`  
		Last Modified: Wed, 20 Sep 2023 17:13:54 GMT  
		Size: 2.6 MB (2627315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2d84b33fdc1c69a8c227d7b0e75f038a4e81d937f06be5b99f42c6ad8c6bc9`  
		Last Modified: Wed, 20 Sep 2023 17:13:53 GMT  
		Size: 455.5 KB (455518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e38f1dbd6155d88625b9f11f5f75df94eb0caa2f4e60cad64d0f28db29e7f2`  
		Last Modified: Mon, 25 Sep 2023 22:30:07 GMT  
		Size: 321.3 MB (321307565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1dcfdbe1f893f30b7617d276b98de89b517719d6d04bc00faa55b15c2dbacf`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d91aa73eb2464c1d4053c046d6010408c5676b65a9efc2c21b96b4ab9f194`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6d7b87a5437483aca0f8715d5a9ee6e1ba000bd59f69145a858673fbaa4339`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55c8f81b83e5f9c9fc83fa02532b653910152495dbf5cb4ba3aa69b6970a9f5`  
		Last Modified: Mon, 25 Sep 2023 22:29:29 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:9a622d6bf544aa44eb653227e282b9b090aa527ff4d67f7c49a0717fbda07f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:4c3452274217d93106a440a673914c34ef9392a734b78c3710bf9a53d6d8f76f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576802498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10abb3cd9e9a827db22e802885dc06dfcfc1444b08ed87a6ebd282badf76924c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:05:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:05:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:05:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:06:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:06:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:06:34 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:06:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Sep 2023 22:24:56 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:24:57 GMT
ARG ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
# Mon, 25 Sep 2023 22:26:18 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:26:23 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:26:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:26:24 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:26:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:26:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:26:24 GMT
USER odoo
# Mon, 25 Sep 2023 22:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:26:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11206b2f0b0742a04b2e5aa673cf9bc01605b066d9fb144ce3973545531f57`  
		Last Modified: Wed, 20 Sep 2023 17:14:18 GMT  
		Size: 221.0 MB (220991931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e852d5c710cf3b695ca69683a47c0c02019debf9d920cb9cf770b83b5b466e3`  
		Last Modified: Wed, 20 Sep 2023 17:13:54 GMT  
		Size: 2.6 MB (2627315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2d84b33fdc1c69a8c227d7b0e75f038a4e81d937f06be5b99f42c6ad8c6bc9`  
		Last Modified: Wed, 20 Sep 2023 17:13:53 GMT  
		Size: 455.5 KB (455518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e38f1dbd6155d88625b9f11f5f75df94eb0caa2f4e60cad64d0f28db29e7f2`  
		Last Modified: Mon, 25 Sep 2023 22:30:07 GMT  
		Size: 321.3 MB (321307565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1dcfdbe1f893f30b7617d276b98de89b517719d6d04bc00faa55b15c2dbacf`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d91aa73eb2464c1d4053c046d6010408c5676b65a9efc2c21b96b4ab9f194`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6d7b87a5437483aca0f8715d5a9ee6e1ba000bd59f69145a858673fbaa4339`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55c8f81b83e5f9c9fc83fa02532b653910152495dbf5cb4ba3aa69b6970a9f5`  
		Last Modified: Mon, 25 Sep 2023 22:29:29 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:9a622d6bf544aa44eb653227e282b9b090aa527ff4d67f7c49a0717fbda07f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:4c3452274217d93106a440a673914c34ef9392a734b78c3710bf9a53d6d8f76f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576802498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10abb3cd9e9a827db22e802885dc06dfcfc1444b08ed87a6ebd282badf76924c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:05:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:05:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:05:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:06:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:06:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:06:34 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:06:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Sep 2023 22:24:56 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:24:57 GMT
ARG ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
# Mon, 25 Sep 2023 22:26:18 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:26:23 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:26:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:26:24 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:26:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:26:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:26:24 GMT
USER odoo
# Mon, 25 Sep 2023 22:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:26:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11206b2f0b0742a04b2e5aa673cf9bc01605b066d9fb144ce3973545531f57`  
		Last Modified: Wed, 20 Sep 2023 17:14:18 GMT  
		Size: 221.0 MB (220991931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e852d5c710cf3b695ca69683a47c0c02019debf9d920cb9cf770b83b5b466e3`  
		Last Modified: Wed, 20 Sep 2023 17:13:54 GMT  
		Size: 2.6 MB (2627315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2d84b33fdc1c69a8c227d7b0e75f038a4e81d937f06be5b99f42c6ad8c6bc9`  
		Last Modified: Wed, 20 Sep 2023 17:13:53 GMT  
		Size: 455.5 KB (455518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e38f1dbd6155d88625b9f11f5f75df94eb0caa2f4e60cad64d0f28db29e7f2`  
		Last Modified: Mon, 25 Sep 2023 22:30:07 GMT  
		Size: 321.3 MB (321307565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1dcfdbe1f893f30b7617d276b98de89b517719d6d04bc00faa55b15c2dbacf`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d91aa73eb2464c1d4053c046d6010408c5676b65a9efc2c21b96b4ab9f194`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6d7b87a5437483aca0f8715d5a9ee6e1ba000bd59f69145a858673fbaa4339`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55c8f81b83e5f9c9fc83fa02532b653910152495dbf5cb4ba3aa69b6970a9f5`  
		Last Modified: Mon, 25 Sep 2023 22:29:29 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
