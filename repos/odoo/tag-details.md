<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240624`](#odoo150-20240624)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240624`](#odoo160-20240624)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240624`](#odoo170-20240624)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:8156619bfaea98ddb87cfc38e6647ba78460294ad6e97df4403888507da119cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:c0f7d609c3a7b43478b294f9623e35546ed25232171cc5e6479fb64819911142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563843315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8e9ef4f9f5c6d15b4bc6c46d98e451e09de483dd33bdf50112aeea9232d0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=15.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: ODOO_RELEASE=20240624 ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: ODOO_RELEASE=20240624 ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c788ec143b1e31f22edfb9da665f794f9160ce4f3c7e4fc52c2211b682da26a`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 220.3 MB (220281643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288e20f82f851123560cd449dc7a9fc8716c268e5f62a168b8fbc474a4b1326`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 2.4 MB (2387212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aad42076144fe8d7bce041b88891ba0fe20802f526a7c791d046c3f3fb5ecbd`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 459.1 KB (459066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7da388b2276b89ec28316553e8c215b567f8e69b9859db987fa0ed0d3aa0072`  
		Last Modified: Tue, 02 Jul 2024 03:23:27 GMT  
		Size: 309.3 MB (309290680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafa843ba3efba202870eebcc6e71b1b519825e3dc37954746334924548ad889`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b402ccf99f768e6ed0113ec1b4e8bc939a3d0518260a84f5ce1fb584a4b1a`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e5f3f374c356bcaf13c9333fb69cfa92926d3b2b65de2c621cfb50baaeff2a`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730e2898b513a4385cbf615c3edfda11b125deb5fd80103407016aa227547fdc`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:4d9550ba549d5e5e68d74c2157b76a93463081015f7282d0329d37c2e28d24b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34536147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e0cbb66987ec3611682d565ab4729accaabf34e8b0009850595974cecd303a`

```dockerfile
```

-	Layers:
	-	`sha256:af91626bb3a7d92f954db11716ad4a798fcc19f07f170c55cb730a161d23becb`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 34.5 MB (34511516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a5c4d64ac2a1ed94f438d09253bb726857a0ca5f4c4c947f7cec7ae3003b4a`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:8156619bfaea98ddb87cfc38e6647ba78460294ad6e97df4403888507da119cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:c0f7d609c3a7b43478b294f9623e35546ed25232171cc5e6479fb64819911142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563843315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8e9ef4f9f5c6d15b4bc6c46d98e451e09de483dd33bdf50112aeea9232d0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=15.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: ODOO_RELEASE=20240624 ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: ODOO_RELEASE=20240624 ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c788ec143b1e31f22edfb9da665f794f9160ce4f3c7e4fc52c2211b682da26a`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 220.3 MB (220281643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288e20f82f851123560cd449dc7a9fc8716c268e5f62a168b8fbc474a4b1326`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 2.4 MB (2387212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aad42076144fe8d7bce041b88891ba0fe20802f526a7c791d046c3f3fb5ecbd`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 459.1 KB (459066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7da388b2276b89ec28316553e8c215b567f8e69b9859db987fa0ed0d3aa0072`  
		Last Modified: Tue, 02 Jul 2024 03:23:27 GMT  
		Size: 309.3 MB (309290680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafa843ba3efba202870eebcc6e71b1b519825e3dc37954746334924548ad889`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b402ccf99f768e6ed0113ec1b4e8bc939a3d0518260a84f5ce1fb584a4b1a`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e5f3f374c356bcaf13c9333fb69cfa92926d3b2b65de2c621cfb50baaeff2a`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730e2898b513a4385cbf615c3edfda11b125deb5fd80103407016aa227547fdc`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4d9550ba549d5e5e68d74c2157b76a93463081015f7282d0329d37c2e28d24b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34536147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e0cbb66987ec3611682d565ab4729accaabf34e8b0009850595974cecd303a`

```dockerfile
```

-	Layers:
	-	`sha256:af91626bb3a7d92f954db11716ad4a798fcc19f07f170c55cb730a161d23becb`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 34.5 MB (34511516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a5c4d64ac2a1ed94f438d09253bb726857a0ca5f4c4c947f7cec7ae3003b4a`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240624`

```console
$ docker pull odoo@sha256:8156619bfaea98ddb87cfc38e6647ba78460294ad6e97df4403888507da119cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240624` - linux; amd64

```console
$ docker pull odoo@sha256:c0f7d609c3a7b43478b294f9623e35546ed25232171cc5e6479fb64819911142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563843315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8e9ef4f9f5c6d15b4bc6c46d98e451e09de483dd33bdf50112aeea9232d0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=15.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: ODOO_RELEASE=20240624 ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: ODOO_RELEASE=20240624 ODOO_SHA=34ce405377bf75beca3d4de1d81d1c89ba15fed9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c788ec143b1e31f22edfb9da665f794f9160ce4f3c7e4fc52c2211b682da26a`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 220.3 MB (220281643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288e20f82f851123560cd449dc7a9fc8716c268e5f62a168b8fbc474a4b1326`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 2.4 MB (2387212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aad42076144fe8d7bce041b88891ba0fe20802f526a7c791d046c3f3fb5ecbd`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 459.1 KB (459066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7da388b2276b89ec28316553e8c215b567f8e69b9859db987fa0ed0d3aa0072`  
		Last Modified: Tue, 02 Jul 2024 03:23:27 GMT  
		Size: 309.3 MB (309290680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafa843ba3efba202870eebcc6e71b1b519825e3dc37954746334924548ad889`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8b402ccf99f768e6ed0113ec1b4e8bc939a3d0518260a84f5ce1fb584a4b1a`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e5f3f374c356bcaf13c9333fb69cfa92926d3b2b65de2c621cfb50baaeff2a`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730e2898b513a4385cbf615c3edfda11b125deb5fd80103407016aa227547fdc`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:4d9550ba549d5e5e68d74c2157b76a93463081015f7282d0329d37c2e28d24b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34536147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e0cbb66987ec3611682d565ab4729accaabf34e8b0009850595974cecd303a`

```dockerfile
```

-	Layers:
	-	`sha256:af91626bb3a7d92f954db11716ad4a798fcc19f07f170c55cb730a161d23becb`  
		Last Modified: Tue, 02 Jul 2024 03:23:21 GMT  
		Size: 34.5 MB (34511516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a5c4d64ac2a1ed94f438d09253bb726857a0ca5f4c4c947f7cec7ae3003b4a`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:0e85d2a5348a4212b33084209eaf4948868ed9f688faa7ca7a6f750a17e047f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f3a5d736436c3305bd9062c3fe91a6f62a78de010058e6065a05fc720cd95c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583157212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92509daea6a81b9f0143fa06d42685942681775b4143decc68480bb05a0d55b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc84e9729462684170d574f22947988772c5499f909ab1925056291209df5a`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 219.6 MB (219594518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b5015f6d6917bf76d611e39519e0d25ae5b59e5d2d216fa227de114926f64`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 2.4 MB (2391079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46203f2cccf00e13ed46f63491113ee70ccb120e11124312edb574fc73d2960`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 459.2 KB (459153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad17dfb6954f330002f0f58845c953bc4ff862a5afa63dee4d3e64d7f0abb0`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 329.3 MB (329287745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16954b1927f067274e518c9814b706f88700861d324eeeb0730fd42fd044a8c0`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cc4e8946fe4be4f10a888455462ff5a3b5ba265590fd357d733c07b69e0d3`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed9f78cdceccc8576ae0c2fbfd025219bd1bd2ddf6a50f3dcbb97aa28e42f9`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c1c70bef979b6dc3692062b6d89a70d6370e74ec9eac978aa32dd4f634bdb`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:755480c2ddfd36f2b4e8ed77eec6292e7e63329681f281e83a0c6db2098d9a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38575384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afab4fd9e575a272bc84814e704e2983c4a92db6bdf33453b622c8d6ded1b827`

```dockerfile
```

-	Layers:
	-	`sha256:7c0a0c65d32f3a3ebcdd2465a1a3ae52f18e3a607188720f5797320047d507f4`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 38.5 MB (38548842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61519c148374ef1fb72e5012e1b1f02f5fb628ea867c412d69e6cd72489b4ae`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:00a239f59d6a2d05c306308949d8d64233a666e79faed21f3c6fedc69ad38780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578779777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bddd733133dbfae1d3d12cceadb0158beb6bf5c9d54be2a240405b3176e6274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f10a35f7aeee17508b32c62a6f45603b3bed94883abbaeab667b310590de9`  
		Last Modified: Thu, 13 Jun 2024 19:43:30 GMT  
		Size: 216.9 MB (216903979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b6f53b4dc3b3909dec9234c8bbde8cb1f77a78b1eab7bae6fda802ac999e18`  
		Last Modified: Thu, 13 Jun 2024 19:43:26 GMT  
		Size: 2.4 MB (2393378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266abce915a37340151813efeae00551a7210b039da8108c27c4018b8720eab`  
		Last Modified: Thu, 13 Jun 2024 19:43:26 GMT  
		Size: 457.8 KB (457833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0299c2855e07b4e671dd689d1ebeebe965da9aa5e874a27ba1ccf910cc2ae`  
		Last Modified: Mon, 24 Jun 2024 18:32:46 GMT  
		Size: 328.9 MB (328935175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d244f7215adc17bfebdb1cfee80b825bfc4ab049dd853174d379006ccc65637e`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8d81d033b20346c836bc7f0c204698e3f40191f35942acce64b0fee670e593`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43447ab8203740fde76b8d764af842cfd69ff062aa9f70093b4802008df59c60`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52303d987ee310abf2711d6b988d72c655d5de6a93edbe4ded872eb16ce760f`  
		Last Modified: Mon, 24 Jun 2024 18:32:39 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:1b3a2dc1ef78f91158158a4ba98e8ef3d9d25a584012bf1c58afd6e76d977f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38582006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09960ef163643cba870f4bb549e9ad63ec174504fb867e1973409d2f345698bb`

```dockerfile
```

-	Layers:
	-	`sha256:b8259604a242aa7d9f504f50de7debbc20bd0a754dd295a476cc4292a8aa7125`  
		Last Modified: Mon, 24 Jun 2024 18:32:39 GMT  
		Size: 38.6 MB (38555168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99a41bfbd8cd4d0f57658426665b5c355151876024ae33a8fa0b4a3adb539b9`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:e596b45922c860cc24bd0f39a3645dc9f068da155963e8b8ad38208531c9bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597709008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f472fe66e62932fae7018e307ae04608e646bf4594874226e1f942b0202c21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:31 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9d00807b24096ab27eed1fd602a0a9744ab1ebd1ab97303fbf1c1c7e89e6e`  
		Last Modified: Fri, 14 Jun 2024 01:14:29 GMT  
		Size: 228.6 MB (228592556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c194818608382b1511ae65b4a77878623526f7b8d4baf42f540d151881ee655`  
		Last Modified: Fri, 14 Jun 2024 01:14:08 GMT  
		Size: 2.6 MB (2634151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8830a4101177704f85a6676632a51375eb01f0355db6b0d08d2d83c298f705`  
		Last Modified: Fri, 14 Jun 2024 01:14:08 GMT  
		Size: 457.8 KB (457839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1820b640a7f895227c07421e5b6434704d4795cefa132459a1e77dd20a7f9be`  
		Last Modified: Mon, 24 Jun 2024 18:21:17 GMT  
		Size: 330.7 MB (330710720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7ba6b3fcb39833ed6082495ba1be32f5f76fa76b3fb70e98d4ab2ad91b0576`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bbd2ec027b2aa49fef1c000e5e34480d9bd19f9526ad7ebdded957f3fa5af6`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10f63b19613ef1d8c0ab743bea507d20958cc80bc8ee7a90cbf6381371a76a`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641519b8a37bcadb40cb1a46e619d45d41d7b0c198884a8576e558df0a9fe35a`  
		Last Modified: Mon, 24 Jun 2024 18:21:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:05b7710a2affd97f4d9ef5f09e5752250175599c848d6636703ca227a2fb1239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38583420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a20e475d48dbc3d12917b6e49a07074d231d89c19dbc268bd1bfeb2a1c8156a`

```dockerfile
```

-	Layers:
	-	`sha256:192aa9bab9406b36f5fc3dabdab1bc8e6846b34d4665995f27f78e90c09fa46e`  
		Last Modified: Mon, 24 Jun 2024 18:21:10 GMT  
		Size: 38.6 MB (38556828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53189ef9f218e860bad1ff2f2ff8f6d28d6b3108097ea76ef6b6714026a6b94d`  
		Last Modified: Mon, 24 Jun 2024 18:21:08 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:0e85d2a5348a4212b33084209eaf4948868ed9f688faa7ca7a6f750a17e047f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f3a5d736436c3305bd9062c3fe91a6f62a78de010058e6065a05fc720cd95c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583157212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92509daea6a81b9f0143fa06d42685942681775b4143decc68480bb05a0d55b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc84e9729462684170d574f22947988772c5499f909ab1925056291209df5a`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 219.6 MB (219594518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b5015f6d6917bf76d611e39519e0d25ae5b59e5d2d216fa227de114926f64`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 2.4 MB (2391079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46203f2cccf00e13ed46f63491113ee70ccb120e11124312edb574fc73d2960`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 459.2 KB (459153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad17dfb6954f330002f0f58845c953bc4ff862a5afa63dee4d3e64d7f0abb0`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 329.3 MB (329287745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16954b1927f067274e518c9814b706f88700861d324eeeb0730fd42fd044a8c0`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cc4e8946fe4be4f10a888455462ff5a3b5ba265590fd357d733c07b69e0d3`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed9f78cdceccc8576ae0c2fbfd025219bd1bd2ddf6a50f3dcbb97aa28e42f9`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c1c70bef979b6dc3692062b6d89a70d6370e74ec9eac978aa32dd4f634bdb`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:755480c2ddfd36f2b4e8ed77eec6292e7e63329681f281e83a0c6db2098d9a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38575384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afab4fd9e575a272bc84814e704e2983c4a92db6bdf33453b622c8d6ded1b827`

```dockerfile
```

-	Layers:
	-	`sha256:7c0a0c65d32f3a3ebcdd2465a1a3ae52f18e3a607188720f5797320047d507f4`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 38.5 MB (38548842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61519c148374ef1fb72e5012e1b1f02f5fb628ea867c412d69e6cd72489b4ae`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:00a239f59d6a2d05c306308949d8d64233a666e79faed21f3c6fedc69ad38780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578779777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bddd733133dbfae1d3d12cceadb0158beb6bf5c9d54be2a240405b3176e6274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f10a35f7aeee17508b32c62a6f45603b3bed94883abbaeab667b310590de9`  
		Last Modified: Thu, 13 Jun 2024 19:43:30 GMT  
		Size: 216.9 MB (216903979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b6f53b4dc3b3909dec9234c8bbde8cb1f77a78b1eab7bae6fda802ac999e18`  
		Last Modified: Thu, 13 Jun 2024 19:43:26 GMT  
		Size: 2.4 MB (2393378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266abce915a37340151813efeae00551a7210b039da8108c27c4018b8720eab`  
		Last Modified: Thu, 13 Jun 2024 19:43:26 GMT  
		Size: 457.8 KB (457833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0299c2855e07b4e671dd689d1ebeebe965da9aa5e874a27ba1ccf910cc2ae`  
		Last Modified: Mon, 24 Jun 2024 18:32:46 GMT  
		Size: 328.9 MB (328935175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d244f7215adc17bfebdb1cfee80b825bfc4ab049dd853174d379006ccc65637e`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8d81d033b20346c836bc7f0c204698e3f40191f35942acce64b0fee670e593`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43447ab8203740fde76b8d764af842cfd69ff062aa9f70093b4802008df59c60`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52303d987ee310abf2711d6b988d72c655d5de6a93edbe4ded872eb16ce760f`  
		Last Modified: Mon, 24 Jun 2024 18:32:39 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1b3a2dc1ef78f91158158a4ba98e8ef3d9d25a584012bf1c58afd6e76d977f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38582006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09960ef163643cba870f4bb549e9ad63ec174504fb867e1973409d2f345698bb`

```dockerfile
```

-	Layers:
	-	`sha256:b8259604a242aa7d9f504f50de7debbc20bd0a754dd295a476cc4292a8aa7125`  
		Last Modified: Mon, 24 Jun 2024 18:32:39 GMT  
		Size: 38.6 MB (38555168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99a41bfbd8cd4d0f57658426665b5c355151876024ae33a8fa0b4a3adb539b9`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e596b45922c860cc24bd0f39a3645dc9f068da155963e8b8ad38208531c9bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597709008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f472fe66e62932fae7018e307ae04608e646bf4594874226e1f942b0202c21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:31 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9d00807b24096ab27eed1fd602a0a9744ab1ebd1ab97303fbf1c1c7e89e6e`  
		Last Modified: Fri, 14 Jun 2024 01:14:29 GMT  
		Size: 228.6 MB (228592556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c194818608382b1511ae65b4a77878623526f7b8d4baf42f540d151881ee655`  
		Last Modified: Fri, 14 Jun 2024 01:14:08 GMT  
		Size: 2.6 MB (2634151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8830a4101177704f85a6676632a51375eb01f0355db6b0d08d2d83c298f705`  
		Last Modified: Fri, 14 Jun 2024 01:14:08 GMT  
		Size: 457.8 KB (457839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1820b640a7f895227c07421e5b6434704d4795cefa132459a1e77dd20a7f9be`  
		Last Modified: Mon, 24 Jun 2024 18:21:17 GMT  
		Size: 330.7 MB (330710720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7ba6b3fcb39833ed6082495ba1be32f5f76fa76b3fb70e98d4ab2ad91b0576`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bbd2ec027b2aa49fef1c000e5e34480d9bd19f9526ad7ebdded957f3fa5af6`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10f63b19613ef1d8c0ab743bea507d20958cc80bc8ee7a90cbf6381371a76a`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641519b8a37bcadb40cb1a46e619d45d41d7b0c198884a8576e558df0a9fe35a`  
		Last Modified: Mon, 24 Jun 2024 18:21:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:05b7710a2affd97f4d9ef5f09e5752250175599c848d6636703ca227a2fb1239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38583420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a20e475d48dbc3d12917b6e49a07074d231d89c19dbc268bd1bfeb2a1c8156a`

```dockerfile
```

-	Layers:
	-	`sha256:192aa9bab9406b36f5fc3dabdab1bc8e6846b34d4665995f27f78e90c09fa46e`  
		Last Modified: Mon, 24 Jun 2024 18:21:10 GMT  
		Size: 38.6 MB (38556828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53189ef9f218e860bad1ff2f2ff8f6d28d6b3108097ea76ef6b6714026a6b94d`  
		Last Modified: Mon, 24 Jun 2024 18:21:08 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240624`

```console
$ docker pull odoo@sha256:0e85d2a5348a4212b33084209eaf4948868ed9f688faa7ca7a6f750a17e047f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240624` - linux; amd64

```console
$ docker pull odoo@sha256:f3a5d736436c3305bd9062c3fe91a6f62a78de010058e6065a05fc720cd95c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583157212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92509daea6a81b9f0143fa06d42685942681775b4143decc68480bb05a0d55b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc84e9729462684170d574f22947988772c5499f909ab1925056291209df5a`  
		Last Modified: Tue, 02 Jul 2024 03:23:22 GMT  
		Size: 219.6 MB (219594518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b5015f6d6917bf76d611e39519e0d25ae5b59e5d2d216fa227de114926f64`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 2.4 MB (2391079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46203f2cccf00e13ed46f63491113ee70ccb120e11124312edb574fc73d2960`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 459.2 KB (459153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad17dfb6954f330002f0f58845c953bc4ff862a5afa63dee4d3e64d7f0abb0`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 329.3 MB (329287745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16954b1927f067274e518c9814b706f88700861d324eeeb0730fd42fd044a8c0`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cc4e8946fe4be4f10a888455462ff5a3b5ba265590fd357d733c07b69e0d3`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed9f78cdceccc8576ae0c2fbfd025219bd1bd2ddf6a50f3dcbb97aa28e42f9`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17c1c70bef979b6dc3692062b6d89a70d6370e74ec9eac978aa32dd4f634bdb`  
		Last Modified: Tue, 02 Jul 2024 03:23:20 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:755480c2ddfd36f2b4e8ed77eec6292e7e63329681f281e83a0c6db2098d9a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38575384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afab4fd9e575a272bc84814e704e2983c4a92db6bdf33453b622c8d6ded1b827`

```dockerfile
```

-	Layers:
	-	`sha256:7c0a0c65d32f3a3ebcdd2465a1a3ae52f18e3a607188720f5797320047d507f4`  
		Last Modified: Tue, 02 Jul 2024 03:23:19 GMT  
		Size: 38.5 MB (38548842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61519c148374ef1fb72e5012e1b1f02f5fb628ea867c412d69e6cd72489b4ae`  
		Last Modified: Tue, 02 Jul 2024 03:23:18 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240624` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:00a239f59d6a2d05c306308949d8d64233a666e79faed21f3c6fedc69ad38780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578779777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bddd733133dbfae1d3d12cceadb0158beb6bf5c9d54be2a240405b3176e6274`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f10a35f7aeee17508b32c62a6f45603b3bed94883abbaeab667b310590de9`  
		Last Modified: Thu, 13 Jun 2024 19:43:30 GMT  
		Size: 216.9 MB (216903979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b6f53b4dc3b3909dec9234c8bbde8cb1f77a78b1eab7bae6fda802ac999e18`  
		Last Modified: Thu, 13 Jun 2024 19:43:26 GMT  
		Size: 2.4 MB (2393378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266abce915a37340151813efeae00551a7210b039da8108c27c4018b8720eab`  
		Last Modified: Thu, 13 Jun 2024 19:43:26 GMT  
		Size: 457.8 KB (457833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0299c2855e07b4e671dd689d1ebeebe965da9aa5e874a27ba1ccf910cc2ae`  
		Last Modified: Mon, 24 Jun 2024 18:32:46 GMT  
		Size: 328.9 MB (328935175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d244f7215adc17bfebdb1cfee80b825bfc4ab049dd853174d379006ccc65637e`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8d81d033b20346c836bc7f0c204698e3f40191f35942acce64b0fee670e593`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43447ab8203740fde76b8d764af842cfd69ff062aa9f70093b4802008df59c60`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52303d987ee310abf2711d6b988d72c655d5de6a93edbe4ded872eb16ce760f`  
		Last Modified: Mon, 24 Jun 2024 18:32:39 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:1b3a2dc1ef78f91158158a4ba98e8ef3d9d25a584012bf1c58afd6e76d977f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38582006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09960ef163643cba870f4bb549e9ad63ec174504fb867e1973409d2f345698bb`

```dockerfile
```

-	Layers:
	-	`sha256:b8259604a242aa7d9f504f50de7debbc20bd0a754dd295a476cc4292a8aa7125`  
		Last Modified: Mon, 24 Jun 2024 18:32:39 GMT  
		Size: 38.6 MB (38555168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99a41bfbd8cd4d0f57658426665b5c355151876024ae33a8fa0b4a3adb539b9`  
		Last Modified: Mon, 24 Jun 2024 18:32:38 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240624` - linux; ppc64le

```console
$ docker pull odoo@sha256:e596b45922c860cc24bd0f39a3645dc9f068da155963e8b8ad38208531c9bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597709008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f472fe66e62932fae7018e307ae04608e646bf4594874226e1f942b0202c21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:31 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Thu, 13 Jun 2024 01:17:33 GMT
CMD ["bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=C.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=16.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=a51d6f097b24096d38959f4cd97ae5fb2cd2807b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9d00807b24096ab27eed1fd602a0a9744ab1ebd1ab97303fbf1c1c7e89e6e`  
		Last Modified: Fri, 14 Jun 2024 01:14:29 GMT  
		Size: 228.6 MB (228592556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c194818608382b1511ae65b4a77878623526f7b8d4baf42f540d151881ee655`  
		Last Modified: Fri, 14 Jun 2024 01:14:08 GMT  
		Size: 2.6 MB (2634151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8830a4101177704f85a6676632a51375eb01f0355db6b0d08d2d83c298f705`  
		Last Modified: Fri, 14 Jun 2024 01:14:08 GMT  
		Size: 457.8 KB (457839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1820b640a7f895227c07421e5b6434704d4795cefa132459a1e77dd20a7f9be`  
		Last Modified: Mon, 24 Jun 2024 18:21:17 GMT  
		Size: 330.7 MB (330710720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7ba6b3fcb39833ed6082495ba1be32f5f76fa76b3fb70e98d4ab2ad91b0576`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bbd2ec027b2aa49fef1c000e5e34480d9bd19f9526ad7ebdded957f3fa5af6`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10f63b19613ef1d8c0ab743bea507d20958cc80bc8ee7a90cbf6381371a76a`  
		Last Modified: Mon, 24 Jun 2024 18:21:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641519b8a37bcadb40cb1a46e619d45d41d7b0c198884a8576e558df0a9fe35a`  
		Last Modified: Mon, 24 Jun 2024 18:21:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:05b7710a2affd97f4d9ef5f09e5752250175599c848d6636703ca227a2fb1239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38583420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a20e475d48dbc3d12917b6e49a07074d231d89c19dbc268bd1bfeb2a1c8156a`

```dockerfile
```

-	Layers:
	-	`sha256:192aa9bab9406b36f5fc3dabdab1bc8e6846b34d4665995f27f78e90c09fa46e`  
		Last Modified: Mon, 24 Jun 2024 18:21:10 GMT  
		Size: 38.6 MB (38556828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53189ef9f218e860bad1ff2f2ff8f6d28d6b3108097ea76ef6b6714026a6b94d`  
		Last Modified: Mon, 24 Jun 2024 18:21:08 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:cfd904b5cbdfb3857709e65e13bfae204a635e4d1bf208ff27bbc88335d06f99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:648f73f441f6c365796c85bd3c1c2981855dffbc2996efbd20885555dcc810c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594677171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a971c8e390d48f0f07140fed96db96d7963441919c74380f64f633ad020756c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ARG RELEASE
# Mon, 24 Jun 2024 09:13:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f61ce99eb895f5f57f2e577ba92d82405da2518f1754c4bedeec5fa9e3515d`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 233.7 MB (233723670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f296950c72ad7a88320aead36aa5339ae5f9339244ccfb62f6ce17854a3345fc`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 2.3 MB (2313751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1087908b082c60609c22ed2db4841f2fe1b534f767c75129f991a95a8ea2b7`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 460.2 KB (460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc2d985b0011a6433376d8c779e0f73df57334dc283e38b55967b7e40eee01`  
		Last Modified: Tue, 02 Jul 2024 03:23:28 GMT  
		Size: 328.6 MB (328643048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235871681e4bb561959bebc95dc884e102e8db333442971273762f9f3c87239`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5f8c48cc8c90b39e9c1f955ba04d288ff49a3760bdd127b98343f4ea99476f`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f249691be652760825dd298183e2a38338af4756b198657a04a6c72010ae85d`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef67c5b9c03e47f2467df88506a11f9d2a516c49e3782ec79e6f4b3f5fda015`  
		Last Modified: Tue, 02 Jul 2024 03:23:25 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c929ee59788ba55a6268320ad4288ecfa84d68bbe1c1f9de26a42b81ac59a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e779c9126971b3460a4247f1045fc333096220df484eeef1ddb915723581c6`

```dockerfile
```

-	Layers:
	-	`sha256:51efd760512e9b63b76ecb7cd5e5a3ac1351ef96ee157e9ed870f0e7ec9f80c9`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d16462c089873d7e5215598968921fd167d9517a2eb70d647aa28045c8d1d4`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:52f02170ee855755e55921e11207233a9c973614fc48e8f533122814451a9499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589506044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297ca0746061b2e6ea277b5742b6812557b79bd6d8ea316418d5c76ddd49a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfabac07be2024b8fccd8a3af3a59f3a7e09ff97be4ba2c865c11fdb0043d4`  
		Last Modified: Mon, 24 Jun 2024 18:29:46 GMT  
		Size: 328.2 MB (328245899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34314723ffd9e320fd561478044b50c27340c99b37eb43329ee689a4eb5429`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518aa46a6ed6e075ea9b5a39a1a60d40f8a676a9678de5e68fbe936e8c1cc8e`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e352ac21c2113b24b9a61063c2e7b22d0a8d2b8813d938b1b632e0694400c`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a97fa68e35c40e6ab7a5824874020d824108aec850e28d2097dd8c53e9e2e`  
		Last Modified: Mon, 24 Jun 2024 18:29:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e3753d52d5a4d713fc351ed3d61e84b40b74ebf4dfd247844920534a4cb11cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41b0b10cdaeaa479067607a09d8713ea5a1ec05744340c3a7c7ac70115cf0d6`

```dockerfile
```

-	Layers:
	-	`sha256:2123ade5ac43e34b8bd186c470d9b1bc9662402a2ff5c4b1e85ea2b39d89bae1`  
		Last Modified: Mon, 24 Jun 2024 18:29:41 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340f4d6bb882266f1fa8bc5c6615fdfd5f43bf12ec40e02e984e1faef4ef64ed`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:76a1170183ea3e1e614a3e76e10ad7de21f6e23ffa30d9cad9c07c35df584b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611177101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df0ae1009b13f5121c2bc2b2415a0e7f3f663ebd478133aa961c9017648be00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6db075a1a9dea80be197ad1d4dc2dc126691d190a41c4183938d85f3863e`  
		Last Modified: Mon, 24 Jun 2024 18:16:16 GMT  
		Size: 330.4 MB (330396320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282130baf4c896c22906d85c0838e337af019ad91416cfd9035440c48f60d3a8`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55709bb12b6c2542ae255950ca1e9610072f32e98e94fae28d07bdd5feccf972`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6285537b99b839b789d323dcb1bbc9b06b26704d3d94ed3f8af28d6747eb4`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342e12641dba5f6ef33d3d8f36315ac2e79f20e3d3a8657a3ea103a515937e5f`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:6d81886173938fb7968321b6254476c48c52a7e7c05db928f284c220be0ef270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38675920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9784ce9e348fbba540f04ab39c47b0b0e35acc076c0e3857e65ee93360ed561`

```dockerfile
```

-	Layers:
	-	`sha256:b05e653f8c0a61b63023a37e33469b1bc99acffdbe744ddb07b857ebe8fc9cef`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 38.6 MB (38648990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85116f7f8a479bc882b5cc0775762ee661c883f2bae113d1d13ac6480a51d5c1`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cfd904b5cbdfb3857709e65e13bfae204a635e4d1bf208ff27bbc88335d06f99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:648f73f441f6c365796c85bd3c1c2981855dffbc2996efbd20885555dcc810c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594677171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a971c8e390d48f0f07140fed96db96d7963441919c74380f64f633ad020756c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ARG RELEASE
# Mon, 24 Jun 2024 09:13:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f61ce99eb895f5f57f2e577ba92d82405da2518f1754c4bedeec5fa9e3515d`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 233.7 MB (233723670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f296950c72ad7a88320aead36aa5339ae5f9339244ccfb62f6ce17854a3345fc`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 2.3 MB (2313751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1087908b082c60609c22ed2db4841f2fe1b534f767c75129f991a95a8ea2b7`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 460.2 KB (460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc2d985b0011a6433376d8c779e0f73df57334dc283e38b55967b7e40eee01`  
		Last Modified: Tue, 02 Jul 2024 03:23:28 GMT  
		Size: 328.6 MB (328643048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235871681e4bb561959bebc95dc884e102e8db333442971273762f9f3c87239`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5f8c48cc8c90b39e9c1f955ba04d288ff49a3760bdd127b98343f4ea99476f`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f249691be652760825dd298183e2a38338af4756b198657a04a6c72010ae85d`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef67c5b9c03e47f2467df88506a11f9d2a516c49e3782ec79e6f4b3f5fda015`  
		Last Modified: Tue, 02 Jul 2024 03:23:25 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c929ee59788ba55a6268320ad4288ecfa84d68bbe1c1f9de26a42b81ac59a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e779c9126971b3460a4247f1045fc333096220df484eeef1ddb915723581c6`

```dockerfile
```

-	Layers:
	-	`sha256:51efd760512e9b63b76ecb7cd5e5a3ac1351ef96ee157e9ed870f0e7ec9f80c9`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d16462c089873d7e5215598968921fd167d9517a2eb70d647aa28045c8d1d4`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:52f02170ee855755e55921e11207233a9c973614fc48e8f533122814451a9499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589506044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297ca0746061b2e6ea277b5742b6812557b79bd6d8ea316418d5c76ddd49a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfabac07be2024b8fccd8a3af3a59f3a7e09ff97be4ba2c865c11fdb0043d4`  
		Last Modified: Mon, 24 Jun 2024 18:29:46 GMT  
		Size: 328.2 MB (328245899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34314723ffd9e320fd561478044b50c27340c99b37eb43329ee689a4eb5429`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518aa46a6ed6e075ea9b5a39a1a60d40f8a676a9678de5e68fbe936e8c1cc8e`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e352ac21c2113b24b9a61063c2e7b22d0a8d2b8813d938b1b632e0694400c`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a97fa68e35c40e6ab7a5824874020d824108aec850e28d2097dd8c53e9e2e`  
		Last Modified: Mon, 24 Jun 2024 18:29:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e3753d52d5a4d713fc351ed3d61e84b40b74ebf4dfd247844920534a4cb11cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41b0b10cdaeaa479067607a09d8713ea5a1ec05744340c3a7c7ac70115cf0d6`

```dockerfile
```

-	Layers:
	-	`sha256:2123ade5ac43e34b8bd186c470d9b1bc9662402a2ff5c4b1e85ea2b39d89bae1`  
		Last Modified: Mon, 24 Jun 2024 18:29:41 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340f4d6bb882266f1fa8bc5c6615fdfd5f43bf12ec40e02e984e1faef4ef64ed`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:76a1170183ea3e1e614a3e76e10ad7de21f6e23ffa30d9cad9c07c35df584b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611177101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df0ae1009b13f5121c2bc2b2415a0e7f3f663ebd478133aa961c9017648be00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6db075a1a9dea80be197ad1d4dc2dc126691d190a41c4183938d85f3863e`  
		Last Modified: Mon, 24 Jun 2024 18:16:16 GMT  
		Size: 330.4 MB (330396320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282130baf4c896c22906d85c0838e337af019ad91416cfd9035440c48f60d3a8`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55709bb12b6c2542ae255950ca1e9610072f32e98e94fae28d07bdd5feccf972`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6285537b99b839b789d323dcb1bbc9b06b26704d3d94ed3f8af28d6747eb4`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342e12641dba5f6ef33d3d8f36315ac2e79f20e3d3a8657a3ea103a515937e5f`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6d81886173938fb7968321b6254476c48c52a7e7c05db928f284c220be0ef270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38675920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9784ce9e348fbba540f04ab39c47b0b0e35acc076c0e3857e65ee93360ed561`

```dockerfile
```

-	Layers:
	-	`sha256:b05e653f8c0a61b63023a37e33469b1bc99acffdbe744ddb07b857ebe8fc9cef`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 38.6 MB (38648990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85116f7f8a479bc882b5cc0775762ee661c883f2bae113d1d13ac6480a51d5c1`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240624`

```console
$ docker pull odoo@sha256:cfd904b5cbdfb3857709e65e13bfae204a635e4d1bf208ff27bbc88335d06f99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240624` - linux; amd64

```console
$ docker pull odoo@sha256:648f73f441f6c365796c85bd3c1c2981855dffbc2996efbd20885555dcc810c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594677171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a971c8e390d48f0f07140fed96db96d7963441919c74380f64f633ad020756c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ARG RELEASE
# Mon, 24 Jun 2024 09:13:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f61ce99eb895f5f57f2e577ba92d82405da2518f1754c4bedeec5fa9e3515d`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 233.7 MB (233723670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f296950c72ad7a88320aead36aa5339ae5f9339244ccfb62f6ce17854a3345fc`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 2.3 MB (2313751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1087908b082c60609c22ed2db4841f2fe1b534f767c75129f991a95a8ea2b7`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 460.2 KB (460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc2d985b0011a6433376d8c779e0f73df57334dc283e38b55967b7e40eee01`  
		Last Modified: Tue, 02 Jul 2024 03:23:28 GMT  
		Size: 328.6 MB (328643048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235871681e4bb561959bebc95dc884e102e8db333442971273762f9f3c87239`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5f8c48cc8c90b39e9c1f955ba04d288ff49a3760bdd127b98343f4ea99476f`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f249691be652760825dd298183e2a38338af4756b198657a04a6c72010ae85d`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef67c5b9c03e47f2467df88506a11f9d2a516c49e3782ec79e6f4b3f5fda015`  
		Last Modified: Tue, 02 Jul 2024 03:23:25 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:c929ee59788ba55a6268320ad4288ecfa84d68bbe1c1f9de26a42b81ac59a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e779c9126971b3460a4247f1045fc333096220df484eeef1ddb915723581c6`

```dockerfile
```

-	Layers:
	-	`sha256:51efd760512e9b63b76ecb7cd5e5a3ac1351ef96ee157e9ed870f0e7ec9f80c9`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d16462c089873d7e5215598968921fd167d9517a2eb70d647aa28045c8d1d4`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240624` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:52f02170ee855755e55921e11207233a9c973614fc48e8f533122814451a9499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589506044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297ca0746061b2e6ea277b5742b6812557b79bd6d8ea316418d5c76ddd49a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfabac07be2024b8fccd8a3af3a59f3a7e09ff97be4ba2c865c11fdb0043d4`  
		Last Modified: Mon, 24 Jun 2024 18:29:46 GMT  
		Size: 328.2 MB (328245899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34314723ffd9e320fd561478044b50c27340c99b37eb43329ee689a4eb5429`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518aa46a6ed6e075ea9b5a39a1a60d40f8a676a9678de5e68fbe936e8c1cc8e`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e352ac21c2113b24b9a61063c2e7b22d0a8d2b8813d938b1b632e0694400c`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a97fa68e35c40e6ab7a5824874020d824108aec850e28d2097dd8c53e9e2e`  
		Last Modified: Mon, 24 Jun 2024 18:29:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:e3753d52d5a4d713fc351ed3d61e84b40b74ebf4dfd247844920534a4cb11cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41b0b10cdaeaa479067607a09d8713ea5a1ec05744340c3a7c7ac70115cf0d6`

```dockerfile
```

-	Layers:
	-	`sha256:2123ade5ac43e34b8bd186c470d9b1bc9662402a2ff5c4b1e85ea2b39d89bae1`  
		Last Modified: Mon, 24 Jun 2024 18:29:41 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340f4d6bb882266f1fa8bc5c6615fdfd5f43bf12ec40e02e984e1faef4ef64ed`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240624` - linux; ppc64le

```console
$ docker pull odoo@sha256:76a1170183ea3e1e614a3e76e10ad7de21f6e23ffa30d9cad9c07c35df584b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611177101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df0ae1009b13f5121c2bc2b2415a0e7f3f663ebd478133aa961c9017648be00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6db075a1a9dea80be197ad1d4dc2dc126691d190a41c4183938d85f3863e`  
		Last Modified: Mon, 24 Jun 2024 18:16:16 GMT  
		Size: 330.4 MB (330396320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282130baf4c896c22906d85c0838e337af019ad91416cfd9035440c48f60d3a8`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55709bb12b6c2542ae255950ca1e9610072f32e98e94fae28d07bdd5feccf972`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6285537b99b839b789d323dcb1bbc9b06b26704d3d94ed3f8af28d6747eb4`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342e12641dba5f6ef33d3d8f36315ac2e79f20e3d3a8657a3ea103a515937e5f`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:6d81886173938fb7968321b6254476c48c52a7e7c05db928f284c220be0ef270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38675920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9784ce9e348fbba540f04ab39c47b0b0e35acc076c0e3857e65ee93360ed561`

```dockerfile
```

-	Layers:
	-	`sha256:b05e653f8c0a61b63023a37e33469b1bc99acffdbe744ddb07b857ebe8fc9cef`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 38.6 MB (38648990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85116f7f8a479bc882b5cc0775762ee661c883f2bae113d1d13ac6480a51d5c1`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:cfd904b5cbdfb3857709e65e13bfae204a635e4d1bf208ff27bbc88335d06f99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:648f73f441f6c365796c85bd3c1c2981855dffbc2996efbd20885555dcc810c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594677171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a971c8e390d48f0f07140fed96db96d7963441919c74380f64f633ad020756c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ARG RELEASE
# Mon, 24 Jun 2024 09:13:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f61ce99eb895f5f57f2e577ba92d82405da2518f1754c4bedeec5fa9e3515d`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 233.7 MB (233723670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f296950c72ad7a88320aead36aa5339ae5f9339244ccfb62f6ce17854a3345fc`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 2.3 MB (2313751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1087908b082c60609c22ed2db4841f2fe1b534f767c75129f991a95a8ea2b7`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 460.2 KB (460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc2d985b0011a6433376d8c779e0f73df57334dc283e38b55967b7e40eee01`  
		Last Modified: Tue, 02 Jul 2024 03:23:28 GMT  
		Size: 328.6 MB (328643048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235871681e4bb561959bebc95dc884e102e8db333442971273762f9f3c87239`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5f8c48cc8c90b39e9c1f955ba04d288ff49a3760bdd127b98343f4ea99476f`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f249691be652760825dd298183e2a38338af4756b198657a04a6c72010ae85d`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef67c5b9c03e47f2467df88506a11f9d2a516c49e3782ec79e6f4b3f5fda015`  
		Last Modified: Tue, 02 Jul 2024 03:23:25 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c929ee59788ba55a6268320ad4288ecfa84d68bbe1c1f9de26a42b81ac59a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e779c9126971b3460a4247f1045fc333096220df484eeef1ddb915723581c6`

```dockerfile
```

-	Layers:
	-	`sha256:51efd760512e9b63b76ecb7cd5e5a3ac1351ef96ee157e9ed870f0e7ec9f80c9`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d16462c089873d7e5215598968921fd167d9517a2eb70d647aa28045c8d1d4`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:52f02170ee855755e55921e11207233a9c973614fc48e8f533122814451a9499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589506044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297ca0746061b2e6ea277b5742b6812557b79bd6d8ea316418d5c76ddd49a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfabac07be2024b8fccd8a3af3a59f3a7e09ff97be4ba2c865c11fdb0043d4`  
		Last Modified: Mon, 24 Jun 2024 18:29:46 GMT  
		Size: 328.2 MB (328245899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34314723ffd9e320fd561478044b50c27340c99b37eb43329ee689a4eb5429`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518aa46a6ed6e075ea9b5a39a1a60d40f8a676a9678de5e68fbe936e8c1cc8e`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e352ac21c2113b24b9a61063c2e7b22d0a8d2b8813d938b1b632e0694400c`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a97fa68e35c40e6ab7a5824874020d824108aec850e28d2097dd8c53e9e2e`  
		Last Modified: Mon, 24 Jun 2024 18:29:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e3753d52d5a4d713fc351ed3d61e84b40b74ebf4dfd247844920534a4cb11cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41b0b10cdaeaa479067607a09d8713ea5a1ec05744340c3a7c7ac70115cf0d6`

```dockerfile
```

-	Layers:
	-	`sha256:2123ade5ac43e34b8bd186c470d9b1bc9662402a2ff5c4b1e85ea2b39d89bae1`  
		Last Modified: Mon, 24 Jun 2024 18:29:41 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340f4d6bb882266f1fa8bc5c6615fdfd5f43bf12ec40e02e984e1faef4ef64ed`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:76a1170183ea3e1e614a3e76e10ad7de21f6e23ffa30d9cad9c07c35df584b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611177101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df0ae1009b13f5121c2bc2b2415a0e7f3f663ebd478133aa961c9017648be00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6db075a1a9dea80be197ad1d4dc2dc126691d190a41c4183938d85f3863e`  
		Last Modified: Mon, 24 Jun 2024 18:16:16 GMT  
		Size: 330.4 MB (330396320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282130baf4c896c22906d85c0838e337af019ad91416cfd9035440c48f60d3a8`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55709bb12b6c2542ae255950ca1e9610072f32e98e94fae28d07bdd5feccf972`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6285537b99b839b789d323dcb1bbc9b06b26704d3d94ed3f8af28d6747eb4`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342e12641dba5f6ef33d3d8f36315ac2e79f20e3d3a8657a3ea103a515937e5f`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6d81886173938fb7968321b6254476c48c52a7e7c05db928f284c220be0ef270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38675920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9784ce9e348fbba540f04ab39c47b0b0e35acc076c0e3857e65ee93360ed561`

```dockerfile
```

-	Layers:
	-	`sha256:b05e653f8c0a61b63023a37e33469b1bc99acffdbe744ddb07b857ebe8fc9cef`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 38.6 MB (38648990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85116f7f8a479bc882b5cc0775762ee661c883f2bae113d1d13ac6480a51d5c1`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json
