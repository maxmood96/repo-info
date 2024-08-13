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
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
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
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
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
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240812`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
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
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240812` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240812` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
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
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
