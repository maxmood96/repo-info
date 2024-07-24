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
$ docker pull odoo@sha256:c3763165ca3e0fa32c61a8b777489a703889290396662a8d4bd0286e0f50b50b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:55346d708022b8c1e22de18b3e8bf944ec97b26a0fca8b3d52ea8bd1d1210f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563903530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f16d4cad28f4b998f7faeda56aa24fa77fbca249511dfdd42f600abdc19486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=15.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: ODOO_RELEASE=20240711 ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: ODOO_RELEASE=20240711 ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7ac8eda157261ef249e81fcbde66e676e31918067b9e1faa5b189bfb87b55c`  
		Last Modified: Tue, 23 Jul 2024 07:22:14 GMT  
		Size: 220.3 MB (220281038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05685d0c15e30d854adb077b640dbb4c564c5a0fe9c0cd35818037c6f707542`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 2.4 MB (2387163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2e8ea268eeb3e69dbe23088a73891f4d2af3b8db2f73cab93b8df5dd44346b`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 459.1 KB (459094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46385143355fbc5023936cda26f76d2bbb9af625e664a6d8eb872606745671c`  
		Last Modified: Tue, 23 Jul 2024 07:22:16 GMT  
		Size: 309.3 MB (309345473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83970500672e4e1c1e1aa921bf2086e13650553298e4df2a63036eea38742c40`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caab37a7c22ed34c8dd42c5abade966ff0c57602711d52a2514f768f9b777a5b`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f81c071040f281072e67abf56fcbe24e4cc4152826eeded7ee096facafc11`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8cf87c960e35aa0b39ecc8b40e9dd8d2ed64eefaf5412b46ce00e8f008c0d7`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:03e4a66ffbc59001e6947e8396b945aa7d947bb225fa22cee41e188788cd065d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34699318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0163e4e30eaee7ec9484ec53ca39bb14d2e6f4e15d798c51c3266767ee8fe`

```dockerfile
```

-	Layers:
	-	`sha256:333b9f174491ef90cabaa6578aa8903115ffb2ad078e0c7bf18cd985dfb123cb`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 34.7 MB (34674687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ce96c466db96e9b1449671f3feab2e391837b963309423d89a4eb6fb205d9b`  
		Last Modified: Tue, 23 Jul 2024 07:22:11 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:c3763165ca3e0fa32c61a8b777489a703889290396662a8d4bd0286e0f50b50b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:55346d708022b8c1e22de18b3e8bf944ec97b26a0fca8b3d52ea8bd1d1210f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563903530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f16d4cad28f4b998f7faeda56aa24fa77fbca249511dfdd42f600abdc19486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=15.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: ODOO_RELEASE=20240711 ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: ODOO_RELEASE=20240711 ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7ac8eda157261ef249e81fcbde66e676e31918067b9e1faa5b189bfb87b55c`  
		Last Modified: Tue, 23 Jul 2024 07:22:14 GMT  
		Size: 220.3 MB (220281038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05685d0c15e30d854adb077b640dbb4c564c5a0fe9c0cd35818037c6f707542`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 2.4 MB (2387163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2e8ea268eeb3e69dbe23088a73891f4d2af3b8db2f73cab93b8df5dd44346b`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 459.1 KB (459094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46385143355fbc5023936cda26f76d2bbb9af625e664a6d8eb872606745671c`  
		Last Modified: Tue, 23 Jul 2024 07:22:16 GMT  
		Size: 309.3 MB (309345473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83970500672e4e1c1e1aa921bf2086e13650553298e4df2a63036eea38742c40`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caab37a7c22ed34c8dd42c5abade966ff0c57602711d52a2514f768f9b777a5b`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f81c071040f281072e67abf56fcbe24e4cc4152826eeded7ee096facafc11`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8cf87c960e35aa0b39ecc8b40e9dd8d2ed64eefaf5412b46ce00e8f008c0d7`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:03e4a66ffbc59001e6947e8396b945aa7d947bb225fa22cee41e188788cd065d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34699318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0163e4e30eaee7ec9484ec53ca39bb14d2e6f4e15d798c51c3266767ee8fe`

```dockerfile
```

-	Layers:
	-	`sha256:333b9f174491ef90cabaa6578aa8903115ffb2ad078e0c7bf18cd985dfb123cb`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 34.7 MB (34674687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ce96c466db96e9b1449671f3feab2e391837b963309423d89a4eb6fb205d9b`  
		Last Modified: Tue, 23 Jul 2024 07:22:11 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240711`

```console
$ docker pull odoo@sha256:c3763165ca3e0fa32c61a8b777489a703889290396662a8d4bd0286e0f50b50b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240711` - linux; amd64

```console
$ docker pull odoo@sha256:55346d708022b8c1e22de18b3e8bf944ec97b26a0fca8b3d52ea8bd1d1210f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563903530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f16d4cad28f4b998f7faeda56aa24fa77fbca249511dfdd42f600abdc19486`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=15.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: ODOO_RELEASE=20240711 ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: ODOO_RELEASE=20240711 ODOO_SHA=32aa2460ab3a2a539e3e99e791592db2ab2a8406
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7ac8eda157261ef249e81fcbde66e676e31918067b9e1faa5b189bfb87b55c`  
		Last Modified: Tue, 23 Jul 2024 07:22:14 GMT  
		Size: 220.3 MB (220281038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05685d0c15e30d854adb077b640dbb4c564c5a0fe9c0cd35818037c6f707542`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 2.4 MB (2387163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2e8ea268eeb3e69dbe23088a73891f4d2af3b8db2f73cab93b8df5dd44346b`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 459.1 KB (459094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46385143355fbc5023936cda26f76d2bbb9af625e664a6d8eb872606745671c`  
		Last Modified: Tue, 23 Jul 2024 07:22:16 GMT  
		Size: 309.3 MB (309345473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83970500672e4e1c1e1aa921bf2086e13650553298e4df2a63036eea38742c40`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caab37a7c22ed34c8dd42c5abade966ff0c57602711d52a2514f768f9b777a5b`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f81c071040f281072e67abf56fcbe24e4cc4152826eeded7ee096facafc11`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8cf87c960e35aa0b39ecc8b40e9dd8d2ed64eefaf5412b46ce00e8f008c0d7`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:03e4a66ffbc59001e6947e8396b945aa7d947bb225fa22cee41e188788cd065d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34699318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0163e4e30eaee7ec9484ec53ca39bb14d2e6f4e15d798c51c3266767ee8fe`

```dockerfile
```

-	Layers:
	-	`sha256:333b9f174491ef90cabaa6578aa8903115ffb2ad078e0c7bf18cd985dfb123cb`  
		Last Modified: Tue, 23 Jul 2024 07:22:12 GMT  
		Size: 34.7 MB (34674687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ce96c466db96e9b1449671f3feab2e391837b963309423d89a4eb6fb205d9b`  
		Last Modified: Tue, 23 Jul 2024 07:22:11 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:2691e8358530688e446264f030d49518238ac0e4d13e6e026adf90062fe32d79
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
$ docker pull odoo@sha256:2405e3d33424be2d1b281fafc5df8ff622b85fc21d3372cc1d951c5c23cec727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583250199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5eae6b196e49215d3792e12f38e9ad73faf404597c657ca47f377702ed7ad3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc75f0337d86913e92fcda4b7ffe5096be51415b255fc7510d8bafe68861dc`  
		Last Modified: Tue, 23 Jul 2024 07:22:48 GMT  
		Size: 219.6 MB (219594107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a8e9b4eaab138ac3b26458239add25d9cf4a25c309812bd6ea41b9ced5096b`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 2.4 MB (2391002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712493a4eac3046ce138796ce7810538365a077f666e815f46601282c0e1183f`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 459.1 KB (459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bb6e7818570d1a6fcc42e7935be0c114eaa2c17e2d98481c1dee10653cebc`  
		Last Modified: Tue, 23 Jul 2024 07:22:49 GMT  
		Size: 329.4 MB (329375239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83970500672e4e1c1e1aa921bf2086e13650553298e4df2a63036eea38742c40`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ede3d485c44d0e51daf0f907fd4c1c17740918169a54d88f6f0698a5d0d4136`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9212b0189a0837342a5a22d2f2275dad052fc79f1fc6a6eb0072dee0551beb0`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f533450ab17892004559dc203136a8a0c92282b703714dce03a89b7b360bd3`  
		Last Modified: Tue, 23 Jul 2024 07:22:45 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:83a8639e21c5271059dc1b1238c1cba54ee021194cc5b11cf904e84aac37f77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38740841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f7dd28b17ed405d5faf04f39c9d8c8fcf121e707c472164a592f05e24be8e`

```dockerfile
```

-	Layers:
	-	`sha256:c99d1deb2afd21049bdf088e79ac1c63acb17a90912e279cadef66f4078aa4f0`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 38.7 MB (38714299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734df295fbdb00840f52373a0ff48f1f1f2900e28326b555a1c7b416be3518a`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:50694a9a24e4c091f40189942d46e5f8c02d2799b8a8f29c1b0822cc8fdc01c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578852501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542c43129b5f7747f72ff9dab502b9a02654e78f46d3fe282303a13f03079e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892185f77cfcac6354372a8675b7665238515fab1ea3a2be2440093165bc8c7e`  
		Last Modified: Tue, 23 Jul 2024 21:59:45 GMT  
		Size: 216.9 MB (216902546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818682d0362073042371c8d1a984e96bae57a7dd0102db5d847b3a69b5235cc4`  
		Last Modified: Tue, 23 Jul 2024 21:59:48 GMT  
		Size: 2.4 MB (2393420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1f7514b2a42ea5edb162e01639f182eabfedc29bc5bfde2ceadd8c8f11919`  
		Last Modified: Tue, 23 Jul 2024 21:59:40 GMT  
		Size: 459.1 KB (459090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc49206832d9cb915c5bbb5834b874dad932c09c7de129d958bdcb3cc24329b`  
		Last Modified: Tue, 23 Jul 2024 21:59:47 GMT  
		Size: 329.0 MB (329018927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3a4e3749ca11bca9e7b358155a218c30ef4e86db59da6a84b602024a9ca48b`  
		Last Modified: Tue, 23 Jul 2024 21:59:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa8757db422ca4e8975861160a79997291cbc06c3c66484c1937d20d92cd69`  
		Last Modified: Tue, 23 Jul 2024 21:59:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dff51fc9a0fcc4b1a2cc3ad946eed516a41d5c5f267cfcb3b210d0ada4c8f1`  
		Last Modified: Tue, 23 Jul 2024 21:59:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f45820906c7ea0824532e839bc06913088655c2b19f9c3d5d732ca687ff0ea`  
		Last Modified: Tue, 23 Jul 2024 21:59:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d45aac73a22b736af84d35e6f6a6c455c6b6956b0e4fb145af6241cdcd6950e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38747610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321eb022629dcec5da12f9d903165af97bb6365ee0d873769a88c39172761229`

```dockerfile
```

-	Layers:
	-	`sha256:d22066b3ac89a6d86399fc2f8e9c7430c0f94489cc48059cca3e0097cf1159ba`  
		Last Modified: Tue, 23 Jul 2024 21:59:41 GMT  
		Size: 38.7 MB (38720771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c2607b67140f31860977eb12781dda018682e7d6f5834153f6415522c186b2`  
		Last Modified: Tue, 23 Jul 2024 21:59:40 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:1d5a7af3451af0f1552ce5958a6a8b84a0696fc7b8e61dcd3c53a7690cc0cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597795854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87598250efb43fffc1781e6ae3f1aacc17047964f8c86157b9b04db8f26b312f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9580f055a1eb6c34a4542ffa863a4893d52b7ef102494021008dc372c6cde9`  
		Last Modified: Tue, 23 Jul 2024 19:40:04 GMT  
		Size: 228.6 MB (228590608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38903e57619504f2567ca9e4ad773a4b2905923d4b3ccdeefa0f979af4387a59`  
		Last Modified: Tue, 23 Jul 2024 19:39:50 GMT  
		Size: 2.6 MB (2634111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00c518bc786cc67dbe79950d2ffb2dfe18eb3ecf6defb5756c2eb09a50c646`  
		Last Modified: Tue, 23 Jul 2024 19:39:49 GMT  
		Size: 459.1 KB (459094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ec69368b416237897d06efb555192f0ff36c3d16ef31c92f953579d81ba3`  
		Last Modified: Tue, 23 Jul 2024 19:40:21 GMT  
		Size: 330.8 MB (330804411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7a9611fe3e10273f80e33812fe5da3ae06cdc9c0a78d7efa0964c963a9f8e`  
		Last Modified: Tue, 23 Jul 2024 19:39:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e1b13b4c630335281709b6bcb436e7e4b77c41e59d71de8b11fd0a65f7971`  
		Last Modified: Tue, 23 Jul 2024 19:39:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12a241aa92a5f968792b5391f8efbeea9f72a88eec5ecd39b9f504882e4d1d2`  
		Last Modified: Tue, 23 Jul 2024 19:39:52 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2959434ef9eaede3d3bc8d2d37265f38aadebc613a3a86a496650048c052f6`  
		Last Modified: Tue, 23 Jul 2024 19:39:52 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:92259c92786717692561c8ae077e386a755c9a69b238cfb52c30562b44b46543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38749023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc3e3321e67ce28bd3a42c199b7c5e95b7bf0b50d823eb998cf42978fb5eea`

```dockerfile
```

-	Layers:
	-	`sha256:f17c14b269c74cb85bd39f05268d97d113343d4f91e9e8cbbdc3342773aeab14`  
		Last Modified: Tue, 23 Jul 2024 19:39:55 GMT  
		Size: 38.7 MB (38722431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c080c16478ea119c13ce8958684dc20193c4c200a5e9f33f4a429c828d7e8f0`  
		Last Modified: Tue, 23 Jul 2024 19:39:49 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:2691e8358530688e446264f030d49518238ac0e4d13e6e026adf90062fe32d79
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
$ docker pull odoo@sha256:2405e3d33424be2d1b281fafc5df8ff622b85fc21d3372cc1d951c5c23cec727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583250199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5eae6b196e49215d3792e12f38e9ad73faf404597c657ca47f377702ed7ad3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc75f0337d86913e92fcda4b7ffe5096be51415b255fc7510d8bafe68861dc`  
		Last Modified: Tue, 23 Jul 2024 07:22:48 GMT  
		Size: 219.6 MB (219594107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a8e9b4eaab138ac3b26458239add25d9cf4a25c309812bd6ea41b9ced5096b`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 2.4 MB (2391002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712493a4eac3046ce138796ce7810538365a077f666e815f46601282c0e1183f`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 459.1 KB (459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bb6e7818570d1a6fcc42e7935be0c114eaa2c17e2d98481c1dee10653cebc`  
		Last Modified: Tue, 23 Jul 2024 07:22:49 GMT  
		Size: 329.4 MB (329375239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83970500672e4e1c1e1aa921bf2086e13650553298e4df2a63036eea38742c40`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ede3d485c44d0e51daf0f907fd4c1c17740918169a54d88f6f0698a5d0d4136`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9212b0189a0837342a5a22d2f2275dad052fc79f1fc6a6eb0072dee0551beb0`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f533450ab17892004559dc203136a8a0c92282b703714dce03a89b7b360bd3`  
		Last Modified: Tue, 23 Jul 2024 07:22:45 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:83a8639e21c5271059dc1b1238c1cba54ee021194cc5b11cf904e84aac37f77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38740841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f7dd28b17ed405d5faf04f39c9d8c8fcf121e707c472164a592f05e24be8e`

```dockerfile
```

-	Layers:
	-	`sha256:c99d1deb2afd21049bdf088e79ac1c63acb17a90912e279cadef66f4078aa4f0`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 38.7 MB (38714299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734df295fbdb00840f52373a0ff48f1f1f2900e28326b555a1c7b416be3518a`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:50694a9a24e4c091f40189942d46e5f8c02d2799b8a8f29c1b0822cc8fdc01c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578852501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542c43129b5f7747f72ff9dab502b9a02654e78f46d3fe282303a13f03079e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892185f77cfcac6354372a8675b7665238515fab1ea3a2be2440093165bc8c7e`  
		Last Modified: Tue, 23 Jul 2024 21:59:45 GMT  
		Size: 216.9 MB (216902546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818682d0362073042371c8d1a984e96bae57a7dd0102db5d847b3a69b5235cc4`  
		Last Modified: Tue, 23 Jul 2024 21:59:48 GMT  
		Size: 2.4 MB (2393420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1f7514b2a42ea5edb162e01639f182eabfedc29bc5bfde2ceadd8c8f11919`  
		Last Modified: Tue, 23 Jul 2024 21:59:40 GMT  
		Size: 459.1 KB (459090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc49206832d9cb915c5bbb5834b874dad932c09c7de129d958bdcb3cc24329b`  
		Last Modified: Tue, 23 Jul 2024 21:59:47 GMT  
		Size: 329.0 MB (329018927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3a4e3749ca11bca9e7b358155a218c30ef4e86db59da6a84b602024a9ca48b`  
		Last Modified: Tue, 23 Jul 2024 21:59:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa8757db422ca4e8975861160a79997291cbc06c3c66484c1937d20d92cd69`  
		Last Modified: Tue, 23 Jul 2024 21:59:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dff51fc9a0fcc4b1a2cc3ad946eed516a41d5c5f267cfcb3b210d0ada4c8f1`  
		Last Modified: Tue, 23 Jul 2024 21:59:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f45820906c7ea0824532e839bc06913088655c2b19f9c3d5d732ca687ff0ea`  
		Last Modified: Tue, 23 Jul 2024 21:59:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d45aac73a22b736af84d35e6f6a6c455c6b6956b0e4fb145af6241cdcd6950e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38747610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321eb022629dcec5da12f9d903165af97bb6365ee0d873769a88c39172761229`

```dockerfile
```

-	Layers:
	-	`sha256:d22066b3ac89a6d86399fc2f8e9c7430c0f94489cc48059cca3e0097cf1159ba`  
		Last Modified: Tue, 23 Jul 2024 21:59:41 GMT  
		Size: 38.7 MB (38720771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c2607b67140f31860977eb12781dda018682e7d6f5834153f6415522c186b2`  
		Last Modified: Tue, 23 Jul 2024 21:59:40 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1d5a7af3451af0f1552ce5958a6a8b84a0696fc7b8e61dcd3c53a7690cc0cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597795854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87598250efb43fffc1781e6ae3f1aacc17047964f8c86157b9b04db8f26b312f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9580f055a1eb6c34a4542ffa863a4893d52b7ef102494021008dc372c6cde9`  
		Last Modified: Tue, 23 Jul 2024 19:40:04 GMT  
		Size: 228.6 MB (228590608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38903e57619504f2567ca9e4ad773a4b2905923d4b3ccdeefa0f979af4387a59`  
		Last Modified: Tue, 23 Jul 2024 19:39:50 GMT  
		Size: 2.6 MB (2634111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00c518bc786cc67dbe79950d2ffb2dfe18eb3ecf6defb5756c2eb09a50c646`  
		Last Modified: Tue, 23 Jul 2024 19:39:49 GMT  
		Size: 459.1 KB (459094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ec69368b416237897d06efb555192f0ff36c3d16ef31c92f953579d81ba3`  
		Last Modified: Tue, 23 Jul 2024 19:40:21 GMT  
		Size: 330.8 MB (330804411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7a9611fe3e10273f80e33812fe5da3ae06cdc9c0a78d7efa0964c963a9f8e`  
		Last Modified: Tue, 23 Jul 2024 19:39:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e1b13b4c630335281709b6bcb436e7e4b77c41e59d71de8b11fd0a65f7971`  
		Last Modified: Tue, 23 Jul 2024 19:39:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12a241aa92a5f968792b5391f8efbeea9f72a88eec5ecd39b9f504882e4d1d2`  
		Last Modified: Tue, 23 Jul 2024 19:39:52 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2959434ef9eaede3d3bc8d2d37265f38aadebc613a3a86a496650048c052f6`  
		Last Modified: Tue, 23 Jul 2024 19:39:52 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:92259c92786717692561c8ae077e386a755c9a69b238cfb52c30562b44b46543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38749023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc3e3321e67ce28bd3a42c199b7c5e95b7bf0b50d823eb998cf42978fb5eea`

```dockerfile
```

-	Layers:
	-	`sha256:f17c14b269c74cb85bd39f05268d97d113343d4f91e9e8cbbdc3342773aeab14`  
		Last Modified: Tue, 23 Jul 2024 19:39:55 GMT  
		Size: 38.7 MB (38722431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c080c16478ea119c13ce8958684dc20193c4c200a5e9f33f4a429c828d7e8f0`  
		Last Modified: Tue, 23 Jul 2024 19:39:49 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240711`

```console
$ docker pull odoo@sha256:2691e8358530688e446264f030d49518238ac0e4d13e6e026adf90062fe32d79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240711` - linux; amd64

```console
$ docker pull odoo@sha256:2405e3d33424be2d1b281fafc5df8ff622b85fc21d3372cc1d951c5c23cec727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583250199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5eae6b196e49215d3792e12f38e9ad73faf404597c657ca47f377702ed7ad3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc75f0337d86913e92fcda4b7ffe5096be51415b255fc7510d8bafe68861dc`  
		Last Modified: Tue, 23 Jul 2024 07:22:48 GMT  
		Size: 219.6 MB (219594107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a8e9b4eaab138ac3b26458239add25d9cf4a25c309812bd6ea41b9ced5096b`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 2.4 MB (2391002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712493a4eac3046ce138796ce7810538365a077f666e815f46601282c0e1183f`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 459.1 KB (459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bb6e7818570d1a6fcc42e7935be0c114eaa2c17e2d98481c1dee10653cebc`  
		Last Modified: Tue, 23 Jul 2024 07:22:49 GMT  
		Size: 329.4 MB (329375239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83970500672e4e1c1e1aa921bf2086e13650553298e4df2a63036eea38742c40`  
		Last Modified: Tue, 23 Jul 2024 07:22:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ede3d485c44d0e51daf0f907fd4c1c17740918169a54d88f6f0698a5d0d4136`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9212b0189a0837342a5a22d2f2275dad052fc79f1fc6a6eb0072dee0551beb0`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f533450ab17892004559dc203136a8a0c92282b703714dce03a89b7b360bd3`  
		Last Modified: Tue, 23 Jul 2024 07:22:45 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:83a8639e21c5271059dc1b1238c1cba54ee021194cc5b11cf904e84aac37f77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38740841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498f7dd28b17ed405d5faf04f39c9d8c8fcf121e707c472164a592f05e24be8e`

```dockerfile
```

-	Layers:
	-	`sha256:c99d1deb2afd21049bdf088e79ac1c63acb17a90912e279cadef66f4078aa4f0`  
		Last Modified: Tue, 23 Jul 2024 07:22:44 GMT  
		Size: 38.7 MB (38714299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734df295fbdb00840f52373a0ff48f1f1f2900e28326b555a1c7b416be3518a`  
		Last Modified: Tue, 23 Jul 2024 07:22:43 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240711` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:50694a9a24e4c091f40189942d46e5f8c02d2799b8a8f29c1b0822cc8fdc01c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578852501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542c43129b5f7747f72ff9dab502b9a02654e78f46d3fe282303a13f03079e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892185f77cfcac6354372a8675b7665238515fab1ea3a2be2440093165bc8c7e`  
		Last Modified: Tue, 23 Jul 2024 21:59:45 GMT  
		Size: 216.9 MB (216902546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818682d0362073042371c8d1a984e96bae57a7dd0102db5d847b3a69b5235cc4`  
		Last Modified: Tue, 23 Jul 2024 21:59:48 GMT  
		Size: 2.4 MB (2393420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1f7514b2a42ea5edb162e01639f182eabfedc29bc5bfde2ceadd8c8f11919`  
		Last Modified: Tue, 23 Jul 2024 21:59:40 GMT  
		Size: 459.1 KB (459090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc49206832d9cb915c5bbb5834b874dad932c09c7de129d958bdcb3cc24329b`  
		Last Modified: Tue, 23 Jul 2024 21:59:47 GMT  
		Size: 329.0 MB (329018927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3a4e3749ca11bca9e7b358155a218c30ef4e86db59da6a84b602024a9ca48b`  
		Last Modified: Tue, 23 Jul 2024 21:59:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa8757db422ca4e8975861160a79997291cbc06c3c66484c1937d20d92cd69`  
		Last Modified: Tue, 23 Jul 2024 21:59:42 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dff51fc9a0fcc4b1a2cc3ad946eed516a41d5c5f267cfcb3b210d0ada4c8f1`  
		Last Modified: Tue, 23 Jul 2024 21:59:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f45820906c7ea0824532e839bc06913088655c2b19f9c3d5d732ca687ff0ea`  
		Last Modified: Tue, 23 Jul 2024 21:59:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:d45aac73a22b736af84d35e6f6a6c455c6b6956b0e4fb145af6241cdcd6950e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38747610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321eb022629dcec5da12f9d903165af97bb6365ee0d873769a88c39172761229`

```dockerfile
```

-	Layers:
	-	`sha256:d22066b3ac89a6d86399fc2f8e9c7430c0f94489cc48059cca3e0097cf1159ba`  
		Last Modified: Tue, 23 Jul 2024 21:59:41 GMT  
		Size: 38.7 MB (38720771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c2607b67140f31860977eb12781dda018682e7d6f5834153f6415522c186b2`  
		Last Modified: Tue, 23 Jul 2024 21:59:40 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240711` - linux; ppc64le

```console
$ docker pull odoo@sha256:1d5a7af3451af0f1552ce5958a6a8b84a0696fc7b8e61dcd3c53a7690cc0cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597795854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87598250efb43fffc1781e6ae3f1aacc17047964f8c86157b9b04db8f26b312f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jul 2024 09:17:21 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Thu, 11 Jul 2024 09:17:21 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=ppc64le
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=16.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240711 ODOO_SHA=0d16aea37be116a0fd07fc13c9c29a244737b419
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
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9580f055a1eb6c34a4542ffa863a4893d52b7ef102494021008dc372c6cde9`  
		Last Modified: Tue, 23 Jul 2024 19:40:04 GMT  
		Size: 228.6 MB (228590608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38903e57619504f2567ca9e4ad773a4b2905923d4b3ccdeefa0f979af4387a59`  
		Last Modified: Tue, 23 Jul 2024 19:39:50 GMT  
		Size: 2.6 MB (2634111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00c518bc786cc67dbe79950d2ffb2dfe18eb3ecf6defb5756c2eb09a50c646`  
		Last Modified: Tue, 23 Jul 2024 19:39:49 GMT  
		Size: 459.1 KB (459094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ec69368b416237897d06efb555192f0ff36c3d16ef31c92f953579d81ba3`  
		Last Modified: Tue, 23 Jul 2024 19:40:21 GMT  
		Size: 330.8 MB (330804411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7a9611fe3e10273f80e33812fe5da3ae06cdc9c0a78d7efa0964c963a9f8e`  
		Last Modified: Tue, 23 Jul 2024 19:39:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e1b13b4c630335281709b6bcb436e7e4b77c41e59d71de8b11fd0a65f7971`  
		Last Modified: Tue, 23 Jul 2024 19:39:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12a241aa92a5f968792b5391f8efbeea9f72a88eec5ecd39b9f504882e4d1d2`  
		Last Modified: Tue, 23 Jul 2024 19:39:52 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2959434ef9eaede3d3bc8d2d37265f38aadebc613a3a86a496650048c052f6`  
		Last Modified: Tue, 23 Jul 2024 19:39:52 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:92259c92786717692561c8ae077e386a755c9a69b238cfb52c30562b44b46543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38749023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dc3e3321e67ce28bd3a42c199b7c5e95b7bf0b50d823eb998cf42978fb5eea`

```dockerfile
```

-	Layers:
	-	`sha256:f17c14b269c74cb85bd39f05268d97d113343d4f91e9e8cbbdc3342773aeab14`  
		Last Modified: Tue, 23 Jul 2024 19:39:55 GMT  
		Size: 38.7 MB (38722431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c080c16478ea119c13ce8958684dc20193c4c200a5e9f33f4a429c828d7e8f0`  
		Last Modified: Tue, 23 Jul 2024 19:39:49 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:29750ac059c97311d1110315eb5e69ebdeb72896775ae5703f2ff9c7e367c6b9
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
$ docker pull odoo@sha256:5b60986dbe6b2db97911f0a1e0875eaadc013576b7156b3c5a54f5f4689b2f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.9 MB (594923929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673383c2274db23312c28c3595cfea7e332782e8d6614ebecd921246996c52d`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa14802fb7d185c79326bf897147319eaf597e19406665a21a9d200bf907a5`  
		Last Modified: Thu, 11 Jul 2024 18:01:30 GMT  
		Size: 233.7 MB (233729244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868477facf9465e69d08c01985e645943a967e5b1204cf17dac0350bfb8d0f7`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 2.3 MB (2313745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e08a715af7a09b244385d395b8349692a6beb6570549928f7a76d78500350eb`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 460.3 KB (460278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a72928d1dbdc1f180ba6088eb4d56eb1c4763895020f1b6b266c694303a9c8`  
		Last Modified: Thu, 11 Jul 2024 18:01:32 GMT  
		Size: 328.9 MB (328884169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f60931f423faddacb3ab69a42d5daefd456a377bbbe6a37cbf525ddf4265f11`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2949b540d78cdc199cbe5ea51109fbffb446753ad6b753bebc022e1b724db56`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f74de41d2390f8d6bca84985775164e160a3accd6de3a4723dd0014c4d60aa1`  
		Last Modified: Thu, 11 Jul 2024 18:01:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345d00d74e0ce8a37bca72a715a1d7cb261217b5567f035918e69d709b152d2`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:ca3831d46f44808c44e2f67dac5879eedcc11a43b12e31f10b0cb7a1ca631e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38720505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75239113c1563771a048f7df8e566912de53acf5579fa254231eef0aa5517239`

```dockerfile
```

-	Layers:
	-	`sha256:467b3b9c7946a88c2a14d14dd29dedb5d2b64846f76b929259ee050b50bb987a`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 38.7 MB (38693630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e91f5ce257d36acb081a7c6ec2a138c5ca06b6e10603db5166bf66bb1c275c`  
		Last Modified: Thu, 11 Jul 2024 18:01:26 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3ee5fabbdb36590f4044cc3e67566ec31bcf2f7eab687e25e5651bacee5233a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589738113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddabb152cc35d91713e71ed4b1b42b1822a15d9ba8b39ed20fba33af1be1d55f`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e7023e2c0e40c540b378ee24905027ddf922f32f55af7cffdeea717ad1042`  
		Last Modified: Thu, 11 Jul 2024 18:18:11 GMT  
		Size: 231.1 MB (231122061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63ebfa847b63f8a44892520527caa1e7d7b0263588124fc8e335db79eec5b1e`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 2.3 MB (2306453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f08239a2c711b7c6214ef1f4210cdbbd0c97bada8a24667e450151422f3e3d`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
		Size: 460.2 KB (460196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b25d4b7cea44905a90fc4f35fad6f065fe59527498cecf980f557940f7c4d`  
		Last Modified: Thu, 11 Jul 2024 18:18:13 GMT  
		Size: 328.5 MB (328486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8445b5f84325871ee9d1935e56f24a13864a037fe26eef5d191024c151b65847`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae7b4ede6f19f566a7e1f3157dd31fa290b618977afec4ff27643fadcdda561`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad23c639139c4e5d6ec9d7280bc1e36b603e174c90b9b2e96a1a2ac0fd91c10`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb68210a88855ee8e62482b881b82a543315a2332a7c2a3a088e2c645379901`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:691111c4a49b656e978f10af7534a4115482b6135da920c664072f93c06f580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38727331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5257be487e5e87a3a0cabf94f131e758fa9d54538dbc75f34ea9d40d2d9674`

```dockerfile
```

-	Layers:
	-	`sha256:aea6517158a91d118b077a8a68ebbaa00df19935971cca56839e630ff569d369`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 38.7 MB (38700155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11a29faa324097a8b09d7268fed366bccefa991a206fe75ca432ac87c461a76`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
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
$ docker pull odoo@sha256:29750ac059c97311d1110315eb5e69ebdeb72896775ae5703f2ff9c7e367c6b9
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
$ docker pull odoo@sha256:5b60986dbe6b2db97911f0a1e0875eaadc013576b7156b3c5a54f5f4689b2f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.9 MB (594923929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673383c2274db23312c28c3595cfea7e332782e8d6614ebecd921246996c52d`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa14802fb7d185c79326bf897147319eaf597e19406665a21a9d200bf907a5`  
		Last Modified: Thu, 11 Jul 2024 18:01:30 GMT  
		Size: 233.7 MB (233729244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868477facf9465e69d08c01985e645943a967e5b1204cf17dac0350bfb8d0f7`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 2.3 MB (2313745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e08a715af7a09b244385d395b8349692a6beb6570549928f7a76d78500350eb`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 460.3 KB (460278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a72928d1dbdc1f180ba6088eb4d56eb1c4763895020f1b6b266c694303a9c8`  
		Last Modified: Thu, 11 Jul 2024 18:01:32 GMT  
		Size: 328.9 MB (328884169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f60931f423faddacb3ab69a42d5daefd456a377bbbe6a37cbf525ddf4265f11`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2949b540d78cdc199cbe5ea51109fbffb446753ad6b753bebc022e1b724db56`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f74de41d2390f8d6bca84985775164e160a3accd6de3a4723dd0014c4d60aa1`  
		Last Modified: Thu, 11 Jul 2024 18:01:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345d00d74e0ce8a37bca72a715a1d7cb261217b5567f035918e69d709b152d2`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ca3831d46f44808c44e2f67dac5879eedcc11a43b12e31f10b0cb7a1ca631e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38720505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75239113c1563771a048f7df8e566912de53acf5579fa254231eef0aa5517239`

```dockerfile
```

-	Layers:
	-	`sha256:467b3b9c7946a88c2a14d14dd29dedb5d2b64846f76b929259ee050b50bb987a`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 38.7 MB (38693630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e91f5ce257d36acb081a7c6ec2a138c5ca06b6e10603db5166bf66bb1c275c`  
		Last Modified: Thu, 11 Jul 2024 18:01:26 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3ee5fabbdb36590f4044cc3e67566ec31bcf2f7eab687e25e5651bacee5233a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589738113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddabb152cc35d91713e71ed4b1b42b1822a15d9ba8b39ed20fba33af1be1d55f`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e7023e2c0e40c540b378ee24905027ddf922f32f55af7cffdeea717ad1042`  
		Last Modified: Thu, 11 Jul 2024 18:18:11 GMT  
		Size: 231.1 MB (231122061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63ebfa847b63f8a44892520527caa1e7d7b0263588124fc8e335db79eec5b1e`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 2.3 MB (2306453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f08239a2c711b7c6214ef1f4210cdbbd0c97bada8a24667e450151422f3e3d`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
		Size: 460.2 KB (460196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b25d4b7cea44905a90fc4f35fad6f065fe59527498cecf980f557940f7c4d`  
		Last Modified: Thu, 11 Jul 2024 18:18:13 GMT  
		Size: 328.5 MB (328486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8445b5f84325871ee9d1935e56f24a13864a037fe26eef5d191024c151b65847`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae7b4ede6f19f566a7e1f3157dd31fa290b618977afec4ff27643fadcdda561`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad23c639139c4e5d6ec9d7280bc1e36b603e174c90b9b2e96a1a2ac0fd91c10`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb68210a88855ee8e62482b881b82a543315a2332a7c2a3a088e2c645379901`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:691111c4a49b656e978f10af7534a4115482b6135da920c664072f93c06f580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38727331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5257be487e5e87a3a0cabf94f131e758fa9d54538dbc75f34ea9d40d2d9674`

```dockerfile
```

-	Layers:
	-	`sha256:aea6517158a91d118b077a8a68ebbaa00df19935971cca56839e630ff569d369`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 38.7 MB (38700155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11a29faa324097a8b09d7268fed366bccefa991a206fe75ca432ac87c461a76`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
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
$ docker pull odoo@sha256:29750ac059c97311d1110315eb5e69ebdeb72896775ae5703f2ff9c7e367c6b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240711` - linux; amd64

```console
$ docker pull odoo@sha256:5b60986dbe6b2db97911f0a1e0875eaadc013576b7156b3c5a54f5f4689b2f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.9 MB (594923929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673383c2274db23312c28c3595cfea7e332782e8d6614ebecd921246996c52d`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa14802fb7d185c79326bf897147319eaf597e19406665a21a9d200bf907a5`  
		Last Modified: Thu, 11 Jul 2024 18:01:30 GMT  
		Size: 233.7 MB (233729244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868477facf9465e69d08c01985e645943a967e5b1204cf17dac0350bfb8d0f7`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 2.3 MB (2313745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e08a715af7a09b244385d395b8349692a6beb6570549928f7a76d78500350eb`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 460.3 KB (460278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a72928d1dbdc1f180ba6088eb4d56eb1c4763895020f1b6b266c694303a9c8`  
		Last Modified: Thu, 11 Jul 2024 18:01:32 GMT  
		Size: 328.9 MB (328884169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f60931f423faddacb3ab69a42d5daefd456a377bbbe6a37cbf525ddf4265f11`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2949b540d78cdc199cbe5ea51109fbffb446753ad6b753bebc022e1b724db56`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f74de41d2390f8d6bca84985775164e160a3accd6de3a4723dd0014c4d60aa1`  
		Last Modified: Thu, 11 Jul 2024 18:01:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345d00d74e0ce8a37bca72a715a1d7cb261217b5567f035918e69d709b152d2`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:ca3831d46f44808c44e2f67dac5879eedcc11a43b12e31f10b0cb7a1ca631e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38720505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75239113c1563771a048f7df8e566912de53acf5579fa254231eef0aa5517239`

```dockerfile
```

-	Layers:
	-	`sha256:467b3b9c7946a88c2a14d14dd29dedb5d2b64846f76b929259ee050b50bb987a`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 38.7 MB (38693630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e91f5ce257d36acb081a7c6ec2a138c5ca06b6e10603db5166bf66bb1c275c`  
		Last Modified: Thu, 11 Jul 2024 18:01:26 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240711` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3ee5fabbdb36590f4044cc3e67566ec31bcf2f7eab687e25e5651bacee5233a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589738113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddabb152cc35d91713e71ed4b1b42b1822a15d9ba8b39ed20fba33af1be1d55f`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e7023e2c0e40c540b378ee24905027ddf922f32f55af7cffdeea717ad1042`  
		Last Modified: Thu, 11 Jul 2024 18:18:11 GMT  
		Size: 231.1 MB (231122061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63ebfa847b63f8a44892520527caa1e7d7b0263588124fc8e335db79eec5b1e`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 2.3 MB (2306453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f08239a2c711b7c6214ef1f4210cdbbd0c97bada8a24667e450151422f3e3d`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
		Size: 460.2 KB (460196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b25d4b7cea44905a90fc4f35fad6f065fe59527498cecf980f557940f7c4d`  
		Last Modified: Thu, 11 Jul 2024 18:18:13 GMT  
		Size: 328.5 MB (328486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8445b5f84325871ee9d1935e56f24a13864a037fe26eef5d191024c151b65847`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae7b4ede6f19f566a7e1f3157dd31fa290b618977afec4ff27643fadcdda561`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad23c639139c4e5d6ec9d7280bc1e36b603e174c90b9b2e96a1a2ac0fd91c10`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb68210a88855ee8e62482b881b82a543315a2332a7c2a3a088e2c645379901`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240711` - unknown; unknown

```console
$ docker pull odoo@sha256:691111c4a49b656e978f10af7534a4115482b6135da920c664072f93c06f580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38727331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5257be487e5e87a3a0cabf94f131e758fa9d54538dbc75f34ea9d40d2d9674`

```dockerfile
```

-	Layers:
	-	`sha256:aea6517158a91d118b077a8a68ebbaa00df19935971cca56839e630ff569d369`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 38.7 MB (38700155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11a29faa324097a8b09d7268fed366bccefa991a206fe75ca432ac87c461a76`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull odoo@sha256:29750ac059c97311d1110315eb5e69ebdeb72896775ae5703f2ff9c7e367c6b9
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
$ docker pull odoo@sha256:5b60986dbe6b2db97911f0a1e0875eaadc013576b7156b3c5a54f5f4689b2f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.9 MB (594923929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673383c2274db23312c28c3595cfea7e332782e8d6614ebecd921246996c52d`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=amd64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa14802fb7d185c79326bf897147319eaf597e19406665a21a9d200bf907a5`  
		Last Modified: Thu, 11 Jul 2024 18:01:30 GMT  
		Size: 233.7 MB (233729244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868477facf9465e69d08c01985e645943a967e5b1204cf17dac0350bfb8d0f7`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 2.3 MB (2313745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e08a715af7a09b244385d395b8349692a6beb6570549928f7a76d78500350eb`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 460.3 KB (460278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a72928d1dbdc1f180ba6088eb4d56eb1c4763895020f1b6b266c694303a9c8`  
		Last Modified: Thu, 11 Jul 2024 18:01:32 GMT  
		Size: 328.9 MB (328884169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f60931f423faddacb3ab69a42d5daefd456a377bbbe6a37cbf525ddf4265f11`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2949b540d78cdc199cbe5ea51109fbffb446753ad6b753bebc022e1b724db56`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f74de41d2390f8d6bca84985775164e160a3accd6de3a4723dd0014c4d60aa1`  
		Last Modified: Thu, 11 Jul 2024 18:01:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d345d00d74e0ce8a37bca72a715a1d7cb261217b5567f035918e69d709b152d2`  
		Last Modified: Thu, 11 Jul 2024 18:01:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:ca3831d46f44808c44e2f67dac5879eedcc11a43b12e31f10b0cb7a1ca631e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38720505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75239113c1563771a048f7df8e566912de53acf5579fa254231eef0aa5517239`

```dockerfile
```

-	Layers:
	-	`sha256:467b3b9c7946a88c2a14d14dd29dedb5d2b64846f76b929259ee050b50bb987a`  
		Last Modified: Thu, 11 Jul 2024 18:01:27 GMT  
		Size: 38.7 MB (38693630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e91f5ce257d36acb081a7c6ec2a138c5ca06b6e10603db5166bf66bb1c275c`  
		Last Modified: Thu, 11 Jul 2024 18:01:26 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3ee5fabbdb36590f4044cc3e67566ec31bcf2f7eab687e25e5651bacee5233a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589738113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddabb152cc35d91713e71ed4b1b42b1822a15d9ba8b39ed20fba33af1be1d55f`
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
# Thu, 11 Jul 2024 09:17:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jul 2024 09:17:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jul 2024 09:17:21 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Jul 2024 09:17:21 GMT
ARG TARGETARCH=arm64
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
ENV ODOO_VERSION=17.0
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_RELEASE=20240711
# Thu, 11 Jul 2024 09:17:21 GMT
ARG ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 11 Jul 2024 09:17:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240711 ODOO_SHA=48a1ea9f9e6cf3d4913234c674cccd8c875a9aa4
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e7023e2c0e40c540b378ee24905027ddf922f32f55af7cffdeea717ad1042`  
		Last Modified: Thu, 11 Jul 2024 18:18:11 GMT  
		Size: 231.1 MB (231122061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63ebfa847b63f8a44892520527caa1e7d7b0263588124fc8e335db79eec5b1e`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 2.3 MB (2306453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f08239a2c711b7c6214ef1f4210cdbbd0c97bada8a24667e450151422f3e3d`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
		Size: 460.2 KB (460196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b25d4b7cea44905a90fc4f35fad6f065fe59527498cecf980f557940f7c4d`  
		Last Modified: Thu, 11 Jul 2024 18:18:13 GMT  
		Size: 328.5 MB (328486934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8445b5f84325871ee9d1935e56f24a13864a037fe26eef5d191024c151b65847`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae7b4ede6f19f566a7e1f3157dd31fa290b618977afec4ff27643fadcdda561`  
		Last Modified: Thu, 11 Jul 2024 18:18:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad23c639139c4e5d6ec9d7280bc1e36b603e174c90b9b2e96a1a2ac0fd91c10`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb68210a88855ee8e62482b881b82a543315a2332a7c2a3a088e2c645379901`  
		Last Modified: Thu, 11 Jul 2024 18:18:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:691111c4a49b656e978f10af7534a4115482b6135da920c664072f93c06f580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38727331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5257be487e5e87a3a0cabf94f131e758fa9d54538dbc75f34ea9d40d2d9674`

```dockerfile
```

-	Layers:
	-	`sha256:aea6517158a91d118b077a8a68ebbaa00df19935971cca56839e630ff569d369`  
		Last Modified: Thu, 11 Jul 2024 18:18:07 GMT  
		Size: 38.7 MB (38700155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11a29faa324097a8b09d7268fed366bccefa991a206fe75ca432ac87c461a76`  
		Last Modified: Thu, 11 Jul 2024 18:18:06 GMT  
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
