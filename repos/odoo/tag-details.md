<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240812`](#odoo150-20240812)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240812`](#odoo160-20240812)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240812`](#odoo170-20240812)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:cf95ea54bdf929424c9c40440d563b4f31a3d2162567439e553781733c3cc008
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:4a6b24c15aa0b8a02d263a82aaea8b78b0d8f55ab3fddca1cc13d3d620274775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563991080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55abd9ff2696369724a89e829e465a6f5ceaa65ae8ff36c3cb19b53d3984e5fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=15.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268ae8db7e5c562bd6af45b5a241ad1515d995c3157766145fba4e74937d9d9`  
		Last Modified: Tue, 13 Aug 2024 01:14:51 GMT  
		Size: 220.3 MB (220280846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be681224f0f3b55b97c87ae9e2ef09873a75a94480eaaae78f9b041c217aef2`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 2.4 MB (2387737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e474e50d54c6a39562830823976480e6a1dab7600cb29532b80f70051ca1b44`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 463.8 KB (463818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90f13110353775493a1206503919ed92d7e9135439b36883963440e4cf95d9`  
		Last Modified: Tue, 13 Aug 2024 01:14:58 GMT  
		Size: 309.4 MB (309427967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a309d1f962e2ed9b76650db55af8538f9ecb0f19b6552ed78b14530e273b81`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6509e81990e837be353575cc8cc2ac1a756bcfeecfbee6b87a16fe856c2cd9a`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0754a09c5acf1be7bff37ae56c9cc5a9a23162fbb6147a07f8be29d1d2c9f7ac`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6880f401bd4ecf3589a497a02a8b858a2780ab67e4cabaa5612e18123dc53e9`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:b081b129349044a9bd331f51b0c84a53f35f27d0229171fdf6fbe9dbbac7f0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2f8d83db028136832f2cb056961426e81bc7867385ee8af5ad2bb38db156cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a364b9e881aa05d8f46bd27e3bbd0ac2c0c74392741c2bae6b5e5adbdbf8329`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2492e3baad359a707f5c01e040ccddff3d1c8fee44b1a3fe460f7c791af3bbb8`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:cf95ea54bdf929424c9c40440d563b4f31a3d2162567439e553781733c3cc008
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:4a6b24c15aa0b8a02d263a82aaea8b78b0d8f55ab3fddca1cc13d3d620274775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563991080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55abd9ff2696369724a89e829e465a6f5ceaa65ae8ff36c3cb19b53d3984e5fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=15.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268ae8db7e5c562bd6af45b5a241ad1515d995c3157766145fba4e74937d9d9`  
		Last Modified: Tue, 13 Aug 2024 01:14:51 GMT  
		Size: 220.3 MB (220280846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be681224f0f3b55b97c87ae9e2ef09873a75a94480eaaae78f9b041c217aef2`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 2.4 MB (2387737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e474e50d54c6a39562830823976480e6a1dab7600cb29532b80f70051ca1b44`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 463.8 KB (463818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90f13110353775493a1206503919ed92d7e9135439b36883963440e4cf95d9`  
		Last Modified: Tue, 13 Aug 2024 01:14:58 GMT  
		Size: 309.4 MB (309427967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a309d1f962e2ed9b76650db55af8538f9ecb0f19b6552ed78b14530e273b81`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6509e81990e837be353575cc8cc2ac1a756bcfeecfbee6b87a16fe856c2cd9a`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0754a09c5acf1be7bff37ae56c9cc5a9a23162fbb6147a07f8be29d1d2c9f7ac`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6880f401bd4ecf3589a497a02a8b858a2780ab67e4cabaa5612e18123dc53e9`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b081b129349044a9bd331f51b0c84a53f35f27d0229171fdf6fbe9dbbac7f0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2f8d83db028136832f2cb056961426e81bc7867385ee8af5ad2bb38db156cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a364b9e881aa05d8f46bd27e3bbd0ac2c0c74392741c2bae6b5e5adbdbf8329`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2492e3baad359a707f5c01e040ccddff3d1c8fee44b1a3fe460f7c791af3bbb8`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240812`

```console
$ docker pull odoo@sha256:cf95ea54bdf929424c9c40440d563b4f31a3d2162567439e553781733c3cc008
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240812` - linux; amd64

```console
$ docker pull odoo@sha256:4a6b24c15aa0b8a02d263a82aaea8b78b0d8f55ab3fddca1cc13d3d620274775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563991080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55abd9ff2696369724a89e829e465a6f5ceaa65ae8ff36c3cb19b53d3984e5fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=15.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268ae8db7e5c562bd6af45b5a241ad1515d995c3157766145fba4e74937d9d9`  
		Last Modified: Tue, 13 Aug 2024 01:14:51 GMT  
		Size: 220.3 MB (220280846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be681224f0f3b55b97c87ae9e2ef09873a75a94480eaaae78f9b041c217aef2`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 2.4 MB (2387737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e474e50d54c6a39562830823976480e6a1dab7600cb29532b80f70051ca1b44`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 463.8 KB (463818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90f13110353775493a1206503919ed92d7e9135439b36883963440e4cf95d9`  
		Last Modified: Tue, 13 Aug 2024 01:14:58 GMT  
		Size: 309.4 MB (309427967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a309d1f962e2ed9b76650db55af8538f9ecb0f19b6552ed78b14530e273b81`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6509e81990e837be353575cc8cc2ac1a756bcfeecfbee6b87a16fe856c2cd9a`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0754a09c5acf1be7bff37ae56c9cc5a9a23162fbb6147a07f8be29d1d2c9f7ac`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6880f401bd4ecf3589a497a02a8b858a2780ab67e4cabaa5612e18123dc53e9`  
		Last Modified: Tue, 13 Aug 2024 01:14:48 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:b081b129349044a9bd331f51b0c84a53f35f27d0229171fdf6fbe9dbbac7f0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2f8d83db028136832f2cb056961426e81bc7867385ee8af5ad2bb38db156cc`

```dockerfile
```

-	Layers:
	-	`sha256:5a364b9e881aa05d8f46bd27e3bbd0ac2c0c74392741c2bae6b5e5adbdbf8329`  
		Last Modified: Tue, 13 Aug 2024 01:14:47 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2492e3baad359a707f5c01e040ccddff3d1c8fee44b1a3fe460f7c791af3bbb8`  
		Last Modified: Tue, 13 Aug 2024 01:14:46 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:53c2d400d604e9fe3cbaa86993e57b13c151b079758a173a0c16660270c9d68c
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
$ docker pull odoo@sha256:b93543cd01dd638138f484569ad4b6aef7ba9cf7dedf5fc36209dc34db449806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583511501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666949e89b97e235f86149da5e8b7321b5f05869d49bd1707795e02f82f975fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fdf6473465ea33d489dd8d1401903da83765f432366a1783d9bb981ef78d3`  
		Last Modified: Tue, 13 Aug 2024 01:14:35 GMT  
		Size: 219.6 MB (219593472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9acc0d5dbedf559219071e2a5de8d1f5c7a1e2cdc1f98aa12cb4e8686d41cb`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 2.4 MB (2391422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20341a02dfa69d8f063050db77027b9c0621d1b041495fb4cd3950e377d048be`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 463.8 KB (463823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d419af5ecb2af82efea4abf82cd55d40291310519938c283edf1bb9adf319`  
		Last Modified: Tue, 13 Aug 2024 01:14:37 GMT  
		Size: 329.6 MB (329632063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ea66e14ee62164410b94bf17e2edad91a3dce48167403742612dab15a40448`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd171703a80c3ed47282cbfcb984d384e5787ff2808d44256a99980954a223`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c55f1e40bd988cc92a4a935c1e639b983ab8d487f98f9de90d5d9f0b3b060`  
		Last Modified: Tue, 13 Aug 2024 01:14:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01d42da3282572b995860a7218a808cb2239a57148206fa0dbd020aed2e934d`  
		Last Modified: Tue, 13 Aug 2024 01:14:34 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e2e86b94639fb6e7cbb8e545d9a983f2c328c46cac88ca47105ba328229da7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94687a547b729ed2bad16b13cbd0d0e38741fa1a28c5ad9e178dfc0ed3378ff4`

```dockerfile
```

-	Layers:
	-	`sha256:44e2361fdb1dbb1c17f5785ac0fd0adb78606d5a2ecd809da64a2d1f08f446ce`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba14f5d93e588e5982db97bcb3e4f9c08bffd03cdc2affbad642b78d35f0e8be`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e463cb143a03b85db5b9da4d68ac48ed4b1a01a20bd464e71cb717ce119822e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579093474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd067560524cc63462f4278c8c40c4d576bc46290829d13520448e0a7dee98d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be25eb721d0419861312b5df4f760175b71b580acb4cad43e26b6d9957190c`  
		Last Modified: Tue, 13 Aug 2024 07:54:00 GMT  
		Size: 216.9 MB (216902583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a43f1300414424575a08b49f9201e117a4a1d53d64d5c2767c4a73c50166da7`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 2.4 MB (2393972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf254f4f3ea16d9bf889ec96ccd335ffcc6f1a967562358a594213f3adb3be5`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 463.8 KB (463817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960cf8e2325ce93efb1bee2af9bd272dedf094cddb25b3549bd702f50dbe7e9d`  
		Last Modified: Tue, 13 Aug 2024 07:54:02 GMT  
		Size: 329.3 MB (329254583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466db4a214fba1c6ca81e1e5a33cfb8dde1da25c415d803557a8584d6b19af`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf753fd18a0920218b18f47c95f78f1f58e5e4cb2c9ecddde5f175077fe74bc7`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9677c42f975e839011d4c8223e71eb16b32f1aa2c294aaffba2ebdccc8b8f8`  
		Last Modified: Tue, 13 Aug 2024 07:53:57 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc29ee35071121afdcf7e33610cb15246d126fe05dd3757cacee3f8ad284cf4`  
		Last Modified: Tue, 13 Aug 2024 07:53:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:45b4a7fc88fc5801201e29759a545b66a18af29c3e69d95d941e12e0ec4e8333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c054d74241693b00268175f2d3a3702e2e349a43172789daae53c7fdcbb384`

```dockerfile
```

-	Layers:
	-	`sha256:88637c3f85bbc8be13d93d3fb0572445bddde1d6cfc18a136771eb674b7edfb8`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2961b29ee635ee980a0ec0568733d1e771392b3144386610e3c0e0030514a9`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:65ec19b08590d107425059f3a182bb24ac07077fbdec749bff3cba74f0fc43be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (598010212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f89c8fdd160261989d8ac12df49e273c546a2f4d83601f662e93d9998de9ada`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51f6a8ccad777c520085b7be04b567b1681a30689bc7279bec9698039227b6`  
		Last Modified: Tue, 13 Aug 2024 07:33:38 GMT  
		Size: 228.6 MB (228589771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601fcd0df6f8eed975a21fc58023759c73318ab41b55b5b9ab0971209cd6026a`  
		Last Modified: Tue, 13 Aug 2024 07:33:33 GMT  
		Size: 2.6 MB (2634236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e218dd53f839d1853febf0b40e8303109791c4e0608dd4cca64fc3261fcc39b`  
		Last Modified: Tue, 13 Aug 2024 07:33:32 GMT  
		Size: 463.8 KB (463847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc79d60ed1ad314810962604a5b9ac7223894216ddf28e9936dde0c19da5572`  
		Last Modified: Tue, 13 Aug 2024 07:33:41 GMT  
		Size: 331.0 MB (331014791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10840c11556949f0a89a8435d9540282103cee1893be856f5dba895214ba7ad4`  
		Last Modified: Tue, 13 Aug 2024 07:33:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d94553d57f03b8413845962aef840506a551a807e154fab8452bef155e7097`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceaf49991f5a3f167e9b41f0b9322cd0c89435ccd8ff2e490301f20650f5c2c`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83355aaea56f6c37888f0166cda6c7e1a56a76f25b306de6abbcce28f07aa86b`  
		Last Modified: Tue, 13 Aug 2024 07:33:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c1d8aa2e1b1bd2b78e6ae93e19a913b4f4b935ead17825800cdbace7f0b01e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097e03fbc34153c1682b7a89355196149e33109828bea47e9bd9f65b58f20cf2`

```dockerfile
```

-	Layers:
	-	`sha256:d625bec2bec9edadd6ceb6dface3c4ef00c17e1fe2015c9703b4860300e4cfec`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea46bbcae11b5366a43d4fec11d2406966aebb855e5e0acfe60eba4a9e88e60`  
		Last Modified: Tue, 13 Aug 2024 07:33:32 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:53c2d400d604e9fe3cbaa86993e57b13c151b079758a173a0c16660270c9d68c
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
$ docker pull odoo@sha256:b93543cd01dd638138f484569ad4b6aef7ba9cf7dedf5fc36209dc34db449806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583511501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666949e89b97e235f86149da5e8b7321b5f05869d49bd1707795e02f82f975fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fdf6473465ea33d489dd8d1401903da83765f432366a1783d9bb981ef78d3`  
		Last Modified: Tue, 13 Aug 2024 01:14:35 GMT  
		Size: 219.6 MB (219593472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9acc0d5dbedf559219071e2a5de8d1f5c7a1e2cdc1f98aa12cb4e8686d41cb`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 2.4 MB (2391422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20341a02dfa69d8f063050db77027b9c0621d1b041495fb4cd3950e377d048be`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 463.8 KB (463823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d419af5ecb2af82efea4abf82cd55d40291310519938c283edf1bb9adf319`  
		Last Modified: Tue, 13 Aug 2024 01:14:37 GMT  
		Size: 329.6 MB (329632063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ea66e14ee62164410b94bf17e2edad91a3dce48167403742612dab15a40448`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd171703a80c3ed47282cbfcb984d384e5787ff2808d44256a99980954a223`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c55f1e40bd988cc92a4a935c1e639b983ab8d487f98f9de90d5d9f0b3b060`  
		Last Modified: Tue, 13 Aug 2024 01:14:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01d42da3282572b995860a7218a808cb2239a57148206fa0dbd020aed2e934d`  
		Last Modified: Tue, 13 Aug 2024 01:14:34 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e2e86b94639fb6e7cbb8e545d9a983f2c328c46cac88ca47105ba328229da7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94687a547b729ed2bad16b13cbd0d0e38741fa1a28c5ad9e178dfc0ed3378ff4`

```dockerfile
```

-	Layers:
	-	`sha256:44e2361fdb1dbb1c17f5785ac0fd0adb78606d5a2ecd809da64a2d1f08f446ce`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba14f5d93e588e5982db97bcb3e4f9c08bffd03cdc2affbad642b78d35f0e8be`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e463cb143a03b85db5b9da4d68ac48ed4b1a01a20bd464e71cb717ce119822e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579093474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd067560524cc63462f4278c8c40c4d576bc46290829d13520448e0a7dee98d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be25eb721d0419861312b5df4f760175b71b580acb4cad43e26b6d9957190c`  
		Last Modified: Tue, 13 Aug 2024 07:54:00 GMT  
		Size: 216.9 MB (216902583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a43f1300414424575a08b49f9201e117a4a1d53d64d5c2767c4a73c50166da7`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 2.4 MB (2393972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf254f4f3ea16d9bf889ec96ccd335ffcc6f1a967562358a594213f3adb3be5`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 463.8 KB (463817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960cf8e2325ce93efb1bee2af9bd272dedf094cddb25b3549bd702f50dbe7e9d`  
		Last Modified: Tue, 13 Aug 2024 07:54:02 GMT  
		Size: 329.3 MB (329254583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466db4a214fba1c6ca81e1e5a33cfb8dde1da25c415d803557a8584d6b19af`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf753fd18a0920218b18f47c95f78f1f58e5e4cb2c9ecddde5f175077fe74bc7`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9677c42f975e839011d4c8223e71eb16b32f1aa2c294aaffba2ebdccc8b8f8`  
		Last Modified: Tue, 13 Aug 2024 07:53:57 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc29ee35071121afdcf7e33610cb15246d126fe05dd3757cacee3f8ad284cf4`  
		Last Modified: Tue, 13 Aug 2024 07:53:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:45b4a7fc88fc5801201e29759a545b66a18af29c3e69d95d941e12e0ec4e8333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c054d74241693b00268175f2d3a3702e2e349a43172789daae53c7fdcbb384`

```dockerfile
```

-	Layers:
	-	`sha256:88637c3f85bbc8be13d93d3fb0572445bddde1d6cfc18a136771eb674b7edfb8`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2961b29ee635ee980a0ec0568733d1e771392b3144386610e3c0e0030514a9`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:65ec19b08590d107425059f3a182bb24ac07077fbdec749bff3cba74f0fc43be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (598010212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f89c8fdd160261989d8ac12df49e273c546a2f4d83601f662e93d9998de9ada`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51f6a8ccad777c520085b7be04b567b1681a30689bc7279bec9698039227b6`  
		Last Modified: Tue, 13 Aug 2024 07:33:38 GMT  
		Size: 228.6 MB (228589771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601fcd0df6f8eed975a21fc58023759c73318ab41b55b5b9ab0971209cd6026a`  
		Last Modified: Tue, 13 Aug 2024 07:33:33 GMT  
		Size: 2.6 MB (2634236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e218dd53f839d1853febf0b40e8303109791c4e0608dd4cca64fc3261fcc39b`  
		Last Modified: Tue, 13 Aug 2024 07:33:32 GMT  
		Size: 463.8 KB (463847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc79d60ed1ad314810962604a5b9ac7223894216ddf28e9936dde0c19da5572`  
		Last Modified: Tue, 13 Aug 2024 07:33:41 GMT  
		Size: 331.0 MB (331014791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10840c11556949f0a89a8435d9540282103cee1893be856f5dba895214ba7ad4`  
		Last Modified: Tue, 13 Aug 2024 07:33:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d94553d57f03b8413845962aef840506a551a807e154fab8452bef155e7097`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceaf49991f5a3f167e9b41f0b9322cd0c89435ccd8ff2e490301f20650f5c2c`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83355aaea56f6c37888f0166cda6c7e1a56a76f25b306de6abbcce28f07aa86b`  
		Last Modified: Tue, 13 Aug 2024 07:33:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c1d8aa2e1b1bd2b78e6ae93e19a913b4f4b935ead17825800cdbace7f0b01e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097e03fbc34153c1682b7a89355196149e33109828bea47e9bd9f65b58f20cf2`

```dockerfile
```

-	Layers:
	-	`sha256:d625bec2bec9edadd6ceb6dface3c4ef00c17e1fe2015c9703b4860300e4cfec`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea46bbcae11b5366a43d4fec11d2406966aebb855e5e0acfe60eba4a9e88e60`  
		Last Modified: Tue, 13 Aug 2024 07:33:32 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240812`

```console
$ docker pull odoo@sha256:53c2d400d604e9fe3cbaa86993e57b13c151b079758a173a0c16660270c9d68c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240812` - linux; amd64

```console
$ docker pull odoo@sha256:b93543cd01dd638138f484569ad4b6aef7ba9cf7dedf5fc36209dc34db449806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583511501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666949e89b97e235f86149da5e8b7321b5f05869d49bd1707795e02f82f975fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fdf6473465ea33d489dd8d1401903da83765f432366a1783d9bb981ef78d3`  
		Last Modified: Tue, 13 Aug 2024 01:14:35 GMT  
		Size: 219.6 MB (219593472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9acc0d5dbedf559219071e2a5de8d1f5c7a1e2cdc1f98aa12cb4e8686d41cb`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 2.4 MB (2391422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20341a02dfa69d8f063050db77027b9c0621d1b041495fb4cd3950e377d048be`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 463.8 KB (463823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d419af5ecb2af82efea4abf82cd55d40291310519938c283edf1bb9adf319`  
		Last Modified: Tue, 13 Aug 2024 01:14:37 GMT  
		Size: 329.6 MB (329632063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ea66e14ee62164410b94bf17e2edad91a3dce48167403742612dab15a40448`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd171703a80c3ed47282cbfcb984d384e5787ff2808d44256a99980954a223`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c55f1e40bd988cc92a4a935c1e639b983ab8d487f98f9de90d5d9f0b3b060`  
		Last Modified: Tue, 13 Aug 2024 01:14:34 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01d42da3282572b995860a7218a808cb2239a57148206fa0dbd020aed2e934d`  
		Last Modified: Tue, 13 Aug 2024 01:14:34 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:e2e86b94639fb6e7cbb8e545d9a983f2c328c46cac88ca47105ba328229da7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94687a547b729ed2bad16b13cbd0d0e38741fa1a28c5ad9e178dfc0ed3378ff4`

```dockerfile
```

-	Layers:
	-	`sha256:44e2361fdb1dbb1c17f5785ac0fd0adb78606d5a2ecd809da64a2d1f08f446ce`  
		Last Modified: Tue, 13 Aug 2024 01:14:33 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba14f5d93e588e5982db97bcb3e4f9c08bffd03cdc2affbad642b78d35f0e8be`  
		Last Modified: Tue, 13 Aug 2024 01:14:32 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240812` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e463cb143a03b85db5b9da4d68ac48ed4b1a01a20bd464e71cb717ce119822e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579093474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd067560524cc63462f4278c8c40c4d576bc46290829d13520448e0a7dee98d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be25eb721d0419861312b5df4f760175b71b580acb4cad43e26b6d9957190c`  
		Last Modified: Tue, 13 Aug 2024 07:54:00 GMT  
		Size: 216.9 MB (216902583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a43f1300414424575a08b49f9201e117a4a1d53d64d5c2767c4a73c50166da7`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 2.4 MB (2393972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf254f4f3ea16d9bf889ec96ccd335ffcc6f1a967562358a594213f3adb3be5`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 463.8 KB (463817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960cf8e2325ce93efb1bee2af9bd272dedf094cddb25b3549bd702f50dbe7e9d`  
		Last Modified: Tue, 13 Aug 2024 07:54:02 GMT  
		Size: 329.3 MB (329254583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30466db4a214fba1c6ca81e1e5a33cfb8dde1da25c415d803557a8584d6b19af`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf753fd18a0920218b18f47c95f78f1f58e5e4cb2c9ecddde5f175077fe74bc7`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9677c42f975e839011d4c8223e71eb16b32f1aa2c294aaffba2ebdccc8b8f8`  
		Last Modified: Tue, 13 Aug 2024 07:53:57 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc29ee35071121afdcf7e33610cb15246d126fe05dd3757cacee3f8ad284cf4`  
		Last Modified: Tue, 13 Aug 2024 07:53:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:45b4a7fc88fc5801201e29759a545b66a18af29c3e69d95d941e12e0ec4e8333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c054d74241693b00268175f2d3a3702e2e349a43172789daae53c7fdcbb384`

```dockerfile
```

-	Layers:
	-	`sha256:88637c3f85bbc8be13d93d3fb0572445bddde1d6cfc18a136771eb674b7edfb8`  
		Last Modified: Tue, 13 Aug 2024 07:53:56 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2961b29ee635ee980a0ec0568733d1e771392b3144386610e3c0e0030514a9`  
		Last Modified: Tue, 13 Aug 2024 07:53:55 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240812` - linux; ppc64le

```console
$ docker pull odoo@sha256:65ec19b08590d107425059f3a182bb24ac07077fbdec749bff3cba74f0fc43be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (598010212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f89c8fdd160261989d8ac12df49e273c546a2f4d83601f662e93d9998de9ada`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51f6a8ccad777c520085b7be04b567b1681a30689bc7279bec9698039227b6`  
		Last Modified: Tue, 13 Aug 2024 07:33:38 GMT  
		Size: 228.6 MB (228589771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601fcd0df6f8eed975a21fc58023759c73318ab41b55b5b9ab0971209cd6026a`  
		Last Modified: Tue, 13 Aug 2024 07:33:33 GMT  
		Size: 2.6 MB (2634236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e218dd53f839d1853febf0b40e8303109791c4e0608dd4cca64fc3261fcc39b`  
		Last Modified: Tue, 13 Aug 2024 07:33:32 GMT  
		Size: 463.8 KB (463847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc79d60ed1ad314810962604a5b9ac7223894216ddf28e9936dde0c19da5572`  
		Last Modified: Tue, 13 Aug 2024 07:33:41 GMT  
		Size: 331.0 MB (331014791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10840c11556949f0a89a8435d9540282103cee1893be856f5dba895214ba7ad4`  
		Last Modified: Tue, 13 Aug 2024 07:33:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d94553d57f03b8413845962aef840506a551a807e154fab8452bef155e7097`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceaf49991f5a3f167e9b41f0b9322cd0c89435ccd8ff2e490301f20650f5c2c`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83355aaea56f6c37888f0166cda6c7e1a56a76f25b306de6abbcce28f07aa86b`  
		Last Modified: Tue, 13 Aug 2024 07:33:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:c1d8aa2e1b1bd2b78e6ae93e19a913b4f4b935ead17825800cdbace7f0b01e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097e03fbc34153c1682b7a89355196149e33109828bea47e9bd9f65b58f20cf2`

```dockerfile
```

-	Layers:
	-	`sha256:d625bec2bec9edadd6ceb6dface3c4ef00c17e1fe2015c9703b4860300e4cfec`  
		Last Modified: Tue, 13 Aug 2024 07:33:34 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea46bbcae11b5366a43d4fec11d2406966aebb855e5e0acfe60eba4a9e88e60`  
		Last Modified: Tue, 13 Aug 2024 07:33:32 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:b3a25a96f7bf0f8d610cb1dcbcb8baa95b94055fcb6a53e32993c20019271f88
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
$ docker pull odoo@sha256:7f7299bd1c385708c37707578e1635b5d5ca99bbc19e4e213cdf5e8b4dd4f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595388513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3725e19640c5f7f2eefcd2d75d3d96681af6d1fc8997f453f069713b3c6abb79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1c9502ac2c40711e258fe5fbeff39b2234453f4a77db921c8afac023de003`  
		Last Modified: Sat, 17 Aug 2024 02:04:28 GMT  
		Size: 233.7 MB (233742043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55de2e47752513c0598cd315998b95b62312aa64904c76761db0a6ee4f437f1`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 2.3 MB (2315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c545b9834dc8d8529c069bec4ab73d9954855f1cd2130cd216305bb324dc758`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 464.9 KB (464901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aa04d8f657ddc69e3ece87ee31d6629d1111e0d7be9eb8ed333f1451995d2f`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 329.3 MB (329327550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776cd7a35f92c05f85fed1be7a4c1fb8f404909fad62b0b0628ee903f0318d3f`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d84f059e26bf9f6c83edc58c115d454bfac38db7f3e7d21645e2f8e7327a5f6`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e3f8f364db6686278c509146b1499caeaecad92f3974f9e18f1a474ca0def`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84b59bd1f30d7d8cf107b02839ebd44387671ef6c10f1fb874d82961a42ec7d`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4716eedc21bb20a98a55e6ac3bde958743f4d6dd75ff373d93153ba37a253c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23682b87ca37b1aa66ca9b79e72cec2f27bb09b55e176ddf115a1fe1f1747d2e`

```dockerfile
```

-	Layers:
	-	`sha256:1fe58ba6648970bb5f6768bf108084286ccf278e114e3c8a56937f7415ea5631`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff81c4dad542bdb25fe981f3aeaae470af063740c0510fff90c0e8805e4c613`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:993937852f8631f76d508ddc7e0c9505d9db58539779a64b10b202909cebef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590183870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d45a27d523bf248db2783a623b722a05f0487e6def9f37e7ba1ab1a526d2a62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b35065ccf4d91ef0f5b605cced722d37f0eddc353e93c16de74979c9e43b1e`  
		Last Modified: Sat, 17 Aug 2024 03:34:43 GMT  
		Size: 328.9 MB (328933372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f926db0c771bbf79dfd7b79da7e1dc84286c7358bf6d7840c18b3c83542be8`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc28d83693f4855fdbee4e622965460139aa9eeb974bcd5aa1e0e1ce51437161`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5c4441a4b9d91ebbc1fc412ea52f574628351aafb3f276aa02aaa5dd94524`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e58dd4413947cd48e434cc8afc93e651b09330a5b05a4508a2f9de652a6ecc`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c10a8ac7b06653b2fe16c211979470205568c51d9864170c69bfce759c44a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a65e05834fda1c14bd0666e1787ae2787fac772af35fbeffe2afc108a64b1c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f3b9c86829097e4e45d586a3a4cebd861d55d83ede3f764d8178ef5b40617cf`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b649b05b090f34f8146e19c8caa54dc225854a1656faff09015259a7a09c38`  
		Last Modified: Sat, 17 Aug 2024 03:34:35 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:2a36c8f24159ac55a565f620f177601166cab0be476ea32991c332f5c4d12470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611855606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa9e05453755e0714d785682599de5634536d61c290e29c980192ee3e7548b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12b96f1bb63707348ac6c758d2bd1be3a7dad754de6e2ff3704e4bfc6e9701`  
		Last Modified: Sat, 17 Aug 2024 02:01:50 GMT  
		Size: 331.1 MB (331055383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cb5d596d3809c291966009e9b24a80677ce6b51c46b5e79413c3d177623b6d`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3186e7549d4d5a4ebb2e541bc0cc44d182179ca74c30f8e8ecd16adae72c35c`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638018d448b5216a8debc54484dc10730a4af18ef0943e918e8350cbf4fba899`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e4775ce900135c2575c3012b1adfc15eddbd6036f8e8e91e7678fd6ebd106d`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1a2a0ec2debb762dfe941ff9d72c37530bc8fcc5b134b5c12213973684721626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f48b8d3307ffe4d254a1d06dd65d1281124df9a687d9c53369a8707a31f7ff`

```dockerfile
```

-	Layers:
	-	`sha256:f9dc11b4af5cac8f2b07a770b2b6c426a39b3e512d3b8c1381214f3f15408444`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c2da1e45d642bedd26f4899dfd005d90ad0e1f14e20e5953712c2e1e94c2fd`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:b3a25a96f7bf0f8d610cb1dcbcb8baa95b94055fcb6a53e32993c20019271f88
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
$ docker pull odoo@sha256:7f7299bd1c385708c37707578e1635b5d5ca99bbc19e4e213cdf5e8b4dd4f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595388513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3725e19640c5f7f2eefcd2d75d3d96681af6d1fc8997f453f069713b3c6abb79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1c9502ac2c40711e258fe5fbeff39b2234453f4a77db921c8afac023de003`  
		Last Modified: Sat, 17 Aug 2024 02:04:28 GMT  
		Size: 233.7 MB (233742043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55de2e47752513c0598cd315998b95b62312aa64904c76761db0a6ee4f437f1`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 2.3 MB (2315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c545b9834dc8d8529c069bec4ab73d9954855f1cd2130cd216305bb324dc758`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 464.9 KB (464901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aa04d8f657ddc69e3ece87ee31d6629d1111e0d7be9eb8ed333f1451995d2f`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 329.3 MB (329327550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776cd7a35f92c05f85fed1be7a4c1fb8f404909fad62b0b0628ee903f0318d3f`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d84f059e26bf9f6c83edc58c115d454bfac38db7f3e7d21645e2f8e7327a5f6`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e3f8f364db6686278c509146b1499caeaecad92f3974f9e18f1a474ca0def`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84b59bd1f30d7d8cf107b02839ebd44387671ef6c10f1fb874d82961a42ec7d`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4716eedc21bb20a98a55e6ac3bde958743f4d6dd75ff373d93153ba37a253c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23682b87ca37b1aa66ca9b79e72cec2f27bb09b55e176ddf115a1fe1f1747d2e`

```dockerfile
```

-	Layers:
	-	`sha256:1fe58ba6648970bb5f6768bf108084286ccf278e114e3c8a56937f7415ea5631`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff81c4dad542bdb25fe981f3aeaae470af063740c0510fff90c0e8805e4c613`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:993937852f8631f76d508ddc7e0c9505d9db58539779a64b10b202909cebef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590183870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d45a27d523bf248db2783a623b722a05f0487e6def9f37e7ba1ab1a526d2a62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b35065ccf4d91ef0f5b605cced722d37f0eddc353e93c16de74979c9e43b1e`  
		Last Modified: Sat, 17 Aug 2024 03:34:43 GMT  
		Size: 328.9 MB (328933372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f926db0c771bbf79dfd7b79da7e1dc84286c7358bf6d7840c18b3c83542be8`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc28d83693f4855fdbee4e622965460139aa9eeb974bcd5aa1e0e1ce51437161`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5c4441a4b9d91ebbc1fc412ea52f574628351aafb3f276aa02aaa5dd94524`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e58dd4413947cd48e434cc8afc93e651b09330a5b05a4508a2f9de652a6ecc`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c10a8ac7b06653b2fe16c211979470205568c51d9864170c69bfce759c44a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a65e05834fda1c14bd0666e1787ae2787fac772af35fbeffe2afc108a64b1c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f3b9c86829097e4e45d586a3a4cebd861d55d83ede3f764d8178ef5b40617cf`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b649b05b090f34f8146e19c8caa54dc225854a1656faff09015259a7a09c38`  
		Last Modified: Sat, 17 Aug 2024 03:34:35 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:2a36c8f24159ac55a565f620f177601166cab0be476ea32991c332f5c4d12470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611855606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa9e05453755e0714d785682599de5634536d61c290e29c980192ee3e7548b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12b96f1bb63707348ac6c758d2bd1be3a7dad754de6e2ff3704e4bfc6e9701`  
		Last Modified: Sat, 17 Aug 2024 02:01:50 GMT  
		Size: 331.1 MB (331055383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cb5d596d3809c291966009e9b24a80677ce6b51c46b5e79413c3d177623b6d`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3186e7549d4d5a4ebb2e541bc0cc44d182179ca74c30f8e8ecd16adae72c35c`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638018d448b5216a8debc54484dc10730a4af18ef0943e918e8350cbf4fba899`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e4775ce900135c2575c3012b1adfc15eddbd6036f8e8e91e7678fd6ebd106d`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1a2a0ec2debb762dfe941ff9d72c37530bc8fcc5b134b5c12213973684721626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f48b8d3307ffe4d254a1d06dd65d1281124df9a687d9c53369a8707a31f7ff`

```dockerfile
```

-	Layers:
	-	`sha256:f9dc11b4af5cac8f2b07a770b2b6c426a39b3e512d3b8c1381214f3f15408444`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c2da1e45d642bedd26f4899dfd005d90ad0e1f14e20e5953712c2e1e94c2fd`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240812`

```console
$ docker pull odoo@sha256:b3a25a96f7bf0f8d610cb1dcbcb8baa95b94055fcb6a53e32993c20019271f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240812` - linux; amd64

```console
$ docker pull odoo@sha256:7f7299bd1c385708c37707578e1635b5d5ca99bbc19e4e213cdf5e8b4dd4f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595388513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3725e19640c5f7f2eefcd2d75d3d96681af6d1fc8997f453f069713b3c6abb79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1c9502ac2c40711e258fe5fbeff39b2234453f4a77db921c8afac023de003`  
		Last Modified: Sat, 17 Aug 2024 02:04:28 GMT  
		Size: 233.7 MB (233742043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55de2e47752513c0598cd315998b95b62312aa64904c76761db0a6ee4f437f1`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 2.3 MB (2315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c545b9834dc8d8529c069bec4ab73d9954855f1cd2130cd216305bb324dc758`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 464.9 KB (464901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aa04d8f657ddc69e3ece87ee31d6629d1111e0d7be9eb8ed333f1451995d2f`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 329.3 MB (329327550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776cd7a35f92c05f85fed1be7a4c1fb8f404909fad62b0b0628ee903f0318d3f`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d84f059e26bf9f6c83edc58c115d454bfac38db7f3e7d21645e2f8e7327a5f6`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e3f8f364db6686278c509146b1499caeaecad92f3974f9e18f1a474ca0def`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84b59bd1f30d7d8cf107b02839ebd44387671ef6c10f1fb874d82961a42ec7d`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:4716eedc21bb20a98a55e6ac3bde958743f4d6dd75ff373d93153ba37a253c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23682b87ca37b1aa66ca9b79e72cec2f27bb09b55e176ddf115a1fe1f1747d2e`

```dockerfile
```

-	Layers:
	-	`sha256:1fe58ba6648970bb5f6768bf108084286ccf278e114e3c8a56937f7415ea5631`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff81c4dad542bdb25fe981f3aeaae470af063740c0510fff90c0e8805e4c613`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240812` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:993937852f8631f76d508ddc7e0c9505d9db58539779a64b10b202909cebef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590183870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d45a27d523bf248db2783a623b722a05f0487e6def9f37e7ba1ab1a526d2a62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b35065ccf4d91ef0f5b605cced722d37f0eddc353e93c16de74979c9e43b1e`  
		Last Modified: Sat, 17 Aug 2024 03:34:43 GMT  
		Size: 328.9 MB (328933372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f926db0c771bbf79dfd7b79da7e1dc84286c7358bf6d7840c18b3c83542be8`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc28d83693f4855fdbee4e622965460139aa9eeb974bcd5aa1e0e1ce51437161`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5c4441a4b9d91ebbc1fc412ea52f574628351aafb3f276aa02aaa5dd94524`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e58dd4413947cd48e434cc8afc93e651b09330a5b05a4508a2f9de652a6ecc`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:c10a8ac7b06653b2fe16c211979470205568c51d9864170c69bfce759c44a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a65e05834fda1c14bd0666e1787ae2787fac772af35fbeffe2afc108a64b1c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f3b9c86829097e4e45d586a3a4cebd861d55d83ede3f764d8178ef5b40617cf`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b649b05b090f34f8146e19c8caa54dc225854a1656faff09015259a7a09c38`  
		Last Modified: Sat, 17 Aug 2024 03:34:35 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240812` - linux; ppc64le

```console
$ docker pull odoo@sha256:2a36c8f24159ac55a565f620f177601166cab0be476ea32991c332f5c4d12470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611855606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa9e05453755e0714d785682599de5634536d61c290e29c980192ee3e7548b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12b96f1bb63707348ac6c758d2bd1be3a7dad754de6e2ff3704e4bfc6e9701`  
		Last Modified: Sat, 17 Aug 2024 02:01:50 GMT  
		Size: 331.1 MB (331055383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cb5d596d3809c291966009e9b24a80677ce6b51c46b5e79413c3d177623b6d`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3186e7549d4d5a4ebb2e541bc0cc44d182179ca74c30f8e8ecd16adae72c35c`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638018d448b5216a8debc54484dc10730a4af18ef0943e918e8350cbf4fba899`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e4775ce900135c2575c3012b1adfc15eddbd6036f8e8e91e7678fd6ebd106d`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:1a2a0ec2debb762dfe941ff9d72c37530bc8fcc5b134b5c12213973684721626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f48b8d3307ffe4d254a1d06dd65d1281124df9a687d9c53369a8707a31f7ff`

```dockerfile
```

-	Layers:
	-	`sha256:f9dc11b4af5cac8f2b07a770b2b6c426a39b3e512d3b8c1381214f3f15408444`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c2da1e45d642bedd26f4899dfd005d90ad0e1f14e20e5953712c2e1e94c2fd`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:b3a25a96f7bf0f8d610cb1dcbcb8baa95b94055fcb6a53e32993c20019271f88
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
$ docker pull odoo@sha256:7f7299bd1c385708c37707578e1635b5d5ca99bbc19e4e213cdf5e8b4dd4f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595388513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3725e19640c5f7f2eefcd2d75d3d96681af6d1fc8997f453f069713b3c6abb79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1c9502ac2c40711e258fe5fbeff39b2234453f4a77db921c8afac023de003`  
		Last Modified: Sat, 17 Aug 2024 02:04:28 GMT  
		Size: 233.7 MB (233742043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55de2e47752513c0598cd315998b95b62312aa64904c76761db0a6ee4f437f1`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 2.3 MB (2315558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c545b9834dc8d8529c069bec4ab73d9954855f1cd2130cd216305bb324dc758`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 464.9 KB (464901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aa04d8f657ddc69e3ece87ee31d6629d1111e0d7be9eb8ed333f1451995d2f`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 329.3 MB (329327550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776cd7a35f92c05f85fed1be7a4c1fb8f404909fad62b0b0628ee903f0318d3f`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d84f059e26bf9f6c83edc58c115d454bfac38db7f3e7d21645e2f8e7327a5f6`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e3f8f364db6686278c509146b1499caeaecad92f3974f9e18f1a474ca0def`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84b59bd1f30d7d8cf107b02839ebd44387671ef6c10f1fb874d82961a42ec7d`  
		Last Modified: Sat, 17 Aug 2024 02:04:26 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:4716eedc21bb20a98a55e6ac3bde958743f4d6dd75ff373d93153ba37a253c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23682b87ca37b1aa66ca9b79e72cec2f27bb09b55e176ddf115a1fe1f1747d2e`

```dockerfile
```

-	Layers:
	-	`sha256:1fe58ba6648970bb5f6768bf108084286ccf278e114e3c8a56937f7415ea5631`  
		Last Modified: Sat, 17 Aug 2024 02:04:25 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff81c4dad542bdb25fe981f3aeaae470af063740c0510fff90c0e8805e4c613`  
		Last Modified: Sat, 17 Aug 2024 02:04:24 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:993937852f8631f76d508ddc7e0c9505d9db58539779a64b10b202909cebef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590183870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d45a27d523bf248db2783a623b722a05f0487e6def9f37e7ba1ab1a526d2a62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b35065ccf4d91ef0f5b605cced722d37f0eddc353e93c16de74979c9e43b1e`  
		Last Modified: Sat, 17 Aug 2024 03:34:43 GMT  
		Size: 328.9 MB (328933372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f926db0c771bbf79dfd7b79da7e1dc84286c7358bf6d7840c18b3c83542be8`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc28d83693f4855fdbee4e622965460139aa9eeb974bcd5aa1e0e1ce51437161`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5c4441a4b9d91ebbc1fc412ea52f574628351aafb3f276aa02aaa5dd94524`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e58dd4413947cd48e434cc8afc93e651b09330a5b05a4508a2f9de652a6ecc`  
		Last Modified: Sat, 17 Aug 2024 03:34:38 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c10a8ac7b06653b2fe16c211979470205568c51d9864170c69bfce759c44a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a65e05834fda1c14bd0666e1787ae2787fac772af35fbeffe2afc108a64b1c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f3b9c86829097e4e45d586a3a4cebd861d55d83ede3f764d8178ef5b40617cf`  
		Last Modified: Sat, 17 Aug 2024 03:34:37 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b649b05b090f34f8146e19c8caa54dc225854a1656faff09015259a7a09c38`  
		Last Modified: Sat, 17 Aug 2024 03:34:35 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:2a36c8f24159ac55a565f620f177601166cab0be476ea32991c332f5c4d12470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611855606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa9e05453755e0714d785682599de5634536d61c290e29c980192ee3e7548b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 12 Aug 2024 11:24:22 GMT
ARG RELEASE
# Mon, 12 Aug 2024 11:24:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 11:24:22 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 11:24:22 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12b96f1bb63707348ac6c758d2bd1be3a7dad754de6e2ff3704e4bfc6e9701`  
		Last Modified: Sat, 17 Aug 2024 02:01:50 GMT  
		Size: 331.1 MB (331055383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cb5d596d3809c291966009e9b24a80677ce6b51c46b5e79413c3d177623b6d`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3186e7549d4d5a4ebb2e541bc0cc44d182179ca74c30f8e8ecd16adae72c35c`  
		Last Modified: Sat, 17 Aug 2024 02:01:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638018d448b5216a8debc54484dc10730a4af18ef0943e918e8350cbf4fba899`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e4775ce900135c2575c3012b1adfc15eddbd6036f8e8e91e7678fd6ebd106d`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1a2a0ec2debb762dfe941ff9d72c37530bc8fcc5b134b5c12213973684721626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f48b8d3307ffe4d254a1d06dd65d1281124df9a687d9c53369a8707a31f7ff`

```dockerfile
```

-	Layers:
	-	`sha256:f9dc11b4af5cac8f2b07a770b2b6c426a39b3e512d3b8c1381214f3f15408444`  
		Last Modified: Sat, 17 Aug 2024 02:01:44 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c2da1e45d642bedd26f4899dfd005d90ad0e1f14e20e5953712c2e1e94c2fd`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
