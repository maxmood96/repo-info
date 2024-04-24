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
$ docker pull odoo@sha256:92c3dd1ae3258370ee4bd3e1189c1cf1cb133ce4d3cbca8a30944a69b10d1487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:7507d5d0009ecefa32fc1a11c096cb8b67e8b34a7a9095ad5b14e92e812e27da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564125835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a4d8409727e445c2782c4aedbbb1ecfc2fa4385d21c9ef12e7839b691b801c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:41:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:41:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:41:41 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:41:41 GMT
ENV ODOO_VERSION=15.0
# Wed, 24 Apr 2024 13:41:41 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 13:41:41 GMT
ARG ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
# Wed, 24 Apr 2024 13:42:51 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 13:42:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 13:42:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 13:42:56 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 13:42:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 13:42:56 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 13:42:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 13:42:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 13:42:56 GMT
USER odoo
# Wed, 24 Apr 2024 13:42:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:42:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844298f77b5290c77d07c814122b04a5a0c27837cb2bdc442a97a023172f418`  
		Last Modified: Wed, 24 Apr 2024 13:44:26 GMT  
		Size: 220.3 MB (220294160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8352c49f618af1258a6a53a2b11a11831bdec468a8a9cfb443fe2064119b09`  
		Last Modified: Wed, 24 Apr 2024 13:44:02 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637b99e2b29aaa41f154e2a407ca74a4895714a3e8bcfd19aebecead0a2f61cb`  
		Last Modified: Wed, 24 Apr 2024 13:44:01 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53ac5d444f3fe18e320950475149eab5541cc4969ddaea47a5d624082535be5`  
		Last Modified: Wed, 24 Apr 2024 13:44:34 GMT  
		Size: 309.3 MB (309309681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54af53156a66914161cad232ac68d788848e8aa38b48f4a366d4b94901a6cac`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc92630e90644ec495762be20b3fcba68728d26207cc66773fa2bedce96cf2`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33e1546538a07b7d4f85eeba4a9bec669dbd2013e4ad0aad9dd96454e9c5d0e`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca1198b4724bfb36c592e45a62d3616f170cbf6c45bbfe25c6281121214a0a5`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:92c3dd1ae3258370ee4bd3e1189c1cf1cb133ce4d3cbca8a30944a69b10d1487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:7507d5d0009ecefa32fc1a11c096cb8b67e8b34a7a9095ad5b14e92e812e27da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564125835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a4d8409727e445c2782c4aedbbb1ecfc2fa4385d21c9ef12e7839b691b801c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:41:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:41:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:41:41 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:41:41 GMT
ENV ODOO_VERSION=15.0
# Wed, 24 Apr 2024 13:41:41 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 13:41:41 GMT
ARG ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
# Wed, 24 Apr 2024 13:42:51 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 13:42:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 13:42:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 13:42:56 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=9f48721922de9b671f233a979117757b1f2422fc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 13:42:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 13:42:56 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 13:42:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 13:42:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 13:42:56 GMT
USER odoo
# Wed, 24 Apr 2024 13:42:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:42:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844298f77b5290c77d07c814122b04a5a0c27837cb2bdc442a97a023172f418`  
		Last Modified: Wed, 24 Apr 2024 13:44:26 GMT  
		Size: 220.3 MB (220294160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8352c49f618af1258a6a53a2b11a11831bdec468a8a9cfb443fe2064119b09`  
		Last Modified: Wed, 24 Apr 2024 13:44:02 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637b99e2b29aaa41f154e2a407ca74a4895714a3e8bcfd19aebecead0a2f61cb`  
		Last Modified: Wed, 24 Apr 2024 13:44:01 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53ac5d444f3fe18e320950475149eab5541cc4969ddaea47a5d624082535be5`  
		Last Modified: Wed, 24 Apr 2024 13:44:34 GMT  
		Size: 309.3 MB (309309681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54af53156a66914161cad232ac68d788848e8aa38b48f4a366d4b94901a6cac`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc92630e90644ec495762be20b3fcba68728d26207cc66773fa2bedce96cf2`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33e1546538a07b7d4f85eeba4a9bec669dbd2013e4ad0aad9dd96454e9c5d0e`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca1198b4724bfb36c592e45a62d3616f170cbf6c45bbfe25c6281121214a0a5`  
		Last Modified: Wed, 24 Apr 2024 13:43:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:dd7e0df431d8ded05c52ac46d12e66bb87341e1e67a5c73dc98635890251a764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:275a9149cece67bfe41598c3e56477be47ca38cdccf113ca7568679e55d7bd35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583150393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee46d24aba9c2f2b861d37aa54e93f944856d631d079587c97ef50070dbaa71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:37:44 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 13:38:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:39:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:39:03 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:39:04 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 13:39:04 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 13:39:04 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 13:40:23 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 13:40:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 13:40:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 13:40:27 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 13:40:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 13:40:28 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 13:40:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 13:40:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 13:40:28 GMT
USER odoo
# Wed, 24 Apr 2024 13:40:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:40:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b10b512b443a629773a6151d15753e241d9c89e695fc8769376c36816475426`  
		Last Modified: Wed, 24 Apr 2024 13:43:38 GMT  
		Size: 219.6 MB (219605091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f954fd7c585d0f341393980922d2e5b0e829b07f8a927c1ef49cb5b9a1e28`  
		Last Modified: Wed, 24 Apr 2024 13:43:13 GMT  
		Size: 2.6 MB (2631177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255380b0477fe6a4565c69b731391d7194a57d85be15c9c95945f92214994e2f`  
		Last Modified: Wed, 24 Apr 2024 13:43:12 GMT  
		Size: 458.4 KB (458387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd57749be81af144d4c22ab1285dc79f86275b5b3c43e23a0408e81c720ae80a`  
		Last Modified: Wed, 24 Apr 2024 13:43:51 GMT  
		Size: 329.0 MB (329019011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f649f9c1aeaf34695d1d85229d6a20f8ba38dd2162990e98ba8ed32b89f6f7ac`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382581a51590a8cbddbd7f11e4e8b7013e61daa75ddf48e41eb42476f1aa6a09`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e196da29193c4add7566aba6e0159eb4a23167fcf459093b035a2454e2feca6`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650aebbdddd1044c5ecf77ebccb020156baca31715b08ace38579d59361d4b0`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8c7bb204c403953d06a319d296dd745bbc2bf383fa66b8846a15e44595447e9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578754105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37eaac62a52a5d1206328db426a9ae0bbb0a5c7172904cc380aa9a2080d838fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 04:46:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 04:46:24 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 04:46:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 04:46:24 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 04:46:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 04:46:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 04:46:24 GMT
USER odoo
# Wed, 24 Apr 2024 04:46:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:46:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4073a3095218233668eba607b98269dee24e5708986a15a4578d4c0acf3f399`  
		Last Modified: Wed, 24 Apr 2024 04:47:11 GMT  
		Size: 328.7 MB (328666473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3248f2359c1295611f5b21b00cce27337e8bc1cf9a525cbf8f71b6cd7596a367`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc71ceeba51f1fa58b766c0b6809582b6031cd578cf0b01cbe5863007d23d9c5`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840c86734b8dfeb2d3c7e4bc8d630b9c1055715b61d7d38a3732863e2ca1285`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37dafa948f61840b414363a4ea8caf26ee532fd9035340ae1b99e2dfacc4db`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:837e940bdce4a7b00f544aa877f1a16beb67e73a12c0c0d12dc3ef71f2fa6ef3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597695567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f21a028cc88fb439f4a66c9389a8518acc0fccbe3bef5343cac42939f58173`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 05:54:44 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 05:54:45 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 05:57:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 05:57:30 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 05:57:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 05:57:31 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 05:57:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 05:57:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 05:57:33 GMT
USER odoo
# Wed, 24 Apr 2024 05:57:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 05:57:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0de980b91e84a4461dde7734420d53311f24d6aaf8c89549c0f373bf9cee55`  
		Last Modified: Wed, 24 Apr 2024 05:58:35 GMT  
		Size: 330.4 MB (330443848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c213a9417b8b46f03d0be61294c06f5d6353b161c13854dd2e42a937cf18ed86`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc02886836a694ff5dad283cc31b5da6fd20a05d2c3907e2882e01eded51bcf4`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0905b66303a77077715efc929f584f536be3cc7c35d36964eafc01f4b5515d`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e11db646b83c30707b2c35571719516f9d274e6f871b8a4fc46a73ecb5897bc`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:dd7e0df431d8ded05c52ac46d12e66bb87341e1e67a5c73dc98635890251a764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:275a9149cece67bfe41598c3e56477be47ca38cdccf113ca7568679e55d7bd35
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583150393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee46d24aba9c2f2b861d37aa54e93f944856d631d079587c97ef50070dbaa71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:37:44 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 13:38:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:39:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:39:03 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:39:04 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 13:39:04 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 13:39:04 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 13:40:23 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 13:40:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 13:40:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 13:40:27 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 13:40:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 13:40:28 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 13:40:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 13:40:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 13:40:28 GMT
USER odoo
# Wed, 24 Apr 2024 13:40:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:40:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b10b512b443a629773a6151d15753e241d9c89e695fc8769376c36816475426`  
		Last Modified: Wed, 24 Apr 2024 13:43:38 GMT  
		Size: 219.6 MB (219605091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f954fd7c585d0f341393980922d2e5b0e829b07f8a927c1ef49cb5b9a1e28`  
		Last Modified: Wed, 24 Apr 2024 13:43:13 GMT  
		Size: 2.6 MB (2631177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255380b0477fe6a4565c69b731391d7194a57d85be15c9c95945f92214994e2f`  
		Last Modified: Wed, 24 Apr 2024 13:43:12 GMT  
		Size: 458.4 KB (458387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd57749be81af144d4c22ab1285dc79f86275b5b3c43e23a0408e81c720ae80a`  
		Last Modified: Wed, 24 Apr 2024 13:43:51 GMT  
		Size: 329.0 MB (329019011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f649f9c1aeaf34695d1d85229d6a20f8ba38dd2162990e98ba8ed32b89f6f7ac`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382581a51590a8cbddbd7f11e4e8b7013e61daa75ddf48e41eb42476f1aa6a09`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e196da29193c4add7566aba6e0159eb4a23167fcf459093b035a2454e2feca6`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3650aebbdddd1044c5ecf77ebccb020156baca31715b08ace38579d59361d4b0`  
		Last Modified: Wed, 24 Apr 2024 13:43:10 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8c7bb204c403953d06a319d296dd745bbc2bf383fa66b8846a15e44595447e9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578754105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37eaac62a52a5d1206328db426a9ae0bbb0a5c7172904cc380aa9a2080d838fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 04:44:58 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 04:46:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 04:46:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 04:46:24 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 04:46:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 04:46:24 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 04:46:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 04:46:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 04:46:24 GMT
USER odoo
# Wed, 24 Apr 2024 04:46:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 04:46:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4073a3095218233668eba607b98269dee24e5708986a15a4578d4c0acf3f399`  
		Last Modified: Wed, 24 Apr 2024 04:47:11 GMT  
		Size: 328.7 MB (328666473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3248f2359c1295611f5b21b00cce27337e8bc1cf9a525cbf8f71b6cd7596a367`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc71ceeba51f1fa58b766c0b6809582b6031cd578cf0b01cbe5863007d23d9c5`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0840c86734b8dfeb2d3c7e4bc8d630b9c1055715b61d7d38a3732863e2ca1285`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37dafa948f61840b414363a4ea8caf26ee532fd9035340ae1b99e2dfacc4db`  
		Last Modified: Wed, 24 Apr 2024 04:46:40 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:837e940bdce4a7b00f544aa877f1a16beb67e73a12c0c0d12dc3ef71f2fa6ef3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597695567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f21a028cc88fb439f4a66c9389a8518acc0fccbe3bef5343cac42939f58173`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Wed, 24 Apr 2024 05:54:44 GMT
ARG ODOO_RELEASE=20240416
# Wed, 24 Apr 2024 05:54:45 GMT
ARG ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
# Wed, 24 Apr 2024 05:57:16 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 24 Apr 2024 05:57:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 24 Apr 2024 05:57:30 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=d9418fee3ef105b40a58d89b8c7c500d34743ed5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 24 Apr 2024 05:57:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Apr 2024 05:57:31 GMT
EXPOSE 8069 8071 8072
# Wed, 24 Apr 2024 05:57:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Apr 2024 05:57:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 24 Apr 2024 05:57:33 GMT
USER odoo
# Wed, 24 Apr 2024 05:57:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 05:57:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0de980b91e84a4461dde7734420d53311f24d6aaf8c89549c0f373bf9cee55`  
		Last Modified: Wed, 24 Apr 2024 05:58:35 GMT  
		Size: 330.4 MB (330443848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c213a9417b8b46f03d0be61294c06f5d6353b161c13854dd2e42a937cf18ed86`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc02886836a694ff5dad283cc31b5da6fd20a05d2c3907e2882e01eded51bcf4`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0905b66303a77077715efc929f584f536be3cc7c35d36964eafc01f4b5515d`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e11db646b83c30707b2c35571719516f9d274e6f871b8a4fc46a73ecb5897bc`  
		Last Modified: Wed, 24 Apr 2024 05:57:49 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:874573f6ea07fb2b2abcf188c6562f0d0a2d4ae3ff5dc35c9e4ec60a97b46a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:fe0791861eb75ceb45c7e68b3c239c7f960e6ecf3119f33320164b8f8ac4e7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.9 MB (601936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd358de70883c9f901b836fba7e30c0968fe7dc9b6f69c3a78f71b8a11e5f00b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:22:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 05:22:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 05:22:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:22:36 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 05:24:47 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 05:25:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:25:01 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 05:25:01 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 21:53:02 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:53:08 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:53:08 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:53:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:53:08 GMT
USER odoo
# Tue, 16 Apr 2024 21:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b654cdca6f84d6c42697064da4d9c97d2f2ddeec98527c983a27266adb432a`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 233.7 MB (233722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d1b850436c5dde7a24152062ed67a4c7d61249c361e63f2b17734922aaa10`  
		Last Modified: Tue, 16 Apr 2024 05:27:30 GMT  
		Size: 2.5 MB (2530416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac1b49930b0907c0df875817503ccf8aafd0e1a3d61414b4f938eca69179a`  
		Last Modified: Tue, 16 Apr 2024 05:27:29 GMT  
		Size: 459.4 KB (459352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402b412e6d22febacf7efb25f61e5d1deaa74105552d2d2d7ae27d4b05de77e6`  
		Last Modified: Tue, 16 Apr 2024 21:57:08 GMT  
		Size: 334.8 MB (334781962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ff767f8568c474ad33f147bb043af427930e6dde7135f294c3cae498e6487`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db1829567ac26e8e72330a0813fece3e091f1199941032967c83ae7d2bc1c38`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba18450f78d3869005992ea8f6255f848a6010301bc2f776c53df9fa56cdfd`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230458b6a0f97567368180519d0f8477065a176c14e972cabd6dce941570c85`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1afb61a2f2ea4969f7c1c4b94af05340c8e771b7a0582886da3e2466073882f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6603c5e3616c65462431fd2045863d051a7385613bd636193f35f685273666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:06:10 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:06:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:06:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:06:18 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:06:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:06:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:06:18 GMT
USER odoo
# Tue, 16 Apr 2024 22:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:06:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867fb137574bcce6eeb7b05beac1823d426fbafdb7533b87d7bc1320991311`  
		Last Modified: Tue, 16 Apr 2024 22:08:46 GMT  
		Size: 334.4 MB (334394960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab792be17c768d7091e22a1b08648376e901ad355178de758c34a5a28604fe`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046ac664962865859052eef31c139a4ea7821c75b735b1335c6e9f4c4c79131`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4a1ea72a4d6c32f31b265fbf3af71ae15dae3a2091e83acb278ea6dabadd0`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa77e53029620532c126dd38559036a440cf1050b88c32cbffc12beb42e448ee`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:5a4581819812482c0b47684711acd4738921e450691c1ab1504a23cdffea9ee4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409c8fb6e654df10a40b348cef12dcfba4d5acf0a0e36d444c1a1ea275fb35ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:20:21 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:20:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:20:36 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:20:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:20:37 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:20:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:20:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:20:39 GMT
USER odoo
# Tue, 16 Apr 2024 22:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:20:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472bba33d86762aeeb53906f1904a3e5c6bf0de11239c11802419f3ad72c1369`  
		Last Modified: Tue, 16 Apr 2024 22:24:58 GMT  
		Size: 336.5 MB (336532414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6c78c91f4cb9a5d56d431bb0bd8d491f83631e63e39ce583a990683626015d`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e7285a0d23794ef8f5ad1731a14ab1d5c1ff039209a5a2b9645740047f90`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b5c1a609c962eb44957b4e4e3c18b01edebc3376121556fbdd16508a1f101`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7b5ef5c8c02170ef3c880ab565ad8b03f28e5d753f1aefd72a9d9f83b98a9`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:874573f6ea07fb2b2abcf188c6562f0d0a2d4ae3ff5dc35c9e4ec60a97b46a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:fe0791861eb75ceb45c7e68b3c239c7f960e6ecf3119f33320164b8f8ac4e7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.9 MB (601936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd358de70883c9f901b836fba7e30c0968fe7dc9b6f69c3a78f71b8a11e5f00b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:22:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 05:22:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 05:22:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:22:36 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 05:24:47 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 05:25:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:25:01 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 05:25:01 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 21:53:02 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:53:08 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:53:08 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:53:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:53:08 GMT
USER odoo
# Tue, 16 Apr 2024 21:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b654cdca6f84d6c42697064da4d9c97d2f2ddeec98527c983a27266adb432a`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 233.7 MB (233722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d1b850436c5dde7a24152062ed67a4c7d61249c361e63f2b17734922aaa10`  
		Last Modified: Tue, 16 Apr 2024 05:27:30 GMT  
		Size: 2.5 MB (2530416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac1b49930b0907c0df875817503ccf8aafd0e1a3d61414b4f938eca69179a`  
		Last Modified: Tue, 16 Apr 2024 05:27:29 GMT  
		Size: 459.4 KB (459352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402b412e6d22febacf7efb25f61e5d1deaa74105552d2d2d7ae27d4b05de77e6`  
		Last Modified: Tue, 16 Apr 2024 21:57:08 GMT  
		Size: 334.8 MB (334781962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ff767f8568c474ad33f147bb043af427930e6dde7135f294c3cae498e6487`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db1829567ac26e8e72330a0813fece3e091f1199941032967c83ae7d2bc1c38`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba18450f78d3869005992ea8f6255f848a6010301bc2f776c53df9fa56cdfd`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230458b6a0f97567368180519d0f8477065a176c14e972cabd6dce941570c85`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1afb61a2f2ea4969f7c1c4b94af05340c8e771b7a0582886da3e2466073882f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6603c5e3616c65462431fd2045863d051a7385613bd636193f35f685273666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:06:10 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:06:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:06:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:06:18 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:06:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:06:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:06:18 GMT
USER odoo
# Tue, 16 Apr 2024 22:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:06:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867fb137574bcce6eeb7b05beac1823d426fbafdb7533b87d7bc1320991311`  
		Last Modified: Tue, 16 Apr 2024 22:08:46 GMT  
		Size: 334.4 MB (334394960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab792be17c768d7091e22a1b08648376e901ad355178de758c34a5a28604fe`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046ac664962865859052eef31c139a4ea7821c75b735b1335c6e9f4c4c79131`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4a1ea72a4d6c32f31b265fbf3af71ae15dae3a2091e83acb278ea6dabadd0`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa77e53029620532c126dd38559036a440cf1050b88c32cbffc12beb42e448ee`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5a4581819812482c0b47684711acd4738921e450691c1ab1504a23cdffea9ee4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409c8fb6e654df10a40b348cef12dcfba4d5acf0a0e36d444c1a1ea275fb35ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:20:21 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:20:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:20:36 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:20:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:20:37 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:20:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:20:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:20:39 GMT
USER odoo
# Tue, 16 Apr 2024 22:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:20:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472bba33d86762aeeb53906f1904a3e5c6bf0de11239c11802419f3ad72c1369`  
		Last Modified: Tue, 16 Apr 2024 22:24:58 GMT  
		Size: 336.5 MB (336532414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6c78c91f4cb9a5d56d431bb0bd8d491f83631e63e39ce583a990683626015d`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e7285a0d23794ef8f5ad1731a14ab1d5c1ff039209a5a2b9645740047f90`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b5c1a609c962eb44957b4e4e3c18b01edebc3376121556fbdd16508a1f101`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7b5ef5c8c02170ef3c880ab565ad8b03f28e5d753f1aefd72a9d9f83b98a9`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:874573f6ea07fb2b2abcf188c6562f0d0a2d4ae3ff5dc35c9e4ec60a97b46a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:fe0791861eb75ceb45c7e68b3c239c7f960e6ecf3119f33320164b8f8ac4e7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.9 MB (601936924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd358de70883c9f901b836fba7e30c0968fe7dc9b6f69c3a78f71b8a11e5f00b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:22:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 05:22:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 05:22:36 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:22:36 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 05:24:47 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 05:25:00 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:25:01 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 05:25:01 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 21:51:10 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 21:53:02 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 21:53:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 21:53:08 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 21:53:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 21:53:08 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 21:53:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 21:53:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 21:53:08 GMT
USER odoo
# Tue, 16 Apr 2024 21:53:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 21:53:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b654cdca6f84d6c42697064da4d9c97d2f2ddeec98527c983a27266adb432a`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 233.7 MB (233722956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d1b850436c5dde7a24152062ed67a4c7d61249c361e63f2b17734922aaa10`  
		Last Modified: Tue, 16 Apr 2024 05:27:30 GMT  
		Size: 2.5 MB (2530416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac1b49930b0907c0df875817503ccf8aafd0e1a3d61414b4f938eca69179a`  
		Last Modified: Tue, 16 Apr 2024 05:27:29 GMT  
		Size: 459.4 KB (459352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402b412e6d22febacf7efb25f61e5d1deaa74105552d2d2d7ae27d4b05de77e6`  
		Last Modified: Tue, 16 Apr 2024 21:57:08 GMT  
		Size: 334.8 MB (334781962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445ff767f8568c474ad33f147bb043af427930e6dde7135f294c3cae498e6487`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db1829567ac26e8e72330a0813fece3e091f1199941032967c83ae7d2bc1c38`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba18450f78d3869005992ea8f6255f848a6010301bc2f776c53df9fa56cdfd`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5230458b6a0f97567368180519d0f8477065a176c14e972cabd6dce941570c85`  
		Last Modified: Tue, 16 Apr 2024 21:56:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1afb61a2f2ea4969f7c1c4b94af05340c8e771b7a0582886da3e2466073882f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596909367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6603c5e3616c65462431fd2045863d051a7385613bd636193f35f685273666`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:31:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 03:31:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 03:31:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 03:31:30 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 03:33:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 03:34:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:34:12 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 03:34:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:04:03 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:06:10 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:06:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:06:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:06:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:06:18 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:06:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:06:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:06:18 GMT
USER odoo
# Tue, 16 Apr 2024 22:06:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:06:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb267bd0bc3c1bc17901616c65684b8d4718d5452f305bf7630a0a8b66e2ad32`  
		Last Modified: Tue, 16 Apr 2024 03:37:09 GMT  
		Size: 231.1 MB (231128831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2afc515c437216aa0bf88cc6798a71595a3d60f075784a8cd2d7fc970df40`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 2.5 MB (2523426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bdbe722fe8856cea412df162f8108a5fd2656cb057e5e9f852089cf20d4c71`  
		Last Modified: Tue, 16 Apr 2024 03:36:49 GMT  
		Size: 459.4 KB (459390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867fb137574bcce6eeb7b05beac1823d426fbafdb7533b87d7bc1320991311`  
		Last Modified: Tue, 16 Apr 2024 22:08:46 GMT  
		Size: 334.4 MB (334394960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab792be17c768d7091e22a1b08648376e901ad355178de758c34a5a28604fe`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046ac664962865859052eef31c139a4ea7821c75b735b1335c6e9f4c4c79131`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac4a1ea72a4d6c32f31b265fbf3af71ae15dae3a2091e83acb278ea6dabadd0`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa77e53029620532c126dd38559036a440cf1050b88c32cbffc12beb42e448ee`  
		Last Modified: Tue, 16 Apr 2024 22:08:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5a4581819812482c0b47684711acd4738921e450691c1ab1504a23cdffea9ee4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409c8fb6e654df10a40b348cef12dcfba4d5acf0a0e36d444c1a1ea275fb35ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 02:21:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 16 Apr 2024 02:21:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 16 Apr 2024 02:21:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 02:21:05 GMT
ARG TARGETARCH
# Tue, 16 Apr 2024 02:27:11 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 16 Apr 2024 02:27:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:27:42 GMT
RUN npm install -g rtlcss
# Tue, 16 Apr 2024 02:27:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_RELEASE=20240416
# Tue, 16 Apr 2024 22:16:47 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Tue, 16 Apr 2024 22:20:21 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Apr 2024 22:20:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Apr 2024 22:20:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Apr 2024 22:20:36 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Apr 2024 22:20:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Apr 2024 22:20:37 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Apr 2024 22:20:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Apr 2024 22:20:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Apr 2024 22:20:39 GMT
USER odoo
# Tue, 16 Apr 2024 22:20:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 22:20:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5e378bf77d1d779985aaeb44c0172f6177d67b64e3085d59a3315e93b67a0`  
		Last Modified: Tue, 16 Apr 2024 02:34:31 GMT  
		Size: 243.3 MB (243300301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1778475e12f3232cd522b672bc8c8e128cb54e5cbf9eabc467cd143ad9e310`  
		Last Modified: Tue, 16 Apr 2024 02:33:58 GMT  
		Size: 2.8 MB (2806132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155b1966fde8cbcc43c9f7c7cc6d8a7ecf2518a2d0fe40e9afdfd234c3fa0c86`  
		Last Modified: Tue, 16 Apr 2024 02:33:57 GMT  
		Size: 459.4 KB (459384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472bba33d86762aeeb53906f1904a3e5c6bf0de11239c11802419f3ad72c1369`  
		Last Modified: Tue, 16 Apr 2024 22:24:58 GMT  
		Size: 336.5 MB (336532414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6c78c91f4cb9a5d56d431bb0bd8d491f83631e63e39ce583a990683626015d`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e7285a0d23794ef8f5ad1731a14ab1d5c1ff039209a5a2b9645740047f90`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b5c1a609c962eb44957b4e4e3c18b01edebc3376121556fbdd16508a1f101`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7b5ef5c8c02170ef3c880ab565ad8b03f28e5d753f1aefd72a9d9f83b98a9`  
		Last Modified: Tue, 16 Apr 2024 22:24:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
