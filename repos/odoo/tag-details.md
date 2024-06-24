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
$ docker pull odoo@sha256:568514348ed4a9471fed4d910d9b70c9e94c159eaaa8f83dec904ec9a236acc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:617220b168338c049374025d743a0ac9a37a2f34b52cc45ef4a17426bad82eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563851956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6041af0a1566e50e4fea94eb5021ab7c87b7cc9d6cae90a40025133ec8564d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7d93a72b0dca56e34e1c4658d7ef80a0e126ce39c5f24aac857d746066bae6`  
		Last Modified: Mon, 24 Jun 2024 17:59:42 GMT  
		Size: 220.3 MB (220282279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cee524cb24efb611d715405a2654a4d09df4984c8c11ff6239391c00ba8086`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 2.4 MB (2387147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58612ebc2a91d141146742bf4259dccee28ba94f5c124e0b79f39ffff9728471`  
		Last Modified: Mon, 24 Jun 2024 17:59:37 GMT  
		Size: 457.8 KB (457812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40d237fa905b2805c5847c13ea514003e3b33869af3c582f61217c115d22561`  
		Last Modified: Mon, 24 Jun 2024 17:59:41 GMT  
		Size: 309.3 MB (309288240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f302d9d332debd6d47857ce47317faa66ecab9eb3c48ed01521974d44548b87`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78c3c5297e112e8b1c9a8a1c54cf3681cd405e0ca31b17fc1f908ca83af0d1`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16b677e54e5bdde3941ba8fadda04aeac82b23b4c82d4ac0280974e66f20cc`  
		Last Modified: Mon, 24 Jun 2024 17:59:41 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a591e813c2484e40dfe2aa2bbc0c378b129c7b22aa1f4408f39aa20b1ac5a`  
		Last Modified: Mon, 24 Jun 2024 17:59:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:f85bc3a5abaae6468298dfd9f90a274314398a3706e0ea10a37db791653d9d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34536001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485d44b9e383d3a5350c792244af9a9657807009a9e97a7bb4b15a8522fe93bf`

```dockerfile
```

-	Layers:
	-	`sha256:96c3426fff38b266b085e818a03f8406f6a2d4f78eedef3b7ee35065bb7c5cc2`  
		Last Modified: Mon, 24 Jun 2024 17:59:37 GMT  
		Size: 34.5 MB (34511370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eef7821ca1e5aa76d9cc32b1122067828183651ea7b330092e1c1a42a6a3855`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:568514348ed4a9471fed4d910d9b70c9e94c159eaaa8f83dec904ec9a236acc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:617220b168338c049374025d743a0ac9a37a2f34b52cc45ef4a17426bad82eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563851956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6041af0a1566e50e4fea94eb5021ab7c87b7cc9d6cae90a40025133ec8564d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7d93a72b0dca56e34e1c4658d7ef80a0e126ce39c5f24aac857d746066bae6`  
		Last Modified: Mon, 24 Jun 2024 17:59:42 GMT  
		Size: 220.3 MB (220282279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cee524cb24efb611d715405a2654a4d09df4984c8c11ff6239391c00ba8086`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 2.4 MB (2387147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58612ebc2a91d141146742bf4259dccee28ba94f5c124e0b79f39ffff9728471`  
		Last Modified: Mon, 24 Jun 2024 17:59:37 GMT  
		Size: 457.8 KB (457812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40d237fa905b2805c5847c13ea514003e3b33869af3c582f61217c115d22561`  
		Last Modified: Mon, 24 Jun 2024 17:59:41 GMT  
		Size: 309.3 MB (309288240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f302d9d332debd6d47857ce47317faa66ecab9eb3c48ed01521974d44548b87`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78c3c5297e112e8b1c9a8a1c54cf3681cd405e0ca31b17fc1f908ca83af0d1`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16b677e54e5bdde3941ba8fadda04aeac82b23b4c82d4ac0280974e66f20cc`  
		Last Modified: Mon, 24 Jun 2024 17:59:41 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a591e813c2484e40dfe2aa2bbc0c378b129c7b22aa1f4408f39aa20b1ac5a`  
		Last Modified: Mon, 24 Jun 2024 17:59:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f85bc3a5abaae6468298dfd9f90a274314398a3706e0ea10a37db791653d9d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34536001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485d44b9e383d3a5350c792244af9a9657807009a9e97a7bb4b15a8522fe93bf`

```dockerfile
```

-	Layers:
	-	`sha256:96c3426fff38b266b085e818a03f8406f6a2d4f78eedef3b7ee35065bb7c5cc2`  
		Last Modified: Mon, 24 Jun 2024 17:59:37 GMT  
		Size: 34.5 MB (34511370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eef7821ca1e5aa76d9cc32b1122067828183651ea7b330092e1c1a42a6a3855`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240624`

```console
$ docker pull odoo@sha256:568514348ed4a9471fed4d910d9b70c9e94c159eaaa8f83dec904ec9a236acc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240624` - linux; amd64

```console
$ docker pull odoo@sha256:617220b168338c049374025d743a0ac9a37a2f34b52cc45ef4a17426bad82eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563851956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6041af0a1566e50e4fea94eb5021ab7c87b7cc9d6cae90a40025133ec8564d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7d93a72b0dca56e34e1c4658d7ef80a0e126ce39c5f24aac857d746066bae6`  
		Last Modified: Mon, 24 Jun 2024 17:59:42 GMT  
		Size: 220.3 MB (220282279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cee524cb24efb611d715405a2654a4d09df4984c8c11ff6239391c00ba8086`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 2.4 MB (2387147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58612ebc2a91d141146742bf4259dccee28ba94f5c124e0b79f39ffff9728471`  
		Last Modified: Mon, 24 Jun 2024 17:59:37 GMT  
		Size: 457.8 KB (457812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40d237fa905b2805c5847c13ea514003e3b33869af3c582f61217c115d22561`  
		Last Modified: Mon, 24 Jun 2024 17:59:41 GMT  
		Size: 309.3 MB (309288240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f302d9d332debd6d47857ce47317faa66ecab9eb3c48ed01521974d44548b87`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b78c3c5297e112e8b1c9a8a1c54cf3681cd405e0ca31b17fc1f908ca83af0d1`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16b677e54e5bdde3941ba8fadda04aeac82b23b4c82d4ac0280974e66f20cc`  
		Last Modified: Mon, 24 Jun 2024 17:59:41 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a591e813c2484e40dfe2aa2bbc0c378b129c7b22aa1f4408f39aa20b1ac5a`  
		Last Modified: Mon, 24 Jun 2024 17:59:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:f85bc3a5abaae6468298dfd9f90a274314398a3706e0ea10a37db791653d9d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34536001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485d44b9e383d3a5350c792244af9a9657807009a9e97a7bb4b15a8522fe93bf`

```dockerfile
```

-	Layers:
	-	`sha256:96c3426fff38b266b085e818a03f8406f6a2d4f78eedef3b7ee35065bb7c5cc2`  
		Last Modified: Mon, 24 Jun 2024 17:59:37 GMT  
		Size: 34.5 MB (34511370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eef7821ca1e5aa76d9cc32b1122067828183651ea7b330092e1c1a42a6a3855`  
		Last Modified: Mon, 24 Jun 2024 17:59:40 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:226e828ca838ed295f130868901a913cc952905e9ad8960ff87cd05816c3dcc5
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
$ docker pull odoo@sha256:2978691640893beb8fb08718c88e2135f108bee11bc0098f1d785d6991bcb494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583164774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f952d9f4f6f387077991e74cd26cbc4bfd8633ecf18c54af1f4ee8d0c26d819`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca111003b81a14f8638080fde693cbf2942140b0c26e8eceb8bd9b99da8b4df`  
		Last Modified: Mon, 24 Jun 2024 17:59:58 GMT  
		Size: 219.6 MB (219594965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8359b34f09f5f886f9ba54d8c94769acc050612a2aed92df261f04c3c1cf395`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
		Size: 2.4 MB (2391092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570c64e3e76537ad5ce852b7af1ccf5b18a613858556de8d7e15aaf868e26f8a`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
		Size: 457.8 KB (457812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f3fcf6050a63fd865d9b0f0ecc14db9320bf846426ba4c0f9d1477cc420128`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 329.3 MB (329284428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daf5d6436868190a8d1736416a98e6ef9105485f462ec9c7c2550a0422d29ae`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c01a80adfb7645290e810e3f4a97a2bc65086284787ec70b67209b3ddaa80`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8a85034c65d73bee24cefaf9c05954fd8227f6523fe2740ec7df3d5885be0`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90e6c57f8cd3f2e7544a37458457ee2178e1771d91c683c79035f3a2292288`  
		Last Modified: Mon, 24 Jun 2024 17:59:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:46fab09c534c07593bcb4a84726bab3d5b490a7674d2015d7b29678794918e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38575238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4526b2115690d5353d7442967c9f9578e24d6dc06ce135d75e782c9d40d20a17`

```dockerfile
```

-	Layers:
	-	`sha256:f410ea22491a952a928238b9ebfbc99c6f3ac079901c2a577d1e7593f3994371`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 38.5 MB (38548696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65651c69ca5029ff328ad396f3553cc3ce66bd4f632c1bc636301a1035a8529f`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
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
$ docker pull odoo@sha256:226e828ca838ed295f130868901a913cc952905e9ad8960ff87cd05816c3dcc5
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
$ docker pull odoo@sha256:2978691640893beb8fb08718c88e2135f108bee11bc0098f1d785d6991bcb494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583164774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f952d9f4f6f387077991e74cd26cbc4bfd8633ecf18c54af1f4ee8d0c26d819`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca111003b81a14f8638080fde693cbf2942140b0c26e8eceb8bd9b99da8b4df`  
		Last Modified: Mon, 24 Jun 2024 17:59:58 GMT  
		Size: 219.6 MB (219594965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8359b34f09f5f886f9ba54d8c94769acc050612a2aed92df261f04c3c1cf395`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
		Size: 2.4 MB (2391092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570c64e3e76537ad5ce852b7af1ccf5b18a613858556de8d7e15aaf868e26f8a`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
		Size: 457.8 KB (457812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f3fcf6050a63fd865d9b0f0ecc14db9320bf846426ba4c0f9d1477cc420128`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 329.3 MB (329284428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daf5d6436868190a8d1736416a98e6ef9105485f462ec9c7c2550a0422d29ae`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c01a80adfb7645290e810e3f4a97a2bc65086284787ec70b67209b3ddaa80`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8a85034c65d73bee24cefaf9c05954fd8227f6523fe2740ec7df3d5885be0`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90e6c57f8cd3f2e7544a37458457ee2178e1771d91c683c79035f3a2292288`  
		Last Modified: Mon, 24 Jun 2024 17:59:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:46fab09c534c07593bcb4a84726bab3d5b490a7674d2015d7b29678794918e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38575238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4526b2115690d5353d7442967c9f9578e24d6dc06ce135d75e782c9d40d20a17`

```dockerfile
```

-	Layers:
	-	`sha256:f410ea22491a952a928238b9ebfbc99c6f3ac079901c2a577d1e7593f3994371`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 38.5 MB (38548696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65651c69ca5029ff328ad396f3553cc3ce66bd4f632c1bc636301a1035a8529f`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
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
$ docker pull odoo@sha256:226e828ca838ed295f130868901a913cc952905e9ad8960ff87cd05816c3dcc5
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
$ docker pull odoo@sha256:2978691640893beb8fb08718c88e2135f108bee11bc0098f1d785d6991bcb494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583164774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f952d9f4f6f387077991e74cd26cbc4bfd8633ecf18c54af1f4ee8d0c26d819`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca111003b81a14f8638080fde693cbf2942140b0c26e8eceb8bd9b99da8b4df`  
		Last Modified: Mon, 24 Jun 2024 17:59:58 GMT  
		Size: 219.6 MB (219594965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8359b34f09f5f886f9ba54d8c94769acc050612a2aed92df261f04c3c1cf395`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
		Size: 2.4 MB (2391092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570c64e3e76537ad5ce852b7af1ccf5b18a613858556de8d7e15aaf868e26f8a`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
		Size: 457.8 KB (457812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f3fcf6050a63fd865d9b0f0ecc14db9320bf846426ba4c0f9d1477cc420128`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 329.3 MB (329284428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daf5d6436868190a8d1736416a98e6ef9105485f462ec9c7c2550a0422d29ae`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c01a80adfb7645290e810e3f4a97a2bc65086284787ec70b67209b3ddaa80`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8a85034c65d73bee24cefaf9c05954fd8227f6523fe2740ec7df3d5885be0`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90e6c57f8cd3f2e7544a37458457ee2178e1771d91c683c79035f3a2292288`  
		Last Modified: Mon, 24 Jun 2024 17:59:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:46fab09c534c07593bcb4a84726bab3d5b490a7674d2015d7b29678794918e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38575238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4526b2115690d5353d7442967c9f9578e24d6dc06ce135d75e782c9d40d20a17`

```dockerfile
```

-	Layers:
	-	`sha256:f410ea22491a952a928238b9ebfbc99c6f3ac079901c2a577d1e7593f3994371`  
		Last Modified: Mon, 24 Jun 2024 17:59:56 GMT  
		Size: 38.5 MB (38548696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65651c69ca5029ff328ad396f3553cc3ce66bd4f632c1bc636301a1035a8529f`  
		Last Modified: Mon, 24 Jun 2024 17:59:55 GMT  
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
$ docker pull odoo@sha256:09b5fed18b4f18114ad9c3798be91304f2814beb100108f170ea52b6b42eac25
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
$ docker pull odoo@sha256:6076943b4df4c2ac9834be8802017dd6846800b3361d4a83fef2d6d576c4e246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594668376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235da3d214253f268d5dc060455876137fee03194e9cdc27337e0bcee8f08d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6986bc3becddfc473be83c85c429103850fd3cba75bc2a499949d35f5ce593d6`  
		Last Modified: Mon, 24 Jun 2024 18:00:03 GMT  
		Size: 233.7 MB (233721931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676630dd64d4a6c4bbe4f0da78507190a347c0f0b4dba11e875b09ad30cb8aa7`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 2.3 MB (2313373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13b49bee19e66aa70384be57424bdf6413de6e608a61b57ecb70024ce88edd`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 458.9 KB (458890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d6e69119bd688817df11a4da2d48a27813cf3bf74ef476293ed879c2dacb81`  
		Last Modified: Mon, 24 Jun 2024 18:00:05 GMT  
		Size: 328.6 MB (328637985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef691d236cdcee8e6e433ab6658ba81ab9be3e7bc5796a85d74aa79a522ecc`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babfb09e2dd84717655832dab1be2614cb53a142a74722cda4becc13ae8b9072`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f27991687d2a51bb543335d6bf51cba7759c997c5a5ba6341d996d99bf4193c`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e083e9237aef8b500425d650dfff1a3094c0d39ef15a9e9ec16d2da577e48407`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:01ff9565fa7b0b696bea45c95a75c6c44e24751cc6fd6b8813af40ffc3797271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc26de38712e6052ca877141846cafb9ffde36d0dd31c38923512fb3ab6c333`

```dockerfile
```

-	Layers:
	-	`sha256:6cfdf7c4612e822b229cf1c15c3c16834d9626fb305de66347c33f079e6aa3d2`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eacf52bdeeeac36c1f6c9f8adfde4b3ceae6103d4e89eb50ec3ffd216d9b6c`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
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
$ docker pull odoo@sha256:09b5fed18b4f18114ad9c3798be91304f2814beb100108f170ea52b6b42eac25
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
$ docker pull odoo@sha256:6076943b4df4c2ac9834be8802017dd6846800b3361d4a83fef2d6d576c4e246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594668376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235da3d214253f268d5dc060455876137fee03194e9cdc27337e0bcee8f08d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6986bc3becddfc473be83c85c429103850fd3cba75bc2a499949d35f5ce593d6`  
		Last Modified: Mon, 24 Jun 2024 18:00:03 GMT  
		Size: 233.7 MB (233721931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676630dd64d4a6c4bbe4f0da78507190a347c0f0b4dba11e875b09ad30cb8aa7`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 2.3 MB (2313373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13b49bee19e66aa70384be57424bdf6413de6e608a61b57ecb70024ce88edd`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 458.9 KB (458890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d6e69119bd688817df11a4da2d48a27813cf3bf74ef476293ed879c2dacb81`  
		Last Modified: Mon, 24 Jun 2024 18:00:05 GMT  
		Size: 328.6 MB (328637985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef691d236cdcee8e6e433ab6658ba81ab9be3e7bc5796a85d74aa79a522ecc`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babfb09e2dd84717655832dab1be2614cb53a142a74722cda4becc13ae8b9072`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f27991687d2a51bb543335d6bf51cba7759c997c5a5ba6341d996d99bf4193c`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e083e9237aef8b500425d650dfff1a3094c0d39ef15a9e9ec16d2da577e48407`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:01ff9565fa7b0b696bea45c95a75c6c44e24751cc6fd6b8813af40ffc3797271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc26de38712e6052ca877141846cafb9ffde36d0dd31c38923512fb3ab6c333`

```dockerfile
```

-	Layers:
	-	`sha256:6cfdf7c4612e822b229cf1c15c3c16834d9626fb305de66347c33f079e6aa3d2`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eacf52bdeeeac36c1f6c9f8adfde4b3ceae6103d4e89eb50ec3ffd216d9b6c`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
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
$ docker pull odoo@sha256:09b5fed18b4f18114ad9c3798be91304f2814beb100108f170ea52b6b42eac25
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
$ docker pull odoo@sha256:6076943b4df4c2ac9834be8802017dd6846800b3361d4a83fef2d6d576c4e246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594668376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235da3d214253f268d5dc060455876137fee03194e9cdc27337e0bcee8f08d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6986bc3becddfc473be83c85c429103850fd3cba75bc2a499949d35f5ce593d6`  
		Last Modified: Mon, 24 Jun 2024 18:00:03 GMT  
		Size: 233.7 MB (233721931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676630dd64d4a6c4bbe4f0da78507190a347c0f0b4dba11e875b09ad30cb8aa7`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 2.3 MB (2313373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13b49bee19e66aa70384be57424bdf6413de6e608a61b57ecb70024ce88edd`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 458.9 KB (458890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d6e69119bd688817df11a4da2d48a27813cf3bf74ef476293ed879c2dacb81`  
		Last Modified: Mon, 24 Jun 2024 18:00:05 GMT  
		Size: 328.6 MB (328637985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef691d236cdcee8e6e433ab6658ba81ab9be3e7bc5796a85d74aa79a522ecc`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babfb09e2dd84717655832dab1be2614cb53a142a74722cda4becc13ae8b9072`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f27991687d2a51bb543335d6bf51cba7759c997c5a5ba6341d996d99bf4193c`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e083e9237aef8b500425d650dfff1a3094c0d39ef15a9e9ec16d2da577e48407`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240624` - unknown; unknown

```console
$ docker pull odoo@sha256:01ff9565fa7b0b696bea45c95a75c6c44e24751cc6fd6b8813af40ffc3797271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc26de38712e6052ca877141846cafb9ffde36d0dd31c38923512fb3ab6c333`

```dockerfile
```

-	Layers:
	-	`sha256:6cfdf7c4612e822b229cf1c15c3c16834d9626fb305de66347c33f079e6aa3d2`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eacf52bdeeeac36c1f6c9f8adfde4b3ceae6103d4e89eb50ec3ffd216d9b6c`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
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
$ docker pull odoo@sha256:09b5fed18b4f18114ad9c3798be91304f2814beb100108f170ea52b6b42eac25
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
$ docker pull odoo@sha256:6076943b4df4c2ac9834be8802017dd6846800b3361d4a83fef2d6d576c4e246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594668376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235da3d214253f268d5dc060455876137fee03194e9cdc27337e0bcee8f08d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6986bc3becddfc473be83c85c429103850fd3cba75bc2a499949d35f5ce593d6`  
		Last Modified: Mon, 24 Jun 2024 18:00:03 GMT  
		Size: 233.7 MB (233721931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676630dd64d4a6c4bbe4f0da78507190a347c0f0b4dba11e875b09ad30cb8aa7`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 2.3 MB (2313373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc13b49bee19e66aa70384be57424bdf6413de6e608a61b57ecb70024ce88edd`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
		Size: 458.9 KB (458890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d6e69119bd688817df11a4da2d48a27813cf3bf74ef476293ed879c2dacb81`  
		Last Modified: Mon, 24 Jun 2024 18:00:05 GMT  
		Size: 328.6 MB (328637985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ef691d236cdcee8e6e433ab6658ba81ab9be3e7bc5796a85d74aa79a522ecc`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babfb09e2dd84717655832dab1be2614cb53a142a74722cda4becc13ae8b9072`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f27991687d2a51bb543335d6bf51cba7759c997c5a5ba6341d996d99bf4193c`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e083e9237aef8b500425d650dfff1a3094c0d39ef15a9e9ec16d2da577e48407`  
		Last Modified: Mon, 24 Jun 2024 18:00:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:01ff9565fa7b0b696bea45c95a75c6c44e24751cc6fd6b8813af40ffc3797271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc26de38712e6052ca877141846cafb9ffde36d0dd31c38923512fb3ab6c333`

```dockerfile
```

-	Layers:
	-	`sha256:6cfdf7c4612e822b229cf1c15c3c16834d9626fb305de66347c33f079e6aa3d2`  
		Last Modified: Mon, 24 Jun 2024 18:00:00 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6eacf52bdeeeac36c1f6c9f8adfde4b3ceae6103d4e89eb50ec3ffd216d9b6c`  
		Last Modified: Mon, 24 Jun 2024 17:59:59 GMT  
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
