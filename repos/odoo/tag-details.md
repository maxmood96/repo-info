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
$ docker pull odoo@sha256:2ec9878811bc973198e1683c03e758344c4232ee88fcd8409ed444b9179a13ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:7ef4ce298432752463e5f328820b2756a551b512d6789bad955dd41d43fd97bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.7 MB (583673978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64d1beb72fa4e6a7b435dc363fa48605250919ac4a17a0b169968bfa86e34c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 25 Nov 2024 09:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7410237afbfbc5e01667f26a4f20eba53b713d19c5aee237d2debecf2729990`  
		Last Modified: Tue, 03 Dec 2024 02:35:32 GMT  
		Size: 219.6 MB (219628425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bbe9d914d49658783bb2a7ece8d22c5f0b8dc5efcd437d6904dbf6ac6a10da`  
		Last Modified: Tue, 03 Dec 2024 02:35:28 GMT  
		Size: 2.6 MB (2575884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19523ee3603dd3b84c9293f65bf86f765d2c0736ef5c4b3def2cfe638c48e0c1`  
		Last Modified: Tue, 03 Dec 2024 02:35:28 GMT  
		Size: 484.1 KB (484129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0becd3a43fb78448160067b2991297769d269a7ce6bc1327a714794f1e2c6d4e`  
		Last Modified: Tue, 03 Dec 2024 02:35:35 GMT  
		Size: 330.7 MB (330730461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da12566ae56755dd83bc7ad9eab67afc8f751d831c30e16425705450a6c4512`  
		Last Modified: Tue, 03 Dec 2024 02:35:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce5274f60034d28e8c2a6f1fb55ca33fab721fc503721dd534ec087d9792e2`  
		Last Modified: Tue, 03 Dec 2024 02:35:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7cfb9d597fd1c8a1a0d90d9f50fdc66578525b52e3b95daa49e888014492a`  
		Last Modified: Tue, 03 Dec 2024 02:35:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4e59322221dca825409e5ab588ab15ef7f69ee32645c56906db981d575f7d`  
		Last Modified: Tue, 03 Dec 2024 02:35:30 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:6c5fc07cce86bde37f9210172013203edb31dd86c318a57b605eee44c01088c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63516364d2cc6be8d1ac4545c49028321a7e690f77ffc593b6c3cf64c7fa8224`

```dockerfile
```

-	Layers:
	-	`sha256:88fcf9199f80969cf43e1c464b320defebce6eaf35b6e97eed50536b9403987e`  
		Last Modified: Tue, 03 Dec 2024 02:35:29 GMT  
		Size: 38.9 MB (38864354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55c19622b41903e5a25c57e7b21128350aafaaa8bb156df316a51521be3adc0`  
		Last Modified: Tue, 03 Dec 2024 02:35:28 GMT  
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
$ docker pull odoo@sha256:2ec9878811bc973198e1683c03e758344c4232ee88fcd8409ed444b9179a13ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:7ef4ce298432752463e5f328820b2756a551b512d6789bad955dd41d43fd97bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.7 MB (583673978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64d1beb72fa4e6a7b435dc363fa48605250919ac4a17a0b169968bfa86e34c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 25 Nov 2024 09:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7410237afbfbc5e01667f26a4f20eba53b713d19c5aee237d2debecf2729990`  
		Last Modified: Tue, 03 Dec 2024 02:35:32 GMT  
		Size: 219.6 MB (219628425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bbe9d914d49658783bb2a7ece8d22c5f0b8dc5efcd437d6904dbf6ac6a10da`  
		Last Modified: Tue, 03 Dec 2024 02:35:28 GMT  
		Size: 2.6 MB (2575884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19523ee3603dd3b84c9293f65bf86f765d2c0736ef5c4b3def2cfe638c48e0c1`  
		Last Modified: Tue, 03 Dec 2024 02:35:28 GMT  
		Size: 484.1 KB (484129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0becd3a43fb78448160067b2991297769d269a7ce6bc1327a714794f1e2c6d4e`  
		Last Modified: Tue, 03 Dec 2024 02:35:35 GMT  
		Size: 330.7 MB (330730461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da12566ae56755dd83bc7ad9eab67afc8f751d831c30e16425705450a6c4512`  
		Last Modified: Tue, 03 Dec 2024 02:35:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce5274f60034d28e8c2a6f1fb55ca33fab721fc503721dd534ec087d9792e2`  
		Last Modified: Tue, 03 Dec 2024 02:35:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7cfb9d597fd1c8a1a0d90d9f50fdc66578525b52e3b95daa49e888014492a`  
		Last Modified: Tue, 03 Dec 2024 02:35:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4e59322221dca825409e5ab588ab15ef7f69ee32645c56906db981d575f7d`  
		Last Modified: Tue, 03 Dec 2024 02:35:30 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6c5fc07cce86bde37f9210172013203edb31dd86c318a57b605eee44c01088c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38891072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63516364d2cc6be8d1ac4545c49028321a7e690f77ffc593b6c3cf64c7fa8224`

```dockerfile
```

-	Layers:
	-	`sha256:88fcf9199f80969cf43e1c464b320defebce6eaf35b6e97eed50536b9403987e`  
		Last Modified: Tue, 03 Dec 2024 02:35:29 GMT  
		Size: 38.9 MB (38864354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55c19622b41903e5a25c57e7b21128350aafaaa8bb156df316a51521be3adc0`  
		Last Modified: Tue, 03 Dec 2024 02:35:28 GMT  
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
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:17`

```console
$ docker pull odoo@sha256:2b56d8e7bc0cd9b7a89afc7ce3e17113fc6b1574db7fb810901e317cbcff7483
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
$ docker pull odoo@sha256:ca44785adfb1b902624066bccf92002e9eeb07d31ed1950f82dfc3eee27341bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.8 MB (598832329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac24b03f5ac1627e8d808570f22c5dc33b1493b7e2fa176a519c77735b8ea85`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30424451599047b1500a0fab1ef9d38f2c828e661bd2e5350c56dfc928350eea`  
		Last Modified: Mon, 25 Nov 2024 20:26:59 GMT  
		Size: 233.8 MB (233782155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baae6af1c87ae5333c07a228ada35da57650976beb0bef2c12caf14b4dddf0b3`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 2.5 MB (2493482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2962f1aa4a8766be7e3cb8bb418bed99a659c0c6f81e13948ffdf5adacdc0e7`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 470.0 KB (469978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f88912933c298c1ac88ca47b1b8b72713000a0bc7b116e8c8ff8e9a9d31c9`  
		Last Modified: Mon, 25 Nov 2024 20:27:00 GMT  
		Size: 332.5 MB (332548585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5964aa3a238938ec8e8e7b63861b243b47dfcf95a583b7fb875a3130221c13`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8bb7da0425f9822cb14c466deaafdd005b3f3d73ee042987946d3d762b91`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c67380a01e5bd54d556ec1c8fe5c6df68fbeb6efd97369f5eda70f3f0aa9c`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f646dc371b996a9bc5e48ab6362656f44b0694c17eb90ac4e531a2e0ff3358`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:816fdc65653221c9aa07481daded72579d70ac8010c8862cccd12b774b1787da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa8e27ecae8da39d6b0f4efba6beb362cd0ec18b6b318592396ce77dab383dd`

```dockerfile
```

-	Layers:
	-	`sha256:5647bcbe946868988a3cac48db6b499b32d8035785b5981671fc1449218c8027`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 39.6 MB (39615938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbaf3c586b91ac4df4945840fcc326d8d1abf77b5ba48f11e3a49ee097d3841`  
		Last Modified: Mon, 25 Nov 2024 20:26:52 GMT  
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
$ docker pull odoo@sha256:f2c54fcfb2376a8540d5021d05de088d2b888df3c1348ec17cccced0b5e8afbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615270446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f105d0d3228af94ff789c1a972ebbdae097e8f07e228e5723ebb2cf7f8c46b7`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
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
	-	`sha256:58056fe26f87028c0af4ca8c6107fec08b0b2b04d2fbe413612d5c17ea83fb87`  
		Last Modified: Mon, 25 Nov 2024 20:39:49 GMT  
		Size: 334.3 MB (334253832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a1d101edc7322ce83fee2afe8c37c3daa4820d3711b6ef1dbb07a1a9245f4f`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f81806a914dc1a42ce92037ffa9723b6808e38a5acdb0a23049f345ac3b216`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafecc0ed4141f1b39c8c58683d3c4540ef373f86e1d318e83821fb407a8253`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b573c90062187a265712dcb628f6bd92a0afb9c2a9957788d2d848887ae03`  
		Last Modified: Mon, 25 Nov 2024 20:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1bc3e0597b01ad5d288653537436026a4a19e17f9964d4cd0e8516535faf6f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39651156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81e8b180999e99bfef4c76f8c2d5d4119001eefa9a2d8a4438b90b2a48ef77`

```dockerfile
```

-	Layers:
	-	`sha256:d77780107d99e547189cfcbc8fcbcae5f7c0be7eb1927097fb2d22e874d401ff`  
		Last Modified: Mon, 25 Nov 2024 20:39:19 GMT  
		Size: 39.6 MB (39624265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37e3220841ba75d53f657aaa3930eb10998475281bc43a7b93d17976f24cf41`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:2b56d8e7bc0cd9b7a89afc7ce3e17113fc6b1574db7fb810901e317cbcff7483
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
$ docker pull odoo@sha256:ca44785adfb1b902624066bccf92002e9eeb07d31ed1950f82dfc3eee27341bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.8 MB (598832329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac24b03f5ac1627e8d808570f22c5dc33b1493b7e2fa176a519c77735b8ea85`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30424451599047b1500a0fab1ef9d38f2c828e661bd2e5350c56dfc928350eea`  
		Last Modified: Mon, 25 Nov 2024 20:26:59 GMT  
		Size: 233.8 MB (233782155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baae6af1c87ae5333c07a228ada35da57650976beb0bef2c12caf14b4dddf0b3`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 2.5 MB (2493482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2962f1aa4a8766be7e3cb8bb418bed99a659c0c6f81e13948ffdf5adacdc0e7`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 470.0 KB (469978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f88912933c298c1ac88ca47b1b8b72713000a0bc7b116e8c8ff8e9a9d31c9`  
		Last Modified: Mon, 25 Nov 2024 20:27:00 GMT  
		Size: 332.5 MB (332548585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5964aa3a238938ec8e8e7b63861b243b47dfcf95a583b7fb875a3130221c13`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8bb7da0425f9822cb14c466deaafdd005b3f3d73ee042987946d3d762b91`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c67380a01e5bd54d556ec1c8fe5c6df68fbeb6efd97369f5eda70f3f0aa9c`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f646dc371b996a9bc5e48ab6362656f44b0694c17eb90ac4e531a2e0ff3358`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:816fdc65653221c9aa07481daded72579d70ac8010c8862cccd12b774b1787da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa8e27ecae8da39d6b0f4efba6beb362cd0ec18b6b318592396ce77dab383dd`

```dockerfile
```

-	Layers:
	-	`sha256:5647bcbe946868988a3cac48db6b499b32d8035785b5981671fc1449218c8027`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 39.6 MB (39615938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbaf3c586b91ac4df4945840fcc326d8d1abf77b5ba48f11e3a49ee097d3841`  
		Last Modified: Mon, 25 Nov 2024 20:26:52 GMT  
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
$ docker pull odoo@sha256:f2c54fcfb2376a8540d5021d05de088d2b888df3c1348ec17cccced0b5e8afbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615270446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f105d0d3228af94ff789c1a972ebbdae097e8f07e228e5723ebb2cf7f8c46b7`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
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
	-	`sha256:58056fe26f87028c0af4ca8c6107fec08b0b2b04d2fbe413612d5c17ea83fb87`  
		Last Modified: Mon, 25 Nov 2024 20:39:49 GMT  
		Size: 334.3 MB (334253832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a1d101edc7322ce83fee2afe8c37c3daa4820d3711b6ef1dbb07a1a9245f4f`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f81806a914dc1a42ce92037ffa9723b6808e38a5acdb0a23049f345ac3b216`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafecc0ed4141f1b39c8c58683d3c4540ef373f86e1d318e83821fb407a8253`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b573c90062187a265712dcb628f6bd92a0afb9c2a9957788d2d848887ae03`  
		Last Modified: Mon, 25 Nov 2024 20:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1bc3e0597b01ad5d288653537436026a4a19e17f9964d4cd0e8516535faf6f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39651156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81e8b180999e99bfef4c76f8c2d5d4119001eefa9a2d8a4438b90b2a48ef77`

```dockerfile
```

-	Layers:
	-	`sha256:d77780107d99e547189cfcbc8fcbcae5f7c0be7eb1927097fb2d22e874d401ff`  
		Last Modified: Mon, 25 Nov 2024 20:39:19 GMT  
		Size: 39.6 MB (39624265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37e3220841ba75d53f657aaa3930eb10998475281bc43a7b93d17976f24cf41`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241209`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:18`

```console
$ docker pull odoo@sha256:b2b9ab3d88118b64d5e068bcbed088939d1e48f1e3d82e6b6597c502bde9fdaf
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
$ docker pull odoo@sha256:6e24e1c4111b3d4e6422a2a6cc73c329211f35d037e5a563f5583ff3a833cec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661830074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a71450e8815f61fb201d43258338c35e31bf23b05821b86a63f12ef5f2341fb`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b298162880546b0acbfc68fe1037765497daabe9b23075ebf0d865b469128e`  
		Last Modified: Tue, 03 Dec 2024 02:36:06 GMT  
		Size: 254.5 MB (254515917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed24007951c8a25815a615577827bef6a978106685168e6b70701cab26bf5f`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 14.2 MB (14231278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57990543a31a0a341f99f77d8ab7721c729618bc66164d44dd9ca0088bae94d`  
		Last Modified: Tue, 03 Dec 2024 02:36:01 GMT  
		Size: 484.9 KB (484916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5b3590f8503223519070eb66300d38afcce3c19c8a47d25c7272679e40adfb`  
		Last Modified: Tue, 03 Dec 2024 02:36:06 GMT  
		Size: 362.8 MB (362843553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94933d4d5f148831da97fde276af64b4116edaaf7cf364d5c241bd8ebafd1193`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e549c47df3a0626c35508881736cd104b9e02ee22bf7b92e582eb390fdf543`  
		Last Modified: Tue, 03 Dec 2024 02:36:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a8fcdbc2b2e0b6aeae4bb2a633af4907f84611e8208393cb237968ef7347f`  
		Last Modified: Tue, 03 Dec 2024 02:36:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87334bbec501e45123f88533d1c2598d83510058b2df3ca7fe80202d01fcc44`  
		Last Modified: Tue, 03 Dec 2024 02:36:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:8042a0fe52359fafabf496e54a3857535b83e5815e7b7c594b006b396bb16c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b279daecafc4e037d7333a88b41e78993f275c17c60ace8d9c2e41ccbbccd3`

```dockerfile
```

-	Layers:
	-	`sha256:e7c9bf01d4e040fa823c1cf511b65198826d2979fff0d74581d80724b037ad5f`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 57.3 MB (57253608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e532368a6f57bdfbcaf88b9c66a9428043eb2f61774101d68b31727027f480a9`  
		Last Modified: Tue, 03 Dec 2024 02:36:01 GMT  
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
$ docker pull odoo@sha256:e0784c78f62995dbcf73f29b96944b644c8585c013f30e9dda3e6942509ae966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 MB (678141152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a0a5cc536355dbe7d0ae13c32ee59a0ee2762e724ccb35555035bc6a48541f`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
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
	-	`sha256:3baa9c2dbb53331df5430f7329e5cffdc177e35aa18bc848434ac3b876d73c0e`  
		Last Modified: Tue, 03 Dec 2024 05:34:06 GMT  
		Size: 363.4 MB (363397822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329757d37af3dbe8b486c2fdb3957735ae4843bbe62fb747bac9ca77cb60f9b`  
		Last Modified: Tue, 03 Dec 2024 05:33:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac160b6dd237c26286c5006f036bd279769451d18ffa382eeca57c327ce5115d`  
		Last Modified: Tue, 03 Dec 2024 05:33:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701f1a008438be31781a9ee5793a4a7619e46df2546e82e3b40900ff4d1cf5c`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda661bf8b75826a1807aeba0b48d6460c524b26a4aa530501de62894f75cdd4`  
		Last Modified: Tue, 03 Dec 2024 05:33:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:45f2a2ec00c24715ab5f082e8c2f97843e402f4412c0678b42ea4f7a34a9d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2b24231b79c25af4b0f0a26875e6781fede5ea6c700a4acd095bce9bbcd323`

```dockerfile
```

-	Layers:
	-	`sha256:506859084a36b2726bb99072b13b697c7dca4b2d5e67523437587bc214cbcc92`  
		Last Modified: Tue, 03 Dec 2024 05:33:41 GMT  
		Size: 57.3 MB (57261771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54403cdd6d09f10e746fef369d6fdb2860093aeb5f4f7a6e5928045a004e7882`  
		Last Modified: Tue, 03 Dec 2024 05:33:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:b2b9ab3d88118b64d5e068bcbed088939d1e48f1e3d82e6b6597c502bde9fdaf
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
$ docker pull odoo@sha256:6e24e1c4111b3d4e6422a2a6cc73c329211f35d037e5a563f5583ff3a833cec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661830074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a71450e8815f61fb201d43258338c35e31bf23b05821b86a63f12ef5f2341fb`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b298162880546b0acbfc68fe1037765497daabe9b23075ebf0d865b469128e`  
		Last Modified: Tue, 03 Dec 2024 02:36:06 GMT  
		Size: 254.5 MB (254515917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed24007951c8a25815a615577827bef6a978106685168e6b70701cab26bf5f`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 14.2 MB (14231278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57990543a31a0a341f99f77d8ab7721c729618bc66164d44dd9ca0088bae94d`  
		Last Modified: Tue, 03 Dec 2024 02:36:01 GMT  
		Size: 484.9 KB (484916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5b3590f8503223519070eb66300d38afcce3c19c8a47d25c7272679e40adfb`  
		Last Modified: Tue, 03 Dec 2024 02:36:06 GMT  
		Size: 362.8 MB (362843553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94933d4d5f148831da97fde276af64b4116edaaf7cf364d5c241bd8ebafd1193`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e549c47df3a0626c35508881736cd104b9e02ee22bf7b92e582eb390fdf543`  
		Last Modified: Tue, 03 Dec 2024 02:36:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a8fcdbc2b2e0b6aeae4bb2a633af4907f84611e8208393cb237968ef7347f`  
		Last Modified: Tue, 03 Dec 2024 02:36:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87334bbec501e45123f88533d1c2598d83510058b2df3ca7fe80202d01fcc44`  
		Last Modified: Tue, 03 Dec 2024 02:36:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8042a0fe52359fafabf496e54a3857535b83e5815e7b7c594b006b396bb16c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b279daecafc4e037d7333a88b41e78993f275c17c60ace8d9c2e41ccbbccd3`

```dockerfile
```

-	Layers:
	-	`sha256:e7c9bf01d4e040fa823c1cf511b65198826d2979fff0d74581d80724b037ad5f`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 57.3 MB (57253608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e532368a6f57bdfbcaf88b9c66a9428043eb2f61774101d68b31727027f480a9`  
		Last Modified: Tue, 03 Dec 2024 02:36:01 GMT  
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
$ docker pull odoo@sha256:e0784c78f62995dbcf73f29b96944b644c8585c013f30e9dda3e6942509ae966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 MB (678141152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a0a5cc536355dbe7d0ae13c32ee59a0ee2762e724ccb35555035bc6a48541f`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
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
	-	`sha256:3baa9c2dbb53331df5430f7329e5cffdc177e35aa18bc848434ac3b876d73c0e`  
		Last Modified: Tue, 03 Dec 2024 05:34:06 GMT  
		Size: 363.4 MB (363397822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329757d37af3dbe8b486c2fdb3957735ae4843bbe62fb747bac9ca77cb60f9b`  
		Last Modified: Tue, 03 Dec 2024 05:33:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac160b6dd237c26286c5006f036bd279769451d18ffa382eeca57c327ce5115d`  
		Last Modified: Tue, 03 Dec 2024 05:33:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701f1a008438be31781a9ee5793a4a7619e46df2546e82e3b40900ff4d1cf5c`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda661bf8b75826a1807aeba0b48d6460c524b26a4aa530501de62894f75cdd4`  
		Last Modified: Tue, 03 Dec 2024 05:33:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:45f2a2ec00c24715ab5f082e8c2f97843e402f4412c0678b42ea4f7a34a9d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2b24231b79c25af4b0f0a26875e6781fede5ea6c700a4acd095bce9bbcd323`

```dockerfile
```

-	Layers:
	-	`sha256:506859084a36b2726bb99072b13b697c7dca4b2d5e67523437587bc214cbcc92`  
		Last Modified: Tue, 03 Dec 2024 05:33:41 GMT  
		Size: 57.3 MB (57261771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54403cdd6d09f10e746fef369d6fdb2860093aeb5f4f7a6e5928045a004e7882`  
		Last Modified: Tue, 03 Dec 2024 05:33:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241209`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:latest`

```console
$ docker pull odoo@sha256:b2b9ab3d88118b64d5e068bcbed088939d1e48f1e3d82e6b6597c502bde9fdaf
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
$ docker pull odoo@sha256:6e24e1c4111b3d4e6422a2a6cc73c329211f35d037e5a563f5583ff3a833cec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661830074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a71450e8815f61fb201d43258338c35e31bf23b05821b86a63f12ef5f2341fb`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b298162880546b0acbfc68fe1037765497daabe9b23075ebf0d865b469128e`  
		Last Modified: Tue, 03 Dec 2024 02:36:06 GMT  
		Size: 254.5 MB (254515917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed24007951c8a25815a615577827bef6a978106685168e6b70701cab26bf5f`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 14.2 MB (14231278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57990543a31a0a341f99f77d8ab7721c729618bc66164d44dd9ca0088bae94d`  
		Last Modified: Tue, 03 Dec 2024 02:36:01 GMT  
		Size: 484.9 KB (484916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5b3590f8503223519070eb66300d38afcce3c19c8a47d25c7272679e40adfb`  
		Last Modified: Tue, 03 Dec 2024 02:36:06 GMT  
		Size: 362.8 MB (362843553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94933d4d5f148831da97fde276af64b4116edaaf7cf364d5c241bd8ebafd1193`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e549c47df3a0626c35508881736cd104b9e02ee22bf7b92e582eb390fdf543`  
		Last Modified: Tue, 03 Dec 2024 02:36:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a8fcdbc2b2e0b6aeae4bb2a633af4907f84611e8208393cb237968ef7347f`  
		Last Modified: Tue, 03 Dec 2024 02:36:03 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87334bbec501e45123f88533d1c2598d83510058b2df3ca7fe80202d01fcc44`  
		Last Modified: Tue, 03 Dec 2024 02:36:04 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:8042a0fe52359fafabf496e54a3857535b83e5815e7b7c594b006b396bb16c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b279daecafc4e037d7333a88b41e78993f275c17c60ace8d9c2e41ccbbccd3`

```dockerfile
```

-	Layers:
	-	`sha256:e7c9bf01d4e040fa823c1cf511b65198826d2979fff0d74581d80724b037ad5f`  
		Last Modified: Tue, 03 Dec 2024 02:36:02 GMT  
		Size: 57.3 MB (57253608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e532368a6f57bdfbcaf88b9c66a9428043eb2f61774101d68b31727027f480a9`  
		Last Modified: Tue, 03 Dec 2024 02:36:01 GMT  
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
$ docker pull odoo@sha256:e0784c78f62995dbcf73f29b96944b644c8585c013f30e9dda3e6942509ae966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.1 MB (678141152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a0a5cc536355dbe7d0ae13c32ee59a0ee2762e724ccb35555035bc6a48541f`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
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
	-	`sha256:3baa9c2dbb53331df5430f7329e5cffdc177e35aa18bc848434ac3b876d73c0e`  
		Last Modified: Tue, 03 Dec 2024 05:34:06 GMT  
		Size: 363.4 MB (363397822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329757d37af3dbe8b486c2fdb3957735ae4843bbe62fb747bac9ca77cb60f9b`  
		Last Modified: Tue, 03 Dec 2024 05:33:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac160b6dd237c26286c5006f036bd279769451d18ffa382eeca57c327ce5115d`  
		Last Modified: Tue, 03 Dec 2024 05:33:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701f1a008438be31781a9ee5793a4a7619e46df2546e82e3b40900ff4d1cf5c`  
		Last Modified: Tue, 03 Dec 2024 05:33:42 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda661bf8b75826a1807aeba0b48d6460c524b26a4aa530501de62894f75cdd4`  
		Last Modified: Tue, 03 Dec 2024 05:33:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:45f2a2ec00c24715ab5f082e8c2f97843e402f4412c0678b42ea4f7a34a9d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2b24231b79c25af4b0f0a26875e6781fede5ea6c700a4acd095bce9bbcd323`

```dockerfile
```

-	Layers:
	-	`sha256:506859084a36b2726bb99072b13b697c7dca4b2d5e67523437587bc214cbcc92`  
		Last Modified: Tue, 03 Dec 2024 05:33:41 GMT  
		Size: 57.3 MB (57261771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54403cdd6d09f10e746fef369d6fdb2860093aeb5f4f7a6e5928045a004e7882`  
		Last Modified: Tue, 03 Dec 2024 05:33:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
