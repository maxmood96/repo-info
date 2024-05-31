<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240522`](#odoo150-20240522)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240522`](#odoo160-20240522)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240522`](#odoo170-20240522)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:92188430ec03d841bceed42314a90280c0fdc8d7d2caa97f539ca5bf94b1e2fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:6a8589298fb7f143bdcabbeadb06bf594424ffbedc6d8af3351207661f64fa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.7 MB (563704620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb3fd0c89682e2038ef00623a76fb58c90680c0760d35a6841f409f04696827`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=15.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=fee63fd1fae4b39df565744c3802bc09d65312d3
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=fee63fd1fae4b39df565744c3802bc09d65312d3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=fee63fd1fae4b39df565744c3802bc09d65312d3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fcdb43dd42f637cb8db6cf4f42121076a379b6aa42594986c95fcb54fc7474`  
		Last Modified: Wed, 29 May 2024 20:01:26 GMT  
		Size: 220.3 MB (220282112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6353fff4727804a924d29712327d1a12c7419a8b5236b91f6a59b8752d9b2892`  
		Last Modified: Wed, 29 May 2024 20:01:22 GMT  
		Size: 2.4 MB (2387208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba079be04f35ac6c5d85e9fe7312b893751301a96600a061bbce9b63d950ee2`  
		Last Modified: Wed, 29 May 2024 20:01:22 GMT  
		Size: 457.8 KB (457797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543d58a4d16bf20f73a8579832b74c79df0b39e1801c80942e6dd7264131e862`  
		Last Modified: Wed, 29 May 2024 20:01:28 GMT  
		Size: 309.1 MB (309141138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40d0730d3a7a0432addb6bb034f52d8162a52846950c770e6c19411c77adc5`  
		Last Modified: Wed, 29 May 2024 20:01:23 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd743d9563b4980ededd274202a0c747977eb4efdb6bb605e4047b3a803a1bdd`  
		Last Modified: Wed, 29 May 2024 20:01:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f48026d5bb38126cfa2a60b3c88602547e3d3a7e1f4e623e57f764880877f29`  
		Last Modified: Wed, 29 May 2024 20:01:24 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fafe206dd4d6c691ce246242d5252717119b0966d3b74bcd2289f1ad4219d1`  
		Last Modified: Wed, 29 May 2024 20:01:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:d51245dafbcca643bef7ac4b4e6e1cda9a8b4f09701cad30c05403c2dcefff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34530673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e55cabddf39382012a850814c56917f4f164e0bf0f56c1683aad42fd18c4fc`

```dockerfile
```

-	Layers:
	-	`sha256:a190c08c31560d2164dffa6ba5d998015dbe4c04b15ec43da27460c78984a488`  
		Last Modified: Wed, 29 May 2024 20:01:23 GMT  
		Size: 34.5 MB (34506399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b168e0eca41a5ff2a6fe6234aad6273de45ce933266ddfcc48936e94804e34f1`  
		Last Modified: Wed, 29 May 2024 20:01:22 GMT  
		Size: 24.3 KB (24274 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:92188430ec03d841bceed42314a90280c0fdc8d7d2caa97f539ca5bf94b1e2fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:6a8589298fb7f143bdcabbeadb06bf594424ffbedc6d8af3351207661f64fa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.7 MB (563704620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb3fd0c89682e2038ef00623a76fb58c90680c0760d35a6841f409f04696827`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=15.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=fee63fd1fae4b39df565744c3802bc09d65312d3
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=fee63fd1fae4b39df565744c3802bc09d65312d3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=fee63fd1fae4b39df565744c3802bc09d65312d3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fcdb43dd42f637cb8db6cf4f42121076a379b6aa42594986c95fcb54fc7474`  
		Last Modified: Wed, 29 May 2024 20:01:26 GMT  
		Size: 220.3 MB (220282112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6353fff4727804a924d29712327d1a12c7419a8b5236b91f6a59b8752d9b2892`  
		Last Modified: Wed, 29 May 2024 20:01:22 GMT  
		Size: 2.4 MB (2387208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba079be04f35ac6c5d85e9fe7312b893751301a96600a061bbce9b63d950ee2`  
		Last Modified: Wed, 29 May 2024 20:01:22 GMT  
		Size: 457.8 KB (457797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543d58a4d16bf20f73a8579832b74c79df0b39e1801c80942e6dd7264131e862`  
		Last Modified: Wed, 29 May 2024 20:01:28 GMT  
		Size: 309.1 MB (309141138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40d0730d3a7a0432addb6bb034f52d8162a52846950c770e6c19411c77adc5`  
		Last Modified: Wed, 29 May 2024 20:01:23 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd743d9563b4980ededd274202a0c747977eb4efdb6bb605e4047b3a803a1bdd`  
		Last Modified: Wed, 29 May 2024 20:01:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f48026d5bb38126cfa2a60b3c88602547e3d3a7e1f4e623e57f764880877f29`  
		Last Modified: Wed, 29 May 2024 20:01:24 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fafe206dd4d6c691ce246242d5252717119b0966d3b74bcd2289f1ad4219d1`  
		Last Modified: Wed, 29 May 2024 20:01:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d51245dafbcca643bef7ac4b4e6e1cda9a8b4f09701cad30c05403c2dcefff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34530673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e55cabddf39382012a850814c56917f4f164e0bf0f56c1683aad42fd18c4fc`

```dockerfile
```

-	Layers:
	-	`sha256:a190c08c31560d2164dffa6ba5d998015dbe4c04b15ec43da27460c78984a488`  
		Last Modified: Wed, 29 May 2024 20:01:23 GMT  
		Size: 34.5 MB (34506399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b168e0eca41a5ff2a6fe6234aad6273de45ce933266ddfcc48936e94804e34f1`  
		Last Modified: Wed, 29 May 2024 20:01:22 GMT  
		Size: 24.3 KB (24274 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240522`

**does not exist** (yet?)

## `odoo:16`

```console
$ docker pull odoo@sha256:2eb189b72b0762ca4484bbddfb76604a885295840477936207ab72912ba7a325
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
$ docker pull odoo@sha256:b1b5d786f33f0f3e3e06235f37956ab082d9b3af4d484ca637ec6992fc25cc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.9 MB (582945378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1796267bb60a628287acb40bd55c0a6989b1e6806b5cf583e8fd457c6e07b02d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05edc06a01918536dfb337f9b32a9c21b1b59c5d3aafb8b5658d91f71c13413e`  
		Last Modified: Wed, 29 May 2024 20:01:41 GMT  
		Size: 219.6 MB (219594574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4486eed2c1c036d7f433e8f62120452fc29e100af134ff100a464435483b108d`  
		Last Modified: Wed, 29 May 2024 20:01:37 GMT  
		Size: 2.4 MB (2391084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda7f81bf19b48c8bf758f8f0e5fb8727e29fbbe30e9300b15804b45e1258c41`  
		Last Modified: Wed, 29 May 2024 20:01:37 GMT  
		Size: 457.8 KB (457787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e03a14b5fad75db4d002a8610b7fecf333ee3f4a3dd7252de357f68c6a7dbc`  
		Last Modified: Wed, 29 May 2024 20:01:43 GMT  
		Size: 329.1 MB (329065565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b8743fd5bef35a233081173b676d5254fc63c18f400895c4efc0ff4bf37de`  
		Last Modified: Wed, 29 May 2024 20:01:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e881fb7b2c8e44e32243ba14ac9282c0aef222feaa0192cec4fa4774a851cb3`  
		Last Modified: Wed, 29 May 2024 20:01:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4916095adbdfa9d91469079e5c3cb7acd68c0dc3d9f8a5dc73dd2599af37270`  
		Last Modified: Wed, 29 May 2024 20:01:39 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683c7f1c401cf2d4e3643c7de2cb30324d297385a217b568992ff0cb934ed19`  
		Last Modified: Wed, 29 May 2024 20:01:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:df75199d1760c9da3f6672ce982509889a577a868a7a0761b8e3ca8d902bd64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38567943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2995e62dd5ec884c58a35668ed34e8b4f40e01b24ee642a87905ca17ae503ba`

```dockerfile
```

-	Layers:
	-	`sha256:d62e75b8e393c5ce31d82957affb0fd7706353037f9f8905c5270745a5323060`  
		Last Modified: Wed, 29 May 2024 20:01:38 GMT  
		Size: 38.5 MB (38541759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82cc841922bc71f96df6f7068cad66001ffd3de9e4325b3a68ac52bcd6f1f9a0`  
		Last Modified: Wed, 29 May 2024 20:01:37 GMT  
		Size: 26.2 KB (26184 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8a503bf02392da3272a0591df7effdf3a0e0d67d15dc5d1e5c7ec261f964fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578578727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8d76533ee1691d06b2480ba49167342fb6c600cac4af3200adabeca535476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f081822e148fbd12e88942138758452276337b5cf8ad49fde3bed38321c60`  
		Last Modified: Thu, 30 May 2024 02:24:03 GMT  
		Size: 216.9 MB (216900476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8080aaf786c4ccd54a7fadc40de3455bf8063851fe27e930efef95cc0aa2619`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 2.4 MB (2393326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bde69a325d29e830b01000a32bc7f9c070f5c69486d3ee433941cdb27533394`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 457.8 KB (457801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde29033b387b8dd6ed28c7113ca1969cd9cc502f91287d2411bd860390655ac`  
		Last Modified: Thu, 30 May 2024 02:24:05 GMT  
		Size: 328.7 MB (328737782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc009f1a96b30a245fcfd3571f3217745ef4eeee359d020bbf0fe63602a0ed0f`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793b7010766fd70ea5a0b4575ba52da73e922a3ba7ab8aec37f1197310763f46`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba4e85ba081af75d5b1c1aa270bf41124b1790a463ad35e8b8e0de64f234b5`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eaa9b67deb0ece918299cfa1ac43c086a01c4b4ae1874508fd271f3fb6eaa1`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:84c503de8522f50f20f20021e33e77c5e2b1d3a215fa408ff680c64777b57779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38574689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a316fd2dac07ec5649c7bb2133113f5711df628823a33688ce8ceffbcac7bbf2`

```dockerfile
```

-	Layers:
	-	`sha256:13b083fe0ccd07df3131dece66ba743af5df664a26142a8bff60ea68a90f7aae`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 38.5 MB (38548219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04f9f5dbed164a4a5cd593e0342bd201b491b20082d215ba9b4129dc54f8a30`  
		Last Modified: Thu, 30 May 2024 02:23:57 GMT  
		Size: 26.5 KB (26470 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:db10a0a1f0e03aabecc89741f0d23cb3d4721fbf60712a5796d9b76a823c4067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.5 MB (597501161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6390fb9ffa4aef0ff29d9e21672ec2d2ff86686507308ce39c52e26816601ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588f519d28b37d2f657d1ccf2699f6427cdbac1c10aeeb81d89beb17392ff2a0`  
		Last Modified: Wed, 29 May 2024 20:37:15 GMT  
		Size: 228.6 MB (228590064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c07145260340efe1b849368d247af11e024543a6ebe489a6b75706bd9fb1c`  
		Last Modified: Wed, 29 May 2024 20:37:09 GMT  
		Size: 2.6 MB (2634169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cf27b02e8e9844c6a965b2d81222ad3da0119e490c06847bca57a24048ed99`  
		Last Modified: Wed, 29 May 2024 20:37:09 GMT  
		Size: 457.8 KB (457834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cc6e9a876473e7da2f435ef91d9e630782af4e35e39338be249bdc2c9f1e77`  
		Last Modified: Wed, 29 May 2024 20:37:18 GMT  
		Size: 330.5 MB (330505495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da58ed72a75a4a70252db7038f306ab5af770b91d8b75f3ba57d3b3119d4affe`  
		Last Modified: Wed, 29 May 2024 20:37:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa066894aec6e19ddb09ba24d277d1b5f3febe230b9ed434bc2004dec83a13e`  
		Last Modified: Wed, 29 May 2024 20:37:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e606ba08684958c8bdc2896dcf63d0fc256c326d67e9a3caf069372753abafaa`  
		Last Modified: Wed, 29 May 2024 20:37:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f9c4632a752a16330e3983ad669d3bc401851c5fd76e7f0280ad167b92289`  
		Last Modified: Wed, 29 May 2024 20:37:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:7d71c1032c465d02503f4af1311fdddb919672e579d88261ee682b8dc0bbf40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38576113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a318c07da20fb822f4a3c7f1ec7514f5e6df1fe86f6f799413d1216e5aeed`

```dockerfile
```

-	Layers:
	-	`sha256:895082fbed19f40d36daa0155166b9da9eca372ff429259d8f1ab6d77b0bd59f`  
		Last Modified: Wed, 29 May 2024 20:37:10 GMT  
		Size: 38.5 MB (38549885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0485d8f12b7e76c5323b4d400e654c04a23d9f72a2e12541361c6708da7186`  
		Last Modified: Wed, 29 May 2024 20:37:08 GMT  
		Size: 26.2 KB (26228 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:2eb189b72b0762ca4484bbddfb76604a885295840477936207ab72912ba7a325
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
$ docker pull odoo@sha256:b1b5d786f33f0f3e3e06235f37956ab082d9b3af4d484ca637ec6992fc25cc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.9 MB (582945378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1796267bb60a628287acb40bd55c0a6989b1e6806b5cf583e8fd457c6e07b02d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05edc06a01918536dfb337f9b32a9c21b1b59c5d3aafb8b5658d91f71c13413e`  
		Last Modified: Wed, 29 May 2024 20:01:41 GMT  
		Size: 219.6 MB (219594574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4486eed2c1c036d7f433e8f62120452fc29e100af134ff100a464435483b108d`  
		Last Modified: Wed, 29 May 2024 20:01:37 GMT  
		Size: 2.4 MB (2391084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda7f81bf19b48c8bf758f8f0e5fb8727e29fbbe30e9300b15804b45e1258c41`  
		Last Modified: Wed, 29 May 2024 20:01:37 GMT  
		Size: 457.8 KB (457787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e03a14b5fad75db4d002a8610b7fecf333ee3f4a3dd7252de357f68c6a7dbc`  
		Last Modified: Wed, 29 May 2024 20:01:43 GMT  
		Size: 329.1 MB (329065565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b8743fd5bef35a233081173b676d5254fc63c18f400895c4efc0ff4bf37de`  
		Last Modified: Wed, 29 May 2024 20:01:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e881fb7b2c8e44e32243ba14ac9282c0aef222feaa0192cec4fa4774a851cb3`  
		Last Modified: Wed, 29 May 2024 20:01:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4916095adbdfa9d91469079e5c3cb7acd68c0dc3d9f8a5dc73dd2599af37270`  
		Last Modified: Wed, 29 May 2024 20:01:39 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683c7f1c401cf2d4e3643c7de2cb30324d297385a217b568992ff0cb934ed19`  
		Last Modified: Wed, 29 May 2024 20:01:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:df75199d1760c9da3f6672ce982509889a577a868a7a0761b8e3ca8d902bd64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38567943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2995e62dd5ec884c58a35668ed34e8b4f40e01b24ee642a87905ca17ae503ba`

```dockerfile
```

-	Layers:
	-	`sha256:d62e75b8e393c5ce31d82957affb0fd7706353037f9f8905c5270745a5323060`  
		Last Modified: Wed, 29 May 2024 20:01:38 GMT  
		Size: 38.5 MB (38541759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82cc841922bc71f96df6f7068cad66001ffd3de9e4325b3a68ac52bcd6f1f9a0`  
		Last Modified: Wed, 29 May 2024 20:01:37 GMT  
		Size: 26.2 KB (26184 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8a503bf02392da3272a0591df7effdf3a0e0d67d15dc5d1e5c7ec261f964fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578578727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8d76533ee1691d06b2480ba49167342fb6c600cac4af3200adabeca535476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f081822e148fbd12e88942138758452276337b5cf8ad49fde3bed38321c60`  
		Last Modified: Thu, 30 May 2024 02:24:03 GMT  
		Size: 216.9 MB (216900476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8080aaf786c4ccd54a7fadc40de3455bf8063851fe27e930efef95cc0aa2619`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 2.4 MB (2393326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bde69a325d29e830b01000a32bc7f9c070f5c69486d3ee433941cdb27533394`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 457.8 KB (457801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde29033b387b8dd6ed28c7113ca1969cd9cc502f91287d2411bd860390655ac`  
		Last Modified: Thu, 30 May 2024 02:24:05 GMT  
		Size: 328.7 MB (328737782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc009f1a96b30a245fcfd3571f3217745ef4eeee359d020bbf0fe63602a0ed0f`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793b7010766fd70ea5a0b4575ba52da73e922a3ba7ab8aec37f1197310763f46`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba4e85ba081af75d5b1c1aa270bf41124b1790a463ad35e8b8e0de64f234b5`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eaa9b67deb0ece918299cfa1ac43c086a01c4b4ae1874508fd271f3fb6eaa1`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:84c503de8522f50f20f20021e33e77c5e2b1d3a215fa408ff680c64777b57779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38574689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a316fd2dac07ec5649c7bb2133113f5711df628823a33688ce8ceffbcac7bbf2`

```dockerfile
```

-	Layers:
	-	`sha256:13b083fe0ccd07df3131dece66ba743af5df664a26142a8bff60ea68a90f7aae`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 38.5 MB (38548219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04f9f5dbed164a4a5cd593e0342bd201b491b20082d215ba9b4129dc54f8a30`  
		Last Modified: Thu, 30 May 2024 02:23:57 GMT  
		Size: 26.5 KB (26470 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:db10a0a1f0e03aabecc89741f0d23cb3d4721fbf60712a5796d9b76a823c4067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.5 MB (597501161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6390fb9ffa4aef0ff29d9e21672ec2d2ff86686507308ce39c52e26816601ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588f519d28b37d2f657d1ccf2699f6427cdbac1c10aeeb81d89beb17392ff2a0`  
		Last Modified: Wed, 29 May 2024 20:37:15 GMT  
		Size: 228.6 MB (228590064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c07145260340efe1b849368d247af11e024543a6ebe489a6b75706bd9fb1c`  
		Last Modified: Wed, 29 May 2024 20:37:09 GMT  
		Size: 2.6 MB (2634169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cf27b02e8e9844c6a965b2d81222ad3da0119e490c06847bca57a24048ed99`  
		Last Modified: Wed, 29 May 2024 20:37:09 GMT  
		Size: 457.8 KB (457834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cc6e9a876473e7da2f435ef91d9e630782af4e35e39338be249bdc2c9f1e77`  
		Last Modified: Wed, 29 May 2024 20:37:18 GMT  
		Size: 330.5 MB (330505495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da58ed72a75a4a70252db7038f306ab5af770b91d8b75f3ba57d3b3119d4affe`  
		Last Modified: Wed, 29 May 2024 20:37:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa066894aec6e19ddb09ba24d277d1b5f3febe230b9ed434bc2004dec83a13e`  
		Last Modified: Wed, 29 May 2024 20:37:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e606ba08684958c8bdc2896dcf63d0fc256c326d67e9a3caf069372753abafaa`  
		Last Modified: Wed, 29 May 2024 20:37:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9f9c4632a752a16330e3983ad669d3bc401851c5fd76e7f0280ad167b92289`  
		Last Modified: Wed, 29 May 2024 20:37:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7d71c1032c465d02503f4af1311fdddb919672e579d88261ee682b8dc0bbf40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38576113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518a318c07da20fb822f4a3c7f1ec7514f5e6df1fe86f6f799413d1216e5aeed`

```dockerfile
```

-	Layers:
	-	`sha256:895082fbed19f40d36daa0155166b9da9eca372ff429259d8f1ab6d77b0bd59f`  
		Last Modified: Wed, 29 May 2024 20:37:10 GMT  
		Size: 38.5 MB (38549885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0485d8f12b7e76c5323b4d400e654c04a23d9f72a2e12541361c6708da7186`  
		Last Modified: Wed, 29 May 2024 20:37:08 GMT  
		Size: 26.2 KB (26228 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240522`

**does not exist** (yet?)

## `odoo:17`

```console
$ docker pull odoo@sha256:9597ee678c40070ac30fa63009c7a13d58247c53c9c1b4ddcceb7b4501eea5fd
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
$ docker pull odoo@sha256:880603abbe06a44c0cd522924857a658fc21ce86d113c0f8513d87b8ad7c29af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601790743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb407f383e179f9f6e1e0d9c44597c604d13c0d10fc0e9fdfb3d8d221ec850dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d916741f1f15fd5069b649299933cc5887d10a2ccbb056811c2c4a87acf80b5b`  
		Last Modified: Wed, 29 May 2024 20:01:59 GMT  
		Size: 233.7 MB (233721257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f06bd7631d24e69aecd8d9789ceec3d9a73f5e57bc98964519c6badb5c3744f`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 2.3 MB (2313388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d17ac75ffa51eb8632be5539b2bf8ffcd6c708f292b54dc43bba1ec5b47c46`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 458.9 KB (458948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d0ba3a7a498f6eba11623e9fe798536c07a5ddb5fa4bf9ee29f4a9c1d3627`  
		Last Modified: Wed, 29 May 2024 20:02:02 GMT  
		Size: 335.8 MB (335760757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d361c9543ce6de2c209aafc6951969c55e6e1b5d9fe8a8e9bfcda1e302005bb0`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f508a43736c0d8168da81a39a40a7f700e6f3b860182f0998f5fe695643a8d`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa690bba6acc686036cf68b1f27112eb0538d528561b48a5e9a80172317c64`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b942dcae61c8bc9ef20b19bba778e33b8c40a0bccd1245805ad818fa5790900`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:bd522790584ce055e0d3362dcaa26dab82a4ba7b5bcea928370caa05dcc7fb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49525727a5bc9bd79a82747a0e82891b76a59ac0a41d981eb1ad77153cf942`

```dockerfile
```

-	Layers:
	-	`sha256:af80ce5281b9ca2eb24d41ebfdbf5fdbfe51adf6f0b3f4040a5d222ef3123cc4`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 39.2 MB (39192841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1da4c12ad03bb3f5c42d2a171ff670838020c8f004033fd315e8f8b307e47e3`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 26.5 KB (26517 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a693628cbf707e6b0732304d3598dc95b64b2fc6ff66b20fdae18854af931ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596618598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233581163c27a01b077bdce6e1a6a1edd49a7668961642e8b370c85ccdcaca32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df60fb2ae7fabd06f5f0fe628403f944bdeba6ceab1507d1d47f8583818c9`  
		Last Modified: Thu, 30 May 2024 02:20:00 GMT  
		Size: 231.1 MB (231129260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b04ceea49496f804f547d035ef6e841f1aba7ba13634b871a0a262553ddc`  
		Last Modified: Thu, 30 May 2024 02:19:56 GMT  
		Size: 2.3 MB (2306364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffb0c1ef8ee904225d9eb157f0951f47e738b7919d7427b352e0fcdf644980d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 458.8 KB (458826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3009fc0ca9a84938ba7632ccbbb79e015de10d56f522f91d5a572b5ecb717`  
		Last Modified: Thu, 30 May 2024 02:20:05 GMT  
		Size: 335.4 MB (335361176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207689c892df07a8c4c6c6e6dde8ed6edebcac90c38b59eb8d9840f21326c98`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd5863589606d080b8aec7ee8fafbd4185ba02cc6f0c1de2687f7730b8fb30`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad8920a2fc0c2f4a513ea1405bca112e1b9f0187c822961a63f7e70323ef2`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e49bae97ebf9195e865e845a98d83141e8998e7ffc54b68328895b45c7a31`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:984e016c32de2f01b3a50ed71dee5d5283965222a4b1799b9f777133cd87097c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48795314c03b1ca80e5b7732f9db1df97f2eea32eeb265f19835c5465e33907b`

```dockerfile
```

-	Layers:
	-	`sha256:f376677805c31ca437af69a2de7f17a49d8c7db2fe9465c5ab8ff3784746c19b`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 39.2 MB (39199354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a42aeafd36498d0983a7a9c5b37104a1246819387fe978af4601edc2030027d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 26.8 KB (26807 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:22fb44ee0617d2c2287729c9d4cc063ba01cdbeb7d5fe17e14c2ed41eebd7eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.3 MB (618293001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b490a3825dc5ac99cd47662bcd5e7bc09bd32fd2e81adeb84b31c967542ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62be6f5f65b553b61acf7267ff22918d248665ec3ec9a1b313b03ef217c4f9`  
		Last Modified: Wed, 29 May 2024 20:30:00 GMT  
		Size: 243.3 MB (243268541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5dbca549a03a5cbe2117251a21b070881d53c88f09c1ae04e307816c15136c`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 2.6 MB (2590095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18644e0e4b87df08e7c9adbfb8deb6d4a17e18bbfceb5bb2df6011fe530c58cd`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 458.9 KB (458899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8100fed10d012faa8008015da5b511f60b8dee46440760ea3dd082dc88a4`  
		Last Modified: Wed, 29 May 2024 20:30:14 GMT  
		Size: 337.5 MB (337511798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050412ca59e9ada9ba40c8b96cc3d4b7b0d1a1d174b088c26ff8846d8ca17c07`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e450bf62e071223d4dfbbed16ae7bc09ef0c67bc771207b6b59c4d5287f608`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2e81751ebfab0458d5faa9cb865296a292023d86b365c8456c41931e3dd101`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72170a90d094a9b391380c725a24c3e1fbfa0f50ced61c68c949d26c8fd6f0c3`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b7898e5ae60c55e5fda5148bf636cfcc902fc5cda1e59080a9ab29a6882c78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39227716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa32bd721966b5b7a264d2b1376c3fe9d77a3a37dbca4b390a7604df7b52fed`

```dockerfile
```

-	Layers:
	-	`sha256:b0b003291c88e1b96a175acc1435e1dc71a766409583a95204d735e96b98b75a`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 39.2 MB (39201148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebd75b346477b649ce59cccca1278fb9423e9d85f895202c526d18d0cce9bbc`  
		Last Modified: Wed, 29 May 2024 20:29:50 GMT  
		Size: 26.6 KB (26568 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:9597ee678c40070ac30fa63009c7a13d58247c53c9c1b4ddcceb7b4501eea5fd
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
$ docker pull odoo@sha256:880603abbe06a44c0cd522924857a658fc21ce86d113c0f8513d87b8ad7c29af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601790743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb407f383e179f9f6e1e0d9c44597c604d13c0d10fc0e9fdfb3d8d221ec850dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d916741f1f15fd5069b649299933cc5887d10a2ccbb056811c2c4a87acf80b5b`  
		Last Modified: Wed, 29 May 2024 20:01:59 GMT  
		Size: 233.7 MB (233721257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f06bd7631d24e69aecd8d9789ceec3d9a73f5e57bc98964519c6badb5c3744f`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 2.3 MB (2313388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d17ac75ffa51eb8632be5539b2bf8ffcd6c708f292b54dc43bba1ec5b47c46`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 458.9 KB (458948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d0ba3a7a498f6eba11623e9fe798536c07a5ddb5fa4bf9ee29f4a9c1d3627`  
		Last Modified: Wed, 29 May 2024 20:02:02 GMT  
		Size: 335.8 MB (335760757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d361c9543ce6de2c209aafc6951969c55e6e1b5d9fe8a8e9bfcda1e302005bb0`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f508a43736c0d8168da81a39a40a7f700e6f3b860182f0998f5fe695643a8d`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa690bba6acc686036cf68b1f27112eb0538d528561b48a5e9a80172317c64`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b942dcae61c8bc9ef20b19bba778e33b8c40a0bccd1245805ad818fa5790900`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:bd522790584ce055e0d3362dcaa26dab82a4ba7b5bcea928370caa05dcc7fb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49525727a5bc9bd79a82747a0e82891b76a59ac0a41d981eb1ad77153cf942`

```dockerfile
```

-	Layers:
	-	`sha256:af80ce5281b9ca2eb24d41ebfdbf5fdbfe51adf6f0b3f4040a5d222ef3123cc4`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 39.2 MB (39192841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1da4c12ad03bb3f5c42d2a171ff670838020c8f004033fd315e8f8b307e47e3`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 26.5 KB (26517 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a693628cbf707e6b0732304d3598dc95b64b2fc6ff66b20fdae18854af931ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596618598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233581163c27a01b077bdce6e1a6a1edd49a7668961642e8b370c85ccdcaca32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df60fb2ae7fabd06f5f0fe628403f944bdeba6ceab1507d1d47f8583818c9`  
		Last Modified: Thu, 30 May 2024 02:20:00 GMT  
		Size: 231.1 MB (231129260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b04ceea49496f804f547d035ef6e841f1aba7ba13634b871a0a262553ddc`  
		Last Modified: Thu, 30 May 2024 02:19:56 GMT  
		Size: 2.3 MB (2306364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffb0c1ef8ee904225d9eb157f0951f47e738b7919d7427b352e0fcdf644980d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 458.8 KB (458826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3009fc0ca9a84938ba7632ccbbb79e015de10d56f522f91d5a572b5ecb717`  
		Last Modified: Thu, 30 May 2024 02:20:05 GMT  
		Size: 335.4 MB (335361176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207689c892df07a8c4c6c6e6dde8ed6edebcac90c38b59eb8d9840f21326c98`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd5863589606d080b8aec7ee8fafbd4185ba02cc6f0c1de2687f7730b8fb30`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad8920a2fc0c2f4a513ea1405bca112e1b9f0187c822961a63f7e70323ef2`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e49bae97ebf9195e865e845a98d83141e8998e7ffc54b68328895b45c7a31`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:984e016c32de2f01b3a50ed71dee5d5283965222a4b1799b9f777133cd87097c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48795314c03b1ca80e5b7732f9db1df97f2eea32eeb265f19835c5465e33907b`

```dockerfile
```

-	Layers:
	-	`sha256:f376677805c31ca437af69a2de7f17a49d8c7db2fe9465c5ab8ff3784746c19b`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 39.2 MB (39199354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a42aeafd36498d0983a7a9c5b37104a1246819387fe978af4601edc2030027d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 26.8 KB (26807 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:22fb44ee0617d2c2287729c9d4cc063ba01cdbeb7d5fe17e14c2ed41eebd7eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.3 MB (618293001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b490a3825dc5ac99cd47662bcd5e7bc09bd32fd2e81adeb84b31c967542ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62be6f5f65b553b61acf7267ff22918d248665ec3ec9a1b313b03ef217c4f9`  
		Last Modified: Wed, 29 May 2024 20:30:00 GMT  
		Size: 243.3 MB (243268541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5dbca549a03a5cbe2117251a21b070881d53c88f09c1ae04e307816c15136c`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 2.6 MB (2590095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18644e0e4b87df08e7c9adbfb8deb6d4a17e18bbfceb5bb2df6011fe530c58cd`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 458.9 KB (458899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8100fed10d012faa8008015da5b511f60b8dee46440760ea3dd082dc88a4`  
		Last Modified: Wed, 29 May 2024 20:30:14 GMT  
		Size: 337.5 MB (337511798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050412ca59e9ada9ba40c8b96cc3d4b7b0d1a1d174b088c26ff8846d8ca17c07`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e450bf62e071223d4dfbbed16ae7bc09ef0c67bc771207b6b59c4d5287f608`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2e81751ebfab0458d5faa9cb865296a292023d86b365c8456c41931e3dd101`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72170a90d094a9b391380c725a24c3e1fbfa0f50ced61c68c949d26c8fd6f0c3`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b7898e5ae60c55e5fda5148bf636cfcc902fc5cda1e59080a9ab29a6882c78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39227716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa32bd721966b5b7a264d2b1376c3fe9d77a3a37dbca4b390a7604df7b52fed`

```dockerfile
```

-	Layers:
	-	`sha256:b0b003291c88e1b96a175acc1435e1dc71a766409583a95204d735e96b98b75a`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 39.2 MB (39201148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebd75b346477b649ce59cccca1278fb9423e9d85f895202c526d18d0cce9bbc`  
		Last Modified: Wed, 29 May 2024 20:29:50 GMT  
		Size: 26.6 KB (26568 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240522`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:9597ee678c40070ac30fa63009c7a13d58247c53c9c1b4ddcceb7b4501eea5fd
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
$ docker pull odoo@sha256:880603abbe06a44c0cd522924857a658fc21ce86d113c0f8513d87b8ad7c29af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601790743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb407f383e179f9f6e1e0d9c44597c604d13c0d10fc0e9fdfb3d8d221ec850dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d916741f1f15fd5069b649299933cc5887d10a2ccbb056811c2c4a87acf80b5b`  
		Last Modified: Wed, 29 May 2024 20:01:59 GMT  
		Size: 233.7 MB (233721257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f06bd7631d24e69aecd8d9789ceec3d9a73f5e57bc98964519c6badb5c3744f`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 2.3 MB (2313388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d17ac75ffa51eb8632be5539b2bf8ffcd6c708f292b54dc43bba1ec5b47c46`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 458.9 KB (458948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d0ba3a7a498f6eba11623e9fe798536c07a5ddb5fa4bf9ee29f4a9c1d3627`  
		Last Modified: Wed, 29 May 2024 20:02:02 GMT  
		Size: 335.8 MB (335760757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d361c9543ce6de2c209aafc6951969c55e6e1b5d9fe8a8e9bfcda1e302005bb0`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f508a43736c0d8168da81a39a40a7f700e6f3b860182f0998f5fe695643a8d`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa690bba6acc686036cf68b1f27112eb0538d528561b48a5e9a80172317c64`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b942dcae61c8bc9ef20b19bba778e33b8c40a0bccd1245805ad818fa5790900`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:bd522790584ce055e0d3362dcaa26dab82a4ba7b5bcea928370caa05dcc7fb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49525727a5bc9bd79a82747a0e82891b76a59ac0a41d981eb1ad77153cf942`

```dockerfile
```

-	Layers:
	-	`sha256:af80ce5281b9ca2eb24d41ebfdbf5fdbfe51adf6f0b3f4040a5d222ef3123cc4`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 39.2 MB (39192841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1da4c12ad03bb3f5c42d2a171ff670838020c8f004033fd315e8f8b307e47e3`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 26.5 KB (26517 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a693628cbf707e6b0732304d3598dc95b64b2fc6ff66b20fdae18854af931ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596618598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233581163c27a01b077bdce6e1a6a1edd49a7668961642e8b370c85ccdcaca32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df60fb2ae7fabd06f5f0fe628403f944bdeba6ceab1507d1d47f8583818c9`  
		Last Modified: Thu, 30 May 2024 02:20:00 GMT  
		Size: 231.1 MB (231129260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b04ceea49496f804f547d035ef6e841f1aba7ba13634b871a0a262553ddc`  
		Last Modified: Thu, 30 May 2024 02:19:56 GMT  
		Size: 2.3 MB (2306364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffb0c1ef8ee904225d9eb157f0951f47e738b7919d7427b352e0fcdf644980d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 458.8 KB (458826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3009fc0ca9a84938ba7632ccbbb79e015de10d56f522f91d5a572b5ecb717`  
		Last Modified: Thu, 30 May 2024 02:20:05 GMT  
		Size: 335.4 MB (335361176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207689c892df07a8c4c6c6e6dde8ed6edebcac90c38b59eb8d9840f21326c98`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd5863589606d080b8aec7ee8fafbd4185ba02cc6f0c1de2687f7730b8fb30`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad8920a2fc0c2f4a513ea1405bca112e1b9f0187c822961a63f7e70323ef2`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e49bae97ebf9195e865e845a98d83141e8998e7ffc54b68328895b45c7a31`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:984e016c32de2f01b3a50ed71dee5d5283965222a4b1799b9f777133cd87097c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48795314c03b1ca80e5b7732f9db1df97f2eea32eeb265f19835c5465e33907b`

```dockerfile
```

-	Layers:
	-	`sha256:f376677805c31ca437af69a2de7f17a49d8c7db2fe9465c5ab8ff3784746c19b`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 39.2 MB (39199354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a42aeafd36498d0983a7a9c5b37104a1246819387fe978af4601edc2030027d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 26.8 KB (26807 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:22fb44ee0617d2c2287729c9d4cc063ba01cdbeb7d5fe17e14c2ed41eebd7eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.3 MB (618293001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b490a3825dc5ac99cd47662bcd5e7bc09bd32fd2e81adeb84b31c967542ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62be6f5f65b553b61acf7267ff22918d248665ec3ec9a1b313b03ef217c4f9`  
		Last Modified: Wed, 29 May 2024 20:30:00 GMT  
		Size: 243.3 MB (243268541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5dbca549a03a5cbe2117251a21b070881d53c88f09c1ae04e307816c15136c`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 2.6 MB (2590095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18644e0e4b87df08e7c9adbfb8deb6d4a17e18bbfceb5bb2df6011fe530c58cd`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 458.9 KB (458899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8100fed10d012faa8008015da5b511f60b8dee46440760ea3dd082dc88a4`  
		Last Modified: Wed, 29 May 2024 20:30:14 GMT  
		Size: 337.5 MB (337511798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050412ca59e9ada9ba40c8b96cc3d4b7b0d1a1d174b088c26ff8846d8ca17c07`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e450bf62e071223d4dfbbed16ae7bc09ef0c67bc771207b6b59c4d5287f608`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2e81751ebfab0458d5faa9cb865296a292023d86b365c8456c41931e3dd101`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72170a90d094a9b391380c725a24c3e1fbfa0f50ced61c68c949d26c8fd6f0c3`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b7898e5ae60c55e5fda5148bf636cfcc902fc5cda1e59080a9ab29a6882c78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39227716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa32bd721966b5b7a264d2b1376c3fe9d77a3a37dbca4b390a7604df7b52fed`

```dockerfile
```

-	Layers:
	-	`sha256:b0b003291c88e1b96a175acc1435e1dc71a766409583a95204d735e96b98b75a`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 39.2 MB (39201148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebd75b346477b649ce59cccca1278fb9423e9d85f895202c526d18d0cce9bbc`  
		Last Modified: Wed, 29 May 2024 20:29:50 GMT  
		Size: 26.6 KB (26568 bytes)  
		MIME: application/vnd.in-toto+json
