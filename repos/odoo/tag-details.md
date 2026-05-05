<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260504`](#odoo170-20260504)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260504`](#odoo180-20260504)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260504`](#odoo190-20260504)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:f4d974041d580ef358ab2d7a49a67439252797a791b7799d3a3432da3ac92722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:9d08fc37124903186688d37db468f0748b9d5bc58bd0163c46c620297a8c9c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.4 MB (610424871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee58cfee7b0e452a99a8c2751092a7c023dde9ff1e3cfbb5e4ca0949bdae583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:36:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:36:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:36:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:36:04 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:36:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:44:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:44:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:44:41 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 22:44:41 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:44:41 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 22:54:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:54:15 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:54:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:54:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:54:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:54:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:54:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:54:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:54:15 GMT
USER odoo
# Mon, 04 May 2026 22:54:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:54:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f07b28e696326f33e45717d0945d9e30bdd52fa06871c2965aa15493c625cc`  
		Last Modified: Mon, 04 May 2026 22:55:38 GMT  
		Size: 233.8 MB (233833925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ce7958885dd8bdb7eb908cf494ab23c383940fe7731f7131a61da5700e505`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 2.6 MB (2603708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11095ce88b19f683925f1d827af30f1ad3e6ddbaa00d31f675f768f9028b8158`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 484.0 KB (483986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d8bbb79c2369a09568c4d034978cecb4a974e41566fdaaacdaad54ae5507a`  
		Last Modified: Mon, 04 May 2026 22:55:40 GMT  
		Size: 343.8 MB (343764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8f1fe54e4a1154791c532de5971e24e2bf8c313618684c57b8d94bb882695f`  
		Last Modified: Mon, 04 May 2026 22:55:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1562909d2050d26273702aeabbe138138f18e250bf12ba10ebc082a48dffac`  
		Last Modified: Mon, 04 May 2026 22:55:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2447b5e9573353e9306860cb53b2ad373a2f86623141bf52831dc3e0858a3`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df16dc059796dc207cce0d58fe9d2aa9aa7b55212a80c56a25e6cbbbaf09de4`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b0898b6d4c32ef9faa07c5d17c5807ef9f32d21c6230793f50da39dcb5ef6180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42904899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70c47037b77643a9fdd234a6a3c1afeca523018c05969e28b1b13ab05fc325`

```dockerfile
```

-	Layers:
	-	`sha256:721d2008ba24d5e23e325c6ba45f6cce4c6845d358c5aed6fbb3e480e1aa2021`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 42.9 MB (42878109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ae742805287879f601e19685eb1e74d186f8d1214566262f95889d39a34bc`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 26.8 KB (26790 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:436f787cb65d226ad7b4ebcdb0afad5570d92bf089e9653154565bd45c3e4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605274803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c41ce03faa12004338e59acd4328de63e7de2a79fff13d6d9bc5d30fd9d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:17 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:31 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:31 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:31 GMT
USER odoo
# Mon, 04 May 2026 20:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea59999641de59431037ca45a7bff25898c1b54dda0cea66b896eee9edba31c`  
		Last Modified: Mon, 04 May 2026 20:58:11 GMT  
		Size: 231.2 MB (231202109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e023a7d4e854b293eaaf9af326db95df181fadb3d7c3ebe1d3242ff1e977a1`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 2.6 MB (2598189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff26802bed98b8e6c8a44783691cd7f34b94cf7e3a676835c3a2e86827a15d0`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 484.0 KB (484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197540263cb05b1d2a3ba789fa3e02c026c42823ae543a0b784dad5541935c3`  
		Last Modified: Mon, 04 May 2026 20:58:16 GMT  
		Size: 343.4 MB (343381521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc04332b9e6d324b7c774b8d6ec3af2d44f140b7dce7272a6c7dadb04201a9`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215d70cd3f71c87e08a7bd6c89437273ee940c0e178776e7928f443cd5be40e`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36018947d52acd91d4ce275a6470517432e0ca66620b0572b9d803b8358302c3`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f49ad7b2b14ecce6c48cc6b3bfbe70f87184f19e372ab9c9bcd26897b481f`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1a7dee8e69d35bbf9e777d2c90a0b3d11c6a55334c094792d5b6a1025d4af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42911559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd91dbb69006c59d7a87b308d36b666122abd383422b429d976123ddd031234`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f7ec0101ee208525b5cddc5ef91270681bdbca1759373a1483faa486cbda7`  
		Last Modified: Mon, 04 May 2026 20:57:55 GMT  
		Size: 42.9 MB (42884616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0b27109c15adb36fa43396ef4ad7e01fbdb3e752b04d242d9f83285a2b1daf`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:f4d974041d580ef358ab2d7a49a67439252797a791b7799d3a3432da3ac92722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:9d08fc37124903186688d37db468f0748b9d5bc58bd0163c46c620297a8c9c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.4 MB (610424871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee58cfee7b0e452a99a8c2751092a7c023dde9ff1e3cfbb5e4ca0949bdae583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:36:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:36:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:36:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:36:04 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:36:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:44:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:44:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:44:41 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 22:44:41 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:44:41 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 22:54:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:54:15 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:54:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:54:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:54:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:54:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:54:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:54:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:54:15 GMT
USER odoo
# Mon, 04 May 2026 22:54:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:54:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f07b28e696326f33e45717d0945d9e30bdd52fa06871c2965aa15493c625cc`  
		Last Modified: Mon, 04 May 2026 22:55:38 GMT  
		Size: 233.8 MB (233833925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ce7958885dd8bdb7eb908cf494ab23c383940fe7731f7131a61da5700e505`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 2.6 MB (2603708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11095ce88b19f683925f1d827af30f1ad3e6ddbaa00d31f675f768f9028b8158`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 484.0 KB (483986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d8bbb79c2369a09568c4d034978cecb4a974e41566fdaaacdaad54ae5507a`  
		Last Modified: Mon, 04 May 2026 22:55:40 GMT  
		Size: 343.8 MB (343764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8f1fe54e4a1154791c532de5971e24e2bf8c313618684c57b8d94bb882695f`  
		Last Modified: Mon, 04 May 2026 22:55:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1562909d2050d26273702aeabbe138138f18e250bf12ba10ebc082a48dffac`  
		Last Modified: Mon, 04 May 2026 22:55:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2447b5e9573353e9306860cb53b2ad373a2f86623141bf52831dc3e0858a3`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df16dc059796dc207cce0d58fe9d2aa9aa7b55212a80c56a25e6cbbbaf09de4`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b0898b6d4c32ef9faa07c5d17c5807ef9f32d21c6230793f50da39dcb5ef6180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42904899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70c47037b77643a9fdd234a6a3c1afeca523018c05969e28b1b13ab05fc325`

```dockerfile
```

-	Layers:
	-	`sha256:721d2008ba24d5e23e325c6ba45f6cce4c6845d358c5aed6fbb3e480e1aa2021`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 42.9 MB (42878109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ae742805287879f601e19685eb1e74d186f8d1214566262f95889d39a34bc`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 26.8 KB (26790 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:436f787cb65d226ad7b4ebcdb0afad5570d92bf089e9653154565bd45c3e4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605274803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c41ce03faa12004338e59acd4328de63e7de2a79fff13d6d9bc5d30fd9d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:17 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:31 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:31 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:31 GMT
USER odoo
# Mon, 04 May 2026 20:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea59999641de59431037ca45a7bff25898c1b54dda0cea66b896eee9edba31c`  
		Last Modified: Mon, 04 May 2026 20:58:11 GMT  
		Size: 231.2 MB (231202109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e023a7d4e854b293eaaf9af326db95df181fadb3d7c3ebe1d3242ff1e977a1`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 2.6 MB (2598189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff26802bed98b8e6c8a44783691cd7f34b94cf7e3a676835c3a2e86827a15d0`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 484.0 KB (484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197540263cb05b1d2a3ba789fa3e02c026c42823ae543a0b784dad5541935c3`  
		Last Modified: Mon, 04 May 2026 20:58:16 GMT  
		Size: 343.4 MB (343381521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc04332b9e6d324b7c774b8d6ec3af2d44f140b7dce7272a6c7dadb04201a9`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215d70cd3f71c87e08a7bd6c89437273ee940c0e178776e7928f443cd5be40e`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36018947d52acd91d4ce275a6470517432e0ca66620b0572b9d803b8358302c3`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f49ad7b2b14ecce6c48cc6b3bfbe70f87184f19e372ab9c9bcd26897b481f`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1a7dee8e69d35bbf9e777d2c90a0b3d11c6a55334c094792d5b6a1025d4af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42911559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd91dbb69006c59d7a87b308d36b666122abd383422b429d976123ddd031234`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f7ec0101ee208525b5cddc5ef91270681bdbca1759373a1483faa486cbda7`  
		Last Modified: Mon, 04 May 2026 20:57:55 GMT  
		Size: 42.9 MB (42884616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0b27109c15adb36fa43396ef4ad7e01fbdb3e752b04d242d9f83285a2b1daf`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260504`

```console
$ docker pull odoo@sha256:f4d974041d580ef358ab2d7a49a67439252797a791b7799d3a3432da3ac92722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260504` - linux; amd64

```console
$ docker pull odoo@sha256:9d08fc37124903186688d37db468f0748b9d5bc58bd0163c46c620297a8c9c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.4 MB (610424871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee58cfee7b0e452a99a8c2751092a7c023dde9ff1e3cfbb5e4ca0949bdae583`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 22:36:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:36:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:36:04 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:36:04 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:36:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:44:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:44:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:44:41 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 22:44:41 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:44:41 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 22:54:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:54:15 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:54:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:54:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:54:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:54:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:54:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:54:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:54:15 GMT
USER odoo
# Mon, 04 May 2026 22:54:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:54:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f07b28e696326f33e45717d0945d9e30bdd52fa06871c2965aa15493c625cc`  
		Last Modified: Mon, 04 May 2026 22:55:38 GMT  
		Size: 233.8 MB (233833925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680ce7958885dd8bdb7eb908cf494ab23c383940fe7731f7131a61da5700e505`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 2.6 MB (2603708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11095ce88b19f683925f1d827af30f1ad3e6ddbaa00d31f675f768f9028b8158`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 484.0 KB (483986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d8bbb79c2369a09568c4d034978cecb4a974e41566fdaaacdaad54ae5507a`  
		Last Modified: Mon, 04 May 2026 22:55:40 GMT  
		Size: 343.8 MB (343764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8f1fe54e4a1154791c532de5971e24e2bf8c313618684c57b8d94bb882695f`  
		Last Modified: Mon, 04 May 2026 22:55:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1562909d2050d26273702aeabbe138138f18e250bf12ba10ebc082a48dffac`  
		Last Modified: Mon, 04 May 2026 22:55:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2447b5e9573353e9306860cb53b2ad373a2f86623141bf52831dc3e0858a3`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df16dc059796dc207cce0d58fe9d2aa9aa7b55212a80c56a25e6cbbbaf09de4`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:b0898b6d4c32ef9faa07c5d17c5807ef9f32d21c6230793f50da39dcb5ef6180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42904899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f70c47037b77643a9fdd234a6a3c1afeca523018c05969e28b1b13ab05fc325`

```dockerfile
```

-	Layers:
	-	`sha256:721d2008ba24d5e23e325c6ba45f6cce4c6845d358c5aed6fbb3e480e1aa2021`  
		Last Modified: Mon, 04 May 2026 22:55:31 GMT  
		Size: 42.9 MB (42878109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ae742805287879f601e19685eb1e74d186f8d1214566262f95889d39a34bc`  
		Last Modified: Mon, 04 May 2026 22:55:28 GMT  
		Size: 26.8 KB (26790 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260504` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:436f787cb65d226ad7b4ebcdb0afad5570d92bf089e9653154565bd45c3e4b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605274803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c41ce03faa12004338e59acd4328de63e7de2a79fff13d6d9bc5d30fd9d3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:17 GMT
ENV ODOO_VERSION=17.0
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:17 GMT
ARG ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:31 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:31 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=43cb8f677cbb325ada98bdd10c5980386deb1a72
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:31 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:31 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:31 GMT
USER odoo
# Mon, 04 May 2026 20:56:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea59999641de59431037ca45a7bff25898c1b54dda0cea66b896eee9edba31c`  
		Last Modified: Mon, 04 May 2026 20:58:11 GMT  
		Size: 231.2 MB (231202109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e023a7d4e854b293eaaf9af326db95df181fadb3d7c3ebe1d3242ff1e977a1`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 2.6 MB (2598189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff26802bed98b8e6c8a44783691cd7f34b94cf7e3a676835c3a2e86827a15d0`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 484.0 KB (484001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197540263cb05b1d2a3ba789fa3e02c026c42823ae543a0b784dad5541935c3`  
		Last Modified: Mon, 04 May 2026 20:58:16 GMT  
		Size: 343.4 MB (343381521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc04332b9e6d324b7c774b8d6ec3af2d44f140b7dce7272a6c7dadb04201a9`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0215d70cd3f71c87e08a7bd6c89437273ee940c0e178776e7928f443cd5be40e`  
		Last Modified: Mon, 04 May 2026 20:57:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36018947d52acd91d4ce275a6470517432e0ca66620b0572b9d803b8358302c3`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f49ad7b2b14ecce6c48cc6b3bfbe70f87184f19e372ab9c9bcd26897b481f`  
		Last Modified: Mon, 04 May 2026 20:57:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:1a7dee8e69d35bbf9e777d2c90a0b3d11c6a55334c094792d5b6a1025d4af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42911559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd91dbb69006c59d7a87b308d36b666122abd383422b429d976123ddd031234`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f7ec0101ee208525b5cddc5ef91270681bdbca1759373a1483faa486cbda7`  
		Last Modified: Mon, 04 May 2026 20:57:55 GMT  
		Size: 42.9 MB (42884616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0b27109c15adb36fa43396ef4ad7e01fbdb3e752b04d242d9f83285a2b1daf`  
		Last Modified: Mon, 04 May 2026 20:57:50 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:b79d87a4ec1a3806d133e12a07dc06402fc37397eb285663b1acfea2001ae52c
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
$ docker pull odoo@sha256:700bf22730189c509e53462b36088abcd281bfe2b84e920a2d16cee4d0bbcef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.7 MB (684745877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df04cb96d09515fa54f0ddac2c4e83252b795a2ef2fe3b7179900dbf715ee613`
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
# Mon, 04 May 2026 21:17:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:17:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:17:23 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:17:23 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 21:17:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:35:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:35:30 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:35:30 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 21:35:30 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:35:30 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 21:59:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:59:24 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:59:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:59:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:59:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:59:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:59:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:59:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:59:24 GMT
USER odoo
# Mon, 04 May 2026 21:59:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:59:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40830fafbae948329fd61bf8df9fea44745118db2724e318bd3bdd4021fc1680`  
		Last Modified: Mon, 04 May 2026 22:01:32 GMT  
		Size: 254.6 MB (254594359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495210ae2080018da5663390ad0c3ad08fba86ba16eeeb8d079c065b809fafb`  
		Last Modified: Mon, 04 May 2026 22:01:20 GMT  
		Size: 14.4 MB (14359944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a209d1d28650ced745764cfff5934a795549a25c6a5165b7ef1c5a68820e4b8`  
		Last Modified: Mon, 04 May 2026 22:01:19 GMT  
		Size: 483.8 KB (483760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a16c97564bdb5e75066aa90d8a1a2d18e7571a3a00613936f07e7c68f46daa7`  
		Last Modified: Mon, 04 May 2026 22:01:35 GMT  
		Size: 385.6 MB (385572393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698476739d903ddbb2c550930f8b353ba3c0cc75ce7ee8eadefa9a002877cef`  
		Last Modified: Mon, 04 May 2026 22:01:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a5b129517cc45f52efe36384df02c653e29fcc4d04c9af0bd4548c3b38b062`  
		Last Modified: Mon, 04 May 2026 22:01:22 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703c531613b415d2452be032f19d2b0e8ed7d96498323583f6dfbc1a5600b742`  
		Last Modified: Mon, 04 May 2026 22:01:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591bab9d3d2938158de96ee1f03e7ed9ace3b99de0e3585eaad987addf72da1d`  
		Last Modified: Mon, 04 May 2026 22:01:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:8fd0272863f988587a9cee72a743f66b106c155246d3897507608962af1a3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62273991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138247e835a350d3c43d4924dc518475e54edf9edbfa0e18f73a2c6f9fd3e553`

```dockerfile
```

-	Layers:
	-	`sha256:95dba43c4cd0fa6c59d9366d34e3c298e8d98ac883b2382f051adf9c37e29a46`  
		Last Modified: Mon, 04 May 2026 22:01:24 GMT  
		Size: 62.2 MB (62247193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ba4838882d1eace8adec559ed2de7c0579a5a0bb29b8e49fba47e5f1ac5be1`  
		Last Modified: Mon, 04 May 2026 22:01:19 GMT  
		Size: 26.8 KB (26798 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:deb8312d6161d461367767ebe3e3d8287b5d4ddaa6056357332998cf8969b4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d50f1bef7b1ef23dcf31832b6ab4a147b2e749e979d51a98b04efb392b92b83`
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
# Mon, 04 May 2026 20:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:57:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:57:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:57:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:57:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:57:18 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 20:58:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:58:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:58:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:58:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:58:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:58:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:58:27 GMT
USER odoo
# Mon, 04 May 2026 20:58:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:58:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06020f82bad6429dda80a5580e2edc922996244bfee4917f7d228f01d5005873`  
		Last Modified: Mon, 04 May 2026 21:00:46 GMT  
		Size: 252.0 MB (252027487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1375dc07ba914d2b5dd39fdf995ee7f4f36236976c8cba239eb754a86ce73`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 14.3 MB (14340777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f76573893a6df9475dd7328f8d5a2ec41556adbbf097a677679c3e396c6d0`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 483.8 KB (483781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da4bcf5509ea1436c286e21e10695d5c06263c11af710f78e4f1211e554814`  
		Last Modified: Mon, 04 May 2026 21:00:49 GMT  
		Size: 385.4 MB (385420382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ff6a3e6deda43a3e5e69e9896c2f20610ca5f49693049cfc4ed438eee76b4`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b2656f3617c78bc8a6f3fff8f99e51a281c6b9dbcd1702cb82881ffad60af`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8f2b7c0ca15824469119a7424b0e5e1fa450444b3b046b72a383eec35620f`  
		Last Modified: Mon, 04 May 2026 21:00:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f1100602f83d9866a405c8bfabfd366b8faf0cd25c2c560ca6caaa7f799b4b`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b9864d920f62cb996d47d41f9beda0ac6a42785ea99a59f0972ca3fa7e37b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8372b847d45130854effa92658e61c7edaf48ddbfd30bdd2b084f81f151952c3`

```dockerfile
```

-	Layers:
	-	`sha256:76ce18f183b90ed66db82ceded4f57c2be3d5b817adaceefa3e55cb25d4f77e7`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 62.3 MB (62254468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322109be1c7e63c7edb9fd92c67d90a20aadc34f947ac13e8e81d50c19c65b0`  
		Last Modified: Mon, 04 May 2026 21:00:31 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:f334b9a7b0e47bcd09254f3d256712902276b73a8402701c991dbd0fbb036ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.9 MB (700904912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bbaea1966035e6549f30229aa2f81987c6a5bac6e8ade2b6eda3167f458ad1`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 21:30:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:20 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:23 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:23 GMT
USER odoo
# Mon, 04 May 2026 21:30:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14496632d4fd75aeed4a4182f7b7d905e64bb28afe53470fd73c4f0bd8e1a`  
		Last Modified: Mon, 04 May 2026 21:34:49 GMT  
		Size: 386.1 MB (386103969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0cfafee5ceec5347f8573072b2948f0c08c3364561993454cca8caa88ac0c`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55420e0387d1062b0a56f48a97455ef17f5a1338162c2299ec3be6aa0d1adc39`  
		Last Modified: Mon, 04 May 2026 21:34:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a673a92e7d6613c73e25f12e5c841ca99101fcefb93faaa96514241c4e218`  
		Last Modified: Mon, 04 May 2026 21:34:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c15ab6c711f3df65150fbad5b55a054ec9534403e43d5993efd21b8d7850c4`  
		Last Modified: Mon, 04 May 2026 21:34:34 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:3ae545b08e4aaf76dd8cc98276f1310d07dfcb63558e1caf589e7933805d0d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62282430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcdddd363a7aff8360838f166586a7aaf20f2a5f8a42f9789d7e2eec17b85f7`

```dockerfile
```

-	Layers:
	-	`sha256:e58d6ab19019feaa768cca6658b132d4856f97d66b3d0928e59b3acfd21c1906`  
		Last Modified: Mon, 04 May 2026 21:34:34 GMT  
		Size: 62.3 MB (62255576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5167a342af79b5e3f4a3af74ea7f60f4b3c07a2f20bac1f7881f54531745ca6`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 26.9 KB (26854 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:b79d87a4ec1a3806d133e12a07dc06402fc37397eb285663b1acfea2001ae52c
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
$ docker pull odoo@sha256:700bf22730189c509e53462b36088abcd281bfe2b84e920a2d16cee4d0bbcef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.7 MB (684745877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df04cb96d09515fa54f0ddac2c4e83252b795a2ef2fe3b7179900dbf715ee613`
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
# Mon, 04 May 2026 21:17:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:17:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:17:23 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:17:23 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 21:17:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:35:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:35:30 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:35:30 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 21:35:30 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:35:30 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 21:59:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:59:24 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:59:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:59:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:59:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:59:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:59:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:59:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:59:24 GMT
USER odoo
# Mon, 04 May 2026 21:59:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:59:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40830fafbae948329fd61bf8df9fea44745118db2724e318bd3bdd4021fc1680`  
		Last Modified: Mon, 04 May 2026 22:01:32 GMT  
		Size: 254.6 MB (254594359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495210ae2080018da5663390ad0c3ad08fba86ba16eeeb8d079c065b809fafb`  
		Last Modified: Mon, 04 May 2026 22:01:20 GMT  
		Size: 14.4 MB (14359944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a209d1d28650ced745764cfff5934a795549a25c6a5165b7ef1c5a68820e4b8`  
		Last Modified: Mon, 04 May 2026 22:01:19 GMT  
		Size: 483.8 KB (483760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a16c97564bdb5e75066aa90d8a1a2d18e7571a3a00613936f07e7c68f46daa7`  
		Last Modified: Mon, 04 May 2026 22:01:35 GMT  
		Size: 385.6 MB (385572393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698476739d903ddbb2c550930f8b353ba3c0cc75ce7ee8eadefa9a002877cef`  
		Last Modified: Mon, 04 May 2026 22:01:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a5b129517cc45f52efe36384df02c653e29fcc4d04c9af0bd4548c3b38b062`  
		Last Modified: Mon, 04 May 2026 22:01:22 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703c531613b415d2452be032f19d2b0e8ed7d96498323583f6dfbc1a5600b742`  
		Last Modified: Mon, 04 May 2026 22:01:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591bab9d3d2938158de96ee1f03e7ed9ace3b99de0e3585eaad987addf72da1d`  
		Last Modified: Mon, 04 May 2026 22:01:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8fd0272863f988587a9cee72a743f66b106c155246d3897507608962af1a3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62273991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138247e835a350d3c43d4924dc518475e54edf9edbfa0e18f73a2c6f9fd3e553`

```dockerfile
```

-	Layers:
	-	`sha256:95dba43c4cd0fa6c59d9366d34e3c298e8d98ac883b2382f051adf9c37e29a46`  
		Last Modified: Mon, 04 May 2026 22:01:24 GMT  
		Size: 62.2 MB (62247193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ba4838882d1eace8adec559ed2de7c0579a5a0bb29b8e49fba47e5f1ac5be1`  
		Last Modified: Mon, 04 May 2026 22:01:19 GMT  
		Size: 26.8 KB (26798 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:deb8312d6161d461367767ebe3e3d8287b5d4ddaa6056357332998cf8969b4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d50f1bef7b1ef23dcf31832b6ab4a147b2e749e979d51a98b04efb392b92b83`
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
# Mon, 04 May 2026 20:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:57:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:57:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:57:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:57:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:57:18 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 20:58:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:58:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:58:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:58:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:58:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:58:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:58:27 GMT
USER odoo
# Mon, 04 May 2026 20:58:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:58:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06020f82bad6429dda80a5580e2edc922996244bfee4917f7d228f01d5005873`  
		Last Modified: Mon, 04 May 2026 21:00:46 GMT  
		Size: 252.0 MB (252027487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1375dc07ba914d2b5dd39fdf995ee7f4f36236976c8cba239eb754a86ce73`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 14.3 MB (14340777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f76573893a6df9475dd7328f8d5a2ec41556adbbf097a677679c3e396c6d0`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 483.8 KB (483781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da4bcf5509ea1436c286e21e10695d5c06263c11af710f78e4f1211e554814`  
		Last Modified: Mon, 04 May 2026 21:00:49 GMT  
		Size: 385.4 MB (385420382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ff6a3e6deda43a3e5e69e9896c2f20610ca5f49693049cfc4ed438eee76b4`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b2656f3617c78bc8a6f3fff8f99e51a281c6b9dbcd1702cb82881ffad60af`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8f2b7c0ca15824469119a7424b0e5e1fa450444b3b046b72a383eec35620f`  
		Last Modified: Mon, 04 May 2026 21:00:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f1100602f83d9866a405c8bfabfd366b8faf0cd25c2c560ca6caaa7f799b4b`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b9864d920f62cb996d47d41f9beda0ac6a42785ea99a59f0972ca3fa7e37b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8372b847d45130854effa92658e61c7edaf48ddbfd30bdd2b084f81f151952c3`

```dockerfile
```

-	Layers:
	-	`sha256:76ce18f183b90ed66db82ceded4f57c2be3d5b817adaceefa3e55cb25d4f77e7`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 62.3 MB (62254468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322109be1c7e63c7edb9fd92c67d90a20aadc34f947ac13e8e81d50c19c65b0`  
		Last Modified: Mon, 04 May 2026 21:00:31 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f334b9a7b0e47bcd09254f3d256712902276b73a8402701c991dbd0fbb036ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.9 MB (700904912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bbaea1966035e6549f30229aa2f81987c6a5bac6e8ade2b6eda3167f458ad1`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 21:30:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:20 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:23 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:23 GMT
USER odoo
# Mon, 04 May 2026 21:30:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14496632d4fd75aeed4a4182f7b7d905e64bb28afe53470fd73c4f0bd8e1a`  
		Last Modified: Mon, 04 May 2026 21:34:49 GMT  
		Size: 386.1 MB (386103969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0cfafee5ceec5347f8573072b2948f0c08c3364561993454cca8caa88ac0c`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55420e0387d1062b0a56f48a97455ef17f5a1338162c2299ec3be6aa0d1adc39`  
		Last Modified: Mon, 04 May 2026 21:34:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a673a92e7d6613c73e25f12e5c841ca99101fcefb93faaa96514241c4e218`  
		Last Modified: Mon, 04 May 2026 21:34:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c15ab6c711f3df65150fbad5b55a054ec9534403e43d5993efd21b8d7850c4`  
		Last Modified: Mon, 04 May 2026 21:34:34 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3ae545b08e4aaf76dd8cc98276f1310d07dfcb63558e1caf589e7933805d0d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62282430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcdddd363a7aff8360838f166586a7aaf20f2a5f8a42f9789d7e2eec17b85f7`

```dockerfile
```

-	Layers:
	-	`sha256:e58d6ab19019feaa768cca6658b132d4856f97d66b3d0928e59b3acfd21c1906`  
		Last Modified: Mon, 04 May 2026 21:34:34 GMT  
		Size: 62.3 MB (62255576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5167a342af79b5e3f4a3af74ea7f60f4b3c07a2f20bac1f7881f54531745ca6`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 26.9 KB (26854 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260504`

```console
$ docker pull odoo@sha256:b79d87a4ec1a3806d133e12a07dc06402fc37397eb285663b1acfea2001ae52c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260504` - linux; amd64

```console
$ docker pull odoo@sha256:700bf22730189c509e53462b36088abcd281bfe2b84e920a2d16cee4d0bbcef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.7 MB (684745877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df04cb96d09515fa54f0ddac2c4e83252b795a2ef2fe3b7179900dbf715ee613`
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
# Mon, 04 May 2026 21:17:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:17:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:17:23 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:17:23 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 21:17:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:35:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:35:30 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:35:30 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 21:35:30 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:35:30 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 21:59:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:59:24 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:59:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:59:24 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:59:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:59:24 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:59:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:59:24 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:59:24 GMT
USER odoo
# Mon, 04 May 2026 21:59:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:59:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40830fafbae948329fd61bf8df9fea44745118db2724e318bd3bdd4021fc1680`  
		Last Modified: Mon, 04 May 2026 22:01:32 GMT  
		Size: 254.6 MB (254594359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495210ae2080018da5663390ad0c3ad08fba86ba16eeeb8d079c065b809fafb`  
		Last Modified: Mon, 04 May 2026 22:01:20 GMT  
		Size: 14.4 MB (14359944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a209d1d28650ced745764cfff5934a795549a25c6a5165b7ef1c5a68820e4b8`  
		Last Modified: Mon, 04 May 2026 22:01:19 GMT  
		Size: 483.8 KB (483760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a16c97564bdb5e75066aa90d8a1a2d18e7571a3a00613936f07e7c68f46daa7`  
		Last Modified: Mon, 04 May 2026 22:01:35 GMT  
		Size: 385.6 MB (385572393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b698476739d903ddbb2c550930f8b353ba3c0cc75ce7ee8eadefa9a002877cef`  
		Last Modified: Mon, 04 May 2026 22:01:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a5b129517cc45f52efe36384df02c653e29fcc4d04c9af0bd4548c3b38b062`  
		Last Modified: Mon, 04 May 2026 22:01:22 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703c531613b415d2452be032f19d2b0e8ed7d96498323583f6dfbc1a5600b742`  
		Last Modified: Mon, 04 May 2026 22:01:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591bab9d3d2938158de96ee1f03e7ed9ace3b99de0e3585eaad987addf72da1d`  
		Last Modified: Mon, 04 May 2026 22:01:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:8fd0272863f988587a9cee72a743f66b106c155246d3897507608962af1a3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62273991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138247e835a350d3c43d4924dc518475e54edf9edbfa0e18f73a2c6f9fd3e553`

```dockerfile
```

-	Layers:
	-	`sha256:95dba43c4cd0fa6c59d9366d34e3c298e8d98ac883b2382f051adf9c37e29a46`  
		Last Modified: Mon, 04 May 2026 22:01:24 GMT  
		Size: 62.2 MB (62247193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ba4838882d1eace8adec559ed2de7c0579a5a0bb29b8e49fba47e5f1ac5be1`  
		Last Modified: Mon, 04 May 2026 22:01:19 GMT  
		Size: 26.8 KB (26798 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260504` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:deb8312d6161d461367767ebe3e3d8287b5d4ddaa6056357332998cf8969b4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681150650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d50f1bef7b1ef23dcf31832b6ab4a147b2e749e979d51a98b04efb392b92b83`
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
# Mon, 04 May 2026 20:57:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:57:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:57:07 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:57:07 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:57:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:57:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:57:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:57:18 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:57:18 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 20:58:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:58:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:58:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:58:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:58:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:58:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:58:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:58:27 GMT
USER odoo
# Mon, 04 May 2026 20:58:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:58:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06020f82bad6429dda80a5580e2edc922996244bfee4917f7d228f01d5005873`  
		Last Modified: Mon, 04 May 2026 21:00:46 GMT  
		Size: 252.0 MB (252027487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1375dc07ba914d2b5dd39fdf995ee7f4f36236976c8cba239eb754a86ce73`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 14.3 MB (14340777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f76573893a6df9475dd7328f8d5a2ec41556adbbf097a677679c3e396c6d0`  
		Last Modified: Mon, 04 May 2026 21:00:32 GMT  
		Size: 483.8 KB (483781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da4bcf5509ea1436c286e21e10695d5c06263c11af710f78e4f1211e554814`  
		Last Modified: Mon, 04 May 2026 21:00:49 GMT  
		Size: 385.4 MB (385420382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ff6a3e6deda43a3e5e69e9896c2f20610ca5f49693049cfc4ed438eee76b4`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b2656f3617c78bc8a6f3fff8f99e51a281c6b9dbcd1702cb82881ffad60af`  
		Last Modified: Mon, 04 May 2026 21:00:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec8f2b7c0ca15824469119a7424b0e5e1fa450444b3b046b72a383eec35620f`  
		Last Modified: Mon, 04 May 2026 21:00:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f1100602f83d9866a405c8bfabfd366b8faf0cd25c2c560ca6caaa7f799b4b`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:b9864d920f62cb996d47d41f9beda0ac6a42785ea99a59f0972ca3fa7e37b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62281419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8372b847d45130854effa92658e61c7edaf48ddbfd30bdd2b084f81f151952c3`

```dockerfile
```

-	Layers:
	-	`sha256:76ce18f183b90ed66db82ceded4f57c2be3d5b817adaceefa3e55cb25d4f77e7`  
		Last Modified: Mon, 04 May 2026 21:00:36 GMT  
		Size: 62.3 MB (62254468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322109be1c7e63c7edb9fd92c67d90a20aadc34f947ac13e8e81d50c19c65b0`  
		Last Modified: Mon, 04 May 2026 21:00:31 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260504` - linux; ppc64le

```console
$ docker pull odoo@sha256:f334b9a7b0e47bcd09254f3d256712902276b73a8402701c991dbd0fbb036ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.9 MB (700904912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bbaea1966035e6549f30229aa2f81987c6a5bac6e8ade2b6eda3167f458ad1`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=18.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
# Mon, 04 May 2026 21:30:19 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:20 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:23 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=f3440ffc9a7be9be64d194419085aa624267f217
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:23 GMT
USER odoo
# Mon, 04 May 2026 21:30:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14496632d4fd75aeed4a4182f7b7d905e64bb28afe53470fd73c4f0bd8e1a`  
		Last Modified: Mon, 04 May 2026 21:34:49 GMT  
		Size: 386.1 MB (386103969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0cfafee5ceec5347f8573072b2948f0c08c3364561993454cca8caa88ac0c`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55420e0387d1062b0a56f48a97455ef17f5a1338162c2299ec3be6aa0d1adc39`  
		Last Modified: Mon, 04 May 2026 21:34:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a673a92e7d6613c73e25f12e5c841ca99101fcefb93faaa96514241c4e218`  
		Last Modified: Mon, 04 May 2026 21:34:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c15ab6c711f3df65150fbad5b55a054ec9534403e43d5993efd21b8d7850c4`  
		Last Modified: Mon, 04 May 2026 21:34:34 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:3ae545b08e4aaf76dd8cc98276f1310d07dfcb63558e1caf589e7933805d0d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62282430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcdddd363a7aff8360838f166586a7aaf20f2a5f8a42f9789d7e2eec17b85f7`

```dockerfile
```

-	Layers:
	-	`sha256:e58d6ab19019feaa768cca6658b132d4856f97d66b3d0928e59b3acfd21c1906`  
		Last Modified: Mon, 04 May 2026 21:34:34 GMT  
		Size: 62.3 MB (62255576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5167a342af79b5e3f4a3af74ea7f60f4b3c07a2f20bac1f7881f54531745ca6`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 26.9 KB (26854 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:5db447482177ca598b97539bc186b61f5f271371ab3a90f3940ecf33b63af7b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:0dde824bc822bdd9cca1a27a62457399092c8d20b2f317f1ecf173dd872053b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.0 MB (704006052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd31e6fde4b70ff1d5582b440dfef472aaa79dacb7e1ce05b3a13f1c6b18e34c`
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
# Mon, 04 May 2026 22:34:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:34:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:34:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:34:27 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:34:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:37:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:37:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:37:48 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 22:45:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:45:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:45:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:45:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:45:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:45:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:45:58 GMT
USER odoo
# Mon, 04 May 2026 22:45:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:45:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a61084b47d12ff9ff9c460de1319913d110aa487350eec23a9dbc49b9a4827`  
		Last Modified: Mon, 04 May 2026 22:48:16 GMT  
		Size: 254.6 MB (254595498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd938f730b56cc320b8794e88ace10a5e70f15c084c88a2367d35f1b7b5fda95`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 14.4 MB (14360245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc2ddb282e5b74c096028b377b3294acd095eed40248515c881b14cf88de75`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 483.7 KB (483746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4810d7d29cd73ee5028c4f6e054521b2083f8a78541d3157840a9540a396e5a6`  
		Last Modified: Mon, 04 May 2026 22:48:18 GMT  
		Size: 404.8 MB (404831145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92b367438d6a45e16c61ff107deea100358757df7a099e1fe3afc184bfba0c7`  
		Last Modified: Mon, 04 May 2026 22:48:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c02b59274565a902b0446129d43aed4fd76608a19d493839a7c28588432a7b`  
		Last Modified: Mon, 04 May 2026 22:48:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b3116247ee6758fab0c1705e59421da1e29fd2730b9be9f867ef7e6f083687`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783125f7b007ce96ee5b3d21201090b5010e6007bf97d1b1335182cf48a66916`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7f23120b8b79ea4f5ffd1fce29b5d1f0705ec47821a931f00a2dc83354215c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70334671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5213dc777473f08f2d8ba2fa48fe932682f485e01577783d36d8ee859c2cf8`

```dockerfile
```

-	Layers:
	-	`sha256:6d828492667cdaad29600af647d116a8a457a8846dac9516db20308bdaf59285`  
		Last Modified: Mon, 04 May 2026 22:48:10 GMT  
		Size: 70.3 MB (70307578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73678c06a5c2b8327a88f541a2126e0dfa83bfdd36bdeb5373df8b4eac7b1d23`  
		Last Modified: Mon, 04 May 2026 22:48:05 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
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
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:9311d0d4d189e632219917e71f155109a7ed2dd79b9d10fa08f70c7cb1149e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 MB (720152190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462e51fefce359eca8c2873175b9bc46dd9a41588f3875cb234c1a62defbdac6`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 21:30:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:42 GMT
USER odoo
# Mon, 04 May 2026 21:30:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ca4a34b44fb175a028c3ada5b65bae28fc1adb51b751e21fbb99c3120121e`  
		Last Modified: Mon, 04 May 2026 21:36:03 GMT  
		Size: 405.4 MB (405351239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580b6becd8fd85d7d6daf76a1006447c0e7d44ccb468acf1982dac1b38d957`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e60f6319a6e806ce2ac57f87431d8233395e24e6942a7bd8ee1477b4e1e6759`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2912ce9dbe3c7b299cd8da5b1768fcd5ea4648c8c53d3277a1148080e5b740`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734dfe26ec38efdae6b47880016a1b6a6f880969651ca8ea859ae3689736ee05`  
		Last Modified: Mon, 04 May 2026 21:35:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:1f21df0d4d66411b00c48ea87c713107336e8ce2363d714c9e6ee0f6f49080be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70343122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e295c83667511cf85b9faa25d5ed7ca54aa48ef4423c679a6af594932fac9c`

```dockerfile
```

-	Layers:
	-	`sha256:90d0dadff204515b51881d5cc02c32dc2be75ce9aa3d868a1b6670be39cbe6c0`  
		Last Modified: Mon, 04 May 2026 21:35:56 GMT  
		Size: 70.3 MB (70315967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885d20c60a99dd57b36368bf2af1f850abe48efbccd4eda2ace00f642445f5a8`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:5db447482177ca598b97539bc186b61f5f271371ab3a90f3940ecf33b63af7b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:0dde824bc822bdd9cca1a27a62457399092c8d20b2f317f1ecf173dd872053b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.0 MB (704006052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd31e6fde4b70ff1d5582b440dfef472aaa79dacb7e1ce05b3a13f1c6b18e34c`
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
# Mon, 04 May 2026 22:34:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:34:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:34:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:34:27 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:34:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:37:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:37:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:37:48 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 22:45:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:45:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:45:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:45:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:45:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:45:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:45:58 GMT
USER odoo
# Mon, 04 May 2026 22:45:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:45:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a61084b47d12ff9ff9c460de1319913d110aa487350eec23a9dbc49b9a4827`  
		Last Modified: Mon, 04 May 2026 22:48:16 GMT  
		Size: 254.6 MB (254595498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd938f730b56cc320b8794e88ace10a5e70f15c084c88a2367d35f1b7b5fda95`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 14.4 MB (14360245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc2ddb282e5b74c096028b377b3294acd095eed40248515c881b14cf88de75`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 483.7 KB (483746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4810d7d29cd73ee5028c4f6e054521b2083f8a78541d3157840a9540a396e5a6`  
		Last Modified: Mon, 04 May 2026 22:48:18 GMT  
		Size: 404.8 MB (404831145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92b367438d6a45e16c61ff107deea100358757df7a099e1fe3afc184bfba0c7`  
		Last Modified: Mon, 04 May 2026 22:48:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c02b59274565a902b0446129d43aed4fd76608a19d493839a7c28588432a7b`  
		Last Modified: Mon, 04 May 2026 22:48:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b3116247ee6758fab0c1705e59421da1e29fd2730b9be9f867ef7e6f083687`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783125f7b007ce96ee5b3d21201090b5010e6007bf97d1b1335182cf48a66916`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7f23120b8b79ea4f5ffd1fce29b5d1f0705ec47821a931f00a2dc83354215c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70334671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5213dc777473f08f2d8ba2fa48fe932682f485e01577783d36d8ee859c2cf8`

```dockerfile
```

-	Layers:
	-	`sha256:6d828492667cdaad29600af647d116a8a457a8846dac9516db20308bdaf59285`  
		Last Modified: Mon, 04 May 2026 22:48:10 GMT  
		Size: 70.3 MB (70307578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73678c06a5c2b8327a88f541a2126e0dfa83bfdd36bdeb5373df8b4eac7b1d23`  
		Last Modified: Mon, 04 May 2026 22:48:05 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
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
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:9311d0d4d189e632219917e71f155109a7ed2dd79b9d10fa08f70c7cb1149e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 MB (720152190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462e51fefce359eca8c2873175b9bc46dd9a41588f3875cb234c1a62defbdac6`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 21:30:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:42 GMT
USER odoo
# Mon, 04 May 2026 21:30:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ca4a34b44fb175a028c3ada5b65bae28fc1adb51b751e21fbb99c3120121e`  
		Last Modified: Mon, 04 May 2026 21:36:03 GMT  
		Size: 405.4 MB (405351239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580b6becd8fd85d7d6daf76a1006447c0e7d44ccb468acf1982dac1b38d957`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e60f6319a6e806ce2ac57f87431d8233395e24e6942a7bd8ee1477b4e1e6759`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2912ce9dbe3c7b299cd8da5b1768fcd5ea4648c8c53d3277a1148080e5b740`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734dfe26ec38efdae6b47880016a1b6a6f880969651ca8ea859ae3689736ee05`  
		Last Modified: Mon, 04 May 2026 21:35:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1f21df0d4d66411b00c48ea87c713107336e8ce2363d714c9e6ee0f6f49080be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70343122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e295c83667511cf85b9faa25d5ed7ca54aa48ef4423c679a6af594932fac9c`

```dockerfile
```

-	Layers:
	-	`sha256:90d0dadff204515b51881d5cc02c32dc2be75ce9aa3d868a1b6670be39cbe6c0`  
		Last Modified: Mon, 04 May 2026 21:35:56 GMT  
		Size: 70.3 MB (70315967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885d20c60a99dd57b36368bf2af1f850abe48efbccd4eda2ace00f642445f5a8`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260504`

```console
$ docker pull odoo@sha256:5db447482177ca598b97539bc186b61f5f271371ab3a90f3940ecf33b63af7b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260504` - linux; amd64

```console
$ docker pull odoo@sha256:0dde824bc822bdd9cca1a27a62457399092c8d20b2f317f1ecf173dd872053b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.0 MB (704006052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd31e6fde4b70ff1d5582b440dfef472aaa79dacb7e1ce05b3a13f1c6b18e34c`
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
# Mon, 04 May 2026 22:34:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:34:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:34:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:34:27 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:34:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:37:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:37:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:37:48 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 22:45:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:45:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:45:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:45:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:45:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:45:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:45:58 GMT
USER odoo
# Mon, 04 May 2026 22:45:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:45:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a61084b47d12ff9ff9c460de1319913d110aa487350eec23a9dbc49b9a4827`  
		Last Modified: Mon, 04 May 2026 22:48:16 GMT  
		Size: 254.6 MB (254595498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd938f730b56cc320b8794e88ace10a5e70f15c084c88a2367d35f1b7b5fda95`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 14.4 MB (14360245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc2ddb282e5b74c096028b377b3294acd095eed40248515c881b14cf88de75`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 483.7 KB (483746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4810d7d29cd73ee5028c4f6e054521b2083f8a78541d3157840a9540a396e5a6`  
		Last Modified: Mon, 04 May 2026 22:48:18 GMT  
		Size: 404.8 MB (404831145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92b367438d6a45e16c61ff107deea100358757df7a099e1fe3afc184bfba0c7`  
		Last Modified: Mon, 04 May 2026 22:48:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c02b59274565a902b0446129d43aed4fd76608a19d493839a7c28588432a7b`  
		Last Modified: Mon, 04 May 2026 22:48:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b3116247ee6758fab0c1705e59421da1e29fd2730b9be9f867ef7e6f083687`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783125f7b007ce96ee5b3d21201090b5010e6007bf97d1b1335182cf48a66916`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:7f23120b8b79ea4f5ffd1fce29b5d1f0705ec47821a931f00a2dc83354215c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70334671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5213dc777473f08f2d8ba2fa48fe932682f485e01577783d36d8ee859c2cf8`

```dockerfile
```

-	Layers:
	-	`sha256:6d828492667cdaad29600af647d116a8a457a8846dac9516db20308bdaf59285`  
		Last Modified: Mon, 04 May 2026 22:48:10 GMT  
		Size: 70.3 MB (70307578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73678c06a5c2b8327a88f541a2126e0dfa83bfdd36bdeb5373df8b4eac7b1d23`  
		Last Modified: Mon, 04 May 2026 22:48:05 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260504` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
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
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260504` - linux; ppc64le

```console
$ docker pull odoo@sha256:9311d0d4d189e632219917e71f155109a7ed2dd79b9d10fa08f70c7cb1149e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 MB (720152190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462e51fefce359eca8c2873175b9bc46dd9a41588f3875cb234c1a62defbdac6`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 21:30:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:42 GMT
USER odoo
# Mon, 04 May 2026 21:30:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ca4a34b44fb175a028c3ada5b65bae28fc1adb51b751e21fbb99c3120121e`  
		Last Modified: Mon, 04 May 2026 21:36:03 GMT  
		Size: 405.4 MB (405351239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580b6becd8fd85d7d6daf76a1006447c0e7d44ccb468acf1982dac1b38d957`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e60f6319a6e806ce2ac57f87431d8233395e24e6942a7bd8ee1477b4e1e6759`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2912ce9dbe3c7b299cd8da5b1768fcd5ea4648c8c53d3277a1148080e5b740`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734dfe26ec38efdae6b47880016a1b6a6f880969651ca8ea859ae3689736ee05`  
		Last Modified: Mon, 04 May 2026 21:35:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260504` - unknown; unknown

```console
$ docker pull odoo@sha256:1f21df0d4d66411b00c48ea87c713107336e8ce2363d714c9e6ee0f6f49080be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70343122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e295c83667511cf85b9faa25d5ed7ca54aa48ef4423c679a6af594932fac9c`

```dockerfile
```

-	Layers:
	-	`sha256:90d0dadff204515b51881d5cc02c32dc2be75ce9aa3d868a1b6670be39cbe6c0`  
		Last Modified: Mon, 04 May 2026 21:35:56 GMT  
		Size: 70.3 MB (70315967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885d20c60a99dd57b36368bf2af1f850abe48efbccd4eda2ace00f642445f5a8`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:5db447482177ca598b97539bc186b61f5f271371ab3a90f3940ecf33b63af7b0
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
$ docker pull odoo@sha256:0dde824bc822bdd9cca1a27a62457399092c8d20b2f317f1ecf173dd872053b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.0 MB (704006052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd31e6fde4b70ff1d5582b440dfef472aaa79dacb7e1ce05b3a13f1c6b18e34c`
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
# Mon, 04 May 2026 22:34:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 22:34:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 22:34:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 22:34:27 GMT
ARG TARGETARCH=amd64
# Mon, 04 May 2026 22:34:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 22:37:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 22:37:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 22:37:48 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 22:37:48 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 22:45:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 22:45:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 22:45:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 22:45:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 22:45:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 22:45:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 22:45:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 22:45:58 GMT
USER odoo
# Mon, 04 May 2026 22:45:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 22:45:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a61084b47d12ff9ff9c460de1319913d110aa487350eec23a9dbc49b9a4827`  
		Last Modified: Mon, 04 May 2026 22:48:16 GMT  
		Size: 254.6 MB (254595498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd938f730b56cc320b8794e88ace10a5e70f15c084c88a2367d35f1b7b5fda95`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 14.4 MB (14360245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc2ddb282e5b74c096028b377b3294acd095eed40248515c881b14cf88de75`  
		Last Modified: Mon, 04 May 2026 22:48:06 GMT  
		Size: 483.7 KB (483746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4810d7d29cd73ee5028c4f6e054521b2083f8a78541d3157840a9540a396e5a6`  
		Last Modified: Mon, 04 May 2026 22:48:18 GMT  
		Size: 404.8 MB (404831145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92b367438d6a45e16c61ff107deea100358757df7a099e1fe3afc184bfba0c7`  
		Last Modified: Mon, 04 May 2026 22:48:07 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c02b59274565a902b0446129d43aed4fd76608a19d493839a7c28588432a7b`  
		Last Modified: Mon, 04 May 2026 22:48:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b3116247ee6758fab0c1705e59421da1e29fd2730b9be9f867ef7e6f083687`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783125f7b007ce96ee5b3d21201090b5010e6007bf97d1b1335182cf48a66916`  
		Last Modified: Mon, 04 May 2026 22:48:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7f23120b8b79ea4f5ffd1fce29b5d1f0705ec47821a931f00a2dc83354215c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70334671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5213dc777473f08f2d8ba2fa48fe932682f485e01577783d36d8ee859c2cf8`

```dockerfile
```

-	Layers:
	-	`sha256:6d828492667cdaad29600af647d116a8a457a8846dac9516db20308bdaf59285`  
		Last Modified: Mon, 04 May 2026 22:48:10 GMT  
		Size: 70.3 MB (70307578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73678c06a5c2b8327a88f541a2126e0dfa83bfdd36bdeb5373df8b4eac7b1d23`  
		Last Modified: Mon, 04 May 2026 22:48:05 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
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
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:9311d0d4d189e632219917e71f155109a7ed2dd79b9d10fa08f70c7cb1149e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.2 MB (720152190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462e51fefce359eca8c2873175b9bc46dd9a41588f3875cb234c1a62defbdac6`
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
# Mon, 04 May 2026 21:26:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 21:26:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 21:26:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 21:26:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 04 May 2026 21:26:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 21:27:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 21:27:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 21:27:11 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 21:27:11 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 21:30:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 21:30:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 21:30:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 21:30:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 21:30:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 21:30:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 21:30:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 21:30:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 21:30:42 GMT
USER odoo
# Mon, 04 May 2026 21:30:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:30:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bb77e2d5c898fb728bb87a75c3fb314e8981427a642239b001c42315cb9819`  
		Last Modified: Mon, 04 May 2026 21:34:41 GMT  
		Size: 265.1 MB (265106964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b63fafb2860936bb943a291e59864bee8876e81b65d41518233bc8aa95e443d`  
		Last Modified: Mon, 04 May 2026 21:34:31 GMT  
		Size: 14.9 MB (14893483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab045f163d03111e55ebea59d2505897b516f612fc35a4112aa8d3001b7cb0`  
		Last Modified: Mon, 04 May 2026 21:34:30 GMT  
		Size: 483.9 KB (483884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ca4a34b44fb175a028c3ada5b65bae28fc1adb51b751e21fbb99c3120121e`  
		Last Modified: Mon, 04 May 2026 21:36:03 GMT  
		Size: 405.4 MB (405351239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580b6becd8fd85d7d6daf76a1006447c0e7d44ccb468acf1982dac1b38d957`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e60f6319a6e806ce2ac57f87431d8233395e24e6942a7bd8ee1477b4e1e6759`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2912ce9dbe3c7b299cd8da5b1768fcd5ea4648c8c53d3277a1148080e5b740`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734dfe26ec38efdae6b47880016a1b6a6f880969651ca8ea859ae3689736ee05`  
		Last Modified: Mon, 04 May 2026 21:35:54 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1f21df0d4d66411b00c48ea87c713107336e8ce2363d714c9e6ee0f6f49080be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70343122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e295c83667511cf85b9faa25d5ed7ca54aa48ef4423c679a6af594932fac9c`

```dockerfile
```

-	Layers:
	-	`sha256:90d0dadff204515b51881d5cc02c32dc2be75ce9aa3d868a1b6670be39cbe6c0`  
		Last Modified: Mon, 04 May 2026 21:35:56 GMT  
		Size: 70.3 MB (70315967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885d20c60a99dd57b36368bf2af1f850abe48efbccd4eda2ace00f642445f5a8`  
		Last Modified: Mon, 04 May 2026 21:35:53 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
