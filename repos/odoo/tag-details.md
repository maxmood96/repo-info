<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241007`](#odoo160-20241007)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241007`](#odoo170-20241007)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241007`](#odoo180-20241007)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:1f8ab5a76e6fdb1cd7a34937608137bd09eb1907b3bdf6fd52336ffbf7a98258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:5911990c6981008e69a5d16b26bc9d4b4ac0d946e40b01061eda762624c0fed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584378814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3a47481d95fd9b7161b03e5b4b56e46b47a6fd5c4fedc030508ffb9c21fca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba9b75b40a22b60cacb371f57788a78ec617476c3fa21576d87f126d9e8969`  
		Last Modified: Mon, 07 Oct 2024 20:00:59 GMT  
		Size: 219.6 MB (219599352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50c0e9dc7ae39a05fb2df0b58213dd132ccc876ce3c5911f3e1386a2407e096`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 2.5 MB (2493913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2b22d9c74af01ca08263c5a8fe7367fd0255b0ca109adbf586da8a3982b338`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 471.6 KB (471596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442c5016862eca54378184cd3bbdd1c3e834cbf95c4107d7fc1a101ae42aa89e`  
		Last Modified: Mon, 07 Oct 2024 20:01:01 GMT  
		Size: 330.4 MB (330382925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4dd047c911d1ce8218ded752789085c6cf10b6ddb5a45e06a0cf0df91218e`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fffa3c7a7fdaff78dd780825bd45f995ec3234f30f0c095e517c518484a310`  
		Last Modified: Mon, 07 Oct 2024 20:00:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b68e5ddb6c1f5202d02dcddc513b7db9a34dd9bca11f07ee9fad6fb3ced0aa`  
		Last Modified: Mon, 07 Oct 2024 20:00:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d125120e819e203c86bca7c280ec05814b9c56fa8bdb99f8be1f289575037a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38804808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956737f469fdb9f4ab0129f30b571d4f1ee7bfa9b4e158e190f59c281798d287`

```dockerfile
```

-	Layers:
	-	`sha256:94802871f3e37e73ba91483ea01a2d6d9d39a29943c91c1ecf71a800bb6ea456`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 38.8 MB (38778261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e20187218e23d70378864ada41a2e92e48950a43a19f4b19b3aa9c9432389cb`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:81d59325453a07e404bd21fa05f08fb63a49ed9670363f1f7c206d54a4e6ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579982940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa8199a291d3783b31450fbf3065fb81c1f14d24f47926a4b9f135f5d7f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f0291d4d9e2db81d33157d590d424fd6e03723cc1d00047d19ddca19d5f16b`  
		Last Modified: Mon, 07 Oct 2024 20:25:10 GMT  
		Size: 216.9 MB (216900083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f2f870ea7a9b4b2f9d4be3c1e09934d97f9e7e56fcf77da5ce76e70846796`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 2.5 MB (2504056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beff7b55b3e3fd58a8be6ad3fa32257d2ac8ae6457056d0c3420fc99393c728`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 471.7 KB (471690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380c1560a15da8c102bdb37057db7c7e3e2b87db378ba9b0732090cb34a9e27`  
		Last Modified: Mon, 07 Oct 2024 20:25:12 GMT  
		Size: 330.0 MB (330029520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb769e447cc3ec8d8a171c617aa29641baeb8dc59000d0975b5fb8dadb4ebc65`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abcdacbbd32c0e27778067aa8bda6ddc2669c1bb2406a7df8c54b9a78696d4`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd10f55220f4b8fdcee7b054a079af3b1acbc87604827230aa01fa614371fe7`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e47548e96347eecade2a960ab613a8a120a85d4f5a28a7d7edd56a3102fd`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e8ccafa9392c95b84532063692d699fe1225b634a93c60d49a507fa88dbfcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38811426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f349479a4092b8be8614d33a5922879be2d757d582509c775f8a23fe29b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:920f986fa71ef5ee5d66d1e7472b0f3e5c706f1c503a95c60c005a58b5ae59f2`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 38.8 MB (38784733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecb6e4fba2c9bc2aebe2afa9fbfacffa9f90964df1b264688397ad8dd3e62`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 26.7 KB (26693 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:1f8ab5a76e6fdb1cd7a34937608137bd09eb1907b3bdf6fd52336ffbf7a98258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:5911990c6981008e69a5d16b26bc9d4b4ac0d946e40b01061eda762624c0fed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584378814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3a47481d95fd9b7161b03e5b4b56e46b47a6fd5c4fedc030508ffb9c21fca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba9b75b40a22b60cacb371f57788a78ec617476c3fa21576d87f126d9e8969`  
		Last Modified: Mon, 07 Oct 2024 20:00:59 GMT  
		Size: 219.6 MB (219599352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50c0e9dc7ae39a05fb2df0b58213dd132ccc876ce3c5911f3e1386a2407e096`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 2.5 MB (2493913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2b22d9c74af01ca08263c5a8fe7367fd0255b0ca109adbf586da8a3982b338`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 471.6 KB (471596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442c5016862eca54378184cd3bbdd1c3e834cbf95c4107d7fc1a101ae42aa89e`  
		Last Modified: Mon, 07 Oct 2024 20:01:01 GMT  
		Size: 330.4 MB (330382925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4dd047c911d1ce8218ded752789085c6cf10b6ddb5a45e06a0cf0df91218e`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fffa3c7a7fdaff78dd780825bd45f995ec3234f30f0c095e517c518484a310`  
		Last Modified: Mon, 07 Oct 2024 20:00:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b68e5ddb6c1f5202d02dcddc513b7db9a34dd9bca11f07ee9fad6fb3ced0aa`  
		Last Modified: Mon, 07 Oct 2024 20:00:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d125120e819e203c86bca7c280ec05814b9c56fa8bdb99f8be1f289575037a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38804808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956737f469fdb9f4ab0129f30b571d4f1ee7bfa9b4e158e190f59c281798d287`

```dockerfile
```

-	Layers:
	-	`sha256:94802871f3e37e73ba91483ea01a2d6d9d39a29943c91c1ecf71a800bb6ea456`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 38.8 MB (38778261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e20187218e23d70378864ada41a2e92e48950a43a19f4b19b3aa9c9432389cb`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:81d59325453a07e404bd21fa05f08fb63a49ed9670363f1f7c206d54a4e6ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579982940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa8199a291d3783b31450fbf3065fb81c1f14d24f47926a4b9f135f5d7f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f0291d4d9e2db81d33157d590d424fd6e03723cc1d00047d19ddca19d5f16b`  
		Last Modified: Mon, 07 Oct 2024 20:25:10 GMT  
		Size: 216.9 MB (216900083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f2f870ea7a9b4b2f9d4be3c1e09934d97f9e7e56fcf77da5ce76e70846796`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 2.5 MB (2504056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beff7b55b3e3fd58a8be6ad3fa32257d2ac8ae6457056d0c3420fc99393c728`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 471.7 KB (471690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380c1560a15da8c102bdb37057db7c7e3e2b87db378ba9b0732090cb34a9e27`  
		Last Modified: Mon, 07 Oct 2024 20:25:12 GMT  
		Size: 330.0 MB (330029520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb769e447cc3ec8d8a171c617aa29641baeb8dc59000d0975b5fb8dadb4ebc65`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abcdacbbd32c0e27778067aa8bda6ddc2669c1bb2406a7df8c54b9a78696d4`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd10f55220f4b8fdcee7b054a079af3b1acbc87604827230aa01fa614371fe7`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e47548e96347eecade2a960ab613a8a120a85d4f5a28a7d7edd56a3102fd`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e8ccafa9392c95b84532063692d699fe1225b634a93c60d49a507fa88dbfcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38811426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f349479a4092b8be8614d33a5922879be2d757d582509c775f8a23fe29b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:920f986fa71ef5ee5d66d1e7472b0f3e5c706f1c503a95c60c005a58b5ae59f2`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 38.8 MB (38784733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecb6e4fba2c9bc2aebe2afa9fbfacffa9f90964df1b264688397ad8dd3e62`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 26.7 KB (26693 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241007`

```console
$ docker pull odoo@sha256:1f8ab5a76e6fdb1cd7a34937608137bd09eb1907b3bdf6fd52336ffbf7a98258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241007` - linux; amd64

```console
$ docker pull odoo@sha256:5911990c6981008e69a5d16b26bc9d4b4ac0d946e40b01061eda762624c0fed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584378814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b3a47481d95fd9b7161b03e5b4b56e46b47a6fd5c4fedc030508ffb9c21fca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaba9b75b40a22b60cacb371f57788a78ec617476c3fa21576d87f126d9e8969`  
		Last Modified: Mon, 07 Oct 2024 20:00:59 GMT  
		Size: 219.6 MB (219599352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50c0e9dc7ae39a05fb2df0b58213dd132ccc876ce3c5911f3e1386a2407e096`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 2.5 MB (2493913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2b22d9c74af01ca08263c5a8fe7367fd0255b0ca109adbf586da8a3982b338`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 471.6 KB (471596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442c5016862eca54378184cd3bbdd1c3e834cbf95c4107d7fc1a101ae42aa89e`  
		Last Modified: Mon, 07 Oct 2024 20:01:01 GMT  
		Size: 330.4 MB (330382925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4dd047c911d1ce8218ded752789085c6cf10b6ddb5a45e06a0cf0df91218e`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fffa3c7a7fdaff78dd780825bd45f995ec3234f30f0c095e517c518484a310`  
		Last Modified: Mon, 07 Oct 2024 20:00:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b68e5ddb6c1f5202d02dcddc513b7db9a34dd9bca11f07ee9fad6fb3ced0aa`  
		Last Modified: Mon, 07 Oct 2024 20:00:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:d125120e819e203c86bca7c280ec05814b9c56fa8bdb99f8be1f289575037a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38804808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956737f469fdb9f4ab0129f30b571d4f1ee7bfa9b4e158e190f59c281798d287`

```dockerfile
```

-	Layers:
	-	`sha256:94802871f3e37e73ba91483ea01a2d6d9d39a29943c91c1ecf71a800bb6ea456`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 38.8 MB (38778261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e20187218e23d70378864ada41a2e92e48950a43a19f4b19b3aa9c9432389cb`  
		Last Modified: Mon, 07 Oct 2024 20:00:56 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241007` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:81d59325453a07e404bd21fa05f08fb63a49ed9670363f1f7c206d54a4e6ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579982940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa8199a291d3783b31450fbf3065fb81c1f14d24f47926a4b9f135f5d7f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f0291d4d9e2db81d33157d590d424fd6e03723cc1d00047d19ddca19d5f16b`  
		Last Modified: Mon, 07 Oct 2024 20:25:10 GMT  
		Size: 216.9 MB (216900083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f2f870ea7a9b4b2f9d4be3c1e09934d97f9e7e56fcf77da5ce76e70846796`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 2.5 MB (2504056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beff7b55b3e3fd58a8be6ad3fa32257d2ac8ae6457056d0c3420fc99393c728`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 471.7 KB (471690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380c1560a15da8c102bdb37057db7c7e3e2b87db378ba9b0732090cb34a9e27`  
		Last Modified: Mon, 07 Oct 2024 20:25:12 GMT  
		Size: 330.0 MB (330029520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb769e447cc3ec8d8a171c617aa29641baeb8dc59000d0975b5fb8dadb4ebc65`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abcdacbbd32c0e27778067aa8bda6ddc2669c1bb2406a7df8c54b9a78696d4`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd10f55220f4b8fdcee7b054a079af3b1acbc87604827230aa01fa614371fe7`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e47548e96347eecade2a960ab613a8a120a85d4f5a28a7d7edd56a3102fd`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:e8ccafa9392c95b84532063692d699fe1225b634a93c60d49a507fa88dbfcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38811426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f349479a4092b8be8614d33a5922879be2d757d582509c775f8a23fe29b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:920f986fa71ef5ee5d66d1e7472b0f3e5c706f1c503a95c60c005a58b5ae59f2`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 38.8 MB (38784733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecb6e4fba2c9bc2aebe2afa9fbfacffa9f90964df1b264688397ad8dd3e62`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 26.7 KB (26693 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:0777c7443e0912725b54be341ba84620576b65c15ab9090d3f07d59701cf2711
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
$ docker pull odoo@sha256:b83832e102b2043d78cf912ce2221808ea7e7b460c837e8e9a2664847d6f1d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9604c9c21589224485598f2f790eccdecf4d6fbf47fd8da3aacf9bbececea66a`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e72ba30aed51d4d6c0c237e8bc3c101132e74ae632f1e4eb10942be7b727e`  
		Last Modified: Mon, 07 Oct 2024 20:01:10 GMT  
		Size: 233.8 MB (233763083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ff36f497e26e69c3be270acdbaae0980ae0af88f9656d7bf0e2c6f53284c8`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 2.4 MB (2405343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fcec3c52a5f23aabdf2f205a460aa9aa230c2ca4a7db3376000d5fbd04f3e`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 472.6 KB (472578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d202538c69c111b18a706c8d54ac975532ec4a020ac0fc9cda7bae244428d1`  
		Last Modified: Mon, 07 Oct 2024 20:01:12 GMT  
		Size: 331.7 MB (331705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e01b86b7e7d04baa375c1e89e199796d3e97de17489556bfad943e4fe78a88`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1c4d0f9821a9672084c08e1dd88de11d03eabaf149afc539f90eceaf93700`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08d0548d80024105b6bea0212d3253ea206a0a41b67a4c837f4b4087e2b034`  
		Last Modified: Mon, 07 Oct 2024 20:01:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:427f42d6e67c6173a2d070089f876df7235cb398147292c38a5fc9a0621f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39507564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe4dafb4e572ef28684d70f9b0d76d77d75aa6c2ac0f413ca540723736f89bc`

```dockerfile
```

-	Layers:
	-	`sha256:c917111b60355c59304c6b634bd422af02b6a246ad09f92fe8790fb204cfd9c1`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 39.5 MB (39480979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba4355a0c07c5d4dc95087814aa74abac7572bf737ea00d359740417e8c4304`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 26.6 KB (26585 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1f1f6da85e17cd21290ace7a21fa67ffa8370e52b20fcab790f41a051ec066c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592698494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec5d5720bf27403a52539c521f18b7695c1e1dfc3dba8bf92edd32bc3f0a08`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaeceaa088b15b07a8b1315a8325a1999e684223cf5e67a6c006b850ac8848e`  
		Last Modified: Mon, 07 Oct 2024 20:21:17 GMT  
		Size: 231.2 MB (231157442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593da4ee3c2b9cf8ba865cf0bcf3b58fc15624ee1dd7685e9f43bf546d2f81c9`  
		Last Modified: Mon, 07 Oct 2024 20:21:12 GMT  
		Size: 2.4 MB (2398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6951d7a9161762682e478a3b71e8822a05e2af33e60248f4913a92e195005a`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 472.7 KB (472696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005b6e94bcd93e08df067e60060f7c0b0f62d8e00f04aee488ef94768fca1f`  
		Last Modified: Mon, 07 Oct 2024 20:21:19 GMT  
		Size: 331.3 MB (331309334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58e977e68009ac44f0b7414f7a0e2ac195bfb9fe4303955acc67a33929ea10`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb71664b6198a3568af98278a1163b9b0168bf6a98b6fda02756af5334c6664`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231c2b8caa3c4c0257307b59bb859d93f314c023f13da4e2a8af313c89796f5`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ac6c81ec328e11241e07e75155f74e05cd7f870ebb6d5ec66a7ee099b24b7`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c5b4fa83d6e0d8a7d6fa4cd9cc9286af10333eebcb69f0729655b79542bc35cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc0439fa6e521d8db24ce56ca24c90db5cdcfcd29f30dd5b2606af5f50a216`

```dockerfile
```

-	Layers:
	-	`sha256:2588008565e78b6555ca86898390d6089bc8dd0919071cb09b668f711f497421`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 39.5 MB (39487492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3abd04ebaea97afb033a95ea0f403614da68216ef25fe607a9479795bdd970`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 26.7 KB (26732 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:c9c7849a8914fc213cf0cdad653fbc49e7b4a3046869cddcaee6148bbb4cac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614348604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fc0aaae4f6d58625a13efbb5a6261c5746b2770724140b65cce56e231c51e`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf22e9ecbdb17bae5948434399d20e985516ae45e11e72048320700f4c3002a`  
		Last Modified: Mon, 07 Oct 2024 20:21:39 GMT  
		Size: 243.3 MB (243294995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72daf6d3193cf48405ab14e7b21e55790dcda77c3e506d6ff2d916be2e81ab`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 2.7 MB (2708338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc1a4222c36d4c42eb25f5f2f0249bf9eabf1c589f406f87173d3e7293431`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 472.7 KB (472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db12d8f486a52172344f99e4ef0b2bfb16d9821239b125e83d7806488074c`  
		Last Modified: Mon, 07 Oct 2024 20:21:44 GMT  
		Size: 333.4 MB (333421873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded5e3af0dbff384e1805596730a23773fee78873edd6dfd2ab51bb230cbab3`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9878389a7cd65810b8a5288fa3df793a4061e0682ff3f2ed10dc7290e97dac1`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac2c5bcd93bd7c3ffd66f4cf3fe9e8de2c28275205ab2358b020bb63aef219`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad903c2d978fb03c0a2e37a11ec79b83d141641bbdd3cb51d967c80754de03e`  
		Last Modified: Mon, 07 Oct 2024 20:21:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:27e1f93d1227d6341fe89aed3f796c5ff11fda59937cd60d8bd66aa924da2700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89987f1998492b30276df26c0f81d79265de5d89aeeecda184af3f8bc302a359`

```dockerfile
```

-	Layers:
	-	`sha256:af3a4e5105b5664b62b8d0b287fee74a6c86c9a5a8a7ba319f13e55e14352b4f`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 39.5 MB (39489286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef433a4d91a323051092d6b2a91ae987563627672e47d65a5552cd3dfd7bb7c`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 26.6 KB (26636 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:0777c7443e0912725b54be341ba84620576b65c15ab9090d3f07d59701cf2711
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
$ docker pull odoo@sha256:b83832e102b2043d78cf912ce2221808ea7e7b460c837e8e9a2664847d6f1d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9604c9c21589224485598f2f790eccdecf4d6fbf47fd8da3aacf9bbececea66a`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e72ba30aed51d4d6c0c237e8bc3c101132e74ae632f1e4eb10942be7b727e`  
		Last Modified: Mon, 07 Oct 2024 20:01:10 GMT  
		Size: 233.8 MB (233763083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ff36f497e26e69c3be270acdbaae0980ae0af88f9656d7bf0e2c6f53284c8`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 2.4 MB (2405343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fcec3c52a5f23aabdf2f205a460aa9aa230c2ca4a7db3376000d5fbd04f3e`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 472.6 KB (472578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d202538c69c111b18a706c8d54ac975532ec4a020ac0fc9cda7bae244428d1`  
		Last Modified: Mon, 07 Oct 2024 20:01:12 GMT  
		Size: 331.7 MB (331705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e01b86b7e7d04baa375c1e89e199796d3e97de17489556bfad943e4fe78a88`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1c4d0f9821a9672084c08e1dd88de11d03eabaf149afc539f90eceaf93700`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08d0548d80024105b6bea0212d3253ea206a0a41b67a4c837f4b4087e2b034`  
		Last Modified: Mon, 07 Oct 2024 20:01:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:427f42d6e67c6173a2d070089f876df7235cb398147292c38a5fc9a0621f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39507564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe4dafb4e572ef28684d70f9b0d76d77d75aa6c2ac0f413ca540723736f89bc`

```dockerfile
```

-	Layers:
	-	`sha256:c917111b60355c59304c6b634bd422af02b6a246ad09f92fe8790fb204cfd9c1`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 39.5 MB (39480979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba4355a0c07c5d4dc95087814aa74abac7572bf737ea00d359740417e8c4304`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 26.6 KB (26585 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1f1f6da85e17cd21290ace7a21fa67ffa8370e52b20fcab790f41a051ec066c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592698494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec5d5720bf27403a52539c521f18b7695c1e1dfc3dba8bf92edd32bc3f0a08`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaeceaa088b15b07a8b1315a8325a1999e684223cf5e67a6c006b850ac8848e`  
		Last Modified: Mon, 07 Oct 2024 20:21:17 GMT  
		Size: 231.2 MB (231157442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593da4ee3c2b9cf8ba865cf0bcf3b58fc15624ee1dd7685e9f43bf546d2f81c9`  
		Last Modified: Mon, 07 Oct 2024 20:21:12 GMT  
		Size: 2.4 MB (2398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6951d7a9161762682e478a3b71e8822a05e2af33e60248f4913a92e195005a`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 472.7 KB (472696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005b6e94bcd93e08df067e60060f7c0b0f62d8e00f04aee488ef94768fca1f`  
		Last Modified: Mon, 07 Oct 2024 20:21:19 GMT  
		Size: 331.3 MB (331309334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58e977e68009ac44f0b7414f7a0e2ac195bfb9fe4303955acc67a33929ea10`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb71664b6198a3568af98278a1163b9b0168bf6a98b6fda02756af5334c6664`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231c2b8caa3c4c0257307b59bb859d93f314c023f13da4e2a8af313c89796f5`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ac6c81ec328e11241e07e75155f74e05cd7f870ebb6d5ec66a7ee099b24b7`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c5b4fa83d6e0d8a7d6fa4cd9cc9286af10333eebcb69f0729655b79542bc35cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc0439fa6e521d8db24ce56ca24c90db5cdcfcd29f30dd5b2606af5f50a216`

```dockerfile
```

-	Layers:
	-	`sha256:2588008565e78b6555ca86898390d6089bc8dd0919071cb09b668f711f497421`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 39.5 MB (39487492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3abd04ebaea97afb033a95ea0f403614da68216ef25fe607a9479795bdd970`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 26.7 KB (26732 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c9c7849a8914fc213cf0cdad653fbc49e7b4a3046869cddcaee6148bbb4cac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614348604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fc0aaae4f6d58625a13efbb5a6261c5746b2770724140b65cce56e231c51e`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf22e9ecbdb17bae5948434399d20e985516ae45e11e72048320700f4c3002a`  
		Last Modified: Mon, 07 Oct 2024 20:21:39 GMT  
		Size: 243.3 MB (243294995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72daf6d3193cf48405ab14e7b21e55790dcda77c3e506d6ff2d916be2e81ab`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 2.7 MB (2708338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc1a4222c36d4c42eb25f5f2f0249bf9eabf1c589f406f87173d3e7293431`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 472.7 KB (472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db12d8f486a52172344f99e4ef0b2bfb16d9821239b125e83d7806488074c`  
		Last Modified: Mon, 07 Oct 2024 20:21:44 GMT  
		Size: 333.4 MB (333421873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded5e3af0dbff384e1805596730a23773fee78873edd6dfd2ab51bb230cbab3`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9878389a7cd65810b8a5288fa3df793a4061e0682ff3f2ed10dc7290e97dac1`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac2c5bcd93bd7c3ffd66f4cf3fe9e8de2c28275205ab2358b020bb63aef219`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad903c2d978fb03c0a2e37a11ec79b83d141641bbdd3cb51d967c80754de03e`  
		Last Modified: Mon, 07 Oct 2024 20:21:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:27e1f93d1227d6341fe89aed3f796c5ff11fda59937cd60d8bd66aa924da2700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89987f1998492b30276df26c0f81d79265de5d89aeeecda184af3f8bc302a359`

```dockerfile
```

-	Layers:
	-	`sha256:af3a4e5105b5664b62b8d0b287fee74a6c86c9a5a8a7ba319f13e55e14352b4f`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 39.5 MB (39489286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef433a4d91a323051092d6b2a91ae987563627672e47d65a5552cd3dfd7bb7c`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 26.6 KB (26636 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241007`

```console
$ docker pull odoo@sha256:0777c7443e0912725b54be341ba84620576b65c15ab9090d3f07d59701cf2711
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241007` - linux; amd64

```console
$ docker pull odoo@sha256:b83832e102b2043d78cf912ce2221808ea7e7b460c837e8e9a2664847d6f1d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9604c9c21589224485598f2f790eccdecf4d6fbf47fd8da3aacf9bbececea66a`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e72ba30aed51d4d6c0c237e8bc3c101132e74ae632f1e4eb10942be7b727e`  
		Last Modified: Mon, 07 Oct 2024 20:01:10 GMT  
		Size: 233.8 MB (233763083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ff36f497e26e69c3be270acdbaae0980ae0af88f9656d7bf0e2c6f53284c8`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 2.4 MB (2405343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fcec3c52a5f23aabdf2f205a460aa9aa230c2ca4a7db3376000d5fbd04f3e`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 472.6 KB (472578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d202538c69c111b18a706c8d54ac975532ec4a020ac0fc9cda7bae244428d1`  
		Last Modified: Mon, 07 Oct 2024 20:01:12 GMT  
		Size: 331.7 MB (331705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e01b86b7e7d04baa375c1e89e199796d3e97de17489556bfad943e4fe78a88`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1c4d0f9821a9672084c08e1dd88de11d03eabaf149afc539f90eceaf93700`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08d0548d80024105b6bea0212d3253ea206a0a41b67a4c837f4b4087e2b034`  
		Last Modified: Mon, 07 Oct 2024 20:01:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:427f42d6e67c6173a2d070089f876df7235cb398147292c38a5fc9a0621f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39507564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe4dafb4e572ef28684d70f9b0d76d77d75aa6c2ac0f413ca540723736f89bc`

```dockerfile
```

-	Layers:
	-	`sha256:c917111b60355c59304c6b634bd422af02b6a246ad09f92fe8790fb204cfd9c1`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 39.5 MB (39480979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba4355a0c07c5d4dc95087814aa74abac7572bf737ea00d359740417e8c4304`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 26.6 KB (26585 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241007` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1f1f6da85e17cd21290ace7a21fa67ffa8370e52b20fcab790f41a051ec066c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592698494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec5d5720bf27403a52539c521f18b7695c1e1dfc3dba8bf92edd32bc3f0a08`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaeceaa088b15b07a8b1315a8325a1999e684223cf5e67a6c006b850ac8848e`  
		Last Modified: Mon, 07 Oct 2024 20:21:17 GMT  
		Size: 231.2 MB (231157442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593da4ee3c2b9cf8ba865cf0bcf3b58fc15624ee1dd7685e9f43bf546d2f81c9`  
		Last Modified: Mon, 07 Oct 2024 20:21:12 GMT  
		Size: 2.4 MB (2398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6951d7a9161762682e478a3b71e8822a05e2af33e60248f4913a92e195005a`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 472.7 KB (472696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005b6e94bcd93e08df067e60060f7c0b0f62d8e00f04aee488ef94768fca1f`  
		Last Modified: Mon, 07 Oct 2024 20:21:19 GMT  
		Size: 331.3 MB (331309334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58e977e68009ac44f0b7414f7a0e2ac195bfb9fe4303955acc67a33929ea10`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb71664b6198a3568af98278a1163b9b0168bf6a98b6fda02756af5334c6664`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231c2b8caa3c4c0257307b59bb859d93f314c023f13da4e2a8af313c89796f5`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ac6c81ec328e11241e07e75155f74e05cd7f870ebb6d5ec66a7ee099b24b7`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:c5b4fa83d6e0d8a7d6fa4cd9cc9286af10333eebcb69f0729655b79542bc35cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc0439fa6e521d8db24ce56ca24c90db5cdcfcd29f30dd5b2606af5f50a216`

```dockerfile
```

-	Layers:
	-	`sha256:2588008565e78b6555ca86898390d6089bc8dd0919071cb09b668f711f497421`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 39.5 MB (39487492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3abd04ebaea97afb033a95ea0f403614da68216ef25fe607a9479795bdd970`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 26.7 KB (26732 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241007` - linux; ppc64le

```console
$ docker pull odoo@sha256:c9c7849a8914fc213cf0cdad653fbc49e7b4a3046869cddcaee6148bbb4cac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614348604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fc0aaae4f6d58625a13efbb5a6261c5746b2770724140b65cce56e231c51e`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf22e9ecbdb17bae5948434399d20e985516ae45e11e72048320700f4c3002a`  
		Last Modified: Mon, 07 Oct 2024 20:21:39 GMT  
		Size: 243.3 MB (243294995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72daf6d3193cf48405ab14e7b21e55790dcda77c3e506d6ff2d916be2e81ab`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 2.7 MB (2708338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc1a4222c36d4c42eb25f5f2f0249bf9eabf1c589f406f87173d3e7293431`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 472.7 KB (472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db12d8f486a52172344f99e4ef0b2bfb16d9821239b125e83d7806488074c`  
		Last Modified: Mon, 07 Oct 2024 20:21:44 GMT  
		Size: 333.4 MB (333421873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded5e3af0dbff384e1805596730a23773fee78873edd6dfd2ab51bb230cbab3`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9878389a7cd65810b8a5288fa3df793a4061e0682ff3f2ed10dc7290e97dac1`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac2c5bcd93bd7c3ffd66f4cf3fe9e8de2c28275205ab2358b020bb63aef219`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad903c2d978fb03c0a2e37a11ec79b83d141641bbdd3cb51d967c80754de03e`  
		Last Modified: Mon, 07 Oct 2024 20:21:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:27e1f93d1227d6341fe89aed3f796c5ff11fda59937cd60d8bd66aa924da2700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89987f1998492b30276df26c0f81d79265de5d89aeeecda184af3f8bc302a359`

```dockerfile
```

-	Layers:
	-	`sha256:af3a4e5105b5664b62b8d0b287fee74a6c86c9a5a8a7ba319f13e55e14352b4f`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 39.5 MB (39489286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef433a4d91a323051092d6b2a91ae987563627672e47d65a5552cd3dfd7bb7c`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 26.6 KB (26636 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:50ae83e4da848f3dff8be5c719b78c23ce02e90ef9c037f79493515aaea756da
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
$ docker pull odoo@sha256:dc33a0e324152fac88f019ef6488e270f8efb5941544c2caf0a91f0b0e253e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650742227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1893d9b7dc87a74c3634ad7a3b7521a3ca13a284ed589df3dd152ddf69b09e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef62493bd7cd8708d8714b1a17dc494c3f2b8c300f95e872891af849ca31482e`  
		Last Modified: Mon, 07 Oct 2024 20:01:42 GMT  
		Size: 254.5 MB (254514364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9437595bc4804aed4e8fd06dec86558747e1fb71ba71b17a04e6031f135bb42`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 14.1 MB (14141430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871be8f3ab2a4502816bea4a5aa0ec0f214dec242840098e448a07ef2d0eec6b`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 472.4 KB (472392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f9d4339ef3b31307ff0b920fb877cd34ebcdc062b7734e8d9440d157bb661f`  
		Last Modified: Mon, 07 Oct 2024 20:01:44 GMT  
		Size: 351.9 MB (351861742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7bbd89133a264d56a0c509cc009e9c7fa7a17bb4996af22c2672aecf8a0a37`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c95907916929aaf045bbc3a30da2837fb35a91a53bfb91ff90929f9b94e9d02`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23316f33dc6ad5c720272ce183012e85998df24bd396260e1e6ce03f1ee2c228`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d823fc0e183f2fb265818c512ba4b1806e70913897cc3d15f77645be13be62d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e97ab119076fcc2c2136b5fec2339c529c0c20a5449cd1759abb285a25a53`

```dockerfile
```

-	Layers:
	-	`sha256:1d60beab70ece80e1df31b9b0729fb27d8010c01a3e8eacc0503d58c8036a498`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 55.4 MB (55430761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed05b4bbf33d5f18fc7accffdfa38d9315e73929f13b86e3c507101a9a845e2`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a89d602077a0c4f5df607c740c839b5bd714384e76eaf6dc2e5c58308e44260f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647137322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb170de1a8e512cacb8815d7276fd42761df4c628d9490e37cedd86374e23a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db3de7eed8eeed22e92a4727203ab6666c16750e82c6375418d387e113f1b0`  
		Last Modified: Mon, 07 Oct 2024 20:14:30 GMT  
		Size: 251.9 MB (251941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e993dcc208a281fc5c342866f2e7b303be7cf42a22c09be93746de2aaddd9`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 14.1 MB (14114724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b04103b45f1de8082792d0efecf02935cdd3225ddabcceb31ffebb9bcb13a63`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 472.3 KB (472347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3df9332ffed51560510cc5282fd2b3ed1a7056e3ed27ce04cb6576e3b88a3f`  
		Last Modified: Mon, 07 Oct 2024 20:14:31 GMT  
		Size: 351.7 MB (351721006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fbffc08b0244d0249515e4cf244815121a1d71b3f5a7aa345e438c54a8e301`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c912a98247a43f9222fdf4508bd089e7ef735988d74877c1bd51f4eaaed65b`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee63add1472e9bd30bb44952949d3fe96a07588540ee73c263bc0c4dd532d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6281a1d295037a444ff3e28358f680ab1ba02643bb55a8f0983e530314e240fa`  
		Last Modified: Mon, 07 Oct 2024 20:14:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:65336e367898ce018881bb502b3132ac4390649083c50d5af11afa74198fd532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edfbe35d1e2fd7ff220f0632bfd1cf33c32714e23afc7651aa133f6d283614`

```dockerfile
```

-	Layers:
	-	`sha256:eb6eb5629344a99ba67ac090f2bc79b11dd8d3404ecc3f7dd674ffde59b1eb81`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 55.4 MB (55438055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3923e3863deed556e7c5fbaa075f8ae6f765c7c06d3852f20536d8d06b74a1d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 27.0 KB (27044 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:55001f5d6370b7cab84078173e901415217dc3068dfce1a226e29f3042f4979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 MB (667105875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506098aea666dccba0a35b99e465c1917adcbe90c446049d1160e39f7aeb7838`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c9e9b81b1464f9ad35312bd065965ed63de78e86416c2391770d1efec1ec1`  
		Last Modified: Sat, 12 Oct 2024 00:16:53 GMT  
		Size: 265.1 MB (265138998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e75377f44be2bcb54e3e0a756d828b8c762ccc07bd274f1812fd27111b9a981`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 14.7 MB (14685435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8cd000d28bbe9f3558dd8cc6817fbc85e1d19b126b62cf09665d0fd664fca0`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 472.4 KB (472376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142532e49f259f299457b90111521c6d9260780edc0b3cf7899b625fe66eee0`  
		Last Modified: Sat, 12 Oct 2024 00:16:56 GMT  
		Size: 352.4 MB (352417212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23a1cf61a19ff6a8f1bb46c7659ceb76b24609b9d1da161c1e4426da70b4de`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101b300b1f160207d3e59d15a27ba9791de9a9faef238c00426067cf2a5a764`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e29d5c90eac89b62df78af3ae837e2eb7622244f35f9d1be39137d27e47df2`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc74b6b45c35604ce7380ae9bbf8953bcc6cc3a0c42d55057aadd79633e98671`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:52fe135e6f8ce01ef0036d1f9f7d6ccdcb043fd60c65493210dcafbef8f6db15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb517e03f27cc0772ae7976990b50abc34e712306e5151ef5416393f96b07ca4`

```dockerfile
```

-	Layers:
	-	`sha256:3dc3959a059203fd2f30920508b70a94ea44db77621e6248cf43b746e9685a2e`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 55.4 MB (55439543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0834a12088a6b68534377cdb96553bfcfc38eedd5dfc30c9b49287ff0c48a5b`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:50ae83e4da848f3dff8be5c719b78c23ce02e90ef9c037f79493515aaea756da
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
$ docker pull odoo@sha256:dc33a0e324152fac88f019ef6488e270f8efb5941544c2caf0a91f0b0e253e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650742227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1893d9b7dc87a74c3634ad7a3b7521a3ca13a284ed589df3dd152ddf69b09e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef62493bd7cd8708d8714b1a17dc494c3f2b8c300f95e872891af849ca31482e`  
		Last Modified: Mon, 07 Oct 2024 20:01:42 GMT  
		Size: 254.5 MB (254514364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9437595bc4804aed4e8fd06dec86558747e1fb71ba71b17a04e6031f135bb42`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 14.1 MB (14141430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871be8f3ab2a4502816bea4a5aa0ec0f214dec242840098e448a07ef2d0eec6b`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 472.4 KB (472392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f9d4339ef3b31307ff0b920fb877cd34ebcdc062b7734e8d9440d157bb661f`  
		Last Modified: Mon, 07 Oct 2024 20:01:44 GMT  
		Size: 351.9 MB (351861742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7bbd89133a264d56a0c509cc009e9c7fa7a17bb4996af22c2672aecf8a0a37`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c95907916929aaf045bbc3a30da2837fb35a91a53bfb91ff90929f9b94e9d02`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23316f33dc6ad5c720272ce183012e85998df24bd396260e1e6ce03f1ee2c228`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d823fc0e183f2fb265818c512ba4b1806e70913897cc3d15f77645be13be62d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e97ab119076fcc2c2136b5fec2339c529c0c20a5449cd1759abb285a25a53`

```dockerfile
```

-	Layers:
	-	`sha256:1d60beab70ece80e1df31b9b0729fb27d8010c01a3e8eacc0503d58c8036a498`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 55.4 MB (55430761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed05b4bbf33d5f18fc7accffdfa38d9315e73929f13b86e3c507101a9a845e2`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a89d602077a0c4f5df607c740c839b5bd714384e76eaf6dc2e5c58308e44260f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647137322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb170de1a8e512cacb8815d7276fd42761df4c628d9490e37cedd86374e23a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db3de7eed8eeed22e92a4727203ab6666c16750e82c6375418d387e113f1b0`  
		Last Modified: Mon, 07 Oct 2024 20:14:30 GMT  
		Size: 251.9 MB (251941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e993dcc208a281fc5c342866f2e7b303be7cf42a22c09be93746de2aaddd9`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 14.1 MB (14114724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b04103b45f1de8082792d0efecf02935cdd3225ddabcceb31ffebb9bcb13a63`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 472.3 KB (472347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3df9332ffed51560510cc5282fd2b3ed1a7056e3ed27ce04cb6576e3b88a3f`  
		Last Modified: Mon, 07 Oct 2024 20:14:31 GMT  
		Size: 351.7 MB (351721006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fbffc08b0244d0249515e4cf244815121a1d71b3f5a7aa345e438c54a8e301`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c912a98247a43f9222fdf4508bd089e7ef735988d74877c1bd51f4eaaed65b`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee63add1472e9bd30bb44952949d3fe96a07588540ee73c263bc0c4dd532d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6281a1d295037a444ff3e28358f680ab1ba02643bb55a8f0983e530314e240fa`  
		Last Modified: Mon, 07 Oct 2024 20:14:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:65336e367898ce018881bb502b3132ac4390649083c50d5af11afa74198fd532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edfbe35d1e2fd7ff220f0632bfd1cf33c32714e23afc7651aa133f6d283614`

```dockerfile
```

-	Layers:
	-	`sha256:eb6eb5629344a99ba67ac090f2bc79b11dd8d3404ecc3f7dd674ffde59b1eb81`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 55.4 MB (55438055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3923e3863deed556e7c5fbaa075f8ae6f765c7c06d3852f20536d8d06b74a1d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 27.0 KB (27044 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:55001f5d6370b7cab84078173e901415217dc3068dfce1a226e29f3042f4979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 MB (667105875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506098aea666dccba0a35b99e465c1917adcbe90c446049d1160e39f7aeb7838`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c9e9b81b1464f9ad35312bd065965ed63de78e86416c2391770d1efec1ec1`  
		Last Modified: Sat, 12 Oct 2024 00:16:53 GMT  
		Size: 265.1 MB (265138998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e75377f44be2bcb54e3e0a756d828b8c762ccc07bd274f1812fd27111b9a981`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 14.7 MB (14685435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8cd000d28bbe9f3558dd8cc6817fbc85e1d19b126b62cf09665d0fd664fca0`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 472.4 KB (472376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142532e49f259f299457b90111521c6d9260780edc0b3cf7899b625fe66eee0`  
		Last Modified: Sat, 12 Oct 2024 00:16:56 GMT  
		Size: 352.4 MB (352417212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23a1cf61a19ff6a8f1bb46c7659ceb76b24609b9d1da161c1e4426da70b4de`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101b300b1f160207d3e59d15a27ba9791de9a9faef238c00426067cf2a5a764`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e29d5c90eac89b62df78af3ae837e2eb7622244f35f9d1be39137d27e47df2`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc74b6b45c35604ce7380ae9bbf8953bcc6cc3a0c42d55057aadd79633e98671`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:52fe135e6f8ce01ef0036d1f9f7d6ccdcb043fd60c65493210dcafbef8f6db15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb517e03f27cc0772ae7976990b50abc34e712306e5151ef5416393f96b07ca4`

```dockerfile
```

-	Layers:
	-	`sha256:3dc3959a059203fd2f30920508b70a94ea44db77621e6248cf43b746e9685a2e`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 55.4 MB (55439543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0834a12088a6b68534377cdb96553bfcfc38eedd5dfc30c9b49287ff0c48a5b`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241007`

```console
$ docker pull odoo@sha256:50ae83e4da848f3dff8be5c719b78c23ce02e90ef9c037f79493515aaea756da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241007` - linux; amd64

```console
$ docker pull odoo@sha256:dc33a0e324152fac88f019ef6488e270f8efb5941544c2caf0a91f0b0e253e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650742227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1893d9b7dc87a74c3634ad7a3b7521a3ca13a284ed589df3dd152ddf69b09e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef62493bd7cd8708d8714b1a17dc494c3f2b8c300f95e872891af849ca31482e`  
		Last Modified: Mon, 07 Oct 2024 20:01:42 GMT  
		Size: 254.5 MB (254514364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9437595bc4804aed4e8fd06dec86558747e1fb71ba71b17a04e6031f135bb42`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 14.1 MB (14141430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871be8f3ab2a4502816bea4a5aa0ec0f214dec242840098e448a07ef2d0eec6b`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 472.4 KB (472392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f9d4339ef3b31307ff0b920fb877cd34ebcdc062b7734e8d9440d157bb661f`  
		Last Modified: Mon, 07 Oct 2024 20:01:44 GMT  
		Size: 351.9 MB (351861742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7bbd89133a264d56a0c509cc009e9c7fa7a17bb4996af22c2672aecf8a0a37`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c95907916929aaf045bbc3a30da2837fb35a91a53bfb91ff90929f9b94e9d02`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23316f33dc6ad5c720272ce183012e85998df24bd396260e1e6ce03f1ee2c228`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:d823fc0e183f2fb265818c512ba4b1806e70913897cc3d15f77645be13be62d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e97ab119076fcc2c2136b5fec2339c529c0c20a5449cd1759abb285a25a53`

```dockerfile
```

-	Layers:
	-	`sha256:1d60beab70ece80e1df31b9b0729fb27d8010c01a3e8eacc0503d58c8036a498`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 55.4 MB (55430761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed05b4bbf33d5f18fc7accffdfa38d9315e73929f13b86e3c507101a9a845e2`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241007` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a89d602077a0c4f5df607c740c839b5bd714384e76eaf6dc2e5c58308e44260f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647137322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb170de1a8e512cacb8815d7276fd42761df4c628d9490e37cedd86374e23a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db3de7eed8eeed22e92a4727203ab6666c16750e82c6375418d387e113f1b0`  
		Last Modified: Mon, 07 Oct 2024 20:14:30 GMT  
		Size: 251.9 MB (251941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e993dcc208a281fc5c342866f2e7b303be7cf42a22c09be93746de2aaddd9`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 14.1 MB (14114724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b04103b45f1de8082792d0efecf02935cdd3225ddabcceb31ffebb9bcb13a63`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 472.3 KB (472347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3df9332ffed51560510cc5282fd2b3ed1a7056e3ed27ce04cb6576e3b88a3f`  
		Last Modified: Mon, 07 Oct 2024 20:14:31 GMT  
		Size: 351.7 MB (351721006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fbffc08b0244d0249515e4cf244815121a1d71b3f5a7aa345e438c54a8e301`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c912a98247a43f9222fdf4508bd089e7ef735988d74877c1bd51f4eaaed65b`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee63add1472e9bd30bb44952949d3fe96a07588540ee73c263bc0c4dd532d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6281a1d295037a444ff3e28358f680ab1ba02643bb55a8f0983e530314e240fa`  
		Last Modified: Mon, 07 Oct 2024 20:14:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:65336e367898ce018881bb502b3132ac4390649083c50d5af11afa74198fd532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edfbe35d1e2fd7ff220f0632bfd1cf33c32714e23afc7651aa133f6d283614`

```dockerfile
```

-	Layers:
	-	`sha256:eb6eb5629344a99ba67ac090f2bc79b11dd8d3404ecc3f7dd674ffde59b1eb81`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 55.4 MB (55438055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3923e3863deed556e7c5fbaa075f8ae6f765c7c06d3852f20536d8d06b74a1d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 27.0 KB (27044 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241007` - linux; ppc64le

```console
$ docker pull odoo@sha256:55001f5d6370b7cab84078173e901415217dc3068dfce1a226e29f3042f4979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 MB (667105875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506098aea666dccba0a35b99e465c1917adcbe90c446049d1160e39f7aeb7838`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c9e9b81b1464f9ad35312bd065965ed63de78e86416c2391770d1efec1ec1`  
		Last Modified: Sat, 12 Oct 2024 00:16:53 GMT  
		Size: 265.1 MB (265138998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e75377f44be2bcb54e3e0a756d828b8c762ccc07bd274f1812fd27111b9a981`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 14.7 MB (14685435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8cd000d28bbe9f3558dd8cc6817fbc85e1d19b126b62cf09665d0fd664fca0`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 472.4 KB (472376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142532e49f259f299457b90111521c6d9260780edc0b3cf7899b625fe66eee0`  
		Last Modified: Sat, 12 Oct 2024 00:16:56 GMT  
		Size: 352.4 MB (352417212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23a1cf61a19ff6a8f1bb46c7659ceb76b24609b9d1da161c1e4426da70b4de`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101b300b1f160207d3e59d15a27ba9791de9a9faef238c00426067cf2a5a764`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e29d5c90eac89b62df78af3ae837e2eb7622244f35f9d1be39137d27e47df2`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc74b6b45c35604ce7380ae9bbf8953bcc6cc3a0c42d55057aadd79633e98671`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:52fe135e6f8ce01ef0036d1f9f7d6ccdcb043fd60c65493210dcafbef8f6db15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb517e03f27cc0772ae7976990b50abc34e712306e5151ef5416393f96b07ca4`

```dockerfile
```

-	Layers:
	-	`sha256:3dc3959a059203fd2f30920508b70a94ea44db77621e6248cf43b746e9685a2e`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 55.4 MB (55439543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0834a12088a6b68534377cdb96553bfcfc38eedd5dfc30c9b49287ff0c48a5b`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:50ae83e4da848f3dff8be5c719b78c23ce02e90ef9c037f79493515aaea756da
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
$ docker pull odoo@sha256:dc33a0e324152fac88f019ef6488e270f8efb5941544c2caf0a91f0b0e253e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650742227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1893d9b7dc87a74c3634ad7a3b7521a3ca13a284ed589df3dd152ddf69b09e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef62493bd7cd8708d8714b1a17dc494c3f2b8c300f95e872891af849ca31482e`  
		Last Modified: Mon, 07 Oct 2024 20:01:42 GMT  
		Size: 254.5 MB (254514364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9437595bc4804aed4e8fd06dec86558747e1fb71ba71b17a04e6031f135bb42`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 14.1 MB (14141430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871be8f3ab2a4502816bea4a5aa0ec0f214dec242840098e448a07ef2d0eec6b`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 472.4 KB (472392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f9d4339ef3b31307ff0b920fb877cd34ebcdc062b7734e8d9440d157bb661f`  
		Last Modified: Mon, 07 Oct 2024 20:01:44 GMT  
		Size: 351.9 MB (351861742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7bbd89133a264d56a0c509cc009e9c7fa7a17bb4996af22c2672aecf8a0a37`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c95907916929aaf045bbc3a30da2837fb35a91a53bfb91ff90929f9b94e9d02`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23316f33dc6ad5c720272ce183012e85998df24bd396260e1e6ce03f1ee2c228`  
		Last Modified: Mon, 07 Oct 2024 20:01:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d823fc0e183f2fb265818c512ba4b1806e70913897cc3d15f77645be13be62d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e97ab119076fcc2c2136b5fec2339c529c0c20a5449cd1759abb285a25a53`

```dockerfile
```

-	Layers:
	-	`sha256:1d60beab70ece80e1df31b9b0729fb27d8010c01a3e8eacc0503d58c8036a498`  
		Last Modified: Mon, 07 Oct 2024 20:01:39 GMT  
		Size: 55.4 MB (55430761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed05b4bbf33d5f18fc7accffdfa38d9315e73929f13b86e3c507101a9a845e2`  
		Last Modified: Mon, 07 Oct 2024 20:01:38 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a89d602077a0c4f5df607c740c839b5bd714384e76eaf6dc2e5c58308e44260f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647137322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb170de1a8e512cacb8815d7276fd42761df4c628d9490e37cedd86374e23a0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db3de7eed8eeed22e92a4727203ab6666c16750e82c6375418d387e113f1b0`  
		Last Modified: Mon, 07 Oct 2024 20:14:30 GMT  
		Size: 251.9 MB (251941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e993dcc208a281fc5c342866f2e7b303be7cf42a22c09be93746de2aaddd9`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 14.1 MB (14114724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b04103b45f1de8082792d0efecf02935cdd3225ddabcceb31ffebb9bcb13a63`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 472.3 KB (472347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3df9332ffed51560510cc5282fd2b3ed1a7056e3ed27ce04cb6576e3b88a3f`  
		Last Modified: Mon, 07 Oct 2024 20:14:31 GMT  
		Size: 351.7 MB (351721006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fbffc08b0244d0249515e4cf244815121a1d71b3f5a7aa345e438c54a8e301`  
		Last Modified: Mon, 07 Oct 2024 20:14:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c912a98247a43f9222fdf4508bd089e7ef735988d74877c1bd51f4eaaed65b`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ee63add1472e9bd30bb44952949d3fe96a07588540ee73c263bc0c4dd532d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6281a1d295037a444ff3e28358f680ab1ba02643bb55a8f0983e530314e240fa`  
		Last Modified: Mon, 07 Oct 2024 20:14:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:65336e367898ce018881bb502b3132ac4390649083c50d5af11afa74198fd532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edfbe35d1e2fd7ff220f0632bfd1cf33c32714e23afc7651aa133f6d283614`

```dockerfile
```

-	Layers:
	-	`sha256:eb6eb5629344a99ba67ac090f2bc79b11dd8d3404ecc3f7dd674ffde59b1eb81`  
		Last Modified: Mon, 07 Oct 2024 20:14:26 GMT  
		Size: 55.4 MB (55438055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3923e3863deed556e7c5fbaa075f8ae6f765c7c06d3852f20536d8d06b74a1d2`  
		Last Modified: Mon, 07 Oct 2024 20:14:24 GMT  
		Size: 27.0 KB (27044 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:55001f5d6370b7cab84078173e901415217dc3068dfce1a226e29f3042f4979c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 MB (667105875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506098aea666dccba0a35b99e465c1917adcbe90c446049d1160e39f7aeb7838`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e110547234fd795b1c6d90b50b5df43ec509107fdf663124acb5e3861c38ef9`  
		Last Modified: Thu, 10 Oct 2024 09:00:03 GMT  
		Size: 34.4 MB (34389412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c9e9b81b1464f9ad35312bd065965ed63de78e86416c2391770d1efec1ec1`  
		Last Modified: Sat, 12 Oct 2024 00:16:53 GMT  
		Size: 265.1 MB (265138998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e75377f44be2bcb54e3e0a756d828b8c762ccc07bd274f1812fd27111b9a981`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 14.7 MB (14685435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8cd000d28bbe9f3558dd8cc6817fbc85e1d19b126b62cf09665d0fd664fca0`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 472.4 KB (472376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142532e49f259f299457b90111521c6d9260780edc0b3cf7899b625fe66eee0`  
		Last Modified: Sat, 12 Oct 2024 00:16:56 GMT  
		Size: 352.4 MB (352417212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23a1cf61a19ff6a8f1bb46c7659ceb76b24609b9d1da161c1e4426da70b4de`  
		Last Modified: Sat, 12 Oct 2024 00:16:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101b300b1f160207d3e59d15a27ba9791de9a9faef238c00426067cf2a5a764`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e29d5c90eac89b62df78af3ae837e2eb7622244f35f9d1be39137d27e47df2`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc74b6b45c35604ce7380ae9bbf8953bcc6cc3a0c42d55057aadd79633e98671`  
		Last Modified: Sat, 12 Oct 2024 00:16:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:52fe135e6f8ce01ef0036d1f9f7d6ccdcb043fd60c65493210dcafbef8f6db15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb517e03f27cc0772ae7976990b50abc34e712306e5151ef5416393f96b07ca4`

```dockerfile
```

-	Layers:
	-	`sha256:3dc3959a059203fd2f30920508b70a94ea44db77621e6248cf43b746e9685a2e`  
		Last Modified: Sat, 12 Oct 2024 00:16:29 GMT  
		Size: 55.4 MB (55439543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0834a12088a6b68534377cdb96553bfcfc38eedd5dfc30c9b49287ff0c48a5b`  
		Last Modified: Sat, 12 Oct 2024 00:16:27 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json
