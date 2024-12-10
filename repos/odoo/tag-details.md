<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241209`](#odoo160-20241209)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241209`](#odoo170-20241209)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241209`](#odoo180-20241209)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:604041698afb0a697ef70e65501a01de657e7f71c42be67fdbe62e8728a1803b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:1f709325e0a13ea6cbd15808e1ae6b7a3bf50a101a6ef55bfa936facca26be54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.7 MB (583736205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660f77bfa474a3f5a9dae61573fe8719d8953b76566b2492fc38ca8011db783c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4475dad4faea782c26de2ba6dd469a13a57c58b6e996abff8373ed8eb4258c0`  
		Last Modified: Mon, 09 Dec 2024 19:30:46 GMT  
		Size: 219.6 MB (219628913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa160dfcece9be696fa950ee37a32966db8ecbd9c893213ebb5be5eaf24f30a7`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 2.6 MB (2575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf3d0d428ae9eeafa14bc8fa7f0dca76fc4dd60c1d62debdde457c40c0ec5d0`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 484.1 KB (484082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5755493006c8ebfdf5276f96c3044ad24db29d1bdf29fc3725c8ef7ad9b3f9f8`  
		Last Modified: Mon, 09 Dec 2024 19:30:48 GMT  
		Size: 330.8 MB (330792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf8e1fcaa51c3cef842a3695e5acd48c263050b400298ed169cccc2ef8a3f70`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15639f8607a07e6d981f3a67f07cb6285dcd5c8a4674c3fc08875ab053b9fe7`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe4fc416e6a93e6aa1def978d0ccf6beaa1d3cba7caada2bf557546d0a9e512`  
		Last Modified: Mon, 09 Dec 2024 19:30:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f608d06c60d0152e4b1b269ae27d098dc6c9c398cc5837b3e3295aa772256316`  
		Last Modified: Mon, 09 Dec 2024 19:30:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:dab53e5d6f02422a2d4577dda53795df571a51f6515e15eabbc36203967dd1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6cf71f68556f1111b9571151ab1380080161b09915153135108f3c242aa5e`

```dockerfile
```

-	Layers:
	-	`sha256:4da08cfb3aea14b8c92efd890ba1912f0c563c23e8b1b12a953cce6d97ab168a`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 38.9 MB (38873115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144695c5670c08ba5c17e5c6cd4838d1ca3f1e3c368c39dce9c01b023e50ba3d`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a54eb685f0d49b70f09c6306de006515f7380143f203a45f62ed448e1c63fc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579121484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e9b979b75eec7fcbc1df9ec274d93be93fc70599c4e05e9aa2af33e9312a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 25 Nov 2024 09:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867e2cf663da3bb6518512f039899bf488edba93373554da5dfc29e3635e070`  
		Last Modified: Tue, 03 Dec 2024 06:38:15 GMT  
		Size: 216.9 MB (216921221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7f5c8836bd40090ae1e0762c3ff13bbca719cc7eafba1e4d62f9a44421ac4`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 2.6 MB (2583699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c271b056c038408296c949bbbf1934c1b2eeba44d7d751cfc8845f6ce025eb`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 484.1 KB (484106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7a67e7778a95ae74ee527ec8c1007a2820bf0046e8aa8a2930161366058eb`  
		Last Modified: Tue, 03 Dec 2024 06:38:17 GMT  
		Size: 330.4 MB (330385104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ead34d4c7b688ac455961279904a24a80fdcb2ced1b8401b9c7a795914cec35`  
		Last Modified: Tue, 03 Dec 2024 06:38:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e144e8490c89a5bc17fb460d77a5bfa1a34f107a6387af009649575c0c1f0e`  
		Last Modified: Tue, 03 Dec 2024 06:38:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b674f17d6a219acbcee274929c400c53dee4f5eb238c64a779903a5e4b6268f`  
		Last Modified: Tue, 03 Dec 2024 06:38:12 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e379203abdf9e79155d72d813b6b3a48fc6a07187ea36fe2cff1a785f015843`  
		Last Modified: Tue, 03 Dec 2024 06:38:12 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:f0fd8d2db270bb0466ea6029d746f27ca6bf3de11415f9d9a58f3447337bfc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38897700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5c9bfba2b497ffa94d1e34b790d93adc9a233e8ad57bdd9c50024b8f2c5259`

```dockerfile
```

-	Layers:
	-	`sha256:4aa29550962a7487a29c8a8d364fd72772988ea7c4a85d0a47cda5a44696301b`  
		Last Modified: Tue, 03 Dec 2024 06:38:11 GMT  
		Size: 38.9 MB (38870830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c825563dc5dba9058e1ae3cf8e77db7f14e60802c05572cffa6436ee57539bf`  
		Last Modified: Tue, 03 Dec 2024 06:38:09 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:604041698afb0a697ef70e65501a01de657e7f71c42be67fdbe62e8728a1803b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:1f709325e0a13ea6cbd15808e1ae6b7a3bf50a101a6ef55bfa936facca26be54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.7 MB (583736205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660f77bfa474a3f5a9dae61573fe8719d8953b76566b2492fc38ca8011db783c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4475dad4faea782c26de2ba6dd469a13a57c58b6e996abff8373ed8eb4258c0`  
		Last Modified: Mon, 09 Dec 2024 19:30:46 GMT  
		Size: 219.6 MB (219628913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa160dfcece9be696fa950ee37a32966db8ecbd9c893213ebb5be5eaf24f30a7`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 2.6 MB (2575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf3d0d428ae9eeafa14bc8fa7f0dca76fc4dd60c1d62debdde457c40c0ec5d0`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 484.1 KB (484082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5755493006c8ebfdf5276f96c3044ad24db29d1bdf29fc3725c8ef7ad9b3f9f8`  
		Last Modified: Mon, 09 Dec 2024 19:30:48 GMT  
		Size: 330.8 MB (330792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf8e1fcaa51c3cef842a3695e5acd48c263050b400298ed169cccc2ef8a3f70`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15639f8607a07e6d981f3a67f07cb6285dcd5c8a4674c3fc08875ab053b9fe7`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe4fc416e6a93e6aa1def978d0ccf6beaa1d3cba7caada2bf557546d0a9e512`  
		Last Modified: Mon, 09 Dec 2024 19:30:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f608d06c60d0152e4b1b269ae27d098dc6c9c398cc5837b3e3295aa772256316`  
		Last Modified: Mon, 09 Dec 2024 19:30:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:dab53e5d6f02422a2d4577dda53795df571a51f6515e15eabbc36203967dd1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6cf71f68556f1111b9571151ab1380080161b09915153135108f3c242aa5e`

```dockerfile
```

-	Layers:
	-	`sha256:4da08cfb3aea14b8c92efd890ba1912f0c563c23e8b1b12a953cce6d97ab168a`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 38.9 MB (38873115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144695c5670c08ba5c17e5c6cd4838d1ca3f1e3c368c39dce9c01b023e50ba3d`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a54eb685f0d49b70f09c6306de006515f7380143f203a45f62ed448e1c63fc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579121484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e9b979b75eec7fcbc1df9ec274d93be93fc70599c4e05e9aa2af33e9312a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 25 Nov 2024 09:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867e2cf663da3bb6518512f039899bf488edba93373554da5dfc29e3635e070`  
		Last Modified: Tue, 03 Dec 2024 06:38:15 GMT  
		Size: 216.9 MB (216921221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd7f5c8836bd40090ae1e0762c3ff13bbca719cc7eafba1e4d62f9a44421ac4`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 2.6 MB (2583699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c271b056c038408296c949bbbf1934c1b2eeba44d7d751cfc8845f6ce025eb`  
		Last Modified: Tue, 03 Dec 2024 06:38:10 GMT  
		Size: 484.1 KB (484106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7a67e7778a95ae74ee527ec8c1007a2820bf0046e8aa8a2930161366058eb`  
		Last Modified: Tue, 03 Dec 2024 06:38:17 GMT  
		Size: 330.4 MB (330385104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ead34d4c7b688ac455961279904a24a80fdcb2ced1b8401b9c7a795914cec35`  
		Last Modified: Tue, 03 Dec 2024 06:38:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e144e8490c89a5bc17fb460d77a5bfa1a34f107a6387af009649575c0c1f0e`  
		Last Modified: Tue, 03 Dec 2024 06:38:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b674f17d6a219acbcee274929c400c53dee4f5eb238c64a779903a5e4b6268f`  
		Last Modified: Tue, 03 Dec 2024 06:38:12 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e379203abdf9e79155d72d813b6b3a48fc6a07187ea36fe2cff1a785f015843`  
		Last Modified: Tue, 03 Dec 2024 06:38:12 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f0fd8d2db270bb0466ea6029d746f27ca6bf3de11415f9d9a58f3447337bfc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38897700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5c9bfba2b497ffa94d1e34b790d93adc9a233e8ad57bdd9c50024b8f2c5259`

```dockerfile
```

-	Layers:
	-	`sha256:4aa29550962a7487a29c8a8d364fd72772988ea7c4a85d0a47cda5a44696301b`  
		Last Modified: Tue, 03 Dec 2024 06:38:11 GMT  
		Size: 38.9 MB (38870830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c825563dc5dba9058e1ae3cf8e77db7f14e60802c05572cffa6436ee57539bf`  
		Last Modified: Tue, 03 Dec 2024 06:38:09 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241209`

```console
$ docker pull odoo@sha256:18f8fdb50d11822400d4c6decdd863bfaec08d97c909dce7fe7b2dac7d94f911
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:16.0-20241209` - linux; amd64

```console
$ docker pull odoo@sha256:1f709325e0a13ea6cbd15808e1ae6b7a3bf50a101a6ef55bfa936facca26be54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.7 MB (583736205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660f77bfa474a3f5a9dae61573fe8719d8953b76566b2492fc38ca8011db783c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=cec2ddcce6dd38867b6983dbe68b2c43b030cd12
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4475dad4faea782c26de2ba6dd469a13a57c58b6e996abff8373ed8eb4258c0`  
		Last Modified: Mon, 09 Dec 2024 19:30:46 GMT  
		Size: 219.6 MB (219628913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa160dfcece9be696fa950ee37a32966db8ecbd9c893213ebb5be5eaf24f30a7`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 2.6 MB (2575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf3d0d428ae9eeafa14bc8fa7f0dca76fc4dd60c1d62debdde457c40c0ec5d0`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 484.1 KB (484082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5755493006c8ebfdf5276f96c3044ad24db29d1bdf29fc3725c8ef7ad9b3f9f8`  
		Last Modified: Mon, 09 Dec 2024 19:30:48 GMT  
		Size: 330.8 MB (330792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf8e1fcaa51c3cef842a3695e5acd48c263050b400298ed169cccc2ef8a3f70`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15639f8607a07e6d981f3a67f07cb6285dcd5c8a4674c3fc08875ab053b9fe7`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe4fc416e6a93e6aa1def978d0ccf6beaa1d3cba7caada2bf557546d0a9e512`  
		Last Modified: Mon, 09 Dec 2024 19:30:45 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f608d06c60d0152e4b1b269ae27d098dc6c9c398cc5837b3e3295aa772256316`  
		Last Modified: Mon, 09 Dec 2024 19:30:45 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241209` - unknown; unknown

```console
$ docker pull odoo@sha256:dab53e5d6f02422a2d4577dda53795df571a51f6515e15eabbc36203967dd1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c6cf71f68556f1111b9571151ab1380080161b09915153135108f3c242aa5e`

```dockerfile
```

-	Layers:
	-	`sha256:4da08cfb3aea14b8c92efd890ba1912f0c563c23e8b1b12a953cce6d97ab168a`  
		Last Modified: Mon, 09 Dec 2024 19:30:44 GMT  
		Size: 38.9 MB (38873115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144695c5670c08ba5c17e5c6cd4838d1ca3f1e3c368c39dce9c01b023e50ba3d`  
		Last Modified: Mon, 09 Dec 2024 19:30:43 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:7487e4c3c5f07b4c52e2c44d675f5c36ed5ab7fb0c727d51e6454343714c6e0d
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
$ docker pull odoo@sha256:71a9307934372513b88cd994ba939077f1f5e10a8ca543111d79abdf3725d588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599026936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf10df5a267709db53380cffdfd0a0074a5bb5e4d8d2d1beef31083571af97a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07942db2a387417e7c149672aa6ba8f4f79a43635f1543a1f169e309f548495b`  
		Last Modified: Mon, 09 Dec 2024 19:30:54 GMT  
		Size: 233.8 MB (233782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12107d5e8217b4f1cfde64910cca231f9a77ebbb9240580e6d0af4d114d7a0`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 2.5 MB (2493494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674369e88543ec3d46e38d23b5b73702345d2cb1fb68356439d9d1f8b29d1257`  
		Last Modified: Mon, 09 Dec 2024 19:30:50 GMT  
		Size: 485.2 KB (485178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81fef57b381d10f50e2145d8ee90e6796618423748fb375c4447f4b19934a7`  
		Last Modified: Mon, 09 Dec 2024 19:30:55 GMT  
		Size: 332.7 MB (332727935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321c465a117558ff2bc61fb311ab6a9acec16d639a253f10664c66836e6f69ab`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a98cc9a6ad9b041183e184d7d69dd796780c7619cbf0f3f66fd121e768a7e42`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3ccf0947770f0e144cc85219bfffa2bf308b6c7b79fa4fee641ffe6d3ecd80`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:9e523861326255ccc417622f85c5993b0ce2fb407860572ed3641013c7131ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39683081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04cb4cb54d5716994c8242d0643dae0727f2115ecf9728ef2a860465894bcd`

```dockerfile
```

-	Layers:
	-	`sha256:1025d566867570057aecbd5ddca39f1a90f3e63b8c4edcbc5add71ea64d240e0`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 39.7 MB (39656246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c426cac7489bc52b39adf65a22a44e4e61392f92d9e58a84f283e105c94990e`  
		Last Modified: Mon, 09 Dec 2024 19:30:50 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:95ea6e12801a53668907db6c49a289598823863e9cd05c9113d011f04dca404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593619343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b6319c208de1ea73a1d23f754d73429b2c99cc9aa3a62e27629f4c7e4b2aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20d1f022d1d141a9953bbfae96125324b3efd6b22622c3596a95aaf028d273`  
		Last Modified: Mon, 25 Nov 2024 20:35:43 GMT  
		Size: 332.1 MB (332149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423175ed130d608fd65bc155744764690738407ae8adf3504f935bdd48d5edd`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875700ae72cdd80764a751e96a89ea3e27697a8f78372b01832b0b2f1be8547`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6061e87ce90a3c02fa7bd484747c2200d711399136dbe216c61d5bca02015351`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6b1aa67f2a61af1f5be66a759f906845bf1f2772824d991c2f12749d19414`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a11b479a8ef73e4156a30f7f9a547bd748ff666262a30d6e13da948203f8eed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39649442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ac5363a6244f3d12b19fa7451203d64217c6d87e4aef92ab24d75d9e45fb5`

```dockerfile
```

-	Layers:
	-	`sha256:e8146aa7abed03d6fc5c588368d9d315861750d7db5834aba8642a9f0da9cfd3`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 39.6 MB (39622455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a38a08112d0b1b545a9a0a06ee2acb9371e75a248f4922d04589de1cd35a55e`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ea280dccc1f80308752f64135a3e4afe77f31652fcb348ee7f8e943a5b995ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 MB (615484511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3ad633f47121247ddfba986ca423408ae6b4e05ba7d7e1ebf4a71752935200`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6497668f768c587276c268c6f71e055cb24f2360455d344f69d4a8e75dc29bf`  
		Last Modified: Mon, 09 Dec 2024 19:45:49 GMT  
		Size: 334.5 MB (334467899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b12dffad1f7790d376788e0ec2d86add55a2e85c0036ff7f0d7a0796035fd`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdd61f27b5789a42d38a5518d8c488c47a2f3eee10399b5b1fe6dd123e788`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed81c73a790c12c2e5c7d3c17e489689f339d19887aa1fb873e7ecfdb50597`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f2a1198f20279fe5e2be8d64e351602d498240e28cb402b54a73234745643c`  
		Last Modified: Mon, 09 Dec 2024 19:45:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:56cedb53a56eaa16cab20d10e4067aac47b1a51e932d9cf5013411db88ce20c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39691464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d4e034d9666b0ed70244002b9dd2a8a9089a133e20911891805cd50c75fbe`

```dockerfile
```

-	Layers:
	-	`sha256:02a27a42d7bf15381c77ee8ddb27e6eef2b60bea219ba97166e116dff98b5bea`  
		Last Modified: Mon, 09 Dec 2024 19:45:30 GMT  
		Size: 39.7 MB (39664573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7294ecb42656ca2cd9a1242e9ad2579db14d3ed71a347a374efa39522448a3`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7487e4c3c5f07b4c52e2c44d675f5c36ed5ab7fb0c727d51e6454343714c6e0d
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
$ docker pull odoo@sha256:71a9307934372513b88cd994ba939077f1f5e10a8ca543111d79abdf3725d588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599026936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf10df5a267709db53380cffdfd0a0074a5bb5e4d8d2d1beef31083571af97a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07942db2a387417e7c149672aa6ba8f4f79a43635f1543a1f169e309f548495b`  
		Last Modified: Mon, 09 Dec 2024 19:30:54 GMT  
		Size: 233.8 MB (233782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12107d5e8217b4f1cfde64910cca231f9a77ebbb9240580e6d0af4d114d7a0`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 2.5 MB (2493494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674369e88543ec3d46e38d23b5b73702345d2cb1fb68356439d9d1f8b29d1257`  
		Last Modified: Mon, 09 Dec 2024 19:30:50 GMT  
		Size: 485.2 KB (485178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81fef57b381d10f50e2145d8ee90e6796618423748fb375c4447f4b19934a7`  
		Last Modified: Mon, 09 Dec 2024 19:30:55 GMT  
		Size: 332.7 MB (332727935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321c465a117558ff2bc61fb311ab6a9acec16d639a253f10664c66836e6f69ab`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a98cc9a6ad9b041183e184d7d69dd796780c7619cbf0f3f66fd121e768a7e42`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3ccf0947770f0e144cc85219bfffa2bf308b6c7b79fa4fee641ffe6d3ecd80`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9e523861326255ccc417622f85c5993b0ce2fb407860572ed3641013c7131ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39683081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04cb4cb54d5716994c8242d0643dae0727f2115ecf9728ef2a860465894bcd`

```dockerfile
```

-	Layers:
	-	`sha256:1025d566867570057aecbd5ddca39f1a90f3e63b8c4edcbc5add71ea64d240e0`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 39.7 MB (39656246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c426cac7489bc52b39adf65a22a44e4e61392f92d9e58a84f283e105c94990e`  
		Last Modified: Mon, 09 Dec 2024 19:30:50 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:95ea6e12801a53668907db6c49a289598823863e9cd05c9113d011f04dca404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593619343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b6319c208de1ea73a1d23f754d73429b2c99cc9aa3a62e27629f4c7e4b2aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20d1f022d1d141a9953bbfae96125324b3efd6b22622c3596a95aaf028d273`  
		Last Modified: Mon, 25 Nov 2024 20:35:43 GMT  
		Size: 332.1 MB (332149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423175ed130d608fd65bc155744764690738407ae8adf3504f935bdd48d5edd`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875700ae72cdd80764a751e96a89ea3e27697a8f78372b01832b0b2f1be8547`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6061e87ce90a3c02fa7bd484747c2200d711399136dbe216c61d5bca02015351`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6b1aa67f2a61af1f5be66a759f906845bf1f2772824d991c2f12749d19414`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a11b479a8ef73e4156a30f7f9a547bd748ff666262a30d6e13da948203f8eed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39649442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ac5363a6244f3d12b19fa7451203d64217c6d87e4aef92ab24d75d9e45fb5`

```dockerfile
```

-	Layers:
	-	`sha256:e8146aa7abed03d6fc5c588368d9d315861750d7db5834aba8642a9f0da9cfd3`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 39.6 MB (39622455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a38a08112d0b1b545a9a0a06ee2acb9371e75a248f4922d04589de1cd35a55e`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ea280dccc1f80308752f64135a3e4afe77f31652fcb348ee7f8e943a5b995ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 MB (615484511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3ad633f47121247ddfba986ca423408ae6b4e05ba7d7e1ebf4a71752935200`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6497668f768c587276c268c6f71e055cb24f2360455d344f69d4a8e75dc29bf`  
		Last Modified: Mon, 09 Dec 2024 19:45:49 GMT  
		Size: 334.5 MB (334467899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b12dffad1f7790d376788e0ec2d86add55a2e85c0036ff7f0d7a0796035fd`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdd61f27b5789a42d38a5518d8c488c47a2f3eee10399b5b1fe6dd123e788`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed81c73a790c12c2e5c7d3c17e489689f339d19887aa1fb873e7ecfdb50597`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f2a1198f20279fe5e2be8d64e351602d498240e28cb402b54a73234745643c`  
		Last Modified: Mon, 09 Dec 2024 19:45:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:56cedb53a56eaa16cab20d10e4067aac47b1a51e932d9cf5013411db88ce20c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39691464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d4e034d9666b0ed70244002b9dd2a8a9089a133e20911891805cd50c75fbe`

```dockerfile
```

-	Layers:
	-	`sha256:02a27a42d7bf15381c77ee8ddb27e6eef2b60bea219ba97166e116dff98b5bea`  
		Last Modified: Mon, 09 Dec 2024 19:45:30 GMT  
		Size: 39.7 MB (39664573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7294ecb42656ca2cd9a1242e9ad2579db14d3ed71a347a374efa39522448a3`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241209`

```console
$ docker pull odoo@sha256:5e5761b9d200ff6e172dbe4adcdf059989cfbafd62e935de27f547a58bfbc41a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241209` - linux; amd64

```console
$ docker pull odoo@sha256:71a9307934372513b88cd994ba939077f1f5e10a8ca543111d79abdf3725d588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599026936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf10df5a267709db53380cffdfd0a0074a5bb5e4d8d2d1beef31083571af97a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07942db2a387417e7c149672aa6ba8f4f79a43635f1543a1f169e309f548495b`  
		Last Modified: Mon, 09 Dec 2024 19:30:54 GMT  
		Size: 233.8 MB (233782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12107d5e8217b4f1cfde64910cca231f9a77ebbb9240580e6d0af4d114d7a0`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 2.5 MB (2493494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674369e88543ec3d46e38d23b5b73702345d2cb1fb68356439d9d1f8b29d1257`  
		Last Modified: Mon, 09 Dec 2024 19:30:50 GMT  
		Size: 485.2 KB (485178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c81fef57b381d10f50e2145d8ee90e6796618423748fb375c4447f4b19934a7`  
		Last Modified: Mon, 09 Dec 2024 19:30:55 GMT  
		Size: 332.7 MB (332727935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321c465a117558ff2bc61fb311ab6a9acec16d639a253f10664c66836e6f69ab`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a98cc9a6ad9b041183e184d7d69dd796780c7619cbf0f3f66fd121e768a7e42`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3ccf0947770f0e144cc85219bfffa2bf308b6c7b79fa4fee641ffe6d3ecd80`  
		Last Modified: Mon, 09 Dec 2024 19:30:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241209` - unknown; unknown

```console
$ docker pull odoo@sha256:9e523861326255ccc417622f85c5993b0ce2fb407860572ed3641013c7131ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39683081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f04cb4cb54d5716994c8242d0643dae0727f2115ecf9728ef2a860465894bcd`

```dockerfile
```

-	Layers:
	-	`sha256:1025d566867570057aecbd5ddca39f1a90f3e63b8c4edcbc5add71ea64d240e0`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 39.7 MB (39656246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c426cac7489bc52b39adf65a22a44e4e61392f92d9e58a84f283e105c94990e`  
		Last Modified: Mon, 09 Dec 2024 19:30:50 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241209` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ea280dccc1f80308752f64135a3e4afe77f31652fcb348ee7f8e943a5b995ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 MB (615484511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3ad633f47121247ddfba986ca423408ae6b4e05ba7d7e1ebf4a71752935200`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=001b05df41497bd08b49c9c44ad489026f4c4542
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6497668f768c587276c268c6f71e055cb24f2360455d344f69d4a8e75dc29bf`  
		Last Modified: Mon, 09 Dec 2024 19:45:49 GMT  
		Size: 334.5 MB (334467899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719b12dffad1f7790d376788e0ec2d86add55a2e85c0036ff7f0d7a0796035fd`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fdd61f27b5789a42d38a5518d8c488c47a2f3eee10399b5b1fe6dd123e788`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed81c73a790c12c2e5c7d3c17e489689f339d19887aa1fb873e7ecfdb50597`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f2a1198f20279fe5e2be8d64e351602d498240e28cb402b54a73234745643c`  
		Last Modified: Mon, 09 Dec 2024 19:45:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241209` - unknown; unknown

```console
$ docker pull odoo@sha256:56cedb53a56eaa16cab20d10e4067aac47b1a51e932d9cf5013411db88ce20c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39691464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438d4e034d9666b0ed70244002b9dd2a8a9089a133e20911891805cd50c75fbe`

```dockerfile
```

-	Layers:
	-	`sha256:02a27a42d7bf15381c77ee8ddb27e6eef2b60bea219ba97166e116dff98b5bea`  
		Last Modified: Mon, 09 Dec 2024 19:45:30 GMT  
		Size: 39.7 MB (39664573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7294ecb42656ca2cd9a1242e9ad2579db14d3ed71a347a374efa39522448a3`  
		Last Modified: Mon, 09 Dec 2024 19:45:24 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:f81284040205b46f4eecc227a676b2e7eef71dc44dfd175e7bdc916320317609
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:3f5fecc810fc79b1f9b078ed73c2918340bbf3c21cd0c54d3d72c2a5fd051a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662536537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a8a85eda81f6dc9706cb0ddfc174b97be2be558cee8f76870b943c3ebe37a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe691131d01ebc88838bfff5f1fa032b9fec54a8e5da19261f8fea25beedfc55`  
		Last Modified: Mon, 09 Dec 2024 19:31:34 GMT  
		Size: 254.5 MB (254515418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119cea40d91772dce45f029fd78520bb5ea523e9f8690806d0dc9c4a5fc7bdf`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 14.2 MB (14231220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f312beacc81dc375a27ee8e6dc42628f84a79d2772624e197387486bb5e2b`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 484.9 KB (484918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea872a1c4dd3c6c51fd86c90eff9b5c3b2d3550468b71da3168cf7001a4350e`  
		Last Modified: Mon, 09 Dec 2024 19:31:37 GMT  
		Size: 363.6 MB (363550571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b481993f58a9db0ab2033372a98f411c0c3cc993433ae39c25220c6bd4456bb`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024eeb1880ccd50051d70dbf92ab1e5cdf53b15bb8a5f290b2bf04c14e230c03`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fd115845b272207eabe1b0ccb257fd8575f97626c978d5537ce2ae9cfff1a`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:cedb7f20d39b119465015adebe46717e77943ba85f8e0b9db61b1697dd1b74b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57751057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7762922b3bb9b2a461627503199d90d0c736b0d8dcccce9d09f6cff23dc9f5f4`

```dockerfile
```

-	Layers:
	-	`sha256:e83d9cfe10362ee828c2128420fbde7d329d2fa88bac1e442271a76f9d757911`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 57.7 MB (57723921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270e6b5c554ec691df116e7dfa9f54fdef3006a81b3daad2f03a45ec2917bf20`  
		Last Modified: Mon, 09 Dec 2024 19:31:30 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e96156949e69f83b91000c0f314fd86b687e9ff34ba29be260f677ee23c19a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658217406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8929e7d9eba77c8558d829005f7e94ec49658f6f074b37f8e538212bb07810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ecc3c41deba94deef9ef13230d21616fb856dd13b8ec0c592f3063a955318`  
		Last Modified: Tue, 03 Dec 2024 06:34:32 GMT  
		Size: 251.9 MB (251940434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730fbb6c4e05b09f822891bb1f189de5a363ff7032d6a5a5efec25322b27e42`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 14.2 MB (14204438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc74bc45ed2dfba386983367267b64df94f08164c3f10d6b199347554437c7`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9d13204a9c897ddbfb1929c28f06ab830c8a8cd8d89454771ebdbe5caf325b`  
		Last Modified: Tue, 03 Dec 2024 06:34:33 GMT  
		Size: 362.7 MB (362692505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80478f154202c3a7cb40eeeffd6b21cba82460cd564533f06db827a974b93053`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039efacf5dca845f0e405783dd1fbd63b4b765f36ac15575f97c066007583d82`  
		Last Modified: Tue, 03 Dec 2024 06:34:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4683dc130afb32799e7770bdcd9f3f5e7f96cfe52e9b3d24a2a063dc4388d6`  
		Last Modified: Tue, 03 Dec 2024 06:34:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c2c74c0eb033c234a0a4020dbf765e6bfb43515d2b00bdcf9148a4698e3b34`  
		Last Modified: Tue, 03 Dec 2024 06:34:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b9551a7a3b66382b486c612307b4128523d3018cbf62188af7b11a8df6205f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9296bb6278447a4d0cd05898122acbb57dafe5f777e87ac0b73f6e15784066e8`

```dockerfile
```

-	Layers:
	-	`sha256:6ed0aebf6960bdca7478c998a29720ae936145d1346d59824f32508700acc15e`  
		Last Modified: Tue, 03 Dec 2024 06:34:27 GMT  
		Size: 57.3 MB (57260906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02242920cb27c914aaeb3598b47354139013a61d736741b7746ceb7cefa5c7f8`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:f81284040205b46f4eecc227a676b2e7eef71dc44dfd175e7bdc916320317609
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:3f5fecc810fc79b1f9b078ed73c2918340bbf3c21cd0c54d3d72c2a5fd051a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662536537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a8a85eda81f6dc9706cb0ddfc174b97be2be558cee8f76870b943c3ebe37a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe691131d01ebc88838bfff5f1fa032b9fec54a8e5da19261f8fea25beedfc55`  
		Last Modified: Mon, 09 Dec 2024 19:31:34 GMT  
		Size: 254.5 MB (254515418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119cea40d91772dce45f029fd78520bb5ea523e9f8690806d0dc9c4a5fc7bdf`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 14.2 MB (14231220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f312beacc81dc375a27ee8e6dc42628f84a79d2772624e197387486bb5e2b`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 484.9 KB (484918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea872a1c4dd3c6c51fd86c90eff9b5c3b2d3550468b71da3168cf7001a4350e`  
		Last Modified: Mon, 09 Dec 2024 19:31:37 GMT  
		Size: 363.6 MB (363550571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b481993f58a9db0ab2033372a98f411c0c3cc993433ae39c25220c6bd4456bb`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024eeb1880ccd50051d70dbf92ab1e5cdf53b15bb8a5f290b2bf04c14e230c03`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fd115845b272207eabe1b0ccb257fd8575f97626c978d5537ce2ae9cfff1a`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cedb7f20d39b119465015adebe46717e77943ba85f8e0b9db61b1697dd1b74b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57751057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7762922b3bb9b2a461627503199d90d0c736b0d8dcccce9d09f6cff23dc9f5f4`

```dockerfile
```

-	Layers:
	-	`sha256:e83d9cfe10362ee828c2128420fbde7d329d2fa88bac1e442271a76f9d757911`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 57.7 MB (57723921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270e6b5c554ec691df116e7dfa9f54fdef3006a81b3daad2f03a45ec2917bf20`  
		Last Modified: Mon, 09 Dec 2024 19:31:30 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e96156949e69f83b91000c0f314fd86b687e9ff34ba29be260f677ee23c19a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658217406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8929e7d9eba77c8558d829005f7e94ec49658f6f074b37f8e538212bb07810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ecc3c41deba94deef9ef13230d21616fb856dd13b8ec0c592f3063a955318`  
		Last Modified: Tue, 03 Dec 2024 06:34:32 GMT  
		Size: 251.9 MB (251940434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730fbb6c4e05b09f822891bb1f189de5a363ff7032d6a5a5efec25322b27e42`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 14.2 MB (14204438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc74bc45ed2dfba386983367267b64df94f08164c3f10d6b199347554437c7`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9d13204a9c897ddbfb1929c28f06ab830c8a8cd8d89454771ebdbe5caf325b`  
		Last Modified: Tue, 03 Dec 2024 06:34:33 GMT  
		Size: 362.7 MB (362692505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80478f154202c3a7cb40eeeffd6b21cba82460cd564533f06db827a974b93053`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039efacf5dca845f0e405783dd1fbd63b4b765f36ac15575f97c066007583d82`  
		Last Modified: Tue, 03 Dec 2024 06:34:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4683dc130afb32799e7770bdcd9f3f5e7f96cfe52e9b3d24a2a063dc4388d6`  
		Last Modified: Tue, 03 Dec 2024 06:34:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c2c74c0eb033c234a0a4020dbf765e6bfb43515d2b00bdcf9148a4698e3b34`  
		Last Modified: Tue, 03 Dec 2024 06:34:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b9551a7a3b66382b486c612307b4128523d3018cbf62188af7b11a8df6205f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9296bb6278447a4d0cd05898122acbb57dafe5f777e87ac0b73f6e15784066e8`

```dockerfile
```

-	Layers:
	-	`sha256:6ed0aebf6960bdca7478c998a29720ae936145d1346d59824f32508700acc15e`  
		Last Modified: Tue, 03 Dec 2024 06:34:27 GMT  
		Size: 57.3 MB (57260906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02242920cb27c914aaeb3598b47354139013a61d736741b7746ceb7cefa5c7f8`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241209`

```console
$ docker pull odoo@sha256:23d8f8124021ff466a3aca0ffa79c914c0dca89b57efefe04eb5f96b1c591c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241209` - linux; amd64

```console
$ docker pull odoo@sha256:3f5fecc810fc79b1f9b078ed73c2918340bbf3c21cd0c54d3d72c2a5fd051a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662536537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a8a85eda81f6dc9706cb0ddfc174b97be2be558cee8f76870b943c3ebe37a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe691131d01ebc88838bfff5f1fa032b9fec54a8e5da19261f8fea25beedfc55`  
		Last Modified: Mon, 09 Dec 2024 19:31:34 GMT  
		Size: 254.5 MB (254515418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119cea40d91772dce45f029fd78520bb5ea523e9f8690806d0dc9c4a5fc7bdf`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 14.2 MB (14231220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f312beacc81dc375a27ee8e6dc42628f84a79d2772624e197387486bb5e2b`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 484.9 KB (484918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea872a1c4dd3c6c51fd86c90eff9b5c3b2d3550468b71da3168cf7001a4350e`  
		Last Modified: Mon, 09 Dec 2024 19:31:37 GMT  
		Size: 363.6 MB (363550571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b481993f58a9db0ab2033372a98f411c0c3cc993433ae39c25220c6bd4456bb`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024eeb1880ccd50051d70dbf92ab1e5cdf53b15bb8a5f290b2bf04c14e230c03`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fd115845b272207eabe1b0ccb257fd8575f97626c978d5537ce2ae9cfff1a`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241209` - unknown; unknown

```console
$ docker pull odoo@sha256:cedb7f20d39b119465015adebe46717e77943ba85f8e0b9db61b1697dd1b74b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57751057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7762922b3bb9b2a461627503199d90d0c736b0d8dcccce9d09f6cff23dc9f5f4`

```dockerfile
```

-	Layers:
	-	`sha256:e83d9cfe10362ee828c2128420fbde7d329d2fa88bac1e442271a76f9d757911`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 57.7 MB (57723921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270e6b5c554ec691df116e7dfa9f54fdef3006a81b3daad2f03a45ec2917bf20`  
		Last Modified: Mon, 09 Dec 2024 19:31:30 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241209` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241209` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:f81284040205b46f4eecc227a676b2e7eef71dc44dfd175e7bdc916320317609
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
$ docker pull odoo@sha256:3f5fecc810fc79b1f9b078ed73c2918340bbf3c21cd0c54d3d72c2a5fd051a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662536537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a8a85eda81f6dc9706cb0ddfc174b97be2be558cee8f76870b943c3ebe37a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=amd64
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe691131d01ebc88838bfff5f1fa032b9fec54a8e5da19261f8fea25beedfc55`  
		Last Modified: Mon, 09 Dec 2024 19:31:34 GMT  
		Size: 254.5 MB (254515418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119cea40d91772dce45f029fd78520bb5ea523e9f8690806d0dc9c4a5fc7bdf`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 14.2 MB (14231220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f312beacc81dc375a27ee8e6dc42628f84a79d2772624e197387486bb5e2b`  
		Last Modified: Mon, 09 Dec 2024 19:31:31 GMT  
		Size: 484.9 KB (484918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea872a1c4dd3c6c51fd86c90eff9b5c3b2d3550468b71da3168cf7001a4350e`  
		Last Modified: Mon, 09 Dec 2024 19:31:37 GMT  
		Size: 363.6 MB (363550571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489e9a130f163b14e624f2f800d183ad4c529e800e1d025ec00c33e5d1f1f741`  
		Last Modified: Mon, 09 Dec 2024 19:30:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b481993f58a9db0ab2033372a98f411c0c3cc993433ae39c25220c6bd4456bb`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024eeb1880ccd50051d70dbf92ab1e5cdf53b15bb8a5f290b2bf04c14e230c03`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fd115845b272207eabe1b0ccb257fd8575f97626c978d5537ce2ae9cfff1a`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cedb7f20d39b119465015adebe46717e77943ba85f8e0b9db61b1697dd1b74b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57751057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7762922b3bb9b2a461627503199d90d0c736b0d8dcccce9d09f6cff23dc9f5f4`

```dockerfile
```

-	Layers:
	-	`sha256:e83d9cfe10362ee828c2128420fbde7d329d2fa88bac1e442271a76f9d757911`  
		Last Modified: Mon, 09 Dec 2024 19:31:32 GMT  
		Size: 57.7 MB (57723921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270e6b5c554ec691df116e7dfa9f54fdef3006a81b3daad2f03a45ec2917bf20`  
		Last Modified: Mon, 09 Dec 2024 19:31:30 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e96156949e69f83b91000c0f314fd86b687e9ff34ba29be260f677ee23c19a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658217406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8929e7d9eba77c8558d829005f7e94ec49658f6f074b37f8e538212bb07810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ecc3c41deba94deef9ef13230d21616fb856dd13b8ec0c592f3063a955318`  
		Last Modified: Tue, 03 Dec 2024 06:34:32 GMT  
		Size: 251.9 MB (251940434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730fbb6c4e05b09f822891bb1f189de5a363ff7032d6a5a5efec25322b27e42`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 14.2 MB (14204438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc74bc45ed2dfba386983367267b64df94f08164c3f10d6b199347554437c7`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9d13204a9c897ddbfb1929c28f06ab830c8a8cd8d89454771ebdbe5caf325b`  
		Last Modified: Tue, 03 Dec 2024 06:34:33 GMT  
		Size: 362.7 MB (362692505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80478f154202c3a7cb40eeeffd6b21cba82460cd564533f06db827a974b93053`  
		Last Modified: Tue, 03 Dec 2024 06:34:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039efacf5dca845f0e405783dd1fbd63b4b765f36ac15575f97c066007583d82`  
		Last Modified: Tue, 03 Dec 2024 06:34:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4683dc130afb32799e7770bdcd9f3f5e7f96cfe52e9b3d24a2a063dc4388d6`  
		Last Modified: Tue, 03 Dec 2024 06:34:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c2c74c0eb033c234a0a4020dbf765e6bfb43515d2b00bdcf9148a4698e3b34`  
		Last Modified: Tue, 03 Dec 2024 06:34:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b9551a7a3b66382b486c612307b4128523d3018cbf62188af7b11a8df6205f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9296bb6278447a4d0cd05898122acbb57dafe5f777e87ac0b73f6e15784066e8`

```dockerfile
```

-	Layers:
	-	`sha256:6ed0aebf6960bdca7478c998a29720ae936145d1346d59824f32508700acc15e`  
		Last Modified: Tue, 03 Dec 2024 06:34:27 GMT  
		Size: 57.3 MB (57260906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02242920cb27c914aaeb3598b47354139013a61d736741b7746ceb7cefa5c7f8`  
		Last Modified: Tue, 03 Dec 2024 06:34:25 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:72b4855b000970e61a5da9c99475e64f556f7fc33cd977df2c77925dba5809fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.8 MB (678842835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe8c04b25d4e0dcfbcae2366c3c820e9965d49afea787cfa850c9ced7087f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 11:09:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Dec 2024 11:09:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Dec 2024 11:09:29 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_RELEASE=20241209
# Mon, 09 Dec 2024 11:09:29 GMT
ARG ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241209 ODOO_SHA=e770c1c522d51a81e1b635babd9be08df17fa604
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Dec 2024 11:09:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Dec 2024 11:09:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Dec 2024 11:09:29 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Dec 2024 11:09:29 GMT
USER odoo
# Mon, 09 Dec 2024 11:09:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Dec 2024 11:09:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3056edf95a7243dfc8434ca76da482b2aa7884e627e2447a9a04a7f18dce0795`  
		Last Modified: Tue, 03 Dec 2024 05:33:49 GMT  
		Size: 265.1 MB (265091049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28cfb7c42f9441ec9fa85e24d455a8f2ac58260bebaa30e4f88a412312dd3`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 14.8 MB (14776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1d9c6bfaa6ceee82a4d08f3784773f158160eb28e90f46dcca5b11f52f30`  
		Last Modified: Tue, 03 Dec 2024 05:33:39 GMT  
		Size: 484.9 KB (484928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b46d2c73745f82abcceafce5241b29086a9addfe801efe90ca8697bfc01df6`  
		Last Modified: Mon, 09 Dec 2024 19:38:46 GMT  
		Size: 364.1 MB (364099505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8adc34a626394b963517a0010bd93b99aa3ebbbe47d55e7ea6979d863b670a`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730c8f028222ff027ee319f51ba54e53c81fa0490351bf10ddc49ffc95e42c0`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c49d4df869432dfaa25a124e3f4874f7c343215cda2ddd2bc526ad38c5288f`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8a93618bd698042102ebbeb7ecc062ebcfb712ba3264b7161bbc25dc028634`  
		Last Modified: Mon, 09 Dec 2024 19:38:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7d7a3d118386cbc40dfd9da35b395ff84f0d15a3949e83564345c30326d173aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57759281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d49477e3e9860fffa7fb72789bab8dfdfc24d38fd0bc8e65dff7547444537c`

```dockerfile
```

-	Layers:
	-	`sha256:ae1069bf41d63a996f339c8e8e9ed21d0ce3c34fa3ebf28678aa2c28e28244dc`  
		Last Modified: Mon, 09 Dec 2024 19:38:39 GMT  
		Size: 57.7 MB (57732084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b6655423883299993ec6d3b2ad3ed7dcd9b12c53b02b9c8401cd6380bd6f0d`  
		Last Modified: Mon, 09 Dec 2024 19:38:37 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json
