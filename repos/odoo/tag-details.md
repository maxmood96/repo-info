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
$ docker pull odoo@sha256:5587485f0c37f3e60856796fe22e70f29b48f20ccf5af444e48f8288b8a15294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:a33a6bf03b22f335840b79885e32f8355c90cb8c54467a0958726ff398392fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564214665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0fa13a6c331c7fa0986388877bae02598eddef4b5a65cfcd1ee59e3f772316`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=15.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=5934248e8cac9b5dc28829da5ac46dcaeceb7714
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: ODOO_RELEASE=20240819 ODOO_SHA=5934248e8cac9b5dc28829da5ac46dcaeceb7714
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: ODOO_RELEASE=20240819 ODOO_SHA=5934248e8cac9b5dc28829da5ac46dcaeceb7714
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4e691ab84b8f126cf199f5d7edbdcfcd85636c2156c3e8c84f5d0501fbeef7`  
		Last Modified: Mon, 19 Aug 2024 17:59:44 GMT  
		Size: 220.3 MB (220281937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c86f4b7d578a58f7106a5ccf56c1131017de4ef91f453647594bfe15e41415`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 2.4 MB (2387743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5123577d6fe4f57743029e511f2d49bc8136a65234dbb1440019f07ef75bfeb6`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 463.8 KB (463828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e84887d9289664ac11450eee85e3eb36e7e26c9e3ec8df024ac1576fd9ed26`  
		Last Modified: Mon, 19 Aug 2024 17:59:45 GMT  
		Size: 309.7 MB (309650439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32e6156a33759e3069e49c2832ed1c322facaa1bed86ae8229628303da940ec`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11888e200e3d6a84b8d91c899e443ef9d26e6f7a9ab98f36edd3b911f154f2`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b540951a0ca31ab9f5d20ddbd419ad7d431c35a1daa689dfa8f6428b1603c66`  
		Last Modified: Mon, 19 Aug 2024 17:59:42 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d564f476c6d95c31b883bec29f8e1f38bab0ce2ab7214804dc1e7f4848ae8ea0`  
		Last Modified: Mon, 19 Aug 2024 17:59:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:49089051258421251cd32a0a4a8734389d6505867c852715bc3a4652c2b3b536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72a4c66cde04e1be2ef8396264a6385b0ef63574bfd12c3926dad264b828f0a`

```dockerfile
```

-	Layers:
	-	`sha256:4a5d5b6197462d207ab3e0d37df5a95e32245c1a35b0f228d9f96fcaecf2a09c`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099a0d057d95738a45b4232e9c110a95e483f13e85802223cd1efb3f543a17b0`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:5587485f0c37f3e60856796fe22e70f29b48f20ccf5af444e48f8288b8a15294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:a33a6bf03b22f335840b79885e32f8355c90cb8c54467a0958726ff398392fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564214665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0fa13a6c331c7fa0986388877bae02598eddef4b5a65cfcd1ee59e3f772316`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=15.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=5934248e8cac9b5dc28829da5ac46dcaeceb7714
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: ODOO_RELEASE=20240819 ODOO_SHA=5934248e8cac9b5dc28829da5ac46dcaeceb7714
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: ODOO_RELEASE=20240819 ODOO_SHA=5934248e8cac9b5dc28829da5ac46dcaeceb7714
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4e691ab84b8f126cf199f5d7edbdcfcd85636c2156c3e8c84f5d0501fbeef7`  
		Last Modified: Mon, 19 Aug 2024 17:59:44 GMT  
		Size: 220.3 MB (220281937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c86f4b7d578a58f7106a5ccf56c1131017de4ef91f453647594bfe15e41415`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 2.4 MB (2387743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5123577d6fe4f57743029e511f2d49bc8136a65234dbb1440019f07ef75bfeb6`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 463.8 KB (463828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e84887d9289664ac11450eee85e3eb36e7e26c9e3ec8df024ac1576fd9ed26`  
		Last Modified: Mon, 19 Aug 2024 17:59:45 GMT  
		Size: 309.7 MB (309650439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32e6156a33759e3069e49c2832ed1c322facaa1bed86ae8229628303da940ec`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11888e200e3d6a84b8d91c899e443ef9d26e6f7a9ab98f36edd3b911f154f2`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b540951a0ca31ab9f5d20ddbd419ad7d431c35a1daa689dfa8f6428b1603c66`  
		Last Modified: Mon, 19 Aug 2024 17:59:42 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d564f476c6d95c31b883bec29f8e1f38bab0ce2ab7214804dc1e7f4848ae8ea0`  
		Last Modified: Mon, 19 Aug 2024 17:59:42 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:49089051258421251cd32a0a4a8734389d6505867c852715bc3a4652c2b3b536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72a4c66cde04e1be2ef8396264a6385b0ef63574bfd12c3926dad264b828f0a`

```dockerfile
```

-	Layers:
	-	`sha256:4a5d5b6197462d207ab3e0d37df5a95e32245c1a35b0f228d9f96fcaecf2a09c`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099a0d057d95738a45b4232e9c110a95e483f13e85802223cd1efb3f543a17b0`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240826`

**does not exist** (yet?)

## `odoo:16`

```console
$ docker pull odoo@sha256:311f3007aa0b53e3c3321a5d5949801ccfc50f94c5c930e324e2320e44c2c1bd
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
$ docker pull odoo@sha256:b3c430788c26bb3f755c9ce4f239ae0af39c4a4bf32a28cf5e5061a1c4653ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583898629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cd37f3efb5f0a695d6a3803ccd30cf241d6b54df8ff90137af63985f9fb5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=amd64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748305a111919812cf97abae571dde9b3012f2b179b96bc3a3dba4cf97e510f6`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 219.6 MB (219593832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c59df25a936e659675413b7012835df37bf3fe819d39e001c8c43c7c86aa17`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 2.4 MB (2391427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1970fa7a30eb6aa4dcde1807608b740132287c2e3e737651c0d411ef719c48`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 463.8 KB (463817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434b0981152e2dab06fe8fe007545c33ebff175ec54f4117c551c61e0c31994`  
		Last Modified: Mon, 19 Aug 2024 17:59:43 GMT  
		Size: 330.0 MB (330018833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59021d4f0e6b80b2d2a58ad2fd851564ad24b61e0eceea539ff568c55cc78b`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d3a96214d2e36b03abdda4e8276f7e3dd5ff2aea0f59a699dcf61b562c7e60`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081751d3e8f84b5813d57d9a6f4f9b8ab1d35b8e2d647858c2704c16e5563dae`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:992f7fbcd17ebf1adcb0358da49c878d3f9b63e1c60dfabcd43874097d09884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8c721c97d18d16fbe0d9e2abe16f739d242c753eb2817dacf8f60843081f8`

```dockerfile
```

-	Layers:
	-	`sha256:efbbe619f8d46824349e6ac5c51a548cb2dd25d8f6195c85313e0a016f98237d`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415917639399a91e65ffd11538ec4d9308ba78f43f09f6a9ce84f491d08223ce`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fb13fb7680338f5d120d46651c2bd5b7cdeb877323c78b11b236fa2c29dbf4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579534056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cbbbbefb53d0a8ed78b8c82735f7e0d88c24432b4ccc689e4abcf1db830192`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=arm64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:5a4be1b53708769f35a1cf4509c4437d309c50e6dd6289858318d16349069cb3`  
		Last Modified: Mon, 19 Aug 2024 18:05:20 GMT  
		Size: 329.7 MB (329695493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb34345753055b0665da8a064baaedf286dd62793221bc7d4219bf72f65ed50`  
		Last Modified: Mon, 19 Aug 2024 18:05:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8487013cc624d9348db6eed44c8bb8bba7e5850f29635a42a263c6524faa9713`  
		Last Modified: Mon, 19 Aug 2024 18:05:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87709a4bb620b2466b0e94cdc582f0422b481ddbae7d5a21c067f14d4d0b8774`  
		Last Modified: Mon, 19 Aug 2024 18:05:14 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4965b12f7c63eaed865c132bdd90774d8df5202ad215889ff95c78e9eb96b55`  
		Last Modified: Mon, 19 Aug 2024 18:05:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:62e8e130005cefe5caadff4ae6b33c4984888523dd1a6724ee57a36dca2d5145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13e29dd138a382adb16a49448dd1079ccbfb8fa9ff6ddd91af621df12ed1e6a`

```dockerfile
```

-	Layers:
	-	`sha256:902ce3c3e241318ca1c1df4355ce6b7c72c4dddc820a0be7fd449f98f6fab266`  
		Last Modified: Mon, 19 Aug 2024 18:05:13 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377193e950b41db2bdd85776c303af8b3dee2a8d6aee7bbb59a20a73487a5272`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:56c510d301f13815becb0b122467aa185345118254bd562cc5be8c604ba11ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 MB (598466109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944018c8f442d034f1c45bf82816259a83e06b636e5ca81541b55f264b16dfc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=ppc64le
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:33cf4e6e7b7e49c26da393e3d088b079a96bf08f3a325652759dfed0c5eab907`  
		Last Modified: Mon, 19 Aug 2024 18:11:17 GMT  
		Size: 331.5 MB (331470698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776d2ebadc2a5148bafe9523d766fda3d26b6c574b20cc30f23b2fff7655815`  
		Last Modified: Mon, 19 Aug 2024 18:10:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ccdb05e286dac13770188886ef1ea918fe09ed993d5f50278ce92b2f87cfb2`  
		Last Modified: Mon, 19 Aug 2024 18:10:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa43a4c40e361ce7fbe21b1d1dcd398ffafd32ae5d4d9077a07cdfe6098c9934`  
		Last Modified: Mon, 19 Aug 2024 18:11:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d27ee7f1569de2c118a7d177cd358fc3368956302aa98516bc1f3ed874235a`  
		Last Modified: Mon, 19 Aug 2024 18:11:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:7afb1c38ec6465f546829ee0e65e8626566b2521b53c8ede0942b31f818b4afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ee76e07c8ec146fc614570c646280c20b509adb82a1fb09657a5398532964`

```dockerfile
```

-	Layers:
	-	`sha256:c8182d0b1d511f8eeb902731fb12ef30cabcf1a6e43144eaf5aab1c00ee1cf0d`  
		Last Modified: Mon, 19 Aug 2024 18:10:59 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19cf8c9f70d0d55b0787d5185eca2084cb9a7306309170127a6ca18317ee702b`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:311f3007aa0b53e3c3321a5d5949801ccfc50f94c5c930e324e2320e44c2c1bd
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
$ docker pull odoo@sha256:b3c430788c26bb3f755c9ce4f239ae0af39c4a4bf32a28cf5e5061a1c4653ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583898629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cd37f3efb5f0a695d6a3803ccd30cf241d6b54df8ff90137af63985f9fb5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=amd64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748305a111919812cf97abae571dde9b3012f2b179b96bc3a3dba4cf97e510f6`  
		Last Modified: Mon, 19 Aug 2024 17:59:41 GMT  
		Size: 219.6 MB (219593832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c59df25a936e659675413b7012835df37bf3fe819d39e001c8c43c7c86aa17`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 2.4 MB (2391427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1970fa7a30eb6aa4dcde1807608b740132287c2e3e737651c0d411ef719c48`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 463.8 KB (463817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434b0981152e2dab06fe8fe007545c33ebff175ec54f4117c551c61e0c31994`  
		Last Modified: Mon, 19 Aug 2024 17:59:43 GMT  
		Size: 330.0 MB (330018833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59021d4f0e6b80b2d2a58ad2fd851564ad24b61e0eceea539ff568c55cc78b`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d3a96214d2e36b03abdda4e8276f7e3dd5ff2aea0f59a699dcf61b562c7e60`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081751d3e8f84b5813d57d9a6f4f9b8ab1d35b8e2d647858c2704c16e5563dae`  
		Last Modified: Mon, 19 Aug 2024 17:59:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:992f7fbcd17ebf1adcb0358da49c878d3f9b63e1c60dfabcd43874097d09884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa8c721c97d18d16fbe0d9e2abe16f739d242c753eb2817dacf8f60843081f8`

```dockerfile
```

-	Layers:
	-	`sha256:efbbe619f8d46824349e6ac5c51a548cb2dd25d8f6195c85313e0a016f98237d`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415917639399a91e65ffd11538ec4d9308ba78f43f09f6a9ce84f491d08223ce`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fb13fb7680338f5d120d46651c2bd5b7cdeb877323c78b11b236fa2c29dbf4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579534056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cbbbbefb53d0a8ed78b8c82735f7e0d88c24432b4ccc689e4abcf1db830192`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=arm64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:5a4be1b53708769f35a1cf4509c4437d309c50e6dd6289858318d16349069cb3`  
		Last Modified: Mon, 19 Aug 2024 18:05:20 GMT  
		Size: 329.7 MB (329695493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb34345753055b0665da8a064baaedf286dd62793221bc7d4219bf72f65ed50`  
		Last Modified: Mon, 19 Aug 2024 18:05:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8487013cc624d9348db6eed44c8bb8bba7e5850f29635a42a263c6524faa9713`  
		Last Modified: Mon, 19 Aug 2024 18:05:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87709a4bb620b2466b0e94cdc582f0422b481ddbae7d5a21c067f14d4d0b8774`  
		Last Modified: Mon, 19 Aug 2024 18:05:14 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4965b12f7c63eaed865c132bdd90774d8df5202ad215889ff95c78e9eb96b55`  
		Last Modified: Mon, 19 Aug 2024 18:05:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:62e8e130005cefe5caadff4ae6b33c4984888523dd1a6724ee57a36dca2d5145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13e29dd138a382adb16a49448dd1079ccbfb8fa9ff6ddd91af621df12ed1e6a`

```dockerfile
```

-	Layers:
	-	`sha256:902ce3c3e241318ca1c1df4355ce6b7c72c4dddc820a0be7fd449f98f6fab266`  
		Last Modified: Mon, 19 Aug 2024 18:05:13 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377193e950b41db2bdd85776c303af8b3dee2a8d6aee7bbb59a20a73487a5272`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:56c510d301f13815becb0b122467aa185345118254bd562cc5be8c604ba11ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 MB (598466109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944018c8f442d034f1c45bf82816259a83e06b636e5ca81541b55f264b16dfc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=ppc64le
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=16.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=3b24f0d4cd39879d60bee66331091e202fa2675b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:33cf4e6e7b7e49c26da393e3d088b079a96bf08f3a325652759dfed0c5eab907`  
		Last Modified: Mon, 19 Aug 2024 18:11:17 GMT  
		Size: 331.5 MB (331470698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776d2ebadc2a5148bafe9523d766fda3d26b6c574b20cc30f23b2fff7655815`  
		Last Modified: Mon, 19 Aug 2024 18:10:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ccdb05e286dac13770188886ef1ea918fe09ed993d5f50278ce92b2f87cfb2`  
		Last Modified: Mon, 19 Aug 2024 18:10:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa43a4c40e361ce7fbe21b1d1dcd398ffafd32ae5d4d9077a07cdfe6098c9934`  
		Last Modified: Mon, 19 Aug 2024 18:11:00 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d27ee7f1569de2c118a7d177cd358fc3368956302aa98516bc1f3ed874235a`  
		Last Modified: Mon, 19 Aug 2024 18:11:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7afb1c38ec6465f546829ee0e65e8626566b2521b53c8ede0942b31f818b4afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ee76e07c8ec146fc614570c646280c20b509adb82a1fb09657a5398532964`

```dockerfile
```

-	Layers:
	-	`sha256:c8182d0b1d511f8eeb902731fb12ef30cabcf1a6e43144eaf5aab1c00ee1cf0d`  
		Last Modified: Mon, 19 Aug 2024 18:10:59 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19cf8c9f70d0d55b0787d5185eca2084cb9a7306309170127a6ca18317ee702b`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240826`

**does not exist** (yet?)

## `odoo:17`

```console
$ docker pull odoo@sha256:5041460069badd99ca2fcdea1cdbee917d989e509c626897ebef2460de7a9b0c
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
$ docker pull odoo@sha256:ae221c17a6872bd751d2dfb7cf52e1f82b54f3f17222eff37c4844acef282a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596366404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b960ed8f0707ca1b4ffd8be8354f4df4c5c944fff02e0f1c383b609803f06cb`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=amd64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f40dea9a8bbe4ba1f3930004e58067f4da59fff61bbdbd844d218eae8e78bf`  
		Last Modified: Mon, 19 Aug 2024 17:59:52 GMT  
		Size: 233.7 MB (233742079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d7c53992f9c4959a2f8847e83ab7e16f00fd822323e56ab6d7e9d0315d1bca`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 2.3 MB (2315604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301785b521d811b1dc753b4aac651384377110def0788b4b5c649c60bb80e49`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 465.0 KB (464966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715013778503ec6b8a7250f92e264e4944956648e32b28df3ddf5296c8a6344d`  
		Last Modified: Mon, 19 Aug 2024 17:59:54 GMT  
		Size: 330.3 MB (330305289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51a7967415a0abd0674f674b3e48bc6cbf151b0796deff99d806838af77eca`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ec0d9a6a97f498758537c2199562dd7da549943e71b12bc756aa617905478`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aabb6c945bcffcad82039c95d15c698495f3eaa65241a230b5573513186937`  
		Last Modified: Mon, 19 Aug 2024 17:59:51 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:21e79fd53d8cfecfc350e54ed9eb2e40896403eca287787e987a6192c2e854da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39032701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034755e9edb7a7720bcf02453a1363fc489de87f8007d96e92b38facd8e78a8a`

```dockerfile
```

-	Layers:
	-	`sha256:0d492eb0793895679e3eadb9802c37dc6e81ba0a8093aec3cf926f36bee3e7d6`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 39.0 MB (39005826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8555682e85706d9b73ccd18d185e5ccf3016271daa273e4839137779aeb9e`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3b4b75bfe35183dc56436fb0fecb87b465beb9ddc185f9ab2004b7f9a9758bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.2 MB (591156569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e4db5fae5bffecebe65ec492ff8921000cb3df91c11e94c86648fc3362ba29`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=arm64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:70cc825e338366d92355acf1bbdd65ec1a8bc2e819c44f170247763488acbfb4`  
		Last Modified: Mon, 19 Aug 2024 18:01:20 GMT  
		Size: 329.9 MB (329906070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a0ae7de802aa28f682711353ee3921d87e5673af25f3c2dc42502437f11825`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad50c0db0b73e3689f039929128b204be0a10dc4c936941dcc3e2137d66b84`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03cca6fbfd4ac65b4da83b6c1296e5bc98d2bbe6a4fadda17f0b5edc67ca761`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10aa33594a7b83d7c0356bfd36c0484296d5ca6911e3f20c9a25a14c32cb82b`  
		Last Modified: Mon, 19 Aug 2024 18:01:14 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:70856f32947d6703a1d54e7d3de293e3ac22fc849a7bd9adab35eb4700112023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39039527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9a3e4b31f782ae4f4443ac15c072cc44801992eff08c31728db4edc99e652a`

```dockerfile
```

-	Layers:
	-	`sha256:baccdbbfc88ff0457b41162c42b836ef6d926c487d013e041382e8214a304312`  
		Last Modified: Mon, 19 Aug 2024 18:01:14 GMT  
		Size: 39.0 MB (39012351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf3381d69c622acb5c0d9412f8e8387d9e23e66a32263070211b3f2438ed38e`  
		Last Modified: Mon, 19 Aug 2024 18:01:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:0fa4cfdaef1f681871cc234db3b95c13d3901b01dc23a926a9d93b1cc2e4f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.8 MB (612842865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76983929f61e1c6ca29ff3f8edb5be4c62944555e977d7cc1c328248ebde2f9`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=ppc64le
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:754183a91166dec24d59ba3eeae06dd3532eb9bbde0e1ce497cdfa07593b0199`  
		Last Modified: Mon, 19 Aug 2024 18:03:16 GMT  
		Size: 332.0 MB (332042638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c585eafd18c3e6d2d4e671ba6e3c802d7df3329dfbd9c330c3aa0c389fd67`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c2589ba67b5f3497a8313661eeed0191457e2881773304605b8ee451d941dc`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd8fa853cea6e1397225f8da372ff8eac5164379f1b1ac5ec0c6e464e4ed01`  
		Last Modified: Mon, 19 Aug 2024 18:03:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:af88a158a2bd0a2eb877e4decd57e13d0e0dea6c330a0a2946dc258f3248fa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39041070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0b8899473b273160f105f4654048d85d55bfb988b60c1cf03be2dd57ded0db`

```dockerfile
```

-	Layers:
	-	`sha256:eb2ff84913d8cd736c95c4a0cf07c2bf25b1e8ef24146d995d1843a3cd9bad46`  
		Last Modified: Mon, 19 Aug 2024 18:03:05 GMT  
		Size: 39.0 MB (39014139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776fd26096a868a62b5219c04d3195481efbec0d0a36a487696cda4068a81a7e`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:5041460069badd99ca2fcdea1cdbee917d989e509c626897ebef2460de7a9b0c
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
$ docker pull odoo@sha256:ae221c17a6872bd751d2dfb7cf52e1f82b54f3f17222eff37c4844acef282a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596366404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b960ed8f0707ca1b4ffd8be8354f4df4c5c944fff02e0f1c383b609803f06cb`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=amd64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f40dea9a8bbe4ba1f3930004e58067f4da59fff61bbdbd844d218eae8e78bf`  
		Last Modified: Mon, 19 Aug 2024 17:59:52 GMT  
		Size: 233.7 MB (233742079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d7c53992f9c4959a2f8847e83ab7e16f00fd822323e56ab6d7e9d0315d1bca`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 2.3 MB (2315604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301785b521d811b1dc753b4aac651384377110def0788b4b5c649c60bb80e49`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 465.0 KB (464966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715013778503ec6b8a7250f92e264e4944956648e32b28df3ddf5296c8a6344d`  
		Last Modified: Mon, 19 Aug 2024 17:59:54 GMT  
		Size: 330.3 MB (330305289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51a7967415a0abd0674f674b3e48bc6cbf151b0796deff99d806838af77eca`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ec0d9a6a97f498758537c2199562dd7da549943e71b12bc756aa617905478`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aabb6c945bcffcad82039c95d15c698495f3eaa65241a230b5573513186937`  
		Last Modified: Mon, 19 Aug 2024 17:59:51 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:21e79fd53d8cfecfc350e54ed9eb2e40896403eca287787e987a6192c2e854da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39032701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034755e9edb7a7720bcf02453a1363fc489de87f8007d96e92b38facd8e78a8a`

```dockerfile
```

-	Layers:
	-	`sha256:0d492eb0793895679e3eadb9802c37dc6e81ba0a8093aec3cf926f36bee3e7d6`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 39.0 MB (39005826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8555682e85706d9b73ccd18d185e5ccf3016271daa273e4839137779aeb9e`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3b4b75bfe35183dc56436fb0fecb87b465beb9ddc185f9ab2004b7f9a9758bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.2 MB (591156569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e4db5fae5bffecebe65ec492ff8921000cb3df91c11e94c86648fc3362ba29`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=arm64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:70cc825e338366d92355acf1bbdd65ec1a8bc2e819c44f170247763488acbfb4`  
		Last Modified: Mon, 19 Aug 2024 18:01:20 GMT  
		Size: 329.9 MB (329906070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a0ae7de802aa28f682711353ee3921d87e5673af25f3c2dc42502437f11825`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad50c0db0b73e3689f039929128b204be0a10dc4c936941dcc3e2137d66b84`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03cca6fbfd4ac65b4da83b6c1296e5bc98d2bbe6a4fadda17f0b5edc67ca761`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10aa33594a7b83d7c0356bfd36c0484296d5ca6911e3f20c9a25a14c32cb82b`  
		Last Modified: Mon, 19 Aug 2024 18:01:14 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:70856f32947d6703a1d54e7d3de293e3ac22fc849a7bd9adab35eb4700112023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39039527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9a3e4b31f782ae4f4443ac15c072cc44801992eff08c31728db4edc99e652a`

```dockerfile
```

-	Layers:
	-	`sha256:baccdbbfc88ff0457b41162c42b836ef6d926c487d013e041382e8214a304312`  
		Last Modified: Mon, 19 Aug 2024 18:01:14 GMT  
		Size: 39.0 MB (39012351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf3381d69c622acb5c0d9412f8e8387d9e23e66a32263070211b3f2438ed38e`  
		Last Modified: Mon, 19 Aug 2024 18:01:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0fa4cfdaef1f681871cc234db3b95c13d3901b01dc23a926a9d93b1cc2e4f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.8 MB (612842865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76983929f61e1c6ca29ff3f8edb5be4c62944555e977d7cc1c328248ebde2f9`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=ppc64le
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:754183a91166dec24d59ba3eeae06dd3532eb9bbde0e1ce497cdfa07593b0199`  
		Last Modified: Mon, 19 Aug 2024 18:03:16 GMT  
		Size: 332.0 MB (332042638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c585eafd18c3e6d2d4e671ba6e3c802d7df3329dfbd9c330c3aa0c389fd67`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c2589ba67b5f3497a8313661eeed0191457e2881773304605b8ee451d941dc`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd8fa853cea6e1397225f8da372ff8eac5164379f1b1ac5ec0c6e464e4ed01`  
		Last Modified: Mon, 19 Aug 2024 18:03:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:af88a158a2bd0a2eb877e4decd57e13d0e0dea6c330a0a2946dc258f3248fa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39041070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0b8899473b273160f105f4654048d85d55bfb988b60c1cf03be2dd57ded0db`

```dockerfile
```

-	Layers:
	-	`sha256:eb2ff84913d8cd736c95c4a0cf07c2bf25b1e8ef24146d995d1843a3cd9bad46`  
		Last Modified: Mon, 19 Aug 2024 18:03:05 GMT  
		Size: 39.0 MB (39014139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776fd26096a868a62b5219c04d3195481efbec0d0a36a487696cda4068a81a7e`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240826`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:5041460069badd99ca2fcdea1cdbee917d989e509c626897ebef2460de7a9b0c
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
$ docker pull odoo@sha256:ae221c17a6872bd751d2dfb7cf52e1f82b54f3f17222eff37c4844acef282a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596366404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b960ed8f0707ca1b4ffd8be8354f4df4c5c944fff02e0f1c383b609803f06cb`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=amd64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f40dea9a8bbe4ba1f3930004e58067f4da59fff61bbdbd844d218eae8e78bf`  
		Last Modified: Mon, 19 Aug 2024 17:59:52 GMT  
		Size: 233.7 MB (233742079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d7c53992f9c4959a2f8847e83ab7e16f00fd822323e56ab6d7e9d0315d1bca`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 2.3 MB (2315604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301785b521d811b1dc753b4aac651384377110def0788b4b5c649c60bb80e49`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 465.0 KB (464966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715013778503ec6b8a7250f92e264e4944956648e32b28df3ddf5296c8a6344d`  
		Last Modified: Mon, 19 Aug 2024 17:59:54 GMT  
		Size: 330.3 MB (330305289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51a7967415a0abd0674f674b3e48bc6cbf151b0796deff99d806838af77eca`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ec0d9a6a97f498758537c2199562dd7da549943e71b12bc756aa617905478`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aabb6c945bcffcad82039c95d15c698495f3eaa65241a230b5573513186937`  
		Last Modified: Mon, 19 Aug 2024 17:59:51 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:21e79fd53d8cfecfc350e54ed9eb2e40896403eca287787e987a6192c2e854da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39032701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034755e9edb7a7720bcf02453a1363fc489de87f8007d96e92b38facd8e78a8a`

```dockerfile
```

-	Layers:
	-	`sha256:0d492eb0793895679e3eadb9802c37dc6e81ba0a8093aec3cf926f36bee3e7d6`  
		Last Modified: Mon, 19 Aug 2024 17:59:50 GMT  
		Size: 39.0 MB (39005826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8555682e85706d9b73ccd18d185e5ccf3016271daa273e4839137779aeb9e`  
		Last Modified: Mon, 19 Aug 2024 17:59:49 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b3b4b75bfe35183dc56436fb0fecb87b465beb9ddc185f9ab2004b7f9a9758bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.2 MB (591156569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e4db5fae5bffecebe65ec492ff8921000cb3df91c11e94c86648fc3362ba29`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=arm64
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:70cc825e338366d92355acf1bbdd65ec1a8bc2e819c44f170247763488acbfb4`  
		Last Modified: Mon, 19 Aug 2024 18:01:20 GMT  
		Size: 329.9 MB (329906070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a0ae7de802aa28f682711353ee3921d87e5673af25f3c2dc42502437f11825`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad50c0db0b73e3689f039929128b204be0a10dc4c936941dcc3e2137d66b84`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03cca6fbfd4ac65b4da83b6c1296e5bc98d2bbe6a4fadda17f0b5edc67ca761`  
		Last Modified: Mon, 19 Aug 2024 18:01:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10aa33594a7b83d7c0356bfd36c0484296d5ca6911e3f20c9a25a14c32cb82b`  
		Last Modified: Mon, 19 Aug 2024 18:01:14 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:70856f32947d6703a1d54e7d3de293e3ac22fc849a7bd9adab35eb4700112023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39039527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9a3e4b31f782ae4f4443ac15c072cc44801992eff08c31728db4edc99e652a`

```dockerfile
```

-	Layers:
	-	`sha256:baccdbbfc88ff0457b41162c42b836ef6d926c487d013e041382e8214a304312`  
		Last Modified: Mon, 19 Aug 2024 18:01:14 GMT  
		Size: 39.0 MB (39012351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf3381d69c622acb5c0d9412f8e8387d9e23e66a32263070211b3f2438ed38e`  
		Last Modified: Mon, 19 Aug 2024 18:01:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:0fa4cfdaef1f681871cc234db3b95c13d3901b01dc23a926a9d93b1cc2e4f509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.8 MB (612842865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76983929f61e1c6ca29ff3f8edb5be4c62944555e977d7cc1c328248ebde2f9`
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
# Mon, 19 Aug 2024 06:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 19 Aug 2024 06:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 19 Aug 2024 06:45:14 GMT
ARG TARGETARCH=ppc64le
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_VERSION=17.0
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_RELEASE=20240819
# Mon, 19 Aug 2024 06:45:14 GMT
ARG ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240819 ODOO_SHA=81689a80a074843ada7c712ba23cde1cfca9b63c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 19 Aug 2024 06:45:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 19 Aug 2024 06:45:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 19 Aug 2024 06:45:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 19 Aug 2024 06:45:14 GMT
USER odoo
# Mon, 19 Aug 2024 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 19 Aug 2024 06:45:14 GMT
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
	-	`sha256:754183a91166dec24d59ba3eeae06dd3532eb9bbde0e1ce497cdfa07593b0199`  
		Last Modified: Mon, 19 Aug 2024 18:03:16 GMT  
		Size: 332.0 MB (332042638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b27eb523dc9481037b42445c04ed0c23fec09e1b385373e625dea455e0809`  
		Last Modified: Mon, 19 Aug 2024 17:59:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c585eafd18c3e6d2d4e671ba6e3c802d7df3329dfbd9c330c3aa0c389fd67`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c2589ba67b5f3497a8313661eeed0191457e2881773304605b8ee451d941dc`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd8fa853cea6e1397225f8da372ff8eac5164379f1b1ac5ec0c6e464e4ed01`  
		Last Modified: Mon, 19 Aug 2024 18:03:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:af88a158a2bd0a2eb877e4decd57e13d0e0dea6c330a0a2946dc258f3248fa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39041070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0b8899473b273160f105f4654048d85d55bfb988b60c1cf03be2dd57ded0db`

```dockerfile
```

-	Layers:
	-	`sha256:eb2ff84913d8cd736c95c4a0cf07c2bf25b1e8ef24146d995d1843a3cd9bad46`  
		Last Modified: Mon, 19 Aug 2024 18:03:05 GMT  
		Size: 39.0 MB (39014139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776fd26096a868a62b5219c04d3195481efbec0d0a36a487696cda4068a81a7e`  
		Last Modified: Mon, 19 Aug 2024 18:03:03 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
