<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240826`](#odoo150-20240826)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240826`](#odoo160-20240826)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240826`](#odoo170-20240826)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:bfad05590228132a733ce91250538f2e5ff39b875084baa8863c7f1009f7127e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:91dae881bc077f71856f31499c8a3293c1f6289661e57e2e9d87fe5507a445e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564268349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6756316fb3c383f6201b95339b687f7bd68eb8a7f9cbf586115cc501a8f52d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=15.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: ODOO_RELEASE=20240826 ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: ODOO_RELEASE=20240826 ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953cec6685f9415cc1cf6a326088c0b5fba59cce7174ad49b0932b9e661d371f`  
		Last Modified: Mon, 26 Aug 2024 22:01:23 GMT  
		Size: 220.3 MB (220281677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898a9f9db612ef49abc8b7b9a345927024e96724803cb00b6739912aa0d38cd`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 2.4 MB (2387831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d22490d0a23fdb589db9968966d0e12caf3ae7702a4c120186529ebd72aa7`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 463.9 KB (463853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc78ff6377fe57215decbb14c242504527eb1c0908bb6388f1a425247f484ca2`  
		Last Modified: Mon, 26 Aug 2024 22:01:27 GMT  
		Size: 309.7 MB (309704269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95abe9fc1cfe2c93a104aa574c40033ecb138a0fe38536ca5cc14cb7d00df8e7`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8539b066c228755e702bbb08c749beba1df80321f824c1c52cca302d37d69308`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da427c4e5dab1c7528cd4d94eca5a54309305bf564981e52e63f433da0b4f48`  
		Last Modified: Mon, 26 Aug 2024 22:01:20 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35da579f02b5903a66be24ed582fc1e3b89565d73dd88e25c9f0dbc2c3d9027`  
		Last Modified: Mon, 26 Aug 2024 22:01:20 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:19891df45872242ac2a69628dd858efdc352ef43581cb68348a2c967bf95712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190f7a07d1ed4afc5db20b99be0397f646b77e0cb42412c3b7c8a8a856b0a0d8`

```dockerfile
```

-	Layers:
	-	`sha256:7bce76c22a3dc2ef464ad85c18bbdec3bb02cac3c288d7c5815bc99cf271dd3a`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a6fcf54a7244051e20203b73336822fcd96c9fd168c7625fa44681c52b776f`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:bfad05590228132a733ce91250538f2e5ff39b875084baa8863c7f1009f7127e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:91dae881bc077f71856f31499c8a3293c1f6289661e57e2e9d87fe5507a445e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564268349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6756316fb3c383f6201b95339b687f7bd68eb8a7f9cbf586115cc501a8f52d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=15.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: ODOO_RELEASE=20240826 ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: ODOO_RELEASE=20240826 ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953cec6685f9415cc1cf6a326088c0b5fba59cce7174ad49b0932b9e661d371f`  
		Last Modified: Mon, 26 Aug 2024 22:01:23 GMT  
		Size: 220.3 MB (220281677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898a9f9db612ef49abc8b7b9a345927024e96724803cb00b6739912aa0d38cd`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 2.4 MB (2387831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d22490d0a23fdb589db9968966d0e12caf3ae7702a4c120186529ebd72aa7`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 463.9 KB (463853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc78ff6377fe57215decbb14c242504527eb1c0908bb6388f1a425247f484ca2`  
		Last Modified: Mon, 26 Aug 2024 22:01:27 GMT  
		Size: 309.7 MB (309704269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95abe9fc1cfe2c93a104aa574c40033ecb138a0fe38536ca5cc14cb7d00df8e7`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8539b066c228755e702bbb08c749beba1df80321f824c1c52cca302d37d69308`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da427c4e5dab1c7528cd4d94eca5a54309305bf564981e52e63f433da0b4f48`  
		Last Modified: Mon, 26 Aug 2024 22:01:20 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35da579f02b5903a66be24ed582fc1e3b89565d73dd88e25c9f0dbc2c3d9027`  
		Last Modified: Mon, 26 Aug 2024 22:01:20 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:19891df45872242ac2a69628dd858efdc352ef43581cb68348a2c967bf95712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190f7a07d1ed4afc5db20b99be0397f646b77e0cb42412c3b7c8a8a856b0a0d8`

```dockerfile
```

-	Layers:
	-	`sha256:7bce76c22a3dc2ef464ad85c18bbdec3bb02cac3c288d7c5815bc99cf271dd3a`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a6fcf54a7244051e20203b73336822fcd96c9fd168c7625fa44681c52b776f`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240826`

```console
$ docker pull odoo@sha256:bfad05590228132a733ce91250538f2e5ff39b875084baa8863c7f1009f7127e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240826` - linux; amd64

```console
$ docker pull odoo@sha256:91dae881bc077f71856f31499c8a3293c1f6289661e57e2e9d87fe5507a445e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564268349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6756316fb3c383f6201b95339b687f7bd68eb8a7f9cbf586115cc501a8f52d2b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=15.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: ODOO_RELEASE=20240826 ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: ODOO_RELEASE=20240826 ODOO_SHA=8619048c1cc90d5e388d93a6d4a63f4d4d05ee82
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953cec6685f9415cc1cf6a326088c0b5fba59cce7174ad49b0932b9e661d371f`  
		Last Modified: Mon, 26 Aug 2024 22:01:23 GMT  
		Size: 220.3 MB (220281677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3898a9f9db612ef49abc8b7b9a345927024e96724803cb00b6739912aa0d38cd`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 2.4 MB (2387831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d22490d0a23fdb589db9968966d0e12caf3ae7702a4c120186529ebd72aa7`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 463.9 KB (463853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc78ff6377fe57215decbb14c242504527eb1c0908bb6388f1a425247f484ca2`  
		Last Modified: Mon, 26 Aug 2024 22:01:27 GMT  
		Size: 309.7 MB (309704269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95abe9fc1cfe2c93a104aa574c40033ecb138a0fe38536ca5cc14cb7d00df8e7`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8539b066c228755e702bbb08c749beba1df80321f824c1c52cca302d37d69308`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da427c4e5dab1c7528cd4d94eca5a54309305bf564981e52e63f433da0b4f48`  
		Last Modified: Mon, 26 Aug 2024 22:01:20 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35da579f02b5903a66be24ed582fc1e3b89565d73dd88e25c9f0dbc2c3d9027`  
		Last Modified: Mon, 26 Aug 2024 22:01:20 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:19891df45872242ac2a69628dd858efdc352ef43581cb68348a2c967bf95712d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190f7a07d1ed4afc5db20b99be0397f646b77e0cb42412c3b7c8a8a856b0a0d8`

```dockerfile
```

-	Layers:
	-	`sha256:7bce76c22a3dc2ef464ad85c18bbdec3bb02cac3c288d7c5815bc99cf271dd3a`  
		Last Modified: Mon, 26 Aug 2024 22:01:19 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a6fcf54a7244051e20203b73336822fcd96c9fd168c7625fa44681c52b776f`  
		Last Modified: Mon, 26 Aug 2024 22:01:18 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:66e7d8aa1203238d2b4459b167dcba3a9d3789adbb2d048f39a0a77aeac9d941
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
$ docker pull odoo@sha256:c740e81a9c82a0161473a79438e9f0d7c71d185077fb47d3eac41513acacf959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (584009770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f366d678237cdc8e430719a51986b065c3e1bd536c092d02d2134685eb79d494`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e6090409f1a3ef7023b8096d724c65ca94331fb1a24a1de0769ec3bddf4c8`  
		Last Modified: Mon, 26 Aug 2024 22:01:33 GMT  
		Size: 219.6 MB (219593403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f408f5e50701e2cb4e948bb7f39e2f35374e26e1ecd26b6a8ac3c909aec37926`  
		Last Modified: Mon, 26 Aug 2024 22:01:28 GMT  
		Size: 2.4 MB (2391423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d018d5ef1ee12b3072ccc5e94d2f18ed095956991447a8dc17478df09352ed8`  
		Last Modified: Mon, 26 Aug 2024 22:01:28 GMT  
		Size: 463.8 KB (463831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018e3386e041cc38d06d23910875b63d66b0f438885991980a521e21cee79206`  
		Last Modified: Mon, 26 Aug 2024 22:01:35 GMT  
		Size: 330.1 MB (330130392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebf1059f49506845c255e39def60a1ee2dbc71528c6a24e433061896ed95bf9`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc3c118061b9cf1b24910e85f56cbb8937a9cd48b9489c8f10b740b687e5c1`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a4a8ddaca75fd0334c395b9c50dd65102c57134271dda6f0566038e5631382`  
		Last Modified: Mon, 26 Aug 2024 22:01:30 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8a25271a3bde7ee31eb1439502db8472a74b24e89730b3a0fffd95a236c7b`  
		Last Modified: Mon, 26 Aug 2024 22:01:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:062b4b9fbbe4f8ebc4c1f9921e847f4c0828f9327d1a3dd6561846eac32a2ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38755710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d8624441ad4c67d3b3cd1027047274503636207773716fe6368cf4cd74020a`

```dockerfile
```

-	Layers:
	-	`sha256:4d4acc5553b6cc6d64321dd8271ee53d8a9e101333c160f55d5b6b55ab79bed4`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 38.7 MB (38729168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77134cc3733e55c08d1470d62df1903a78599b7fc81bbe20c0546c6b0db174a`  
		Last Modified: Mon, 26 Aug 2024 22:01:27 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f7b757a86867521b638f0a2733634800154a7612d3be97e0ce048badd40d2751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.6 MB (579603924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b16f27896f747d88d8c6dde473f0256c90906bbcd98895a0db6dffb5c50880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4916f0ae01714a20a0a5ff458b90344ffaaefc6345c7905aa37f82a43593a4`  
		Last Modified: Mon, 19 Aug 2024 18:05:16 GMT  
		Size: 216.9 MB (216902229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc4b7cedc1a31fafa7f7d54399d12b095bdebd5ad02fa63495ae04863b893`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 2.4 MB (2394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b92a7253330c959ed65950618df7f6853cbcd2c9d050c3f4bfd4171fc5755f`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 463.8 KB (463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb57055b1fe5a93c3c409741f5abc796c4a4836ca8d1d48c5c44a6ee7219185`  
		Last Modified: Mon, 26 Aug 2024 22:05:15 GMT  
		Size: 329.8 MB (329765357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55772105757940c9533b527d920930ec79227ae39169f88b6aad060a47a7a30a`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9012b6049fc14ee725f7f19a5f0d5566e6de3a56ac1f451ba6bfe8dc453ea17`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6772afa91ec6e415c6d2586f50f0f519ab9a3b5ff03006c50ec90312605e`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d80e9444c1d3e8b24d47761975498aae700e4933abb1c09051c6a89b73ed67`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:4f9bcd5eb9338afc178b3851acfc6b03c1d5fc9bc1c59fa7644e225cf3c6a4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b1081bb54d9e90f8b490be2411d7dcb079524a762400f4ba3852e2fbc857d6`

```dockerfile
```

-	Layers:
	-	`sha256:54a48aee74fb803ace7bc2582d2bb467ca70064981872213ff6f8141daf8c550`  
		Last Modified: Mon, 26 Aug 2024 22:05:10 GMT  
		Size: 38.7 MB (38735640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed223ae9b3e039e47e6b92d805bfb55e0fb03eb9bd607c3b290e27620d9607c`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:0af1c97f1b580b1e41fb7de6e063daca46bff9d2cdfde77825ced4f4e65eb015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598554452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4e35be5d9896931e701f54236bdee1b0cb090fd751d393092cda813ee4cf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473977bf1d2bc93688151522365af64276b55d1bd7ed26f1f54dce620240eae5`  
		Last Modified: Mon, 19 Aug 2024 18:11:08 GMT  
		Size: 228.6 MB (228589663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866217a2e7bca4e7ecb960007dfb531409e7b88588617898dd9736a9784b083e`  
		Last Modified: Mon, 19 Aug 2024 18:10:58 GMT  
		Size: 2.6 MB (2634314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1361f8b87aa4ec2df887c300d21f906c8bcdb3c7a7635a5c69e3c002758856c`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 463.9 KB (463862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8857417051d743c1e0dd980e814c9a3d0e352059c7cecf891e6c9870eb3d9e9a`  
		Last Modified: Mon, 26 Aug 2024 22:12:34 GMT  
		Size: 331.6 MB (331559044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9797729063bd42bebbccae298ddff7d87b91142900486b0ed829f5d6aa7a480`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f88e0f6508cc50b157289bdcadeb259379e6dcdbfa51c3d843d55eac9d4e3f`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93943b19efc3cd9617b9236f23cac4744d6762876f510f3ac3cd523fc07fb6b6`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5049b24dac127a4a3f0070e593b3853523651832908efd0dbc752c8d6dfac574`  
		Last Modified: Mon, 26 Aug 2024 22:12:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:1b9977617871ecc7555bcc4bdf192253406f69d4086613efa2f5cd0281d796fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38763891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e2fe38cede86742ad8e921c84be66c19eaea759e0a7b45bfd0bebd8a140fe2`

```dockerfile
```

-	Layers:
	-	`sha256:b5d5f466ad05f6e34c8b4ce78e3e1966303e3152c309ab36e0cfb670a65a2738`  
		Last Modified: Mon, 26 Aug 2024 22:12:18 GMT  
		Size: 38.7 MB (38737300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310d92b44612dde43e7929949b4b127b252964d1cc272537c9079eabc152e939`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 26.6 KB (26591 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:66e7d8aa1203238d2b4459b167dcba3a9d3789adbb2d048f39a0a77aeac9d941
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
$ docker pull odoo@sha256:c740e81a9c82a0161473a79438e9f0d7c71d185077fb47d3eac41513acacf959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (584009770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f366d678237cdc8e430719a51986b065c3e1bd536c092d02d2134685eb79d494`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e6090409f1a3ef7023b8096d724c65ca94331fb1a24a1de0769ec3bddf4c8`  
		Last Modified: Mon, 26 Aug 2024 22:01:33 GMT  
		Size: 219.6 MB (219593403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f408f5e50701e2cb4e948bb7f39e2f35374e26e1ecd26b6a8ac3c909aec37926`  
		Last Modified: Mon, 26 Aug 2024 22:01:28 GMT  
		Size: 2.4 MB (2391423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d018d5ef1ee12b3072ccc5e94d2f18ed095956991447a8dc17478df09352ed8`  
		Last Modified: Mon, 26 Aug 2024 22:01:28 GMT  
		Size: 463.8 KB (463831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018e3386e041cc38d06d23910875b63d66b0f438885991980a521e21cee79206`  
		Last Modified: Mon, 26 Aug 2024 22:01:35 GMT  
		Size: 330.1 MB (330130392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebf1059f49506845c255e39def60a1ee2dbc71528c6a24e433061896ed95bf9`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc3c118061b9cf1b24910e85f56cbb8937a9cd48b9489c8f10b740b687e5c1`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a4a8ddaca75fd0334c395b9c50dd65102c57134271dda6f0566038e5631382`  
		Last Modified: Mon, 26 Aug 2024 22:01:30 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8a25271a3bde7ee31eb1439502db8472a74b24e89730b3a0fffd95a236c7b`  
		Last Modified: Mon, 26 Aug 2024 22:01:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:062b4b9fbbe4f8ebc4c1f9921e847f4c0828f9327d1a3dd6561846eac32a2ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38755710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d8624441ad4c67d3b3cd1027047274503636207773716fe6368cf4cd74020a`

```dockerfile
```

-	Layers:
	-	`sha256:4d4acc5553b6cc6d64321dd8271ee53d8a9e101333c160f55d5b6b55ab79bed4`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 38.7 MB (38729168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77134cc3733e55c08d1470d62df1903a78599b7fc81bbe20c0546c6b0db174a`  
		Last Modified: Mon, 26 Aug 2024 22:01:27 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f7b757a86867521b638f0a2733634800154a7612d3be97e0ce048badd40d2751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.6 MB (579603924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b16f27896f747d88d8c6dde473f0256c90906bbcd98895a0db6dffb5c50880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4916f0ae01714a20a0a5ff458b90344ffaaefc6345c7905aa37f82a43593a4`  
		Last Modified: Mon, 19 Aug 2024 18:05:16 GMT  
		Size: 216.9 MB (216902229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc4b7cedc1a31fafa7f7d54399d12b095bdebd5ad02fa63495ae04863b893`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 2.4 MB (2394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b92a7253330c959ed65950618df7f6853cbcd2c9d050c3f4bfd4171fc5755f`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 463.8 KB (463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb57055b1fe5a93c3c409741f5abc796c4a4836ca8d1d48c5c44a6ee7219185`  
		Last Modified: Mon, 26 Aug 2024 22:05:15 GMT  
		Size: 329.8 MB (329765357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55772105757940c9533b527d920930ec79227ae39169f88b6aad060a47a7a30a`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9012b6049fc14ee725f7f19a5f0d5566e6de3a56ac1f451ba6bfe8dc453ea17`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6772afa91ec6e415c6d2586f50f0f519ab9a3b5ff03006c50ec90312605e`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d80e9444c1d3e8b24d47761975498aae700e4933abb1c09051c6a89b73ed67`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4f9bcd5eb9338afc178b3851acfc6b03c1d5fc9bc1c59fa7644e225cf3c6a4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b1081bb54d9e90f8b490be2411d7dcb079524a762400f4ba3852e2fbc857d6`

```dockerfile
```

-	Layers:
	-	`sha256:54a48aee74fb803ace7bc2582d2bb467ca70064981872213ff6f8141daf8c550`  
		Last Modified: Mon, 26 Aug 2024 22:05:10 GMT  
		Size: 38.7 MB (38735640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed223ae9b3e039e47e6b92d805bfb55e0fb03eb9bd607c3b290e27620d9607c`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0af1c97f1b580b1e41fb7de6e063daca46bff9d2cdfde77825ced4f4e65eb015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598554452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4e35be5d9896931e701f54236bdee1b0cb090fd751d393092cda813ee4cf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473977bf1d2bc93688151522365af64276b55d1bd7ed26f1f54dce620240eae5`  
		Last Modified: Mon, 19 Aug 2024 18:11:08 GMT  
		Size: 228.6 MB (228589663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866217a2e7bca4e7ecb960007dfb531409e7b88588617898dd9736a9784b083e`  
		Last Modified: Mon, 19 Aug 2024 18:10:58 GMT  
		Size: 2.6 MB (2634314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1361f8b87aa4ec2df887c300d21f906c8bcdb3c7a7635a5c69e3c002758856c`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 463.9 KB (463862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8857417051d743c1e0dd980e814c9a3d0e352059c7cecf891e6c9870eb3d9e9a`  
		Last Modified: Mon, 26 Aug 2024 22:12:34 GMT  
		Size: 331.6 MB (331559044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9797729063bd42bebbccae298ddff7d87b91142900486b0ed829f5d6aa7a480`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f88e0f6508cc50b157289bdcadeb259379e6dcdbfa51c3d843d55eac9d4e3f`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93943b19efc3cd9617b9236f23cac4744d6762876f510f3ac3cd523fc07fb6b6`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5049b24dac127a4a3f0070e593b3853523651832908efd0dbc752c8d6dfac574`  
		Last Modified: Mon, 26 Aug 2024 22:12:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1b9977617871ecc7555bcc4bdf192253406f69d4086613efa2f5cd0281d796fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38763891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e2fe38cede86742ad8e921c84be66c19eaea759e0a7b45bfd0bebd8a140fe2`

```dockerfile
```

-	Layers:
	-	`sha256:b5d5f466ad05f6e34c8b4ce78e3e1966303e3152c309ab36e0cfb670a65a2738`  
		Last Modified: Mon, 26 Aug 2024 22:12:18 GMT  
		Size: 38.7 MB (38737300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310d92b44612dde43e7929949b4b127b252964d1cc272537c9079eabc152e939`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 26.6 KB (26591 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240826`

```console
$ docker pull odoo@sha256:66e7d8aa1203238d2b4459b167dcba3a9d3789adbb2d048f39a0a77aeac9d941
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240826` - linux; amd64

```console
$ docker pull odoo@sha256:c740e81a9c82a0161473a79438e9f0d7c71d185077fb47d3eac41513acacf959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.0 MB (584009770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f366d678237cdc8e430719a51986b065c3e1bd536c092d02d2134685eb79d494`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e6090409f1a3ef7023b8096d724c65ca94331fb1a24a1de0769ec3bddf4c8`  
		Last Modified: Mon, 26 Aug 2024 22:01:33 GMT  
		Size: 219.6 MB (219593403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f408f5e50701e2cb4e948bb7f39e2f35374e26e1ecd26b6a8ac3c909aec37926`  
		Last Modified: Mon, 26 Aug 2024 22:01:28 GMT  
		Size: 2.4 MB (2391423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d018d5ef1ee12b3072ccc5e94d2f18ed095956991447a8dc17478df09352ed8`  
		Last Modified: Mon, 26 Aug 2024 22:01:28 GMT  
		Size: 463.8 KB (463831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018e3386e041cc38d06d23910875b63d66b0f438885991980a521e21cee79206`  
		Last Modified: Mon, 26 Aug 2024 22:01:35 GMT  
		Size: 330.1 MB (330130392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebf1059f49506845c255e39def60a1ee2dbc71528c6a24e433061896ed95bf9`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc3c118061b9cf1b24910e85f56cbb8937a9cd48b9489c8f10b740b687e5c1`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a4a8ddaca75fd0334c395b9c50dd65102c57134271dda6f0566038e5631382`  
		Last Modified: Mon, 26 Aug 2024 22:01:30 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8a25271a3bde7ee31eb1439502db8472a74b24e89730b3a0fffd95a236c7b`  
		Last Modified: Mon, 26 Aug 2024 22:01:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:062b4b9fbbe4f8ebc4c1f9921e847f4c0828f9327d1a3dd6561846eac32a2ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38755710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d8624441ad4c67d3b3cd1027047274503636207773716fe6368cf4cd74020a`

```dockerfile
```

-	Layers:
	-	`sha256:4d4acc5553b6cc6d64321dd8271ee53d8a9e101333c160f55d5b6b55ab79bed4`  
		Last Modified: Mon, 26 Aug 2024 22:01:29 GMT  
		Size: 38.7 MB (38729168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77134cc3733e55c08d1470d62df1903a78599b7fc81bbe20c0546c6b0db174a`  
		Last Modified: Mon, 26 Aug 2024 22:01:27 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240826` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f7b757a86867521b638f0a2733634800154a7612d3be97e0ce048badd40d2751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.6 MB (579603924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b16f27896f747d88d8c6dde473f0256c90906bbcd98895a0db6dffb5c50880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4916f0ae01714a20a0a5ff458b90344ffaaefc6345c7905aa37f82a43593a4`  
		Last Modified: Mon, 19 Aug 2024 18:05:16 GMT  
		Size: 216.9 MB (216902229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc4b7cedc1a31fafa7f7d54399d12b095bdebd5ad02fa63495ae04863b893`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 2.4 MB (2394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b92a7253330c959ed65950618df7f6853cbcd2c9d050c3f4bfd4171fc5755f`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 463.8 KB (463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb57055b1fe5a93c3c409741f5abc796c4a4836ca8d1d48c5c44a6ee7219185`  
		Last Modified: Mon, 26 Aug 2024 22:05:15 GMT  
		Size: 329.8 MB (329765357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55772105757940c9533b527d920930ec79227ae39169f88b6aad060a47a7a30a`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9012b6049fc14ee725f7f19a5f0d5566e6de3a56ac1f451ba6bfe8dc453ea17`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314e6772afa91ec6e415c6d2586f50f0f519ab9a3b5ff03006c50ec90312605e`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d80e9444c1d3e8b24d47761975498aae700e4933abb1c09051c6a89b73ed67`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:4f9bcd5eb9338afc178b3851acfc6b03c1d5fc9bc1c59fa7644e225cf3c6a4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b1081bb54d9e90f8b490be2411d7dcb079524a762400f4ba3852e2fbc857d6`

```dockerfile
```

-	Layers:
	-	`sha256:54a48aee74fb803ace7bc2582d2bb467ca70064981872213ff6f8141daf8c550`  
		Last Modified: Mon, 26 Aug 2024 22:05:10 GMT  
		Size: 38.7 MB (38735640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed223ae9b3e039e47e6b92d805bfb55e0fb03eb9bd607c3b290e27620d9607c`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240826` - linux; ppc64le

```console
$ docker pull odoo@sha256:0af1c97f1b580b1e41fb7de6e063daca46bff9d2cdfde77825ced4f4e65eb015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598554452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4e35be5d9896931e701f54236bdee1b0cb090fd751d393092cda813ee4cf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=C.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=16.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=4c360e9de7eee5401ea217e3a451d301d7547029
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473977bf1d2bc93688151522365af64276b55d1bd7ed26f1f54dce620240eae5`  
		Last Modified: Mon, 19 Aug 2024 18:11:08 GMT  
		Size: 228.6 MB (228589663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866217a2e7bca4e7ecb960007dfb531409e7b88588617898dd9736a9784b083e`  
		Last Modified: Mon, 19 Aug 2024 18:10:58 GMT  
		Size: 2.6 MB (2634314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1361f8b87aa4ec2df887c300d21f906c8bcdb3c7a7635a5c69e3c002758856c`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 463.9 KB (463862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8857417051d743c1e0dd980e814c9a3d0e352059c7cecf891e6c9870eb3d9e9a`  
		Last Modified: Mon, 26 Aug 2024 22:12:34 GMT  
		Size: 331.6 MB (331559044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9797729063bd42bebbccae298ddff7d87b91142900486b0ed829f5d6aa7a480`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f88e0f6508cc50b157289bdcadeb259379e6dcdbfa51c3d843d55eac9d4e3f`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93943b19efc3cd9617b9236f23cac4744d6762876f510f3ac3cd523fc07fb6b6`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5049b24dac127a4a3f0070e593b3853523651832908efd0dbc752c8d6dfac574`  
		Last Modified: Mon, 26 Aug 2024 22:12:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:1b9977617871ecc7555bcc4bdf192253406f69d4086613efa2f5cd0281d796fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38763891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e2fe38cede86742ad8e921c84be66c19eaea759e0a7b45bfd0bebd8a140fe2`

```dockerfile
```

-	Layers:
	-	`sha256:b5d5f466ad05f6e34c8b4ce78e3e1966303e3152c309ab36e0cfb670a65a2738`  
		Last Modified: Mon, 26 Aug 2024 22:12:18 GMT  
		Size: 38.7 MB (38737300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310d92b44612dde43e7929949b4b127b252964d1cc272537c9079eabc152e939`  
		Last Modified: Mon, 26 Aug 2024 22:12:16 GMT  
		Size: 26.6 KB (26591 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:cee5e480a79b9ec36d923e36f54ea2b713c28429caf29557d911dd62e2c1cd0a
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
$ docker pull odoo@sha256:fdb9c80b25fbfbb17cb0dab5b0485255d4507dc7588f6140e085dad48a9455d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 MB (596490653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5276d013373a314b125b07f1aad699a596e6b1e5f362ad1f71806382c2dbed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef41a7c8da96cf1ca69f45d9d8608a0c017207cd6de5c78e5590a364ca22f1e6`  
		Last Modified: Mon, 26 Aug 2024 22:01:24 GMT  
		Size: 233.7 MB (233741816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f25f100dbe9926e38793dbbf4760d8a47a33340092f03ed349c58deb933354`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 2.3 MB (2315758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21167727e18c6961d051deaccc8cd31945573f0f1ffdbd3e7e818ba1523fedc`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 464.9 KB (464915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842917c142818ca7f84f34e562efde62052216a1cd62169355d75f86fe14d3d`  
		Last Modified: Mon, 26 Aug 2024 22:01:26 GMT  
		Size: 330.4 MB (330429698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f479f5215cdb2d96eb29ccc3d8547e087a4d2cc5b9e869a7833a037d42486`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955c3020d5a4d5c2f2077185d6decfbfd64da77a75209f66051d70d93f1f2720`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebb24645a95982bc5b16c699b126c2798561fe1d8d3984107b162e349d424c`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1eec4cf1e839a5d4912a8b128fdcf443a63200a13bff6258043f26d09625a21`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e2f0f75a15dfbe7e6c4e26fd748a23bcf1f639bd75c6041c30fc346affc9596d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39037420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838c7ceae05072c0baed5fe9e472147ddfd1d548583922fe4bcf96060ceba99`

```dockerfile
```

-	Layers:
	-	`sha256:d22e5162f342757044105780008e2b244992b1a9c28998548a401731ca0c6dc1`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 39.0 MB (39010545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45bea61895ff81bc769db787df5eb63474a19eaae80a3587cfb7b920e80d49e5`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f5a7f8ff52d2b49f4ca2969456956d44167fd788e2f0cab15bb680d6e58c6001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591301670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0a04db5e01098ceb5c75aa0bd78d2d2455150a3ff23fd13176de87006d190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:ade1ad6eac09a3316704de654e0fb59bbf9004e922771273b24dd3cf9bda9a45`  
		Last Modified: Mon, 26 Aug 2024 22:02:22 GMT  
		Size: 330.1 MB (330051165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4565a373012ffb0da2e909f9fdf1057e43910873f7a9dc8347b442238c1a6`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a02cd321ac917958a3768c49ccd311a86434f8cb3ab55f15bb503d3b6c032`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b20cbfb10e95b480b1c9970fa2c18e6a8577abbb580f224f7b3e378f29cf4`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5853ae3a5df299bd78aabba7894c091cfa682904c45d3a832febb527b012ef`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:528d45180c41772ae20e180552ac313a7f41ded6a3f7075b17032359b445d917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39044230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cbd68e39ddf86432be80716f5bea81a3c62c6fd366d3aed5d29746dcf95e7c`

```dockerfile
```

-	Layers:
	-	`sha256:f367f778917a023765a4a0c21a1ebff98ea6ede9b9929f02f8fc5cc2a99c6463`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 39.0 MB (39017054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cb34dc5bf85b178160a54c46efd3bb284155ba107699577bea7fc7f99f5961`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:f129aed39ff771d108dad2492d3de4540c9ec2ed93a25414de2c50971ea52ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 MB (612959287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8361ec71ce199f078733d85efa85d1e8f482fdcb304035b196da23e5384f67f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:6cf80db5dba06a2486e607dec5802889dfe61f4d665b697389c813d17813e2a6`  
		Last Modified: Mon, 26 Aug 2024 22:05:26 GMT  
		Size: 332.2 MB (332159061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7e9328690ec814e87896a4f74c74ec767736aa76dcfb086f23298e8e15f71`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b8423da35bf77bbd97056cb2025d6c7e82037c4835d0dbc9c836d8e7df850`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a31ea83f0d1009c6609076b4aa53c3ceeb7174886da10e31d663fffe2a38f1`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77112b68c3f58d87bcaaf1f473fea4afd961a5b067719ce58582cbf5b2de5b9d`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d1f45886f871d582df7fefb4ea36cd29c1c7eccc6361dc4d5b6bdecd74c029ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39045772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b6e910eae0fb39ffe2d70f66cc4850fcdc21886716e3ff5ae0233c40bbca93`

```dockerfile
```

-	Layers:
	-	`sha256:74de53e8c3f574c41f6dfd212bd66c48f0c0cdc87dbbb7481b24bc2e4d4d75fb`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 39.0 MB (39018842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641c423bf503cd010ce1fbfe25b8d8eaeb9c9e8e5e65c07416e9f7f160c6ec9`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cee5e480a79b9ec36d923e36f54ea2b713c28429caf29557d911dd62e2c1cd0a
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
$ docker pull odoo@sha256:fdb9c80b25fbfbb17cb0dab5b0485255d4507dc7588f6140e085dad48a9455d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 MB (596490653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5276d013373a314b125b07f1aad699a596e6b1e5f362ad1f71806382c2dbed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef41a7c8da96cf1ca69f45d9d8608a0c017207cd6de5c78e5590a364ca22f1e6`  
		Last Modified: Mon, 26 Aug 2024 22:01:24 GMT  
		Size: 233.7 MB (233741816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f25f100dbe9926e38793dbbf4760d8a47a33340092f03ed349c58deb933354`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 2.3 MB (2315758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21167727e18c6961d051deaccc8cd31945573f0f1ffdbd3e7e818ba1523fedc`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 464.9 KB (464915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842917c142818ca7f84f34e562efde62052216a1cd62169355d75f86fe14d3d`  
		Last Modified: Mon, 26 Aug 2024 22:01:26 GMT  
		Size: 330.4 MB (330429698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f479f5215cdb2d96eb29ccc3d8547e087a4d2cc5b9e869a7833a037d42486`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955c3020d5a4d5c2f2077185d6decfbfd64da77a75209f66051d70d93f1f2720`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebb24645a95982bc5b16c699b126c2798561fe1d8d3984107b162e349d424c`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1eec4cf1e839a5d4912a8b128fdcf443a63200a13bff6258043f26d09625a21`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e2f0f75a15dfbe7e6c4e26fd748a23bcf1f639bd75c6041c30fc346affc9596d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39037420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838c7ceae05072c0baed5fe9e472147ddfd1d548583922fe4bcf96060ceba99`

```dockerfile
```

-	Layers:
	-	`sha256:d22e5162f342757044105780008e2b244992b1a9c28998548a401731ca0c6dc1`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 39.0 MB (39010545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45bea61895ff81bc769db787df5eb63474a19eaae80a3587cfb7b920e80d49e5`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f5a7f8ff52d2b49f4ca2969456956d44167fd788e2f0cab15bb680d6e58c6001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591301670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0a04db5e01098ceb5c75aa0bd78d2d2455150a3ff23fd13176de87006d190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:ade1ad6eac09a3316704de654e0fb59bbf9004e922771273b24dd3cf9bda9a45`  
		Last Modified: Mon, 26 Aug 2024 22:02:22 GMT  
		Size: 330.1 MB (330051165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4565a373012ffb0da2e909f9fdf1057e43910873f7a9dc8347b442238c1a6`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a02cd321ac917958a3768c49ccd311a86434f8cb3ab55f15bb503d3b6c032`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b20cbfb10e95b480b1c9970fa2c18e6a8577abbb580f224f7b3e378f29cf4`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5853ae3a5df299bd78aabba7894c091cfa682904c45d3a832febb527b012ef`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:528d45180c41772ae20e180552ac313a7f41ded6a3f7075b17032359b445d917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39044230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cbd68e39ddf86432be80716f5bea81a3c62c6fd366d3aed5d29746dcf95e7c`

```dockerfile
```

-	Layers:
	-	`sha256:f367f778917a023765a4a0c21a1ebff98ea6ede9b9929f02f8fc5cc2a99c6463`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 39.0 MB (39017054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cb34dc5bf85b178160a54c46efd3bb284155ba107699577bea7fc7f99f5961`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f129aed39ff771d108dad2492d3de4540c9ec2ed93a25414de2c50971ea52ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 MB (612959287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8361ec71ce199f078733d85efa85d1e8f482fdcb304035b196da23e5384f67f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:6cf80db5dba06a2486e607dec5802889dfe61f4d665b697389c813d17813e2a6`  
		Last Modified: Mon, 26 Aug 2024 22:05:26 GMT  
		Size: 332.2 MB (332159061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7e9328690ec814e87896a4f74c74ec767736aa76dcfb086f23298e8e15f71`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b8423da35bf77bbd97056cb2025d6c7e82037c4835d0dbc9c836d8e7df850`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a31ea83f0d1009c6609076b4aa53c3ceeb7174886da10e31d663fffe2a38f1`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77112b68c3f58d87bcaaf1f473fea4afd961a5b067719ce58582cbf5b2de5b9d`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d1f45886f871d582df7fefb4ea36cd29c1c7eccc6361dc4d5b6bdecd74c029ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39045772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b6e910eae0fb39ffe2d70f66cc4850fcdc21886716e3ff5ae0233c40bbca93`

```dockerfile
```

-	Layers:
	-	`sha256:74de53e8c3f574c41f6dfd212bd66c48f0c0cdc87dbbb7481b24bc2e4d4d75fb`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 39.0 MB (39018842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641c423bf503cd010ce1fbfe25b8d8eaeb9c9e8e5e65c07416e9f7f160c6ec9`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240826`

```console
$ docker pull odoo@sha256:cee5e480a79b9ec36d923e36f54ea2b713c28429caf29557d911dd62e2c1cd0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240826` - linux; amd64

```console
$ docker pull odoo@sha256:fdb9c80b25fbfbb17cb0dab5b0485255d4507dc7588f6140e085dad48a9455d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 MB (596490653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5276d013373a314b125b07f1aad699a596e6b1e5f362ad1f71806382c2dbed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef41a7c8da96cf1ca69f45d9d8608a0c017207cd6de5c78e5590a364ca22f1e6`  
		Last Modified: Mon, 26 Aug 2024 22:01:24 GMT  
		Size: 233.7 MB (233741816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f25f100dbe9926e38793dbbf4760d8a47a33340092f03ed349c58deb933354`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 2.3 MB (2315758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21167727e18c6961d051deaccc8cd31945573f0f1ffdbd3e7e818ba1523fedc`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 464.9 KB (464915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842917c142818ca7f84f34e562efde62052216a1cd62169355d75f86fe14d3d`  
		Last Modified: Mon, 26 Aug 2024 22:01:26 GMT  
		Size: 330.4 MB (330429698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f479f5215cdb2d96eb29ccc3d8547e087a4d2cc5b9e869a7833a037d42486`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955c3020d5a4d5c2f2077185d6decfbfd64da77a75209f66051d70d93f1f2720`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebb24645a95982bc5b16c699b126c2798561fe1d8d3984107b162e349d424c`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1eec4cf1e839a5d4912a8b128fdcf443a63200a13bff6258043f26d09625a21`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:e2f0f75a15dfbe7e6c4e26fd748a23bcf1f639bd75c6041c30fc346affc9596d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39037420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838c7ceae05072c0baed5fe9e472147ddfd1d548583922fe4bcf96060ceba99`

```dockerfile
```

-	Layers:
	-	`sha256:d22e5162f342757044105780008e2b244992b1a9c28998548a401731ca0c6dc1`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 39.0 MB (39010545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45bea61895ff81bc769db787df5eb63474a19eaae80a3587cfb7b920e80d49e5`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240826` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f5a7f8ff52d2b49f4ca2969456956d44167fd788e2f0cab15bb680d6e58c6001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591301670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0a04db5e01098ceb5c75aa0bd78d2d2455150a3ff23fd13176de87006d190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:ade1ad6eac09a3316704de654e0fb59bbf9004e922771273b24dd3cf9bda9a45`  
		Last Modified: Mon, 26 Aug 2024 22:02:22 GMT  
		Size: 330.1 MB (330051165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4565a373012ffb0da2e909f9fdf1057e43910873f7a9dc8347b442238c1a6`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a02cd321ac917958a3768c49ccd311a86434f8cb3ab55f15bb503d3b6c032`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b20cbfb10e95b480b1c9970fa2c18e6a8577abbb580f224f7b3e378f29cf4`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5853ae3a5df299bd78aabba7894c091cfa682904c45d3a832febb527b012ef`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:528d45180c41772ae20e180552ac313a7f41ded6a3f7075b17032359b445d917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39044230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cbd68e39ddf86432be80716f5bea81a3c62c6fd366d3aed5d29746dcf95e7c`

```dockerfile
```

-	Layers:
	-	`sha256:f367f778917a023765a4a0c21a1ebff98ea6ede9b9929f02f8fc5cc2a99c6463`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 39.0 MB (39017054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cb34dc5bf85b178160a54c46efd3bb284155ba107699577bea7fc7f99f5961`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240826` - linux; ppc64le

```console
$ docker pull odoo@sha256:f129aed39ff771d108dad2492d3de4540c9ec2ed93a25414de2c50971ea52ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 MB (612959287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8361ec71ce199f078733d85efa85d1e8f482fdcb304035b196da23e5384f67f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:6cf80db5dba06a2486e607dec5802889dfe61f4d665b697389c813d17813e2a6`  
		Last Modified: Mon, 26 Aug 2024 22:05:26 GMT  
		Size: 332.2 MB (332159061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7e9328690ec814e87896a4f74c74ec767736aa76dcfb086f23298e8e15f71`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b8423da35bf77bbd97056cb2025d6c7e82037c4835d0dbc9c836d8e7df850`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a31ea83f0d1009c6609076b4aa53c3ceeb7174886da10e31d663fffe2a38f1`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77112b68c3f58d87bcaaf1f473fea4afd961a5b067719ce58582cbf5b2de5b9d`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240826` - unknown; unknown

```console
$ docker pull odoo@sha256:d1f45886f871d582df7fefb4ea36cd29c1c7eccc6361dc4d5b6bdecd74c029ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39045772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b6e910eae0fb39ffe2d70f66cc4850fcdc21886716e3ff5ae0233c40bbca93`

```dockerfile
```

-	Layers:
	-	`sha256:74de53e8c3f574c41f6dfd212bd66c48f0c0cdc87dbbb7481b24bc2e4d4d75fb`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 39.0 MB (39018842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641c423bf503cd010ce1fbfe25b8d8eaeb9c9e8e5e65c07416e9f7f160c6ec9`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:cee5e480a79b9ec36d923e36f54ea2b713c28429caf29557d911dd62e2c1cd0a
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
$ docker pull odoo@sha256:fdb9c80b25fbfbb17cb0dab5b0485255d4507dc7588f6140e085dad48a9455d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 MB (596490653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5276d013373a314b125b07f1aad699a596e6b1e5f362ad1f71806382c2dbed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=amd64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef41a7c8da96cf1ca69f45d9d8608a0c017207cd6de5c78e5590a364ca22f1e6`  
		Last Modified: Mon, 26 Aug 2024 22:01:24 GMT  
		Size: 233.7 MB (233741816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f25f100dbe9926e38793dbbf4760d8a47a33340092f03ed349c58deb933354`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 2.3 MB (2315758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21167727e18c6961d051deaccc8cd31945573f0f1ffdbd3e7e818ba1523fedc`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 464.9 KB (464915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842917c142818ca7f84f34e562efde62052216a1cd62169355d75f86fe14d3d`  
		Last Modified: Mon, 26 Aug 2024 22:01:26 GMT  
		Size: 330.4 MB (330429698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f479f5215cdb2d96eb29ccc3d8547e087a4d2cc5b9e869a7833a037d42486`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955c3020d5a4d5c2f2077185d6decfbfd64da77a75209f66051d70d93f1f2720`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ebb24645a95982bc5b16c699b126c2798561fe1d8d3984107b162e349d424c`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1eec4cf1e839a5d4912a8b128fdcf443a63200a13bff6258043f26d09625a21`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e2f0f75a15dfbe7e6c4e26fd748a23bcf1f639bd75c6041c30fc346affc9596d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39037420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b838c7ceae05072c0baed5fe9e472147ddfd1d548583922fe4bcf96060ceba99`

```dockerfile
```

-	Layers:
	-	`sha256:d22e5162f342757044105780008e2b244992b1a9c28998548a401731ca0c6dc1`  
		Last Modified: Mon, 26 Aug 2024 22:01:22 GMT  
		Size: 39.0 MB (39010545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45bea61895ff81bc769db787df5eb63474a19eaae80a3587cfb7b920e80d49e5`  
		Last Modified: Mon, 26 Aug 2024 22:01:21 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f5a7f8ff52d2b49f4ca2969456956d44167fd788e2f0cab15bb680d6e58c6001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591301670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0a04db5e01098ceb5c75aa0bd78d2d2455150a3ff23fd13176de87006d190`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=arm64
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:ade1ad6eac09a3316704de654e0fb59bbf9004e922771273b24dd3cf9bda9a45`  
		Last Modified: Mon, 26 Aug 2024 22:02:22 GMT  
		Size: 330.1 MB (330051165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4565a373012ffb0da2e909f9fdf1057e43910873f7a9dc8347b442238c1a6`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a02cd321ac917958a3768c49ccd311a86434f8cb3ab55f15bb503d3b6c032`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b20cbfb10e95b480b1c9970fa2c18e6a8577abbb580f224f7b3e378f29cf4`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5853ae3a5df299bd78aabba7894c091cfa682904c45d3a832febb527b012ef`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:528d45180c41772ae20e180552ac313a7f41ded6a3f7075b17032359b445d917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39044230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cbd68e39ddf86432be80716f5bea81a3c62c6fd366d3aed5d29746dcf95e7c`

```dockerfile
```

-	Layers:
	-	`sha256:f367f778917a023765a4a0c21a1ebff98ea6ede9b9929f02f8fc5cc2a99c6463`  
		Last Modified: Mon, 26 Aug 2024 22:02:15 GMT  
		Size: 39.0 MB (39017054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21cb34dc5bf85b178160a54c46efd3bb284155ba107699577bea7fc7f99f5961`  
		Last Modified: Mon, 26 Aug 2024 22:02:14 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:f129aed39ff771d108dad2492d3de4540c9ec2ed93a25414de2c50971ea52ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 MB (612959287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8361ec71ce199f078733d85efa85d1e8f482fdcb304035b196da23e5384f67f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Aug 2024 08:31:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 26 Aug 2024 08:31:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 26 Aug 2024 08:31:43 GMT
ARG TARGETARCH=ppc64le
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_VERSION=17.0
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_RELEASE=20240826
# Mon, 26 Aug 2024 08:31:43 GMT
ARG ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240826 ODOO_SHA=7f40f642e89d8ecd43d748c23dc4251fcdca84ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 26 Aug 2024 08:31:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 26 Aug 2024 08:31:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 26 Aug 2024 08:31:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 26 Aug 2024 08:31:43 GMT
USER odoo
# Mon, 26 Aug 2024 08:31:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Aug 2024 08:31:43 GMT
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
	-	`sha256:6cf80db5dba06a2486e607dec5802889dfe61f4d665b697389c813d17813e2a6`  
		Last Modified: Mon, 26 Aug 2024 22:05:26 GMT  
		Size: 332.2 MB (332159061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7e9328690ec814e87896a4f74c74ec767736aa76dcfb086f23298e8e15f71`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b8423da35bf77bbd97056cb2025d6c7e82037c4835d0dbc9c836d8e7df850`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a31ea83f0d1009c6609076b4aa53c3ceeb7174886da10e31d663fffe2a38f1`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77112b68c3f58d87bcaaf1f473fea4afd961a5b067719ce58582cbf5b2de5b9d`  
		Last Modified: Mon, 26 Aug 2024 22:05:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d1f45886f871d582df7fefb4ea36cd29c1c7eccc6361dc4d5b6bdecd74c029ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39045772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b6e910eae0fb39ffe2d70f66cc4850fcdc21886716e3ff5ae0233c40bbca93`

```dockerfile
```

-	Layers:
	-	`sha256:74de53e8c3f574c41f6dfd212bd66c48f0c0cdc87dbbb7481b24bc2e4d4d75fb`  
		Last Modified: Mon, 26 Aug 2024 22:05:09 GMT  
		Size: 39.0 MB (39018842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641c423bf503cd010ce1fbfe25b8d8eaeb9c9e8e5e65c07416e9f7f160c6ec9`  
		Last Modified: Mon, 26 Aug 2024 22:05:07 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json
