<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250123`](#odoo160-20250123)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250123`](#odoo170-20250123)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250123`](#odoo180-20250123)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:c9fb8e5262adfb1445cf3d82aef3767053e38a676f8f28b544c3156dfa024992
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:938985a38d162f18ccf333a4f31d1ef1d6ec032e9cf8fb3845cd40001e9adf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583908762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7cb9ff01259f6401a4bb6f369eccf64cd2b0f9e947f0cc690772083254c67f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1c0bb85c1bc3d821adfd6d2fedc340f0717cf60eda4feb9767f554e065e8d`  
		Last Modified: Thu, 23 Jan 2025 18:30:07 GMT  
		Size: 219.6 MB (219627931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0cf4ab28d55a0dc7f20f3813abb0ec98418ef880f2ea42fc849ea4eab4bfef`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 2.6 MB (2575883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ff889b356b4b6a4a0a8ea2799caa6ef387fad645229dbd95c2b962d8c4cb4`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 484.9 KB (484901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d48305d11285e6987a602a25e59fcc2b9998175fa2b57446aa6aac552fba9d`  
		Last Modified: Thu, 23 Jan 2025 18:30:09 GMT  
		Size: 331.0 MB (330964953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb8c330bda40b3c096334738b3c5e42949fb4716dd0b5f591c456edac7b7b0`  
		Last Modified: Thu, 23 Jan 2025 18:30:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4833e8a9e28828946c46a9c42a2b8db798069778ff3dae88b6fb631b74f67c7d`  
		Last Modified: Thu, 23 Jan 2025 18:30:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f159914bc5c170cbff54df97faa3edf2d281b8ce40224da1a7007114ce97474`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0195c99782a0de7b292ec853e541c465ec084bbcb7bf1bf35045f6c2aa4f135f`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:708cf24f0231906be056d1d26c2b34b4df5c8a74a46f4543fd3025cc674ddacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38854352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5232d6ffb201884182e62cf6c6e8a2cd48b3409d6bca3835cdcce6f426f3cf`

```dockerfile
```

-	Layers:
	-	`sha256:23a0547671afdad07eeb5869fa452a7b6934b285c710f896fe205f4436d4d18e`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 38.8 MB (38827635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b51eac73d414d9964b2fd2df6783c84fb297e060fca230bfd37e43eac54c647`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e36433e7445ca0ce9852f950451fd7547036dd7d16ddebc211ebfd2bd365c313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579367178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa62859cf53ae0c79f30acb5f7e1f9dcb78b3043ad0dabe38fbe48ae6e777aa4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fc77a1c24f6f39ad23a453460da8ab5168d76ef9175f84641eedccdba299b4`  
		Last Modified: Thu, 23 Jan 2025 19:05:40 GMT  
		Size: 330.6 MB (330628694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eed5534b55ad477dcad8fc67cc500bbb935246beb92574b4b5aa39e830b9d46`  
		Last Modified: Thu, 23 Jan 2025 19:05:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d38f2bc4c1e28043917edeb0d0eb0eaf3eaaa7c1570c7521d0bd31ada1fa95`  
		Last Modified: Thu, 23 Jan 2025 19:05:24 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920befec9590291b3082a908661e7cd88f079085cd47cbe87b099646c543c1a9`  
		Last Modified: Thu, 23 Jan 2025 19:05:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43423dc91c64bf212d60ba06db2e771af2f5614328200c7fc0a0c57de0545994`  
		Last Modified: Thu, 23 Jan 2025 19:05:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:0de4a689c01982fb9eb71a863df267dd4ee99ddaa46c2b27b1913d4f1f3fff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38860957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621d37f59048aedacc18b8309fd8029595f5eb5a961aba831c08f3dc589ed110`

```dockerfile
```

-	Layers:
	-	`sha256:1328c420e3adefe32e10ad88974c01c965eda5df5f779a408b978d7a3e2c3223`  
		Last Modified: Thu, 23 Jan 2025 19:05:22 GMT  
		Size: 38.8 MB (38834087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c6c541dce1188f65706b3c34ee9bef28ad8db7bb9974b8be5dfaed3b63d1d2`  
		Last Modified: Thu, 23 Jan 2025 19:05:26 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:c9fb8e5262adfb1445cf3d82aef3767053e38a676f8f28b544c3156dfa024992
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:938985a38d162f18ccf333a4f31d1ef1d6ec032e9cf8fb3845cd40001e9adf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583908762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7cb9ff01259f6401a4bb6f369eccf64cd2b0f9e947f0cc690772083254c67f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1c0bb85c1bc3d821adfd6d2fedc340f0717cf60eda4feb9767f554e065e8d`  
		Last Modified: Thu, 23 Jan 2025 18:30:07 GMT  
		Size: 219.6 MB (219627931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0cf4ab28d55a0dc7f20f3813abb0ec98418ef880f2ea42fc849ea4eab4bfef`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 2.6 MB (2575883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ff889b356b4b6a4a0a8ea2799caa6ef387fad645229dbd95c2b962d8c4cb4`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 484.9 KB (484901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d48305d11285e6987a602a25e59fcc2b9998175fa2b57446aa6aac552fba9d`  
		Last Modified: Thu, 23 Jan 2025 18:30:09 GMT  
		Size: 331.0 MB (330964953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb8c330bda40b3c096334738b3c5e42949fb4716dd0b5f591c456edac7b7b0`  
		Last Modified: Thu, 23 Jan 2025 18:30:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4833e8a9e28828946c46a9c42a2b8db798069778ff3dae88b6fb631b74f67c7d`  
		Last Modified: Thu, 23 Jan 2025 18:30:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f159914bc5c170cbff54df97faa3edf2d281b8ce40224da1a7007114ce97474`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0195c99782a0de7b292ec853e541c465ec084bbcb7bf1bf35045f6c2aa4f135f`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:708cf24f0231906be056d1d26c2b34b4df5c8a74a46f4543fd3025cc674ddacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38854352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5232d6ffb201884182e62cf6c6e8a2cd48b3409d6bca3835cdcce6f426f3cf`

```dockerfile
```

-	Layers:
	-	`sha256:23a0547671afdad07eeb5869fa452a7b6934b285c710f896fe205f4436d4d18e`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 38.8 MB (38827635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b51eac73d414d9964b2fd2df6783c84fb297e060fca230bfd37e43eac54c647`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e36433e7445ca0ce9852f950451fd7547036dd7d16ddebc211ebfd2bd365c313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579367178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa62859cf53ae0c79f30acb5f7e1f9dcb78b3043ad0dabe38fbe48ae6e777aa4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fc77a1c24f6f39ad23a453460da8ab5168d76ef9175f84641eedccdba299b4`  
		Last Modified: Thu, 23 Jan 2025 19:05:40 GMT  
		Size: 330.6 MB (330628694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eed5534b55ad477dcad8fc67cc500bbb935246beb92574b4b5aa39e830b9d46`  
		Last Modified: Thu, 23 Jan 2025 19:05:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d38f2bc4c1e28043917edeb0d0eb0eaf3eaaa7c1570c7521d0bd31ada1fa95`  
		Last Modified: Thu, 23 Jan 2025 19:05:24 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920befec9590291b3082a908661e7cd88f079085cd47cbe87b099646c543c1a9`  
		Last Modified: Thu, 23 Jan 2025 19:05:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43423dc91c64bf212d60ba06db2e771af2f5614328200c7fc0a0c57de0545994`  
		Last Modified: Thu, 23 Jan 2025 19:05:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0de4a689c01982fb9eb71a863df267dd4ee99ddaa46c2b27b1913d4f1f3fff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38860957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621d37f59048aedacc18b8309fd8029595f5eb5a961aba831c08f3dc589ed110`

```dockerfile
```

-	Layers:
	-	`sha256:1328c420e3adefe32e10ad88974c01c965eda5df5f779a408b978d7a3e2c3223`  
		Last Modified: Thu, 23 Jan 2025 19:05:22 GMT  
		Size: 38.8 MB (38834087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c6c541dce1188f65706b3c34ee9bef28ad8db7bb9974b8be5dfaed3b63d1d2`  
		Last Modified: Thu, 23 Jan 2025 19:05:26 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250123`

```console
$ docker pull odoo@sha256:c9fb8e5262adfb1445cf3d82aef3767053e38a676f8f28b544c3156dfa024992
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250123` - linux; amd64

```console
$ docker pull odoo@sha256:938985a38d162f18ccf333a4f31d1ef1d6ec032e9cf8fb3845cd40001e9adf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583908762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7cb9ff01259f6401a4bb6f369eccf64cd2b0f9e947f0cc690772083254c67f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1c0bb85c1bc3d821adfd6d2fedc340f0717cf60eda4feb9767f554e065e8d`  
		Last Modified: Thu, 23 Jan 2025 18:30:07 GMT  
		Size: 219.6 MB (219627931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0cf4ab28d55a0dc7f20f3813abb0ec98418ef880f2ea42fc849ea4eab4bfef`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 2.6 MB (2575883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ff889b356b4b6a4a0a8ea2799caa6ef387fad645229dbd95c2b962d8c4cb4`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 484.9 KB (484901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d48305d11285e6987a602a25e59fcc2b9998175fa2b57446aa6aac552fba9d`  
		Last Modified: Thu, 23 Jan 2025 18:30:09 GMT  
		Size: 331.0 MB (330964953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb8c330bda40b3c096334738b3c5e42949fb4716dd0b5f591c456edac7b7b0`  
		Last Modified: Thu, 23 Jan 2025 18:30:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4833e8a9e28828946c46a9c42a2b8db798069778ff3dae88b6fb631b74f67c7d`  
		Last Modified: Thu, 23 Jan 2025 18:30:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f159914bc5c170cbff54df97faa3edf2d281b8ce40224da1a7007114ce97474`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0195c99782a0de7b292ec853e541c465ec084bbcb7bf1bf35045f6c2aa4f135f`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:708cf24f0231906be056d1d26c2b34b4df5c8a74a46f4543fd3025cc674ddacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38854352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5232d6ffb201884182e62cf6c6e8a2cd48b3409d6bca3835cdcce6f426f3cf`

```dockerfile
```

-	Layers:
	-	`sha256:23a0547671afdad07eeb5869fa452a7b6934b285c710f896fe205f4436d4d18e`  
		Last Modified: Thu, 23 Jan 2025 18:30:05 GMT  
		Size: 38.8 MB (38827635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b51eac73d414d9964b2fd2df6783c84fb297e060fca230bfd37e43eac54c647`  
		Last Modified: Thu, 23 Jan 2025 18:30:03 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250123` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e36433e7445ca0ce9852f950451fd7547036dd7d16ddebc211ebfd2bd365c313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579367178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa62859cf53ae0c79f30acb5f7e1f9dcb78b3043ad0dabe38fbe48ae6e777aa4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=62823d0d042f2bfba7d4114db2c9272d48c136c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fc77a1c24f6f39ad23a453460da8ab5168d76ef9175f84641eedccdba299b4`  
		Last Modified: Thu, 23 Jan 2025 19:05:40 GMT  
		Size: 330.6 MB (330628694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eed5534b55ad477dcad8fc67cc500bbb935246beb92574b4b5aa39e830b9d46`  
		Last Modified: Thu, 23 Jan 2025 19:05:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d38f2bc4c1e28043917edeb0d0eb0eaf3eaaa7c1570c7521d0bd31ada1fa95`  
		Last Modified: Thu, 23 Jan 2025 19:05:24 GMT  
		Size: 552.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920befec9590291b3082a908661e7cd88f079085cd47cbe87b099646c543c1a9`  
		Last Modified: Thu, 23 Jan 2025 19:05:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43423dc91c64bf212d60ba06db2e771af2f5614328200c7fc0a0c57de0545994`  
		Last Modified: Thu, 23 Jan 2025 19:05:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:0de4a689c01982fb9eb71a863df267dd4ee99ddaa46c2b27b1913d4f1f3fff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38860957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621d37f59048aedacc18b8309fd8029595f5eb5a961aba831c08f3dc589ed110`

```dockerfile
```

-	Layers:
	-	`sha256:1328c420e3adefe32e10ad88974c01c965eda5df5f779a408b978d7a3e2c3223`  
		Last Modified: Thu, 23 Jan 2025 19:05:22 GMT  
		Size: 38.8 MB (38834087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c6c541dce1188f65706b3c34ee9bef28ad8db7bb9974b8be5dfaed3b63d1d2`  
		Last Modified: Thu, 23 Jan 2025 19:05:26 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:7216e481367d104cb1e5755b37fac92e13b1c8a5b1c09ec3bf3ec167e61a0354
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
$ docker pull odoo@sha256:1c52686c997e6261ec340fea781485be9cf6daba35de3f5a22ccdc5d4e8b8289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599449541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373ac9b15b592518d599c297f0df0f7c9cd7c074a5da97f9fb35552739627c4`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec1d8c0a804563286aca3b38ee8e6df3c1482b20ebd94dde58b9b4f5d9d4b07`  
		Last Modified: Thu, 23 Jan 2025 18:29:56 GMT  
		Size: 233.8 MB (233775076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6c72db725e633a420eb09eb2430060b1cf010670b65556d9f528867ce1258`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 2.5 MB (2493438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6c967b2ccf41978f7c5d833ee49740d97a33ef014796b9675a5f91e10c1080`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 485.9 KB (485928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607049532b07d3f2b1daba94044f428290357172257365b23716026cd9a0b297`  
		Last Modified: Thu, 23 Jan 2025 18:29:57 GMT  
		Size: 333.2 MB (333156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2c4cdd7c5c13c54b319690222ce4dcd5055478141b7ebb7e1d28760d0619f`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfb1d6f8e8a4198af1244b4cfa2f477d2717928590e29d4e27b6040a95c2fb`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b344fb2f75cbddc7c357d3278b83d5f9d03157a573190494cd664beace5a77f7`  
		Last Modified: Thu, 23 Jan 2025 18:29:55 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd18708ebe7d4525ef1af3c8174d5d0a45bf702f713b45b66a4aec0b8d9493`  
		Last Modified: Thu, 23 Jan 2025 18:29:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:da6ee9941942f3fb3b6e2f94c15f8e4f54ce2d8f7275f72851ed73561b9ebe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39707477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d59e0664b35b62e18b98f323a6c84c029db36087644b1691204278c27031001`

```dockerfile
```

-	Layers:
	-	`sha256:b196c623e139485c60311c01ac28aff187bf973be1b9920b64696eccd61dbc72`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 39.7 MB (39680642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121fe8c77a180a6d2996c64e1759bed82c2f452b3c6760b95cd63cfa03274512`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:025fe6c60bef25416e6d49921f27aebe4c3e420d5d344e7b2d21876547706046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.2 MB (594246157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dce53dd0c39812060b7bc9b5ae1052091909a8449b5f6b31e68c497dfb20467`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47509ae080d81976ff421f567111d7b1740f900bddc537b8ba87fc0747e30a`  
		Last Modified: Thu, 23 Jan 2025 19:02:22 GMT  
		Size: 332.8 MB (332769283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af393f9b44ebcb7b2cbd5e0fc99ecbb1167d5dec7e3560193371b56f7bca4869`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401f9094f20623a61ed72721a00d75f1b91fa0e86eba2d44f910c45ce64b6d`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059f7ee7ab40eb04c4958432811f4f22d23980d322a8608e008385b69ad3c40`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46c6188ad9885d093dfdd94c7c4d14c3449274055ba3b35d703b25ecb86cc6e`  
		Last Modified: Thu, 23 Jan 2025 19:02:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:35f19c4e642f3e34877b486853c2842f89c6a115896d48d1c36240c96c45b81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39714140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23caf5c4b77800a4aee941aff44ba2ead4a2cfc93c79a4f522fad153b89c7b72`

```dockerfile
```

-	Layers:
	-	`sha256:e6e3a264cb7699301c15488255cc877885259110a3c1825ddab0d0fb837a2411`  
		Last Modified: Thu, 23 Jan 2025 19:02:16 GMT  
		Size: 39.7 MB (39687153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19eb53bc48dbdb3c6548c1df01e2656454cb118d979210e349a0421711196471`  
		Last Modified: Thu, 23 Jan 2025 19:02:14 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:48efe7619e464789588570b13f117e904b7926e031a3d5dfc1d2f2b5e13c29e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615918459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7919caa0ddddd9e869a1bdfd4c069d8c1a771e4d1780450a0bb9c50346a0f9ef`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7a177c4d89737bce29237db846a511dc0d97e4f40f85595674cf8ac3ccfb5`  
		Last Modified: Thu, 23 Jan 2025 18:39:20 GMT  
		Size: 334.9 MB (334881481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c675d430baa5ce08af67011869bbb09e071b25ea3ec5b673acc549f285fdd`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb82735a287fbe5d85302dcd1af7c0c2c516e1b760d4b13691baae4cfc87c5`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5883d7616672912ae723edbceb901df6595e1c12d6a86d1e5307e8fce45e03e6`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66774c6d4093ddd83a9895f41c6569cd1774a0615732197176c19d57eb68db70`  
		Last Modified: Thu, 23 Jan 2025 18:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:3a953d7842e3fee3c563410505c47ecdbc45f6571d68fd6e0e0cba3d9dad8860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e257ea48c4e2a41087b3bfd395d12c82730b8ee2a664c7e777dbf358d24d6f4`

```dockerfile
```

-	Layers:
	-	`sha256:60496336541720721b57b5227868ce20939c1303f7d9fd932c629b25439d1b85`  
		Last Modified: Thu, 23 Jan 2025 18:39:10 GMT  
		Size: 39.7 MB (39688969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de70e13e48233548cf4cb7a3a8b30eda02a8bf956be16f5bc60111396039c75`  
		Last Modified: Thu, 23 Jan 2025 18:39:07 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7216e481367d104cb1e5755b37fac92e13b1c8a5b1c09ec3bf3ec167e61a0354
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
$ docker pull odoo@sha256:1c52686c997e6261ec340fea781485be9cf6daba35de3f5a22ccdc5d4e8b8289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599449541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373ac9b15b592518d599c297f0df0f7c9cd7c074a5da97f9fb35552739627c4`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec1d8c0a804563286aca3b38ee8e6df3c1482b20ebd94dde58b9b4f5d9d4b07`  
		Last Modified: Thu, 23 Jan 2025 18:29:56 GMT  
		Size: 233.8 MB (233775076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6c72db725e633a420eb09eb2430060b1cf010670b65556d9f528867ce1258`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 2.5 MB (2493438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6c967b2ccf41978f7c5d833ee49740d97a33ef014796b9675a5f91e10c1080`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 485.9 KB (485928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607049532b07d3f2b1daba94044f428290357172257365b23716026cd9a0b297`  
		Last Modified: Thu, 23 Jan 2025 18:29:57 GMT  
		Size: 333.2 MB (333156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2c4cdd7c5c13c54b319690222ce4dcd5055478141b7ebb7e1d28760d0619f`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfb1d6f8e8a4198af1244b4cfa2f477d2717928590e29d4e27b6040a95c2fb`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b344fb2f75cbddc7c357d3278b83d5f9d03157a573190494cd664beace5a77f7`  
		Last Modified: Thu, 23 Jan 2025 18:29:55 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd18708ebe7d4525ef1af3c8174d5d0a45bf702f713b45b66a4aec0b8d9493`  
		Last Modified: Thu, 23 Jan 2025 18:29:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:da6ee9941942f3fb3b6e2f94c15f8e4f54ce2d8f7275f72851ed73561b9ebe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39707477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d59e0664b35b62e18b98f323a6c84c029db36087644b1691204278c27031001`

```dockerfile
```

-	Layers:
	-	`sha256:b196c623e139485c60311c01ac28aff187bf973be1b9920b64696eccd61dbc72`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 39.7 MB (39680642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121fe8c77a180a6d2996c64e1759bed82c2f452b3c6760b95cd63cfa03274512`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:025fe6c60bef25416e6d49921f27aebe4c3e420d5d344e7b2d21876547706046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.2 MB (594246157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dce53dd0c39812060b7bc9b5ae1052091909a8449b5f6b31e68c497dfb20467`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47509ae080d81976ff421f567111d7b1740f900bddc537b8ba87fc0747e30a`  
		Last Modified: Thu, 23 Jan 2025 19:02:22 GMT  
		Size: 332.8 MB (332769283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af393f9b44ebcb7b2cbd5e0fc99ecbb1167d5dec7e3560193371b56f7bca4869`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401f9094f20623a61ed72721a00d75f1b91fa0e86eba2d44f910c45ce64b6d`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059f7ee7ab40eb04c4958432811f4f22d23980d322a8608e008385b69ad3c40`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46c6188ad9885d093dfdd94c7c4d14c3449274055ba3b35d703b25ecb86cc6e`  
		Last Modified: Thu, 23 Jan 2025 19:02:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:35f19c4e642f3e34877b486853c2842f89c6a115896d48d1c36240c96c45b81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39714140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23caf5c4b77800a4aee941aff44ba2ead4a2cfc93c79a4f522fad153b89c7b72`

```dockerfile
```

-	Layers:
	-	`sha256:e6e3a264cb7699301c15488255cc877885259110a3c1825ddab0d0fb837a2411`  
		Last Modified: Thu, 23 Jan 2025 19:02:16 GMT  
		Size: 39.7 MB (39687153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19eb53bc48dbdb3c6548c1df01e2656454cb118d979210e349a0421711196471`  
		Last Modified: Thu, 23 Jan 2025 19:02:14 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:48efe7619e464789588570b13f117e904b7926e031a3d5dfc1d2f2b5e13c29e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615918459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7919caa0ddddd9e869a1bdfd4c069d8c1a771e4d1780450a0bb9c50346a0f9ef`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7a177c4d89737bce29237db846a511dc0d97e4f40f85595674cf8ac3ccfb5`  
		Last Modified: Thu, 23 Jan 2025 18:39:20 GMT  
		Size: 334.9 MB (334881481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c675d430baa5ce08af67011869bbb09e071b25ea3ec5b673acc549f285fdd`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb82735a287fbe5d85302dcd1af7c0c2c516e1b760d4b13691baae4cfc87c5`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5883d7616672912ae723edbceb901df6595e1c12d6a86d1e5307e8fce45e03e6`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66774c6d4093ddd83a9895f41c6569cd1774a0615732197176c19d57eb68db70`  
		Last Modified: Thu, 23 Jan 2025 18:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3a953d7842e3fee3c563410505c47ecdbc45f6571d68fd6e0e0cba3d9dad8860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e257ea48c4e2a41087b3bfd395d12c82730b8ee2a664c7e777dbf358d24d6f4`

```dockerfile
```

-	Layers:
	-	`sha256:60496336541720721b57b5227868ce20939c1303f7d9fd932c629b25439d1b85`  
		Last Modified: Thu, 23 Jan 2025 18:39:10 GMT  
		Size: 39.7 MB (39688969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de70e13e48233548cf4cb7a3a8b30eda02a8bf956be16f5bc60111396039c75`  
		Last Modified: Thu, 23 Jan 2025 18:39:07 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250123`

```console
$ docker pull odoo@sha256:7216e481367d104cb1e5755b37fac92e13b1c8a5b1c09ec3bf3ec167e61a0354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250123` - linux; amd64

```console
$ docker pull odoo@sha256:1c52686c997e6261ec340fea781485be9cf6daba35de3f5a22ccdc5d4e8b8289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599449541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373ac9b15b592518d599c297f0df0f7c9cd7c074a5da97f9fb35552739627c4`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec1d8c0a804563286aca3b38ee8e6df3c1482b20ebd94dde58b9b4f5d9d4b07`  
		Last Modified: Thu, 23 Jan 2025 18:29:56 GMT  
		Size: 233.8 MB (233775076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6c72db725e633a420eb09eb2430060b1cf010670b65556d9f528867ce1258`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 2.5 MB (2493438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6c967b2ccf41978f7c5d833ee49740d97a33ef014796b9675a5f91e10c1080`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 485.9 KB (485928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607049532b07d3f2b1daba94044f428290357172257365b23716026cd9a0b297`  
		Last Modified: Thu, 23 Jan 2025 18:29:57 GMT  
		Size: 333.2 MB (333156970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2c4cdd7c5c13c54b319690222ce4dcd5055478141b7ebb7e1d28760d0619f`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfb1d6f8e8a4198af1244b4cfa2f477d2717928590e29d4e27b6040a95c2fb`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b344fb2f75cbddc7c357d3278b83d5f9d03157a573190494cd664beace5a77f7`  
		Last Modified: Thu, 23 Jan 2025 18:29:55 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd18708ebe7d4525ef1af3c8174d5d0a45bf702f713b45b66a4aec0b8d9493`  
		Last Modified: Thu, 23 Jan 2025 18:29:55 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:da6ee9941942f3fb3b6e2f94c15f8e4f54ce2d8f7275f72851ed73561b9ebe52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39707477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d59e0664b35b62e18b98f323a6c84c029db36087644b1691204278c27031001`

```dockerfile
```

-	Layers:
	-	`sha256:b196c623e139485c60311c01ac28aff187bf973be1b9920b64696eccd61dbc72`  
		Last Modified: Thu, 23 Jan 2025 18:29:54 GMT  
		Size: 39.7 MB (39680642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121fe8c77a180a6d2996c64e1759bed82c2f452b3c6760b95cd63cfa03274512`  
		Last Modified: Thu, 23 Jan 2025 18:29:53 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250123` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:025fe6c60bef25416e6d49921f27aebe4c3e420d5d344e7b2d21876547706046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.2 MB (594246157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dce53dd0c39812060b7bc9b5ae1052091909a8449b5f6b31e68c497dfb20467`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47509ae080d81976ff421f567111d7b1740f900bddc537b8ba87fc0747e30a`  
		Last Modified: Thu, 23 Jan 2025 19:02:22 GMT  
		Size: 332.8 MB (332769283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af393f9b44ebcb7b2cbd5e0fc99ecbb1167d5dec7e3560193371b56f7bca4869`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3401f9094f20623a61ed72721a00d75f1b91fa0e86eba2d44f910c45ce64b6d`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059f7ee7ab40eb04c4958432811f4f22d23980d322a8608e008385b69ad3c40`  
		Last Modified: Thu, 23 Jan 2025 19:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46c6188ad9885d093dfdd94c7c4d14c3449274055ba3b35d703b25ecb86cc6e`  
		Last Modified: Thu, 23 Jan 2025 19:02:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:35f19c4e642f3e34877b486853c2842f89c6a115896d48d1c36240c96c45b81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39714140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23caf5c4b77800a4aee941aff44ba2ead4a2cfc93c79a4f522fad153b89c7b72`

```dockerfile
```

-	Layers:
	-	`sha256:e6e3a264cb7699301c15488255cc877885259110a3c1825ddab0d0fb837a2411`  
		Last Modified: Thu, 23 Jan 2025 19:02:16 GMT  
		Size: 39.7 MB (39687153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19eb53bc48dbdb3c6548c1df01e2656454cb118d979210e349a0421711196471`  
		Last Modified: Thu, 23 Jan 2025 19:02:14 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250123` - linux; ppc64le

```console
$ docker pull odoo@sha256:48efe7619e464789588570b13f117e904b7926e031a3d5dfc1d2f2b5e13c29e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615918459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7919caa0ddddd9e869a1bdfd4c069d8c1a771e4d1780450a0bb9c50346a0f9ef`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=17.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=63c4ed2e00c754ff5fecfc87a4c3fd8c518d56e7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7a177c4d89737bce29237db846a511dc0d97e4f40f85595674cf8ac3ccfb5`  
		Last Modified: Thu, 23 Jan 2025 18:39:20 GMT  
		Size: 334.9 MB (334881481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c675d430baa5ce08af67011869bbb09e071b25ea3ec5b673acc549f285fdd`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb82735a287fbe5d85302dcd1af7c0c2c516e1b760d4b13691baae4cfc87c5`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5883d7616672912ae723edbceb901df6595e1c12d6a86d1e5307e8fce45e03e6`  
		Last Modified: Thu, 23 Jan 2025 18:39:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66774c6d4093ddd83a9895f41c6569cd1774a0615732197176c19d57eb68db70`  
		Last Modified: Thu, 23 Jan 2025 18:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:3a953d7842e3fee3c563410505c47ecdbc45f6571d68fd6e0e0cba3d9dad8860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39715859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e257ea48c4e2a41087b3bfd395d12c82730b8ee2a664c7e777dbf358d24d6f4`

```dockerfile
```

-	Layers:
	-	`sha256:60496336541720721b57b5227868ce20939c1303f7d9fd932c629b25439d1b85`  
		Last Modified: Thu, 23 Jan 2025 18:39:10 GMT  
		Size: 39.7 MB (39688969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8de70e13e48233548cf4cb7a3a8b30eda02a8bf956be16f5bc60111396039c75`  
		Last Modified: Thu, 23 Jan 2025 18:39:07 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:cd226c03d7c11b873547f44ded6eb4c93cfca65fbe387f5e0a910aa745c6c05d
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
$ docker pull odoo@sha256:8d6511d94ad00483460f285a2a48f62ef8e6885e2d5d0ba6be9bfeb16ef81faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.9 MB (665909748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7dd48cc0180cc3d1f3d5bf76bd1e16d5a05e99cc437980e5caff6073fcb13`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7654019d4b20b10437539b1cfa692f0a21825e3ddfdfe640e93b7332ef2510`  
		Last Modified: Thu, 23 Jan 2025 18:30:53 GMT  
		Size: 254.5 MB (254519197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b583fc9c4e7b0a5fedb7332d3fd1a21b9478109b2bb6d0a95b5170fef8a16df`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 14.2 MB (14231248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b491b2a2e1cc29d3a94332e54fa44ef1cc2544383173a2ded502bbebcf13c`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 485.7 KB (485712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c1cdbfdd48b9f41d176b9cfb1c064839cd40a1a55c23174d8d95f5fd15d93b`  
		Last Modified: Thu, 23 Jan 2025 18:30:55 GMT  
		Size: 366.9 MB (366919182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf432aef498eb8f874c1ff9e73c375cbb9626579f1cc126a165cb61a267979d9`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fe67542d159b5a3f795f90ca42909f6b68e30ecacb594619318e299281a502`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0de367115fdf665b827922b87273aae2d2f6ad8df9473cd7526edb8d968fe`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe9b5c20ec0224b0e33d7297a93826afa7f7a3562fe5dede80baaf3e35437f8`  
		Last Modified: Thu, 23 Jan 2025 18:30:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:f3939086ea98217dbf92c98006d1fe3316ffe3a61ab59fcc631a901d0433d4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58415977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e950f51e96d53246f97daa7cf4ba58773ce41e900525593cb4d7b58a0f94f750`

```dockerfile
```

-	Layers:
	-	`sha256:bf927b21d84000b3d588663ae3cb54395f074137ef4fc0c1b7f5f1d78fb2af10`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 58.4 MB (58388841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc6fe822bf8e86376a0743ca4efd77b6870e6a45763f8cc9e09acf393028b08`  
		Last Modified: Thu, 23 Jan 2025 18:30:49 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29244f05b35308e6b0dcc11a74f394b80097a4b72c828beadcd783dcdcf11194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 MB (662290322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cc35601dc86e58a2140f16f592500147d92a91abe6e55a765712633f3ff6df`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db86ce3dd26b502fae6356f1be60d20f60bca1257b178d439b027dd3d1551e8`  
		Last Modified: Thu, 23 Jan 2025 19:12:22 GMT  
		Size: 366.8 MB (366762952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc2a74806b232f6c02e473854dd4b67b0f3df220feb3ec6159234556ba688e`  
		Last Modified: Thu, 23 Jan 2025 19:12:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e19f402f1113207312deb900ba4cd2d014644efb8c400558900d0283c5b090`  
		Last Modified: Thu, 23 Jan 2025 19:12:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa11488a63d584ccad9cf0cf01eeecf6374787cd959fb75d0d5e0c9f8ab312`  
		Last Modified: Thu, 23 Jan 2025 19:12:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181922030ccc2bec60dd5227083af70ef9853bb81db3ea8a848a6501baaa8a8`  
		Last Modified: Thu, 23 Jan 2025 19:12:18 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:9da8fbd404ec6c26419b2701a384c9cabc9fe5c74903c5e93119c6bc8c6aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58423432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee151e4feb6ba7bca0095c696c64e8a86f5a5b47000f65526c4b70c9740e3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:0c05270638dd0a3ea03ca8574027da77a052eb512f3ca81c0100daf17ce2db81`  
		Last Modified: Thu, 23 Jan 2025 19:12:15 GMT  
		Size: 58.4 MB (58396132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b28159976b0b036069f5e558914a334f2497bd1993291ccaa87ccfa029d5723`  
		Last Modified: Thu, 23 Jan 2025 19:12:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:f7dec6e90a76beb82e54e21b2ee5e8c41cce7f3d09596dcad1b1216d5e8d4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.2 MB (682198668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c543545e2f6ce3c4072185d911b2e440dc50210525a043333c9fdd8b2bee9f`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca86fa2495de7cdd13fac0b048f953ea403243242c7c29b21193f3f3e6cbd72`  
		Last Modified: Thu, 23 Jan 2025 18:33:51 GMT  
		Size: 367.5 MB (367455965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c6daff8c8e8af849f8d909e99e4734669fa1a1b780d82f78599281064bb3f`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6883ffaa3307bb091332b5f1e9a37e18d13feb0eb673a4509d8403ad4cdaddb`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334934d145a22292a420dd908b841d2fae1d68d7fb65a7f5087d73912abc67fc`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831a255fc926f8c449d4e06ca65fdedbe2034d7db0e1a61b9194bf68090a9e6`  
		Last Modified: Thu, 23 Jan 2025 18:33:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:34d060256482cc498352e732aff4b950df314764b091fbb3dfb682a66582a9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58424202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3226f58de0c39291f7bea03d567d75a377e916614b9055141e5ed92846edaa`

```dockerfile
```

-	Layers:
	-	`sha256:16dbc78fb2a481f1dc2f5b22d98c44bb9fa7a4909357bfdbec935e15fda8295b`  
		Last Modified: Thu, 23 Jan 2025 18:33:28 GMT  
		Size: 58.4 MB (58397004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ad14f054bba01aed51ca9bc58c55721c30d9644fc87fbb87de9494a1c0172b`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:cd226c03d7c11b873547f44ded6eb4c93cfca65fbe387f5e0a910aa745c6c05d
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
$ docker pull odoo@sha256:8d6511d94ad00483460f285a2a48f62ef8e6885e2d5d0ba6be9bfeb16ef81faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.9 MB (665909748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7dd48cc0180cc3d1f3d5bf76bd1e16d5a05e99cc437980e5caff6073fcb13`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7654019d4b20b10437539b1cfa692f0a21825e3ddfdfe640e93b7332ef2510`  
		Last Modified: Thu, 23 Jan 2025 18:30:53 GMT  
		Size: 254.5 MB (254519197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b583fc9c4e7b0a5fedb7332d3fd1a21b9478109b2bb6d0a95b5170fef8a16df`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 14.2 MB (14231248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b491b2a2e1cc29d3a94332e54fa44ef1cc2544383173a2ded502bbebcf13c`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 485.7 KB (485712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c1cdbfdd48b9f41d176b9cfb1c064839cd40a1a55c23174d8d95f5fd15d93b`  
		Last Modified: Thu, 23 Jan 2025 18:30:55 GMT  
		Size: 366.9 MB (366919182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf432aef498eb8f874c1ff9e73c375cbb9626579f1cc126a165cb61a267979d9`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fe67542d159b5a3f795f90ca42909f6b68e30ecacb594619318e299281a502`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0de367115fdf665b827922b87273aae2d2f6ad8df9473cd7526edb8d968fe`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe9b5c20ec0224b0e33d7297a93826afa7f7a3562fe5dede80baaf3e35437f8`  
		Last Modified: Thu, 23 Jan 2025 18:30:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f3939086ea98217dbf92c98006d1fe3316ffe3a61ab59fcc631a901d0433d4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58415977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e950f51e96d53246f97daa7cf4ba58773ce41e900525593cb4d7b58a0f94f750`

```dockerfile
```

-	Layers:
	-	`sha256:bf927b21d84000b3d588663ae3cb54395f074137ef4fc0c1b7f5f1d78fb2af10`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 58.4 MB (58388841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc6fe822bf8e86376a0743ca4efd77b6870e6a45763f8cc9e09acf393028b08`  
		Last Modified: Thu, 23 Jan 2025 18:30:49 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29244f05b35308e6b0dcc11a74f394b80097a4b72c828beadcd783dcdcf11194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 MB (662290322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cc35601dc86e58a2140f16f592500147d92a91abe6e55a765712633f3ff6df`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db86ce3dd26b502fae6356f1be60d20f60bca1257b178d439b027dd3d1551e8`  
		Last Modified: Thu, 23 Jan 2025 19:12:22 GMT  
		Size: 366.8 MB (366762952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc2a74806b232f6c02e473854dd4b67b0f3df220feb3ec6159234556ba688e`  
		Last Modified: Thu, 23 Jan 2025 19:12:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e19f402f1113207312deb900ba4cd2d014644efb8c400558900d0283c5b090`  
		Last Modified: Thu, 23 Jan 2025 19:12:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa11488a63d584ccad9cf0cf01eeecf6374787cd959fb75d0d5e0c9f8ab312`  
		Last Modified: Thu, 23 Jan 2025 19:12:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181922030ccc2bec60dd5227083af70ef9853bb81db3ea8a848a6501baaa8a8`  
		Last Modified: Thu, 23 Jan 2025 19:12:18 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9da8fbd404ec6c26419b2701a384c9cabc9fe5c74903c5e93119c6bc8c6aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58423432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee151e4feb6ba7bca0095c696c64e8a86f5a5b47000f65526c4b70c9740e3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:0c05270638dd0a3ea03ca8574027da77a052eb512f3ca81c0100daf17ce2db81`  
		Last Modified: Thu, 23 Jan 2025 19:12:15 GMT  
		Size: 58.4 MB (58396132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b28159976b0b036069f5e558914a334f2497bd1993291ccaa87ccfa029d5723`  
		Last Modified: Thu, 23 Jan 2025 19:12:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f7dec6e90a76beb82e54e21b2ee5e8c41cce7f3d09596dcad1b1216d5e8d4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.2 MB (682198668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c543545e2f6ce3c4072185d911b2e440dc50210525a043333c9fdd8b2bee9f`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca86fa2495de7cdd13fac0b048f953ea403243242c7c29b21193f3f3e6cbd72`  
		Last Modified: Thu, 23 Jan 2025 18:33:51 GMT  
		Size: 367.5 MB (367455965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c6daff8c8e8af849f8d909e99e4734669fa1a1b780d82f78599281064bb3f`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6883ffaa3307bb091332b5f1e9a37e18d13feb0eb673a4509d8403ad4cdaddb`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334934d145a22292a420dd908b841d2fae1d68d7fb65a7f5087d73912abc67fc`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831a255fc926f8c449d4e06ca65fdedbe2034d7db0e1a61b9194bf68090a9e6`  
		Last Modified: Thu, 23 Jan 2025 18:33:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:34d060256482cc498352e732aff4b950df314764b091fbb3dfb682a66582a9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58424202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3226f58de0c39291f7bea03d567d75a377e916614b9055141e5ed92846edaa`

```dockerfile
```

-	Layers:
	-	`sha256:16dbc78fb2a481f1dc2f5b22d98c44bb9fa7a4909357bfdbec935e15fda8295b`  
		Last Modified: Thu, 23 Jan 2025 18:33:28 GMT  
		Size: 58.4 MB (58397004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ad14f054bba01aed51ca9bc58c55721c30d9644fc87fbb87de9494a1c0172b`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250123`

```console
$ docker pull odoo@sha256:cd226c03d7c11b873547f44ded6eb4c93cfca65fbe387f5e0a910aa745c6c05d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250123` - linux; amd64

```console
$ docker pull odoo@sha256:8d6511d94ad00483460f285a2a48f62ef8e6885e2d5d0ba6be9bfeb16ef81faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.9 MB (665909748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7dd48cc0180cc3d1f3d5bf76bd1e16d5a05e99cc437980e5caff6073fcb13`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7654019d4b20b10437539b1cfa692f0a21825e3ddfdfe640e93b7332ef2510`  
		Last Modified: Thu, 23 Jan 2025 18:30:53 GMT  
		Size: 254.5 MB (254519197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b583fc9c4e7b0a5fedb7332d3fd1a21b9478109b2bb6d0a95b5170fef8a16df`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 14.2 MB (14231248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b491b2a2e1cc29d3a94332e54fa44ef1cc2544383173a2ded502bbebcf13c`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 485.7 KB (485712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c1cdbfdd48b9f41d176b9cfb1c064839cd40a1a55c23174d8d95f5fd15d93b`  
		Last Modified: Thu, 23 Jan 2025 18:30:55 GMT  
		Size: 366.9 MB (366919182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf432aef498eb8f874c1ff9e73c375cbb9626579f1cc126a165cb61a267979d9`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fe67542d159b5a3f795f90ca42909f6b68e30ecacb594619318e299281a502`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0de367115fdf665b827922b87273aae2d2f6ad8df9473cd7526edb8d968fe`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe9b5c20ec0224b0e33d7297a93826afa7f7a3562fe5dede80baaf3e35437f8`  
		Last Modified: Thu, 23 Jan 2025 18:30:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:f3939086ea98217dbf92c98006d1fe3316ffe3a61ab59fcc631a901d0433d4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58415977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e950f51e96d53246f97daa7cf4ba58773ce41e900525593cb4d7b58a0f94f750`

```dockerfile
```

-	Layers:
	-	`sha256:bf927b21d84000b3d588663ae3cb54395f074137ef4fc0c1b7f5f1d78fb2af10`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 58.4 MB (58388841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc6fe822bf8e86376a0743ca4efd77b6870e6a45763f8cc9e09acf393028b08`  
		Last Modified: Thu, 23 Jan 2025 18:30:49 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250123` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29244f05b35308e6b0dcc11a74f394b80097a4b72c828beadcd783dcdcf11194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 MB (662290322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cc35601dc86e58a2140f16f592500147d92a91abe6e55a765712633f3ff6df`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db86ce3dd26b502fae6356f1be60d20f60bca1257b178d439b027dd3d1551e8`  
		Last Modified: Thu, 23 Jan 2025 19:12:22 GMT  
		Size: 366.8 MB (366762952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc2a74806b232f6c02e473854dd4b67b0f3df220feb3ec6159234556ba688e`  
		Last Modified: Thu, 23 Jan 2025 19:12:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e19f402f1113207312deb900ba4cd2d014644efb8c400558900d0283c5b090`  
		Last Modified: Thu, 23 Jan 2025 19:12:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa11488a63d584ccad9cf0cf01eeecf6374787cd959fb75d0d5e0c9f8ab312`  
		Last Modified: Thu, 23 Jan 2025 19:12:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181922030ccc2bec60dd5227083af70ef9853bb81db3ea8a848a6501baaa8a8`  
		Last Modified: Thu, 23 Jan 2025 19:12:18 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:9da8fbd404ec6c26419b2701a384c9cabc9fe5c74903c5e93119c6bc8c6aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58423432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee151e4feb6ba7bca0095c696c64e8a86f5a5b47000f65526c4b70c9740e3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:0c05270638dd0a3ea03ca8574027da77a052eb512f3ca81c0100daf17ce2db81`  
		Last Modified: Thu, 23 Jan 2025 19:12:15 GMT  
		Size: 58.4 MB (58396132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b28159976b0b036069f5e558914a334f2497bd1993291ccaa87ccfa029d5723`  
		Last Modified: Thu, 23 Jan 2025 19:12:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250123` - linux; ppc64le

```console
$ docker pull odoo@sha256:f7dec6e90a76beb82e54e21b2ee5e8c41cce7f3d09596dcad1b1216d5e8d4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.2 MB (682198668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c543545e2f6ce3c4072185d911b2e440dc50210525a043333c9fdd8b2bee9f`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca86fa2495de7cdd13fac0b048f953ea403243242c7c29b21193f3f3e6cbd72`  
		Last Modified: Thu, 23 Jan 2025 18:33:51 GMT  
		Size: 367.5 MB (367455965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c6daff8c8e8af849f8d909e99e4734669fa1a1b780d82f78599281064bb3f`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6883ffaa3307bb091332b5f1e9a37e18d13feb0eb673a4509d8403ad4cdaddb`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334934d145a22292a420dd908b841d2fae1d68d7fb65a7f5087d73912abc67fc`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831a255fc926f8c449d4e06ca65fdedbe2034d7db0e1a61b9194bf68090a9e6`  
		Last Modified: Thu, 23 Jan 2025 18:33:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250123` - unknown; unknown

```console
$ docker pull odoo@sha256:34d060256482cc498352e732aff4b950df314764b091fbb3dfb682a66582a9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58424202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3226f58de0c39291f7bea03d567d75a377e916614b9055141e5ed92846edaa`

```dockerfile
```

-	Layers:
	-	`sha256:16dbc78fb2a481f1dc2f5b22d98c44bb9fa7a4909357bfdbec935e15fda8295b`  
		Last Modified: Thu, 23 Jan 2025 18:33:28 GMT  
		Size: 58.4 MB (58397004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ad14f054bba01aed51ca9bc58c55721c30d9644fc87fbb87de9494a1c0172b`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:cd226c03d7c11b873547f44ded6eb4c93cfca65fbe387f5e0a910aa745c6c05d
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
$ docker pull odoo@sha256:8d6511d94ad00483460f285a2a48f62ef8e6885e2d5d0ba6be9bfeb16ef81faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.9 MB (665909748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca7dd48cc0180cc3d1f3d5bf76bd1e16d5a05e99cc437980e5caff6073fcb13`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=amd64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7654019d4b20b10437539b1cfa692f0a21825e3ddfdfe640e93b7332ef2510`  
		Last Modified: Thu, 23 Jan 2025 18:30:53 GMT  
		Size: 254.5 MB (254519197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b583fc9c4e7b0a5fedb7332d3fd1a21b9478109b2bb6d0a95b5170fef8a16df`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 14.2 MB (14231248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b491b2a2e1cc29d3a94332e54fa44ef1cc2544383173a2ded502bbebcf13c`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 485.7 KB (485712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c1cdbfdd48b9f41d176b9cfb1c064839cd40a1a55c23174d8d95f5fd15d93b`  
		Last Modified: Thu, 23 Jan 2025 18:30:55 GMT  
		Size: 366.9 MB (366919182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf432aef498eb8f874c1ff9e73c375cbb9626579f1cc126a165cb61a267979d9`  
		Last Modified: Thu, 23 Jan 2025 18:30:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fe67542d159b5a3f795f90ca42909f6b68e30ecacb594619318e299281a502`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0de367115fdf665b827922b87273aae2d2f6ad8df9473cd7526edb8d968fe`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe9b5c20ec0224b0e33d7297a93826afa7f7a3562fe5dede80baaf3e35437f8`  
		Last Modified: Thu, 23 Jan 2025 18:30:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f3939086ea98217dbf92c98006d1fe3316ffe3a61ab59fcc631a901d0433d4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58415977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e950f51e96d53246f97daa7cf4ba58773ce41e900525593cb4d7b58a0f94f750`

```dockerfile
```

-	Layers:
	-	`sha256:bf927b21d84000b3d588663ae3cb54395f074137ef4fc0c1b7f5f1d78fb2af10`  
		Last Modified: Thu, 23 Jan 2025 18:30:51 GMT  
		Size: 58.4 MB (58388841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc6fe822bf8e86376a0743ca4efd77b6870e6a45763f8cc9e09acf393028b08`  
		Last Modified: Thu, 23 Jan 2025 18:30:49 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29244f05b35308e6b0dcc11a74f394b80097a4b72c828beadcd783dcdcf11194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 MB (662290322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cc35601dc86e58a2140f16f592500147d92a91abe6e55a765712633f3ff6df`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db86ce3dd26b502fae6356f1be60d20f60bca1257b178d439b027dd3d1551e8`  
		Last Modified: Thu, 23 Jan 2025 19:12:22 GMT  
		Size: 366.8 MB (366762952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc2a74806b232f6c02e473854dd4b67b0f3df220feb3ec6159234556ba688e`  
		Last Modified: Thu, 23 Jan 2025 19:12:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e19f402f1113207312deb900ba4cd2d014644efb8c400558900d0283c5b090`  
		Last Modified: Thu, 23 Jan 2025 19:12:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa11488a63d584ccad9cf0cf01eeecf6374787cd959fb75d0d5e0c9f8ab312`  
		Last Modified: Thu, 23 Jan 2025 19:12:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181922030ccc2bec60dd5227083af70ef9853bb81db3ea8a848a6501baaa8a8`  
		Last Modified: Thu, 23 Jan 2025 19:12:18 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9da8fbd404ec6c26419b2701a384c9cabc9fe5c74903c5e93119c6bc8c6aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58423432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee151e4feb6ba7bca0095c696c64e8a86f5a5b47000f65526c4b70c9740e3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:0c05270638dd0a3ea03ca8574027da77a052eb512f3ca81c0100daf17ce2db81`  
		Last Modified: Thu, 23 Jan 2025 19:12:15 GMT  
		Size: 58.4 MB (58396132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b28159976b0b036069f5e558914a334f2497bd1993291ccaa87ccfa029d5723`  
		Last Modified: Thu, 23 Jan 2025 19:12:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:f7dec6e90a76beb82e54e21b2ee5e8c41cce7f3d09596dcad1b1216d5e8d4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.2 MB (682198668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c543545e2f6ce3c4072185d911b2e440dc50210525a043333c9fdd8b2bee9f`
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
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca86fa2495de7cdd13fac0b048f953ea403243242c7c29b21193f3f3e6cbd72`  
		Last Modified: Thu, 23 Jan 2025 18:33:51 GMT  
		Size: 367.5 MB (367455965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c6daff8c8e8af849f8d909e99e4734669fa1a1b780d82f78599281064bb3f`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6883ffaa3307bb091332b5f1e9a37e18d13feb0eb673a4509d8403ad4cdaddb`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334934d145a22292a420dd908b841d2fae1d68d7fb65a7f5087d73912abc67fc`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831a255fc926f8c449d4e06ca65fdedbe2034d7db0e1a61b9194bf68090a9e6`  
		Last Modified: Thu, 23 Jan 2025 18:33:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:34d060256482cc498352e732aff4b950df314764b091fbb3dfb682a66582a9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58424202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3226f58de0c39291f7bea03d567d75a377e916614b9055141e5ed92846edaa`

```dockerfile
```

-	Layers:
	-	`sha256:16dbc78fb2a481f1dc2f5b22d98c44bb9fa7a4909357bfdbec935e15fda8295b`  
		Last Modified: Thu, 23 Jan 2025 18:33:28 GMT  
		Size: 58.4 MB (58397004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ad14f054bba01aed51ca9bc58c55721c30d9644fc87fbb87de9494a1c0172b`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
