## `odoo:latest`

```console
$ docker pull odoo@sha256:b1309b954d5ae10482a76aa1af95bcf00050f9393e54828ca156721b9dd29e50
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
$ docker pull odoo@sha256:203fd4b933c18268c117b5c2e671d89de5cb8676290595034f346c7f04b25346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702858293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855474d437af8645d32a6834473afb08559cbed87fccf8d2f6b5dd9407ac5d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:00 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:00 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa6831676b190d2d5c94bebb83e2d7cd548fca345b58005e187b8c00173ba4`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 254.6 MB (254568981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982dac0b7116a77d0eb99ee64e15b332d2cf2f96cebe15d2aa5bcb2d9204d756`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 14.4 MB (14360003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f028cd970fe13e97149da5e7f82e1c550bc50f2418dd6011df4619970e969f6`  
		Last Modified: Wed, 15 Apr 2026 20:51:25 GMT  
		Size: 481.4 KB (481366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ff53452d59ba35b1bd4b37ff467f6bb3880f5cce747216fdba4dbdf132e80`  
		Last Modified: Wed, 15 Apr 2026 20:51:42 GMT  
		Size: 403.7 MB (403712522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73630db1a964b498227c4f86424955d1c411538db2a20435744280eb1f9717ff`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d081f790e2cfe3abfa8c77cee76a77914248582f099ace5a1e20e9047fc4bb5`  
		Last Modified: Wed, 15 Apr 2026 20:51:28 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4cc5f93bd32323f0de1f58dd576ef83f84a1bc6eccc844b24d3ef14f207c3`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea73638335432cdad3c918408fcfded01b1405664cff7ac8506b290783c9d5`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:91c3684489350a201530f634f1552067930cc2bf64b4734ac48e222f5dc2e697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6892742651b994073abb1090a7e90ea8f972ed048f2756647081f920b1cd78a`

```dockerfile
```

-	Layers:
	-	`sha256:32480b99579928e5f58c073257cddce4d5ee82d9845e9dff3f1c239edb083e1c`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 70.0 MB (69986881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88a36028d6640f54fbca3cb33a441005382e1cb6d9b075c9010c7d730e8c16c`  
		Last Modified: Wed, 15 Apr 2026 20:51:26 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b03cc2fef19b099c21728ff00dd9adf63c1a284970b68757f4cafa777416dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.2 MB (699214693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8b22aa944d037587c91ba8ac8bf9784a173ee9c51279ca326ad4cf337ac12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:17 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f3e489f476902259b1bc1a369e63e4809cc22574b7c0c9d7b9fb0a1ca5124`  
		Last Modified: Wed, 15 Apr 2026 20:52:28 GMT  
		Size: 252.0 MB (251996977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd763d85262711f9837b628e3300d4935048ad99b8de3992a4fb29fa9f25c`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 14.3 MB (14340843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8355eee5c2271a157cd610a9d3d833d13f83cc5f93349ad0e991202f0d5d5`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 481.3 KB (481292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373fccc9b39bc95f6c8fe75ab832c594126aa9f0b97ef7c45eba05b36c20a8f`  
		Last Modified: Wed, 15 Apr 2026 20:52:31 GMT  
		Size: 403.5 MB (403517357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b3bec6120f3993e425e937df871efe1fe55cb9b3b215456296b98b7a55b3b5`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140fc9b0365e2b42fc087bbfb151f1acc84a2a98ae3a4d81bddf5c593bbc59d0`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25abd3207920dd469e960eae98e11e44f77c87c176b6fa71043c41cde68642e5`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea3afe04b0d7a9325fce3ea62ed44eac45e665c4dd7bfda8ad6b0f66af848f`  
		Last Modified: Wed, 15 Apr 2026 20:52:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:308a050c74211c7285f0b974d3a33d31b10c41a1b7ae69a98dc43ed381c580d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261935b51308992317a71304703ebbb4364ea334cfabdaecf74b8e417c41c103`

```dockerfile
```

-	Layers:
	-	`sha256:0ca8ad645980fc26d92ab6c47b5dd33a2f9486fa53cf3fe1790b21371bdce16c`  
		Last Modified: Wed, 15 Apr 2026 20:52:23 GMT  
		Size: 70.0 MB (69994168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02593a4bab326b36fbb467b3dff444e7294144d4ceb74598f1e995d53793306d`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:087480bffa7e68cc5dddd001504af53923ee4aa1f4b665eef5108bf77aab2087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.0 MB (719013665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ed7eccbe507c9454de569ec64657032216848e6b617d055a7c2c6ee104a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 22:11:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:11:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
USER odoo
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d300d3e84719cea202904a8e5ca0786e9fea0d6d4d6858f3da33405553073`  
		Last Modified: Wed, 15 Apr 2026 22:17:52 GMT  
		Size: 404.2 MB (404211454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432b5a45562f2f4c3b31e2fedd997d7635ebdcc7c279dbddd2662476a35911b`  
		Last Modified: Wed, 15 Apr 2026 22:17:39 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba7b9ff260f0c5bde6d56479d191cc96520d4657d9f1ac5bb5b3d593ff58f8`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f381381dd7596b8eddbd9df8b74602e34d0e8453863a22ab0dc1cb37833dce`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871085cd3fd32e086680453022914a22a3391e0851d133c92366e39c5d6216c2`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:3c23d345179d740cb0f19de9c2a0c8e48b04716294860f54fa9214d82099b7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d3e0665e4db8d1045fd4a44596ba2894e685052865fc8e4368f58424085d54`

```dockerfile
```

-	Layers:
	-	`sha256:b3b85b8c5e943bccb0dd3d10303ba0969576284ba049b5787b3882d4cb760575`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 70.0 MB (69995270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b50952403bf0f989c877184390e524e43cd625037b5be1d156be2dd0be0db43`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
