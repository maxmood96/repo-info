<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240711`](#odoo150-20240711)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240711`](#odoo160-20240711)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240711`](#odoo170-20240711)
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

## `odoo:15.0-20240711`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:16`

```console
$ docker pull odoo@sha256:8d0915960a70e4ed470c2fca2ce13c2950180bf71326a923dd5d778e398f0e28
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
$ docker pull odoo@sha256:1177992a1a6ade58c8b17073dd73c9507d38b86a49294f1cd8228062b39a1b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578772292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a370289c621009f8cda0acd765dedcde2fa02d07881460976de80583e6b695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5008088c99789a9cca9fd8d8572096fcb794156fa980930a84073a48b26ab2`  
		Last Modified: Tue, 02 Jul 2024 16:30:20 GMT  
		Size: 216.9 MB (216902307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df5fd8dbffefd07d94b6f5f1221e5dab3e54aa581ade1789d2ea15af811539e`  
		Last Modified: Tue, 02 Jul 2024 16:30:16 GMT  
		Size: 2.4 MB (2393343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e1c9fbb2dfea8256ae53600905e079d2d6cd2a09183ab0bb1a302dfd625c4c`  
		Last Modified: Tue, 02 Jul 2024 16:30:15 GMT  
		Size: 459.1 KB (459081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504a46d0df7d1748a4547f94764f357e5c7af815efcda27a6ac46d13cf4367f0`  
		Last Modified: Tue, 02 Jul 2024 16:30:24 GMT  
		Size: 328.9 MB (328945513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a74e0bf6868b9a166f4b83f59203d395fafa89dd1e985a5a76eab60cafed196`  
		Last Modified: Tue, 02 Jul 2024 16:30:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162e2aefbe0a4e5af8aa1a3cc451ba870dc3ac81a3cd1fd9d257755d203f39ef`  
		Last Modified: Tue, 02 Jul 2024 16:30:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de7f20f84f0c1dfb15e4554d73160ca0dec271db4b0704eee99543a30401705`  
		Last Modified: Tue, 02 Jul 2024 16:30:18 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97f36bd0a9096e5e440b3a5709eeb037ac20e29be2017c436bffee89339f09c`  
		Last Modified: Tue, 02 Jul 2024 16:30:18 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d52b799d60ce68d1d907bdae676df3500b14fd7cfc20bb4e5e9df008c75b0eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38582152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7f84c80df8576211beb4069875db9ccf9d6f89be839bc10d7baa888a1800db`

```dockerfile
```

-	Layers:
	-	`sha256:eb5ccc71703bcb8fa9aff8806779832d8751ce1752032964af086d558158f70d`  
		Last Modified: Tue, 02 Jul 2024 16:30:18 GMT  
		Size: 38.6 MB (38555314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80abcc3c83320c1b4e86746891210f1102792e219fa075ff392d51b1e45c6dd7`  
		Last Modified: Tue, 02 Jul 2024 16:30:15 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:7f1e307353f31227c8affd9188f843ecd8db81cb9950e84ad5593881bbd6dc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597711403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af84c4e6bb81ddeeb14f34cdde9609efc753d99d1042647f4ca360dea227cbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2366a685af706be6286ad4e282181ccb7f03487530109218173270d95756c`  
		Last Modified: Tue, 02 Jul 2024 11:51:28 GMT  
		Size: 228.6 MB (228589448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9071ecabb0fcf5b24b573e185f510d5e5becc8d551e53cf96a8dded0197136fe`  
		Last Modified: Tue, 02 Jul 2024 11:51:20 GMT  
		Size: 2.6 MB (2634061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d9dda7b0e53108bedb2e84d111eee7e04c7d730011b1d298c1b68b64f1f98`  
		Last Modified: Tue, 02 Jul 2024 11:51:19 GMT  
		Size: 459.1 KB (459106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef800364ca90eab13f5ef438496fb820ad7ae28ba389e9e13fd91f159c549770`  
		Last Modified: Tue, 02 Jul 2024 11:51:39 GMT  
		Size: 330.7 MB (330727167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf389ed988ecaa8c5007247fa18d38a39f65305b4983b0c83125fa33c340130a`  
		Last Modified: Tue, 02 Jul 2024 11:51:20 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29bdc03f831254a6598f294d0e4e6c9a1354aa36fbaf80280d3f70db35bd2b0`  
		Last Modified: Tue, 02 Jul 2024 11:51:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b852b8f534447acd6a7d79eb81d4cb3b487ca03ed0217230392b81845c7358`  
		Last Modified: Tue, 02 Jul 2024 11:51:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1cce39717f985a8abbdad0b75727c2718e5c0bf873bc8db62c648cbb5b8faf`  
		Last Modified: Tue, 02 Jul 2024 11:51:22 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:57e057a33b5d376913c3629899d6f19e43e8f43ab0bd635b522ab8705eeb4242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38583564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222e9743cbff3ab32ca89cdef8bb89ff2783ef5627af13c19ef1e029e908a50`

```dockerfile
```

-	Layers:
	-	`sha256:2165174aeedaf5d3eb8cd857d7ac607af4dc1788b14d2b0e623b4d177ef4b4ee`  
		Last Modified: Tue, 02 Jul 2024 11:51:21 GMT  
		Size: 38.6 MB (38556974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fb3bf469ed34cdd524a9156b00e29c4e74b46420b48dcc80fe8d37fd6f9475`  
		Last Modified: Tue, 02 Jul 2024 11:51:19 GMT  
		Size: 26.6 KB (26590 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:8d0915960a70e4ed470c2fca2ce13c2950180bf71326a923dd5d778e398f0e28
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
$ docker pull odoo@sha256:1177992a1a6ade58c8b17073dd73c9507d38b86a49294f1cd8228062b39a1b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578772292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a370289c621009f8cda0acd765dedcde2fa02d07881460976de80583e6b695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5008088c99789a9cca9fd8d8572096fcb794156fa980930a84073a48b26ab2`  
		Last Modified: Tue, 02 Jul 2024 16:30:20 GMT  
		Size: 216.9 MB (216902307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df5fd8dbffefd07d94b6f5f1221e5dab3e54aa581ade1789d2ea15af811539e`  
		Last Modified: Tue, 02 Jul 2024 16:30:16 GMT  
		Size: 2.4 MB (2393343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e1c9fbb2dfea8256ae53600905e079d2d6cd2a09183ab0bb1a302dfd625c4c`  
		Last Modified: Tue, 02 Jul 2024 16:30:15 GMT  
		Size: 459.1 KB (459081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504a46d0df7d1748a4547f94764f357e5c7af815efcda27a6ac46d13cf4367f0`  
		Last Modified: Tue, 02 Jul 2024 16:30:24 GMT  
		Size: 328.9 MB (328945513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a74e0bf6868b9a166f4b83f59203d395fafa89dd1e985a5a76eab60cafed196`  
		Last Modified: Tue, 02 Jul 2024 16:30:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162e2aefbe0a4e5af8aa1a3cc451ba870dc3ac81a3cd1fd9d257755d203f39ef`  
		Last Modified: Tue, 02 Jul 2024 16:30:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de7f20f84f0c1dfb15e4554d73160ca0dec271db4b0704eee99543a30401705`  
		Last Modified: Tue, 02 Jul 2024 16:30:18 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97f36bd0a9096e5e440b3a5709eeb037ac20e29be2017c436bffee89339f09c`  
		Last Modified: Tue, 02 Jul 2024 16:30:18 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d52b799d60ce68d1d907bdae676df3500b14fd7cfc20bb4e5e9df008c75b0eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38582152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7f84c80df8576211beb4069875db9ccf9d6f89be839bc10d7baa888a1800db`

```dockerfile
```

-	Layers:
	-	`sha256:eb5ccc71703bcb8fa9aff8806779832d8751ce1752032964af086d558158f70d`  
		Last Modified: Tue, 02 Jul 2024 16:30:18 GMT  
		Size: 38.6 MB (38555314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80abcc3c83320c1b4e86746891210f1102792e219fa075ff392d51b1e45c6dd7`  
		Last Modified: Tue, 02 Jul 2024 16:30:15 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:7f1e307353f31227c8affd9188f843ecd8db81cb9950e84ad5593881bbd6dc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597711403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af84c4e6bb81ddeeb14f34cdde9609efc753d99d1042647f4ca360dea227cbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2366a685af706be6286ad4e282181ccb7f03487530109218173270d95756c`  
		Last Modified: Tue, 02 Jul 2024 11:51:28 GMT  
		Size: 228.6 MB (228589448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9071ecabb0fcf5b24b573e185f510d5e5becc8d551e53cf96a8dded0197136fe`  
		Last Modified: Tue, 02 Jul 2024 11:51:20 GMT  
		Size: 2.6 MB (2634061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d9dda7b0e53108bedb2e84d111eee7e04c7d730011b1d298c1b68b64f1f98`  
		Last Modified: Tue, 02 Jul 2024 11:51:19 GMT  
		Size: 459.1 KB (459106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef800364ca90eab13f5ef438496fb820ad7ae28ba389e9e13fd91f159c549770`  
		Last Modified: Tue, 02 Jul 2024 11:51:39 GMT  
		Size: 330.7 MB (330727167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf389ed988ecaa8c5007247fa18d38a39f65305b4983b0c83125fa33c340130a`  
		Last Modified: Tue, 02 Jul 2024 11:51:20 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29bdc03f831254a6598f294d0e4e6c9a1354aa36fbaf80280d3f70db35bd2b0`  
		Last Modified: Tue, 02 Jul 2024 11:51:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b852b8f534447acd6a7d79eb81d4cb3b487ca03ed0217230392b81845c7358`  
		Last Modified: Tue, 02 Jul 2024 11:51:21 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1cce39717f985a8abbdad0b75727c2718e5c0bf873bc8db62c648cbb5b8faf`  
		Last Modified: Tue, 02 Jul 2024 11:51:22 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:57e057a33b5d376913c3629899d6f19e43e8f43ab0bd635b522ab8705eeb4242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38583564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c222e9743cbff3ab32ca89cdef8bb89ff2783ef5627af13c19ef1e029e908a50`

```dockerfile
```

-	Layers:
	-	`sha256:2165174aeedaf5d3eb8cd857d7ac607af4dc1788b14d2b0e623b4d177ef4b4ee`  
		Last Modified: Tue, 02 Jul 2024 11:51:21 GMT  
		Size: 38.6 MB (38556974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fb3bf469ed34cdd524a9156b00e29c4e74b46420b48dcc80fe8d37fd6f9475`  
		Last Modified: Tue, 02 Jul 2024 11:51:19 GMT  
		Size: 26.6 KB (26590 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240711`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:17`

```console
$ docker pull odoo@sha256:659aa6c82eac446e1167701b823ca50270d8e3620bfdcb3f5e850b95cfa30a30
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
$ docker pull odoo@sha256:6f6a342acd83e75f0a8823b4752a907b2d2542742092f890f66b4b2be81e515a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589499297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f93978783058b7e08cf76f6e6d86f72e6f138deffbcc7939f548af6d3536a0`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38892debd8f7b1a6d3edecbfcabcd2c55f64c5bf2d9c950814ff9e28c374d117`  
		Last Modified: Tue, 02 Jul 2024 16:25:24 GMT  
		Size: 231.1 MB (231129344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33bd67e4fb7a220c0a754507380b8f0cb42ea0d52e5d2a77e94d95ef75b87d3`  
		Last Modified: Tue, 02 Jul 2024 16:25:20 GMT  
		Size: 2.3 MB (2306449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a24f6195fdd859a502bea9c6acc99fc1f29c6cd17516bd3ff315855a8d9c77c`  
		Last Modified: Tue, 02 Jul 2024 16:25:20 GMT  
		Size: 460.2 KB (460200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b8feb41e84ef3f81148dee7bec042bc24f5b69ec519052e767f09c2e17184`  
		Last Modified: Tue, 02 Jul 2024 16:25:35 GMT  
		Size: 328.2 MB (328240843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18840c92b05b627faf4eb25c71960402825365c3bef6b9e456a4516bdb9642`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1a8b8868e6432ac928abecfd7c73e373ef880dc3857d89bcdb11d3ef762516`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9870824078f0b1d91cbb5bcf246dd81ff32f3db970a0196a9c81217b2522ff`  
		Last Modified: Tue, 02 Jul 2024 16:25:22 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24d15be22771fbc78ab4f66df56e5a6c6e0ddb57c9f5518c8f7a882aa9966c9`  
		Last Modified: Tue, 02 Jul 2024 16:25:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f07e07560ae4327f3c772d1acaec1d0eb94c6cf375389886f24c296f2f3575e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f092650bc64217a184b423f4b2ddb86221dad4492a66cece40210ea13ab007b`

```dockerfile
```

-	Layers:
	-	`sha256:d0c7e0943978028051b6a1cf3f3faf0b6bb8c69e9d65505db4e75b95a0628bea`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a457b089044bc1757fc864a18899bbc9520ccaa654f89e8dc4e78116806fca99`  
		Last Modified: Tue, 02 Jul 2024 16:25:19 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:e2640cb796634fa292466ff18af959e9d6fbc073673a4d8227821b2ccdf93355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611417433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122fd2e74b4f577d85a3de9485c4c654224f2d577c680efea6d000472a986f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jul 2024 09:17:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jul 2024 09:17:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
USER odoo
# Thu, 11 Jul 2024 09:17:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459fc9beeaf8a55196e594d64d56605d3f7f5ee6b009bcedb296baee0f55afa6`  
		Last Modified: Thu, 11 Jul 2024 18:12:19 GMT  
		Size: 243.3 MB (243275080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188a455585f87f6a53aedf08965b76fdf3c420b7520453c7ce26cbdda56d5719`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 2.6 MB (2590403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e820aa8a3bc25cdf789603ae3cf89e79611ac799658288db81dd7c559681a9b`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 460.3 KB (460296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d59c838bfa2841533c289e863d2dee38b825dac7c71c4684fd740336e5d1f8`  
		Last Modified: Thu, 11 Jul 2024 18:12:21 GMT  
		Size: 330.6 MB (330628132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55b166028d8e1fb37de5da4392b2c6da8ed832bcfb492d53c74a25feda0d0f`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02512aa46d52ee3d5c2b53aa74e8db28c24879e8457101822ff0b994d0caf00d`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f548d8460c32f2eb64982c1625526a95ad10b33d51343f7e0b9d385f57cda`  
		Last Modified: Thu, 11 Jul 2024 18:12:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de18390fe4fae002a8d231f5f643f173dfa96b875382adfe0429140970aded5`  
		Last Modified: Thu, 11 Jul 2024 18:12:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:12f06137735a154df22f613b83933d060271050a8b48a943bcd37948c0ec00a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c816ef75e803a13dd505d68dbd3d13daf8b1d1927eda185f23535f0770dea4a3`

```dockerfile
```

-	Layers:
	-	`sha256:4649b9a88613cfdc7690c9074f0efdf23395b8b8fbcd7275a2ce6b9adc5631dd`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 38.7 MB (38701943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736f140df0b5a35cb33d6f703c930aded005bd44fa67369ce88f8e3102965405`  
		Last Modified: Thu, 11 Jul 2024 18:12:12 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:659aa6c82eac446e1167701b823ca50270d8e3620bfdcb3f5e850b95cfa30a30
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
$ docker pull odoo@sha256:6f6a342acd83e75f0a8823b4752a907b2d2542742092f890f66b4b2be81e515a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589499297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f93978783058b7e08cf76f6e6d86f72e6f138deffbcc7939f548af6d3536a0`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38892debd8f7b1a6d3edecbfcabcd2c55f64c5bf2d9c950814ff9e28c374d117`  
		Last Modified: Tue, 02 Jul 2024 16:25:24 GMT  
		Size: 231.1 MB (231129344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33bd67e4fb7a220c0a754507380b8f0cb42ea0d52e5d2a77e94d95ef75b87d3`  
		Last Modified: Tue, 02 Jul 2024 16:25:20 GMT  
		Size: 2.3 MB (2306449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a24f6195fdd859a502bea9c6acc99fc1f29c6cd17516bd3ff315855a8d9c77c`  
		Last Modified: Tue, 02 Jul 2024 16:25:20 GMT  
		Size: 460.2 KB (460200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b8feb41e84ef3f81148dee7bec042bc24f5b69ec519052e767f09c2e17184`  
		Last Modified: Tue, 02 Jul 2024 16:25:35 GMT  
		Size: 328.2 MB (328240843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18840c92b05b627faf4eb25c71960402825365c3bef6b9e456a4516bdb9642`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1a8b8868e6432ac928abecfd7c73e373ef880dc3857d89bcdb11d3ef762516`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9870824078f0b1d91cbb5bcf246dd81ff32f3db970a0196a9c81217b2522ff`  
		Last Modified: Tue, 02 Jul 2024 16:25:22 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24d15be22771fbc78ab4f66df56e5a6c6e0ddb57c9f5518c8f7a882aa9966c9`  
		Last Modified: Tue, 02 Jul 2024 16:25:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f07e07560ae4327f3c772d1acaec1d0eb94c6cf375389886f24c296f2f3575e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f092650bc64217a184b423f4b2ddb86221dad4492a66cece40210ea13ab007b`

```dockerfile
```

-	Layers:
	-	`sha256:d0c7e0943978028051b6a1cf3f3faf0b6bb8c69e9d65505db4e75b95a0628bea`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a457b089044bc1757fc864a18899bbc9520ccaa654f89e8dc4e78116806fca99`  
		Last Modified: Tue, 02 Jul 2024 16:25:19 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e2640cb796634fa292466ff18af959e9d6fbc073673a4d8227821b2ccdf93355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611417433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122fd2e74b4f577d85a3de9485c4c654224f2d577c680efea6d000472a986f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jul 2024 09:17:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jul 2024 09:17:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
USER odoo
# Thu, 11 Jul 2024 09:17:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459fc9beeaf8a55196e594d64d56605d3f7f5ee6b009bcedb296baee0f55afa6`  
		Last Modified: Thu, 11 Jul 2024 18:12:19 GMT  
		Size: 243.3 MB (243275080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188a455585f87f6a53aedf08965b76fdf3c420b7520453c7ce26cbdda56d5719`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 2.6 MB (2590403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e820aa8a3bc25cdf789603ae3cf89e79611ac799658288db81dd7c559681a9b`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 460.3 KB (460296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d59c838bfa2841533c289e863d2dee38b825dac7c71c4684fd740336e5d1f8`  
		Last Modified: Thu, 11 Jul 2024 18:12:21 GMT  
		Size: 330.6 MB (330628132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55b166028d8e1fb37de5da4392b2c6da8ed832bcfb492d53c74a25feda0d0f`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02512aa46d52ee3d5c2b53aa74e8db28c24879e8457101822ff0b994d0caf00d`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f548d8460c32f2eb64982c1625526a95ad10b33d51343f7e0b9d385f57cda`  
		Last Modified: Thu, 11 Jul 2024 18:12:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de18390fe4fae002a8d231f5f643f173dfa96b875382adfe0429140970aded5`  
		Last Modified: Thu, 11 Jul 2024 18:12:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:12f06137735a154df22f613b83933d060271050a8b48a943bcd37948c0ec00a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c816ef75e803a13dd505d68dbd3d13daf8b1d1927eda185f23535f0770dea4a3`

```dockerfile
```

-	Layers:
	-	`sha256:4649b9a88613cfdc7690c9074f0efdf23395b8b8fbcd7275a2ce6b9adc5631dd`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 38.7 MB (38701943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736f140df0b5a35cb33d6f703c930aded005bd44fa67369ce88f8e3102965405`  
		Last Modified: Thu, 11 Jul 2024 18:12:12 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240711`

```console
$ docker pull odoo@sha256:a71d3f7437b9e77cc6f951070b500bb74cf4d71d992764eb5a12413459765f89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240711` - linux; ppc64le

```console
$ docker pull odoo@sha256:e2640cb796634fa292466ff18af959e9d6fbc073673a4d8227821b2ccdf93355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611417433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122fd2e74b4f577d85a3de9485c4c654224f2d577c680efea6d000472a986f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jul 2024 09:17:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jul 2024 09:17:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
USER odoo
# Thu, 11 Jul 2024 09:17:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459fc9beeaf8a55196e594d64d56605d3f7f5ee6b009bcedb296baee0f55afa6`  
		Last Modified: Thu, 11 Jul 2024 18:12:19 GMT  
		Size: 243.3 MB (243275080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188a455585f87f6a53aedf08965b76fdf3c420b7520453c7ce26cbdda56d5719`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 2.6 MB (2590403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e820aa8a3bc25cdf789603ae3cf89e79611ac799658288db81dd7c559681a9b`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 460.3 KB (460296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d59c838bfa2841533c289e863d2dee38b825dac7c71c4684fd740336e5d1f8`  
		Last Modified: Thu, 11 Jul 2024 18:12:21 GMT  
		Size: 330.6 MB (330628132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55b166028d8e1fb37de5da4392b2c6da8ed832bcfb492d53c74a25feda0d0f`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02512aa46d52ee3d5c2b53aa74e8db28c24879e8457101822ff0b994d0caf00d`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f548d8460c32f2eb64982c1625526a95ad10b33d51343f7e0b9d385f57cda`  
		Last Modified: Thu, 11 Jul 2024 18:12:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de18390fe4fae002a8d231f5f643f173dfa96b875382adfe0429140970aded5`  
		Last Modified: Thu, 11 Jul 2024 18:12:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:12f06137735a154df22f613b83933d060271050a8b48a943bcd37948c0ec00a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c816ef75e803a13dd505d68dbd3d13daf8b1d1927eda185f23535f0770dea4a3`

```dockerfile
```

-	Layers:
	-	`sha256:4649b9a88613cfdc7690c9074f0efdf23395b8b8fbcd7275a2ce6b9adc5631dd`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 38.7 MB (38701943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736f140df0b5a35cb33d6f703c930aded005bd44fa67369ce88f8e3102965405`  
		Last Modified: Thu, 11 Jul 2024 18:12:12 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:659aa6c82eac446e1167701b823ca50270d8e3620bfdcb3f5e850b95cfa30a30
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
$ docker pull odoo@sha256:6f6a342acd83e75f0a8823b4752a907b2d2542742092f890f66b4b2be81e515a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589499297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f93978783058b7e08cf76f6e6d86f72e6f138deffbcc7939f548af6d3536a0`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38892debd8f7b1a6d3edecbfcabcd2c55f64c5bf2d9c950814ff9e28c374d117`  
		Last Modified: Tue, 02 Jul 2024 16:25:24 GMT  
		Size: 231.1 MB (231129344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33bd67e4fb7a220c0a754507380b8f0cb42ea0d52e5d2a77e94d95ef75b87d3`  
		Last Modified: Tue, 02 Jul 2024 16:25:20 GMT  
		Size: 2.3 MB (2306449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a24f6195fdd859a502bea9c6acc99fc1f29c6cd17516bd3ff315855a8d9c77c`  
		Last Modified: Tue, 02 Jul 2024 16:25:20 GMT  
		Size: 460.2 KB (460200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b8feb41e84ef3f81148dee7bec042bc24f5b69ec519052e767f09c2e17184`  
		Last Modified: Tue, 02 Jul 2024 16:25:35 GMT  
		Size: 328.2 MB (328240843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18840c92b05b627faf4eb25c71960402825365c3bef6b9e456a4516bdb9642`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1a8b8868e6432ac928abecfd7c73e373ef880dc3857d89bcdb11d3ef762516`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9870824078f0b1d91cbb5bcf246dd81ff32f3db970a0196a9c81217b2522ff`  
		Last Modified: Tue, 02 Jul 2024 16:25:22 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24d15be22771fbc78ab4f66df56e5a6c6e0ddb57c9f5518c8f7a882aa9966c9`  
		Last Modified: Tue, 02 Jul 2024 16:25:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f07e07560ae4327f3c772d1acaec1d0eb94c6cf375389886f24c296f2f3575e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f092650bc64217a184b423f4b2ddb86221dad4492a66cece40210ea13ab007b`

```dockerfile
```

-	Layers:
	-	`sha256:d0c7e0943978028051b6a1cf3f3faf0b6bb8c69e9d65505db4e75b95a0628bea`  
		Last Modified: Tue, 02 Jul 2024 16:25:21 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a457b089044bc1757fc864a18899bbc9520ccaa654f89e8dc4e78116806fca99`  
		Last Modified: Tue, 02 Jul 2024 16:25:19 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:e2640cb796634fa292466ff18af959e9d6fbc073673a4d8227821b2ccdf93355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611417433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122fd2e74b4f577d85a3de9485c4c654224f2d577c680efea6d000472a986f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 11 Jul 2024 09:17:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 11 Jul 2024 09:17:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
USER odoo
# Thu, 11 Jul 2024 09:17:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459fc9beeaf8a55196e594d64d56605d3f7f5ee6b009bcedb296baee0f55afa6`  
		Last Modified: Thu, 11 Jul 2024 18:12:19 GMT  
		Size: 243.3 MB (243275080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188a455585f87f6a53aedf08965b76fdf3c420b7520453c7ce26cbdda56d5719`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 2.6 MB (2590403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e820aa8a3bc25cdf789603ae3cf89e79611ac799658288db81dd7c559681a9b`  
		Last Modified: Thu, 11 Jul 2024 18:12:13 GMT  
		Size: 460.3 KB (460296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d59c838bfa2841533c289e863d2dee38b825dac7c71c4684fd740336e5d1f8`  
		Last Modified: Thu, 11 Jul 2024 18:12:21 GMT  
		Size: 330.6 MB (330628132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55b166028d8e1fb37de5da4392b2c6da8ed832bcfb492d53c74a25feda0d0f`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02512aa46d52ee3d5c2b53aa74e8db28c24879e8457101822ff0b994d0caf00d`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f548d8460c32f2eb64982c1625526a95ad10b33d51343f7e0b9d385f57cda`  
		Last Modified: Thu, 11 Jul 2024 18:12:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de18390fe4fae002a8d231f5f643f173dfa96b875382adfe0429140970aded5`  
		Last Modified: Thu, 11 Jul 2024 18:12:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:12f06137735a154df22f613b83933d060271050a8b48a943bcd37948c0ec00a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38728874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c816ef75e803a13dd505d68dbd3d13daf8b1d1927eda185f23535f0770dea4a3`

```dockerfile
```

-	Layers:
	-	`sha256:4649b9a88613cfdc7690c9074f0efdf23395b8b8fbcd7275a2ce6b9adc5631dd`  
		Last Modified: Thu, 11 Jul 2024 18:12:14 GMT  
		Size: 38.7 MB (38701943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736f140df0b5a35cb33d6f703c930aded005bd44fa67369ce88f8e3102965405`  
		Last Modified: Thu, 11 Jul 2024 18:12:12 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
