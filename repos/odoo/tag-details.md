<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:f38e01014c2414aecea84ffd03f199ef9e448e9245205aac30d05e7676575af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:8c1a8620bd37511c05cadbe9f5eee9c56e87dfd924e0636bef6e48399a0ff2fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.4 MB (563383400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67414affbedcc398c66cbe1cf336f6a67283f725cc12064e01b4ad11cb2a5cfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:22:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:22:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:22:12 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:22:12 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Feb 2024 11:22:12 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 11:22:12 GMT
ARG ODOO_SHA=22c94f752c7b0501711a74721d3f2e10f16ca410
# Tue, 13 Feb 2024 11:23:20 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=22c94f752c7b0501711a74721d3f2e10f16ca410
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 11:23:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 11:23:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 11:23:25 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=22c94f752c7b0501711a74721d3f2e10f16ca410
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 11:23:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 11:23:26 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 11:23:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 11:23:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 11:23:26 GMT
USER odoo
# Tue, 13 Feb 2024 11:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 11:23:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503d586dde6058081085a71407e0daec70122616b9a175f52944fcf0f6cae634`  
		Last Modified: Tue, 13 Feb 2024 11:24:56 GMT  
		Size: 220.3 MB (220291578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fd8ca8a48200ac393e61d324250d6da85bc0dfaa29c83841e7b384b4ae90dd`  
		Last Modified: Tue, 13 Feb 2024 11:24:31 GMT  
		Size: 2.6 MB (2625899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d81bf30e1590e8be1f898a405b5ae2775c64d0de45831fcd3fbb2241409a1`  
		Last Modified: Tue, 13 Feb 2024 11:24:32 GMT  
		Size: 462.9 KB (462933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c17601761a18e5e53b90e663642ef5540be638165bb737c41fb4df15b231f`  
		Last Modified: Tue, 13 Feb 2024 11:25:04 GMT  
		Size: 308.6 MB (308578107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ea100f34b1658c303852a307e875cf3c2cbe12cc86d398cf43d4ea7e8c4b53`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c77f9aec5007ec5918a6c72599c0994c5b846110a20ba4769725b1151269f2`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c7ef56d491b3700aa4bbb978a521aad15e1d06cf4831aed0537564d99bdbb1`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c757bf6c1afc660d7dc25dd59eb73aa05e9b4c60d760f4dea8509522e8ec60`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:f38e01014c2414aecea84ffd03f199ef9e448e9245205aac30d05e7676575af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:8c1a8620bd37511c05cadbe9f5eee9c56e87dfd924e0636bef6e48399a0ff2fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.4 MB (563383400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67414affbedcc398c66cbe1cf336f6a67283f725cc12064e01b4ad11cb2a5cfa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:22:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:22:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:22:12 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:22:12 GMT
ENV ODOO_VERSION=15.0
# Tue, 13 Feb 2024 11:22:12 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 11:22:12 GMT
ARG ODOO_SHA=22c94f752c7b0501711a74721d3f2e10f16ca410
# Tue, 13 Feb 2024 11:23:20 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=22c94f752c7b0501711a74721d3f2e10f16ca410
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 11:23:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 11:23:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 11:23:25 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=22c94f752c7b0501711a74721d3f2e10f16ca410
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 11:23:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 11:23:26 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 11:23:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 11:23:26 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 11:23:26 GMT
USER odoo
# Tue, 13 Feb 2024 11:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 11:23:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503d586dde6058081085a71407e0daec70122616b9a175f52944fcf0f6cae634`  
		Last Modified: Tue, 13 Feb 2024 11:24:56 GMT  
		Size: 220.3 MB (220291578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fd8ca8a48200ac393e61d324250d6da85bc0dfaa29c83841e7b384b4ae90dd`  
		Last Modified: Tue, 13 Feb 2024 11:24:31 GMT  
		Size: 2.6 MB (2625899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d81bf30e1590e8be1f898a405b5ae2775c64d0de45831fcd3fbb2241409a1`  
		Last Modified: Tue, 13 Feb 2024 11:24:32 GMT  
		Size: 462.9 KB (462933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5c17601761a18e5e53b90e663642ef5540be638165bb737c41fb4df15b231f`  
		Last Modified: Tue, 13 Feb 2024 11:25:04 GMT  
		Size: 308.6 MB (308578107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ea100f34b1658c303852a307e875cf3c2cbe12cc86d398cf43d4ea7e8c4b53`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c77f9aec5007ec5918a6c72599c0994c5b846110a20ba4769725b1151269f2`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c7ef56d491b3700aa4bbb978a521aad15e1d06cf4831aed0537564d99bdbb1`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c757bf6c1afc660d7dc25dd59eb73aa05e9b4c60d760f4dea8509522e8ec60`  
		Last Modified: Tue, 13 Feb 2024 11:24:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:94d2609a49eedda07bcbf41b4b63aef64afcccfaaa6f191b654e29e6cedcc072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:e389356c974abea879e128248758eac5bb29f075ec5188a31dee458cb09d1589
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 MB (579297506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf0a80f7fa582355c2f2af1c3bcdeb5ec3b97cc930795181f7563c4c824bbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:18:16 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 11:19:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:19:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:19:35 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:19:36 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Feb 2024 11:19:36 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 11:19:36 GMT
ARG ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
# Tue, 13 Feb 2024 11:20:53 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 11:20:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 11:20:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 11:20:58 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 11:20:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 11:20:58 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 11:20:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 11:20:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 11:20:58 GMT
USER odoo
# Tue, 13 Feb 2024 11:20:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 11:20:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f8764e315ffe4d9162112c693dc2de9180d54741bcc86a94a2e8dc63796`  
		Last Modified: Tue, 13 Feb 2024 11:24:08 GMT  
		Size: 219.6 MB (219603078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c251911a36e7b29cdc68e2e6ad3c227877483a27881808128a45cdf7f29cd97`  
		Last Modified: Tue, 13 Feb 2024 11:23:43 GMT  
		Size: 2.6 MB (2629960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b94be8a611fcadb8c1bb3ac916cbf8b7c765cb563396dcb2461b5150d88e9`  
		Last Modified: Tue, 13 Feb 2024 11:23:44 GMT  
		Size: 462.9 KB (462884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730754a879b69b2f1c8d2c5cdb4253f98b599c910dbbcf7fad6acdfeba237837`  
		Last Modified: Tue, 13 Feb 2024 11:24:20 GMT  
		Size: 325.2 MB (325176691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01152b4a4be8a60b9847b6743d494a2d271e2337b81b51aa7fc00d9e375d392`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428873047ebe4de7e2bc7228862bc795c92d96ab03f2b22d985c9825779efb94`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a64d750f2bcd706074650135247218e86f8636d4fd95f5c827fb188b56792b`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b77568b02524cacdccef80e662f0a1696da2ddec1567d13d078b16969c61e84`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:575c728afde3af38fa0bb74b399dda7da19ef6c200cc20753a2416fd3557b274
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574914132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51fad52e928a92c21402338fbfb081aa4ffbee162cce78c4ca7e69218addbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:47:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 02:47:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 02:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 02:47:36 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 02:48:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 02:48:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:48:53 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 02:48:53 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Feb 2024 02:48:53 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 02:48:53 GMT
ARG ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
# Tue, 13 Feb 2024 02:50:06 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 02:50:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 02:50:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 02:50:14 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 02:50:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 02:50:14 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 02:50:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 02:50:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 02:50:14 GMT
USER odoo
# Tue, 13 Feb 2024 02:50:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:50:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2f618c4954544d5a1d56ef7354df8c3a0a52e4c057e074c37924915ca2fd1`  
		Last Modified: Tue, 13 Feb 2024 02:50:56 GMT  
		Size: 216.9 MB (216902917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473596c65e4b7b8b68f3b2d5b8b44b1d170a7c2d419f7047936e9222e56adb`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 2.6 MB (2635157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628656e229343de1b693a2b98cf92fb4f3b3bb43b28acb4438d79491525761f`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 462.9 KB (462916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac526a4f5c55086579dd42d39e3028d0227f59f4cf95c1d2c6ec36516246a6`  
		Last Modified: Tue, 13 Feb 2024 02:51:06 GMT  
		Size: 324.8 MB (324839606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669b77706e0456479a66acaa77278cd2edc4dcdcbc1869d9266cd2e8c157d74a`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c119d89d91134726de6e2434bea475509163ecb4f5f158cf0a1d324d76d311f7`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700729a3545140f9874d82c3ee260884aa10faa8a97115177b03e9fd8459594`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dba29eee9802bea3be780a650b079cf2c456300892d2e048f2c26d325c92cf`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:758461072f328ca7632687e38fac3a6f50f6f07e89c79bbdc460d0eb9bcbcb22
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593858486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4baadf078799c9258c9e83deb18e991d221c676fcc2d04c2be08571794c2f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:09:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 04:09:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 04:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 04:09:40 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 04:13:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 04:13:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:13:49 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 04:13:49 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Feb 2024 04:13:50 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 04:13:51 GMT
ARG ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
# Tue, 13 Feb 2024 04:16:57 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 04:17:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 04:17:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 04:17:23 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 04:17:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 04:17:28 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 04:17:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 04:17:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 04:17:31 GMT
USER odoo
# Tue, 13 Feb 2024 04:17:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:17:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47bb6241f7f89a639b08014441cb2820f9f7f4509216e43e8bbd6357c7bda0`  
		Last Modified: Tue, 13 Feb 2024 04:18:30 GMT  
		Size: 228.6 MB (228600171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9749dac12780aa7b6979dc392d78966a3978c3a71436c61a00cc276c9b3ab`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 2.9 MB (2875930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38c3b73d7742aebbefe4d2d4b68642d916e808d2f230032f15cc77e6bb0c9`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 463.0 KB (462957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df7326086e5e44119fdbd80e9f650e8c15cfc5b32609d60f25ca09dbe45c060`  
		Last Modified: Tue, 13 Feb 2024 04:18:43 GMT  
		Size: 326.6 MB (326619160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8613efa9dcdf75b6e2fc7e3dfae5d60413149f88d56583a5073de2d55b29097`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7479ed28e4ef2ae3b6a971cf9d0c59dbcd69a0e250d9ba8882b485173cc808`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4f70af51e1cb9321eea7026c2eff98944e2512a352ebeae1dfed4d95a5605`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074d491ada69bffa097e01eb33f6bc28ca4bf3b1f816ceeddacba410d7d17e8c`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:94d2609a49eedda07bcbf41b4b63aef64afcccfaaa6f191b654e29e6cedcc072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:e389356c974abea879e128248758eac5bb29f075ec5188a31dee458cb09d1589
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.3 MB (579297506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14cf0a80f7fa582355c2f2af1c3bcdeb5ec3b97cc930795181f7563c4c824bbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:18:16 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 11:19:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:19:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:19:35 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:19:36 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Feb 2024 11:19:36 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 11:19:36 GMT
ARG ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
# Tue, 13 Feb 2024 11:20:53 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 11:20:57 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 11:20:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 11:20:58 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 11:20:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 11:20:58 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 11:20:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 11:20:58 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 11:20:58 GMT
USER odoo
# Tue, 13 Feb 2024 11:20:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 11:20:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f8764e315ffe4d9162112c693dc2de9180d54741bcc86a94a2e8dc63796`  
		Last Modified: Tue, 13 Feb 2024 11:24:08 GMT  
		Size: 219.6 MB (219603078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c251911a36e7b29cdc68e2e6ad3c227877483a27881808128a45cdf7f29cd97`  
		Last Modified: Tue, 13 Feb 2024 11:23:43 GMT  
		Size: 2.6 MB (2629960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b94be8a611fcadb8c1bb3ac916cbf8b7c765cb563396dcb2461b5150d88e9`  
		Last Modified: Tue, 13 Feb 2024 11:23:44 GMT  
		Size: 462.9 KB (462884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730754a879b69b2f1c8d2c5cdb4253f98b599c910dbbcf7fad6acdfeba237837`  
		Last Modified: Tue, 13 Feb 2024 11:24:20 GMT  
		Size: 325.2 MB (325176691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01152b4a4be8a60b9847b6743d494a2d271e2337b81b51aa7fc00d9e375d392`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428873047ebe4de7e2bc7228862bc795c92d96ab03f2b22d985c9825779efb94`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a64d750f2bcd706074650135247218e86f8636d4fd95f5c827fb188b56792b`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b77568b02524cacdccef80e662f0a1696da2ddec1567d13d078b16969c61e84`  
		Last Modified: Tue, 13 Feb 2024 11:23:41 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:575c728afde3af38fa0bb74b399dda7da19ef6c200cc20753a2416fd3557b274
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574914132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51fad52e928a92c21402338fbfb081aa4ffbee162cce78c4ca7e69218addbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:47:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 02:47:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 02:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 02:47:36 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 02:48:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 02:48:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:48:53 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 02:48:53 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Feb 2024 02:48:53 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 02:48:53 GMT
ARG ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
# Tue, 13 Feb 2024 02:50:06 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 02:50:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 02:50:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 02:50:14 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 02:50:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 02:50:14 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 02:50:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 02:50:14 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 02:50:14 GMT
USER odoo
# Tue, 13 Feb 2024 02:50:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 02:50:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2f618c4954544d5a1d56ef7354df8c3a0a52e4c057e074c37924915ca2fd1`  
		Last Modified: Tue, 13 Feb 2024 02:50:56 GMT  
		Size: 216.9 MB (216902917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473596c65e4b7b8b68f3b2d5b8b44b1d170a7c2d419f7047936e9222e56adb`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 2.6 MB (2635157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628656e229343de1b693a2b98cf92fb4f3b3bb43b28acb4438d79491525761f`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 462.9 KB (462916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac526a4f5c55086579dd42d39e3028d0227f59f4cf95c1d2c6ec36516246a6`  
		Last Modified: Tue, 13 Feb 2024 02:51:06 GMT  
		Size: 324.8 MB (324839606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669b77706e0456479a66acaa77278cd2edc4dcdcbc1869d9266cd2e8c157d74a`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c119d89d91134726de6e2434bea475509163ecb4f5f158cf0a1d324d76d311f7`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700729a3545140f9874d82c3ee260884aa10faa8a97115177b03e9fd8459594`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dba29eee9802bea3be780a650b079cf2c456300892d2e048f2c26d325c92cf`  
		Last Modified: Tue, 13 Feb 2024 02:50:36 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:758461072f328ca7632687e38fac3a6f50f6f07e89c79bbdc460d0eb9bcbcb22
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593858486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4baadf078799c9258c9e83deb18e991d221c676fcc2d04c2be08571794c2f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:09:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 04:09:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 04:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 04:09:40 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 04:13:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 04:13:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:13:49 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 04:13:49 GMT
ENV ODOO_VERSION=16.0
# Tue, 13 Feb 2024 04:13:50 GMT
ARG ODOO_RELEASE=20240209
# Tue, 13 Feb 2024 04:13:51 GMT
ARG ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
# Tue, 13 Feb 2024 04:16:57 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Feb 2024 04:17:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 13 Feb 2024 04:17:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Feb 2024 04:17:23 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=69ba8f990effddcb2b9de0b3e9d5a53e98c868e3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Feb 2024 04:17:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Feb 2024 04:17:28 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Feb 2024 04:17:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Feb 2024 04:17:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Feb 2024 04:17:31 GMT
USER odoo
# Tue, 13 Feb 2024 04:17:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 04:17:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47bb6241f7f89a639b08014441cb2820f9f7f4509216e43e8bbd6357c7bda0`  
		Last Modified: Tue, 13 Feb 2024 04:18:30 GMT  
		Size: 228.6 MB (228600171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9749dac12780aa7b6979dc392d78966a3978c3a71436c61a00cc276c9b3ab`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 2.9 MB (2875930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38c3b73d7742aebbefe4d2d4b68642d916e808d2f230032f15cc77e6bb0c9`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 463.0 KB (462957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df7326086e5e44119fdbd80e9f650e8c15cfc5b32609d60f25ca09dbe45c060`  
		Last Modified: Tue, 13 Feb 2024 04:18:43 GMT  
		Size: 326.6 MB (326619160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8613efa9dcdf75b6e2fc7e3dfae5d60413149f88d56583a5073de2d55b29097`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7479ed28e4ef2ae3b6a971cf9d0c59dbcd69a0e250d9ba8882b485173cc808`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4f70af51e1cb9321eea7026c2eff98944e2512a352ebeae1dfed4d95a5605`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074d491ada69bffa097e01eb33f6bc28ca4bf3b1f816ceeddacba410d7d17e8c`  
		Last Modified: Tue, 13 Feb 2024 04:17:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:a4e061fb27f47729f536f8f6e6224cc882962da50fce10453aebe027e17199b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:71867bbac71b87148822fabe5b6b6d4f057ba52abecfdb9828540f2cb7c986a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597706488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf5bb3c65fcefbdf62e5accaf255759b7cfea6902575c31de8a396025826564`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:35:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 07:35:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 07:35:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 07:35:31 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 07:37:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 07:38:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:38:10 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 07:38:10 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 19:34:47 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 19:34:47 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 19:36:42 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 19:36:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 19:36:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 19:36:48 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 19:36:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 19:36:48 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 19:36:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 19:36:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 19:36:48 GMT
USER odoo
# Fri, 09 Feb 2024 19:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 19:36:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac85bef58e703dd1f2a6b5e92abae5881e4b24f17ab28a5a8096b5377aeabb8e`  
		Last Modified: Fri, 02 Feb 2024 07:41:06 GMT  
		Size: 233.7 MB (233729954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d882394f41f2a4c6b7c83a944ce7f1c5ef15a9912fc65853f50d0a97fdbe0`  
		Last Modified: Fri, 02 Feb 2024 07:40:38 GMT  
		Size: 2.5 MB (2526516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74632a57a875cdae24a2c30c7fe335e7dd4d38a07bb1419e5ba707147ac5033e`  
		Last Modified: Fri, 02 Feb 2024 07:40:38 GMT  
		Size: 461.9 KB (461936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0578d78c00f651689d4e1307032a7a0b19e28b3c77ad3744939e8e8c9b6a95aa`  
		Last Modified: Fri, 09 Feb 2024 19:40:44 GMT  
		Size: 330.5 MB (330537731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00551d34b90765a9ba1c62f5e3258c6d2cefaabd248a4d48e704c3700816f423`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedd37c5e5ce13c3a8d1fc1ca738153c097a89c900f0305f77cc07b73109b3d`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cc1cbcc3cf87c66d35088c89b660717776d2d943de78d5c1607555e547a404`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934e9d403d1e704aaf60360f068be995be6b2f7af7a6c0987fcce7663576a5f`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2a10d2c49a60ecf84b45addb5aa4133bca9650e8dcce707f09537f1789bbdbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592636202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dcbfbdd864a823f4330acb9d7be9fa054167376c82808e14f0e44b2e63c3896`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:32:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 02:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 02:32:42 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 02:32:42 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 02:34:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 02:35:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:35:06 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 02:35:06 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 18:41:14 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 18:43:26 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 18:43:34 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 18:43:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 18:43:34 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 18:43:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 18:43:35 GMT
USER odoo
# Fri, 09 Feb 2024 18:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 18:43:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9f9245a07d25c7260502d93847bace4fc08bb5fa8ef2f83ffce4049ff452ca`  
		Last Modified: Fri, 02 Feb 2024 02:37:50 GMT  
		Size: 231.1 MB (231117766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae5cd10dad8d1c65d89401aa8ddd719b347287b77a1e30591c2908aeb407f64`  
		Last Modified: Fri, 02 Feb 2024 02:37:30 GMT  
		Size: 2.5 MB (2519211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce15c16419ffc086802af9393d065baf1711cf9945fb2e2e9204f6bbf78c3e`  
		Last Modified: Fri, 02 Feb 2024 02:37:30 GMT  
		Size: 461.9 KB (461941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ad600a2d7389044aa4f3525f5caa896441098af2fba0780302fc8afb69cb1`  
		Last Modified: Fri, 09 Feb 2024 18:46:03 GMT  
		Size: 330.1 MB (330134713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b97473dd465c902fd21a11ff090c06e68e0c719852615b749a76c6b5a9b2fb`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e6641548b9d5edc19aca2be76499cf045006d121fe1f66c21cd24c55d5aa74`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56778f787ecff1ef13f80903379123aabe4bb1c19947c8ba8ae00d9478b1d8b`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1156bac975373ca4d7f02a734a58917835920deb276ad5a129ec5d9fdc68ca26`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:ff269c3f09a0205d0219d36074c288837bedee9247de98ce610373c70b9f5448
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614496174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efabcb2aba9c4dfcfd32b62a6f4cb4397882322c858cbd069bf5a5c2a3461a8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 00:53:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 00:53:03 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 00:53:03 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 00:58:18 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 00:58:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:46 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 00:58:47 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 19:26:57 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 19:26:58 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 19:30:08 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 19:30:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 19:30:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 19:30:27 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 19:30:29 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 19:30:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 19:30:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 19:30:32 GMT
USER odoo
# Fri, 09 Feb 2024 19:30:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 19:30:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8951dde2ff85fefb08eba04905bb7b9036eeb192a5f9e347f49800d1e17eaa0`  
		Last Modified: Fri, 02 Feb 2024 01:02:57 GMT  
		Size: 243.3 MB (243293508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0bec2d89d1cbf0e2118f298590ce1f7e03461c712154e991726afabb733e1f`  
		Last Modified: Fri, 02 Feb 2024 01:02:25 GMT  
		Size: 2.8 MB (2803398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fab5f9a8b115216c7724249ea9ebc166d270544fe47cdea2285aa7aaf5f22ac`  
		Last Modified: Fri, 02 Feb 2024 01:02:25 GMT  
		Size: 462.0 KB (461965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2a87268a74d3848da1daa184c7ecf0ae41af9db88c813d99435d3317859e7`  
		Last Modified: Fri, 09 Feb 2024 19:34:34 GMT  
		Size: 332.3 MB (332275659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e31aecc58792b6803cf4d139ed877cde88e7ca1cba30bd07761d930fc69c6de`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b598e88e58699d109c882858a08e438513354be420299fb56eb0f0481374934`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbca43ad0b9cdb2162de890b8861e8eebe359cd3f39d90075f938e9a4b116f85`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82138e24c4decd9762c7a6b07fcd15acc693190565156ac80609a851406848`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:a4e061fb27f47729f536f8f6e6224cc882962da50fce10453aebe027e17199b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:71867bbac71b87148822fabe5b6b6d4f057ba52abecfdb9828540f2cb7c986a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597706488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf5bb3c65fcefbdf62e5accaf255759b7cfea6902575c31de8a396025826564`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:35:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 07:35:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 07:35:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 07:35:31 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 07:37:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 07:38:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:38:10 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 07:38:10 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 19:34:47 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 19:34:47 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 19:36:42 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 19:36:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 19:36:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 19:36:48 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 19:36:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 19:36:48 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 19:36:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 19:36:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 19:36:48 GMT
USER odoo
# Fri, 09 Feb 2024 19:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 19:36:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac85bef58e703dd1f2a6b5e92abae5881e4b24f17ab28a5a8096b5377aeabb8e`  
		Last Modified: Fri, 02 Feb 2024 07:41:06 GMT  
		Size: 233.7 MB (233729954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d882394f41f2a4c6b7c83a944ce7f1c5ef15a9912fc65853f50d0a97fdbe0`  
		Last Modified: Fri, 02 Feb 2024 07:40:38 GMT  
		Size: 2.5 MB (2526516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74632a57a875cdae24a2c30c7fe335e7dd4d38a07bb1419e5ba707147ac5033e`  
		Last Modified: Fri, 02 Feb 2024 07:40:38 GMT  
		Size: 461.9 KB (461936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0578d78c00f651689d4e1307032a7a0b19e28b3c77ad3744939e8e8c9b6a95aa`  
		Last Modified: Fri, 09 Feb 2024 19:40:44 GMT  
		Size: 330.5 MB (330537731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00551d34b90765a9ba1c62f5e3258c6d2cefaabd248a4d48e704c3700816f423`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedd37c5e5ce13c3a8d1fc1ca738153c097a89c900f0305f77cc07b73109b3d`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cc1cbcc3cf87c66d35088c89b660717776d2d943de78d5c1607555e547a404`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934e9d403d1e704aaf60360f068be995be6b2f7af7a6c0987fcce7663576a5f`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2a10d2c49a60ecf84b45addb5aa4133bca9650e8dcce707f09537f1789bbdbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592636202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dcbfbdd864a823f4330acb9d7be9fa054167376c82808e14f0e44b2e63c3896`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:32:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 02:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 02:32:42 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 02:32:42 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 02:34:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 02:35:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:35:06 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 02:35:06 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 18:41:14 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 18:43:26 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 18:43:34 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 18:43:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 18:43:34 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 18:43:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 18:43:35 GMT
USER odoo
# Fri, 09 Feb 2024 18:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 18:43:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9f9245a07d25c7260502d93847bace4fc08bb5fa8ef2f83ffce4049ff452ca`  
		Last Modified: Fri, 02 Feb 2024 02:37:50 GMT  
		Size: 231.1 MB (231117766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae5cd10dad8d1c65d89401aa8ddd719b347287b77a1e30591c2908aeb407f64`  
		Last Modified: Fri, 02 Feb 2024 02:37:30 GMT  
		Size: 2.5 MB (2519211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce15c16419ffc086802af9393d065baf1711cf9945fb2e2e9204f6bbf78c3e`  
		Last Modified: Fri, 02 Feb 2024 02:37:30 GMT  
		Size: 461.9 KB (461941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ad600a2d7389044aa4f3525f5caa896441098af2fba0780302fc8afb69cb1`  
		Last Modified: Fri, 09 Feb 2024 18:46:03 GMT  
		Size: 330.1 MB (330134713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b97473dd465c902fd21a11ff090c06e68e0c719852615b749a76c6b5a9b2fb`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e6641548b9d5edc19aca2be76499cf045006d121fe1f66c21cd24c55d5aa74`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56778f787ecff1ef13f80903379123aabe4bb1c19947c8ba8ae00d9478b1d8b`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1156bac975373ca4d7f02a734a58917835920deb276ad5a129ec5d9fdc68ca26`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ff269c3f09a0205d0219d36074c288837bedee9247de98ce610373c70b9f5448
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614496174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efabcb2aba9c4dfcfd32b62a6f4cb4397882322c858cbd069bf5a5c2a3461a8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 00:53:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 00:53:03 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 00:53:03 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 00:58:18 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 00:58:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:46 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 00:58:47 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 19:26:57 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 19:26:58 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 19:30:08 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 19:30:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 19:30:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 19:30:27 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 19:30:29 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 19:30:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 19:30:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 19:30:32 GMT
USER odoo
# Fri, 09 Feb 2024 19:30:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 19:30:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8951dde2ff85fefb08eba04905bb7b9036eeb192a5f9e347f49800d1e17eaa0`  
		Last Modified: Fri, 02 Feb 2024 01:02:57 GMT  
		Size: 243.3 MB (243293508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0bec2d89d1cbf0e2118f298590ce1f7e03461c712154e991726afabb733e1f`  
		Last Modified: Fri, 02 Feb 2024 01:02:25 GMT  
		Size: 2.8 MB (2803398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fab5f9a8b115216c7724249ea9ebc166d270544fe47cdea2285aa7aaf5f22ac`  
		Last Modified: Fri, 02 Feb 2024 01:02:25 GMT  
		Size: 462.0 KB (461965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2a87268a74d3848da1daa184c7ecf0ae41af9db88c813d99435d3317859e7`  
		Last Modified: Fri, 09 Feb 2024 19:34:34 GMT  
		Size: 332.3 MB (332275659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e31aecc58792b6803cf4d139ed877cde88e7ca1cba30bd07761d930fc69c6de`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b598e88e58699d109c882858a08e438513354be420299fb56eb0f0481374934`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbca43ad0b9cdb2162de890b8861e8eebe359cd3f39d90075f938e9a4b116f85`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82138e24c4decd9762c7a6b07fcd15acc693190565156ac80609a851406848`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:a4e061fb27f47729f536f8f6e6224cc882962da50fce10453aebe027e17199b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:71867bbac71b87148822fabe5b6b6d4f057ba52abecfdb9828540f2cb7c986a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597706488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf5bb3c65fcefbdf62e5accaf255759b7cfea6902575c31de8a396025826564`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:35:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 07:35:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 07:35:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 07:35:31 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 07:37:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 07:38:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 07:38:10 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 07:38:10 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 19:34:47 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 19:34:47 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 19:36:42 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 19:36:47 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 19:36:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 19:36:48 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 19:36:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 19:36:48 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 19:36:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 19:36:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 19:36:48 GMT
USER odoo
# Fri, 09 Feb 2024 19:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 19:36:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac85bef58e703dd1f2a6b5e92abae5881e4b24f17ab28a5a8096b5377aeabb8e`  
		Last Modified: Fri, 02 Feb 2024 07:41:06 GMT  
		Size: 233.7 MB (233729954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d882394f41f2a4c6b7c83a944ce7f1c5ef15a9912fc65853f50d0a97fdbe0`  
		Last Modified: Fri, 02 Feb 2024 07:40:38 GMT  
		Size: 2.5 MB (2526516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74632a57a875cdae24a2c30c7fe335e7dd4d38a07bb1419e5ba707147ac5033e`  
		Last Modified: Fri, 02 Feb 2024 07:40:38 GMT  
		Size: 461.9 KB (461936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0578d78c00f651689d4e1307032a7a0b19e28b3c77ad3744939e8e8c9b6a95aa`  
		Last Modified: Fri, 09 Feb 2024 19:40:44 GMT  
		Size: 330.5 MB (330537731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00551d34b90765a9ba1c62f5e3258c6d2cefaabd248a4d48e704c3700816f423`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedd37c5e5ce13c3a8d1fc1ca738153c097a89c900f0305f77cc07b73109b3d`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cc1cbcc3cf87c66d35088c89b660717776d2d943de78d5c1607555e547a404`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934e9d403d1e704aaf60360f068be995be6b2f7af7a6c0987fcce7663576a5f`  
		Last Modified: Fri, 09 Feb 2024 19:40:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2a10d2c49a60ecf84b45addb5aa4133bca9650e8dcce707f09537f1789bbdbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592636202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dcbfbdd864a823f4330acb9d7be9fa054167376c82808e14f0e44b2e63c3896`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:32:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 02:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 02:32:42 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 02:32:42 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 02:34:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 02:35:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:35:06 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 02:35:06 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 18:41:14 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 18:43:26 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 18:43:34 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 18:43:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 18:43:34 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 18:43:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 18:43:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 18:43:35 GMT
USER odoo
# Fri, 09 Feb 2024 18:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 18:43:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9f9245a07d25c7260502d93847bace4fc08bb5fa8ef2f83ffce4049ff452ca`  
		Last Modified: Fri, 02 Feb 2024 02:37:50 GMT  
		Size: 231.1 MB (231117766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae5cd10dad8d1c65d89401aa8ddd719b347287b77a1e30591c2908aeb407f64`  
		Last Modified: Fri, 02 Feb 2024 02:37:30 GMT  
		Size: 2.5 MB (2519211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce15c16419ffc086802af9393d065baf1711cf9945fb2e2e9204f6bbf78c3e`  
		Last Modified: Fri, 02 Feb 2024 02:37:30 GMT  
		Size: 461.9 KB (461941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ad600a2d7389044aa4f3525f5caa896441098af2fba0780302fc8afb69cb1`  
		Last Modified: Fri, 09 Feb 2024 18:46:03 GMT  
		Size: 330.1 MB (330134713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b97473dd465c902fd21a11ff090c06e68e0c719852615b749a76c6b5a9b2fb`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e6641548b9d5edc19aca2be76499cf045006d121fe1f66c21cd24c55d5aa74`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56778f787ecff1ef13f80903379123aabe4bb1c19947c8ba8ae00d9478b1d8b`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1156bac975373ca4d7f02a734a58917835920deb276ad5a129ec5d9fdc68ca26`  
		Last Modified: Fri, 09 Feb 2024 18:45:21 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:ff269c3f09a0205d0219d36074c288837bedee9247de98ce610373c70b9f5448
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614496174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efabcb2aba9c4dfcfd32b62a6f4cb4397882322c858cbd069bf5a5c2a3461a8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 02 Feb 2024 00:53:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 02 Feb 2024 00:53:03 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 00:53:03 GMT
ARG TARGETARCH
# Fri, 02 Feb 2024 00:58:18 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Feb 2024 00:58:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:58:46 GMT
RUN npm install -g rtlcss
# Fri, 02 Feb 2024 00:58:47 GMT
ENV ODOO_VERSION=17.0
# Fri, 09 Feb 2024 19:26:57 GMT
ARG ODOO_RELEASE=20240209
# Fri, 09 Feb 2024 19:26:58 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 09 Feb 2024 19:30:08 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 09 Feb 2024 19:30:25 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 09 Feb 2024 19:30:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 09 Feb 2024 19:30:27 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 09 Feb 2024 19:30:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 09 Feb 2024 19:30:29 GMT
EXPOSE 8069 8071 8072
# Fri, 09 Feb 2024 19:30:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 09 Feb 2024 19:30:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 09 Feb 2024 19:30:32 GMT
USER odoo
# Fri, 09 Feb 2024 19:30:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Feb 2024 19:30:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8951dde2ff85fefb08eba04905bb7b9036eeb192a5f9e347f49800d1e17eaa0`  
		Last Modified: Fri, 02 Feb 2024 01:02:57 GMT  
		Size: 243.3 MB (243293508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0bec2d89d1cbf0e2118f298590ce1f7e03461c712154e991726afabb733e1f`  
		Last Modified: Fri, 02 Feb 2024 01:02:25 GMT  
		Size: 2.8 MB (2803398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fab5f9a8b115216c7724249ea9ebc166d270544fe47cdea2285aa7aaf5f22ac`  
		Last Modified: Fri, 02 Feb 2024 01:02:25 GMT  
		Size: 462.0 KB (461965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed2a87268a74d3848da1daa184c7ecf0ae41af9db88c813d99435d3317859e7`  
		Last Modified: Fri, 09 Feb 2024 19:34:34 GMT  
		Size: 332.3 MB (332275659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e31aecc58792b6803cf4d139ed877cde88e7ca1cba30bd07761d930fc69c6de`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b598e88e58699d109c882858a08e438513354be420299fb56eb0f0481374934`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbca43ad0b9cdb2162de890b8861e8eebe359cd3f39d90075f938e9a4b116f85`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82138e24c4decd9762c7a6b07fcd15acc693190565156ac80609a851406848`  
		Last Modified: Fri, 09 Feb 2024 19:33:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
