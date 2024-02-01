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
$ docker pull odoo@sha256:ac0d6f0a8d9872c71b8728e53515720839eca80e3a8132949fd4362ada077675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:eeb36fb12dbdd75c8beab443f977496c746619073eabcd197a111c9832ad0e41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08ba771842ec26b5c3bf7b62ea484e41b9c92f0460171c5d4e81a8de6e5671f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 01 Feb 2024 01:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 01 Feb 2024 01:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 01:49:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 01 Feb 2024 01:49:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:49:11 GMT
RUN npm install -g rtlcss
# Thu, 01 Feb 2024 01:49:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 01 Feb 2024 01:49:11 GMT
ARG ODOO_RELEASE=20240126
# Thu, 01 Feb 2024 01:49:11 GMT
ARG ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
# Thu, 01 Feb 2024 01:50:19 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 01 Feb 2024 01:50:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 01 Feb 2024 01:50:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 01 Feb 2024 01:50:24 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 01 Feb 2024 01:50:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 01 Feb 2024 01:50:24 GMT
EXPOSE 8069 8071 8072
# Thu, 01 Feb 2024 01:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 01 Feb 2024 01:50:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 01 Feb 2024 01:50:24 GMT
USER odoo
# Thu, 01 Feb 2024 01:50:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 01:50:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d995f5f95895befb5e23d812fc326dff7e89ff032fd9645de8ffe076d1dd8`  
		Last Modified: Thu, 01 Feb 2024 01:51:56 GMT  
		Size: 220.3 MB (220297785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17807fa505460cf145e384898ba6dc8c52a21f4a8baad252c584c29f5b5b3fb2`  
		Last Modified: Thu, 01 Feb 2024 01:51:32 GMT  
		Size: 2.6 MB (2625811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4fcba6b9084b5c94dc95bce302a90fd2c7e36df9de737f0dfa21813758dc60`  
		Last Modified: Thu, 01 Feb 2024 01:51:31 GMT  
		Size: 460.3 KB (460324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af2933d9014e8ddd32a73471270167d7ffb5b89d9f098f3ca3a14f0d28c6e3a`  
		Last Modified: Thu, 01 Feb 2024 01:52:04 GMT  
		Size: 308.5 MB (308514363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb4b8e870869e2a93391d1f6412cef2b1c96d56a8f2dc52c242aeead4dd42e8`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d5e0439120b8037b635e014f8c870a4d5236be460a88aaf960520e56b89653`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaf42a591858845fb226e6d61aeb1d3ffd76672a3d7305ddba4063997507282`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5decd9759b7836bf5991e7d02f8f0b7687f6d1437e39a3df0a46af547d959bf4`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:ac0d6f0a8d9872c71b8728e53515720839eca80e3a8132949fd4362ada077675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:eeb36fb12dbdd75c8beab443f977496c746619073eabcd197a111c9832ad0e41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563318575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08ba771842ec26b5c3bf7b62ea484e41b9c92f0460171c5d4e81a8de6e5671f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 01 Feb 2024 01:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 01 Feb 2024 01:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 01:49:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 01 Feb 2024 01:49:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:49:11 GMT
RUN npm install -g rtlcss
# Thu, 01 Feb 2024 01:49:11 GMT
ENV ODOO_VERSION=15.0
# Thu, 01 Feb 2024 01:49:11 GMT
ARG ODOO_RELEASE=20240126
# Thu, 01 Feb 2024 01:49:11 GMT
ARG ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
# Thu, 01 Feb 2024 01:50:19 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 01 Feb 2024 01:50:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 01 Feb 2024 01:50:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 01 Feb 2024 01:50:24 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 01 Feb 2024 01:50:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 01 Feb 2024 01:50:24 GMT
EXPOSE 8069 8071 8072
# Thu, 01 Feb 2024 01:50:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 01 Feb 2024 01:50:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 01 Feb 2024 01:50:24 GMT
USER odoo
# Thu, 01 Feb 2024 01:50:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 01:50:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d995f5f95895befb5e23d812fc326dff7e89ff032fd9645de8ffe076d1dd8`  
		Last Modified: Thu, 01 Feb 2024 01:51:56 GMT  
		Size: 220.3 MB (220297785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17807fa505460cf145e384898ba6dc8c52a21f4a8baad252c584c29f5b5b3fb2`  
		Last Modified: Thu, 01 Feb 2024 01:51:32 GMT  
		Size: 2.6 MB (2625811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4fcba6b9084b5c94dc95bce302a90fd2c7e36df9de737f0dfa21813758dc60`  
		Last Modified: Thu, 01 Feb 2024 01:51:31 GMT  
		Size: 460.3 KB (460324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af2933d9014e8ddd32a73471270167d7ffb5b89d9f098f3ca3a14f0d28c6e3a`  
		Last Modified: Thu, 01 Feb 2024 01:52:04 GMT  
		Size: 308.5 MB (308514363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb4b8e870869e2a93391d1f6412cef2b1c96d56a8f2dc52c242aeead4dd42e8`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d5e0439120b8037b635e014f8c870a4d5236be460a88aaf960520e56b89653`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaf42a591858845fb226e6d61aeb1d3ffd76672a3d7305ddba4063997507282`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5decd9759b7836bf5991e7d02f8f0b7687f6d1437e39a3df0a46af547d959bf4`  
		Last Modified: Thu, 01 Feb 2024 01:51:29 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:97ddccdaf299a882e604f2f7764aa3d557c714c73a69e3930973e1b1ea805ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:5107e8b651960aeea7fb599ebfbfb297db074393410bab24b9c54450dced4fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 MB (578048134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e820958248b4ba2555e6decd6de3955f620cd4da58bb990f62fe4b26a9e3b201`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 01 Feb 2024 01:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 01 Feb 2024 01:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 01:45:14 GMT
ARG TARGETARCH
# Thu, 01 Feb 2024 01:46:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 01 Feb 2024 01:46:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:46:36 GMT
RUN npm install -g rtlcss
# Thu, 01 Feb 2024 01:46:36 GMT
ENV ODOO_VERSION=16.0
# Thu, 01 Feb 2024 01:46:37 GMT
ARG ODOO_RELEASE=20240126
# Thu, 01 Feb 2024 01:46:37 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Thu, 01 Feb 2024 01:47:59 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 01 Feb 2024 01:48:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 01 Feb 2024 01:48:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 01 Feb 2024 01:48:04 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 01 Feb 2024 01:48:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 01 Feb 2024 01:48:04 GMT
EXPOSE 8069 8071 8072
# Thu, 01 Feb 2024 01:48:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 01 Feb 2024 01:48:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 01 Feb 2024 01:48:05 GMT
USER odoo
# Thu, 01 Feb 2024 01:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 01:48:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143e90cebe7abe8b32c01c678e9650a1603ebd1c5f6e6df261ad7523f2ffef0e`  
		Last Modified: Thu, 01 Feb 2024 01:51:07 GMT  
		Size: 219.6 MB (219606136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f72d96f19396e06ecf6811c8588ac18ad8bdd5679d8fda3316097a0ff028a60`  
		Last Modified: Thu, 01 Feb 2024 01:50:43 GMT  
		Size: 2.6 MB (2629871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195a028377091ca4bd6b2d482c0148f8c977dd43a7c65825639fb3536640b06a`  
		Last Modified: Thu, 01 Feb 2024 01:50:42 GMT  
		Size: 460.3 KB (460320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113da6b51e397926b5cf2ace86fe044cf3c933b3e33ab1bb8488697a75e28dc4`  
		Last Modified: Thu, 01 Feb 2024 01:51:19 GMT  
		Size: 323.9 MB (323931511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8489f07f3fa36f4ce4bac0769c5cdb5d6690ca999f8ab46c8042e48227095`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1ed2ae2c430e9679d40d3f7310308d6343c5d7cd99df15213dc256013d3928`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8c9f5eb5c551702a1800c0f3076fe2ae8f2469b3ff0ea21933053ee9b8c947`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405217a4655eadf877a7e68cd9880660f52d012e4a9000e19e554c85c322b6d3`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ad73330c8d96630267903e0d6b839f03d4af5086c90335e31b3eeb91d5fe5ee5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.6 MB (573643853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec54843bdfcc534cc7e7d116f81f8302f32552636da245a175cddcd718a24995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:51:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 01 Feb 2024 07:51:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 01 Feb 2024 07:51:03 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 07:51:03 GMT
ARG TARGETARCH
# Thu, 01 Feb 2024 07:52:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 01 Feb 2024 07:52:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:52:13 GMT
RUN npm install -g rtlcss
# Thu, 01 Feb 2024 07:52:13 GMT
ENV ODOO_VERSION=16.0
# Thu, 01 Feb 2024 07:52:13 GMT
ARG ODOO_RELEASE=20240126
# Thu, 01 Feb 2024 07:52:13 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Thu, 01 Feb 2024 07:53:22 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 01 Feb 2024 07:53:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 01 Feb 2024 07:53:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 01 Feb 2024 07:53:30 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 01 Feb 2024 07:53:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 01 Feb 2024 07:53:30 GMT
EXPOSE 8069 8071 8072
# Thu, 01 Feb 2024 07:53:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 01 Feb 2024 07:53:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 01 Feb 2024 07:53:30 GMT
USER odoo
# Thu, 01 Feb 2024 07:53:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 07:53:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801c94d9b99558dd0c91673ac235a10cd79d8fcd77503950fea57c65e927dd6a`  
		Last Modified: Thu, 01 Feb 2024 07:54:08 GMT  
		Size: 216.9 MB (216909917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159feb7898d903ca4efcdf32c36396f982df611b948792a9e6baeb14650253ad`  
		Last Modified: Thu, 01 Feb 2024 07:53:50 GMT  
		Size: 2.6 MB (2634870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2542a05a5da97fcd4df51265ddc59cd08d41ca17f355cc5652da440c6ccb8ea9`  
		Last Modified: Thu, 01 Feb 2024 07:53:50 GMT  
		Size: 460.3 KB (460323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b499ca8410ca1009649c9f66a2c7b66177d25cd0187d1538ae822c132d5ed7`  
		Last Modified: Thu, 01 Feb 2024 07:54:18 GMT  
		Size: 323.6 MB (323571940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c673013c69e2bcb978fd9f0db2780b4e30c23ca6e47546c9fcc344c702e6bab`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb50bbb581dd33660b7895930e0e5ada368eee89eac65cb2580b210438b478f`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b6a644b519a1ad1dae9fac521309e112cfb5a8c13a4bc95933a14be37c4e1b`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3c6fbfb78790b50ffa9b176e85ec21c0884faa43b8cc89be6373e226f676a6`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:d6318f4ff0b0123a3d161ae94bc584bc767ce03ca6b5eca69585dfa02b7e78c8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592577773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82bbfbe88d8b27f97cdef42d870c90d2705a121cae8e59f2deb2530c150ffe9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Jan 2024 23:13:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Jan 2024 23:13:55 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 23:13:55 GMT
ARG TARGETARCH
# Wed, 31 Jan 2024 23:17:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Jan 2024 23:17:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:17:26 GMT
RUN npm install -g rtlcss
# Wed, 31 Jan 2024 23:17:26 GMT
ENV ODOO_VERSION=16.0
# Wed, 31 Jan 2024 23:17:27 GMT
ARG ODOO_RELEASE=20240126
# Wed, 31 Jan 2024 23:17:28 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Wed, 31 Jan 2024 23:19:55 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 31 Jan 2024 23:20:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 31 Jan 2024 23:20:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 31 Jan 2024 23:20:16 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 31 Jan 2024 23:20:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 31 Jan 2024 23:20:17 GMT
EXPOSE 8069 8071 8072
# Wed, 31 Jan 2024 23:20:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 31 Jan 2024 23:20:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 31 Jan 2024 23:20:18 GMT
USER odoo
# Wed, 31 Jan 2024 23:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 23:20:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9929ebe968903c7ec659cd63387380ce6d67d71d89b3aaff7e25e88498d9f4f`  
		Last Modified: Wed, 31 Jan 2024 23:21:14 GMT  
		Size: 228.6 MB (228600719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4578f48d13366c6e89de835bdb1e621b304fe3b451be28831a26dc755fdbe21`  
		Last Modified: Wed, 31 Jan 2024 23:20:45 GMT  
		Size: 2.9 MB (2875696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ded20fc2d90d22e13985962e19406b67532f1b91a78efd931c3ce6e0e3a34`  
		Last Modified: Wed, 31 Jan 2024 23:20:44 GMT  
		Size: 460.4 KB (460376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64ef0a9967542f01bae6dde2934bd0097f526d5acbe4b602c59d355e6a13e19`  
		Last Modified: Wed, 31 Jan 2024 23:21:27 GMT  
		Size: 325.3 MB (325344872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368e3921b0be526f7f11ae9913312d79589a9681e91d65d0e9cb740b5a02cf3`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40d3d76056920c26b3ba5126a7d870b69512ae8708b11ef417d2286e9a914f7`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a914ea1d0c02fa225ccdb9a275a9d3404885a3b1c8b5ba97464833ffae55d011`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e508865adb2b6eee0ae39bf16668cad1dc96edf9b47c7372a2d059d35090b`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:97ddccdaf299a882e604f2f7764aa3d557c714c73a69e3930973e1b1ea805ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:5107e8b651960aeea7fb599ebfbfb297db074393410bab24b9c54450dced4fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 MB (578048134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e820958248b4ba2555e6decd6de3955f620cd4da58bb990f62fe4b26a9e3b201`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:45:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 01 Feb 2024 01:45:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 01 Feb 2024 01:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 01:45:14 GMT
ARG TARGETARCH
# Thu, 01 Feb 2024 01:46:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 01 Feb 2024 01:46:35 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:46:36 GMT
RUN npm install -g rtlcss
# Thu, 01 Feb 2024 01:46:36 GMT
ENV ODOO_VERSION=16.0
# Thu, 01 Feb 2024 01:46:37 GMT
ARG ODOO_RELEASE=20240126
# Thu, 01 Feb 2024 01:46:37 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Thu, 01 Feb 2024 01:47:59 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 01 Feb 2024 01:48:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 01 Feb 2024 01:48:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 01 Feb 2024 01:48:04 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 01 Feb 2024 01:48:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 01 Feb 2024 01:48:04 GMT
EXPOSE 8069 8071 8072
# Thu, 01 Feb 2024 01:48:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 01 Feb 2024 01:48:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 01 Feb 2024 01:48:05 GMT
USER odoo
# Thu, 01 Feb 2024 01:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 01:48:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143e90cebe7abe8b32c01c678e9650a1603ebd1c5f6e6df261ad7523f2ffef0e`  
		Last Modified: Thu, 01 Feb 2024 01:51:07 GMT  
		Size: 219.6 MB (219606136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f72d96f19396e06ecf6811c8588ac18ad8bdd5679d8fda3316097a0ff028a60`  
		Last Modified: Thu, 01 Feb 2024 01:50:43 GMT  
		Size: 2.6 MB (2629871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195a028377091ca4bd6b2d482c0148f8c977dd43a7c65825639fb3536640b06a`  
		Last Modified: Thu, 01 Feb 2024 01:50:42 GMT  
		Size: 460.3 KB (460320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113da6b51e397926b5cf2ace86fe044cf3c933b3e33ab1bb8488697a75e28dc4`  
		Last Modified: Thu, 01 Feb 2024 01:51:19 GMT  
		Size: 323.9 MB (323931511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f8489f07f3fa36f4ce4bac0769c5cdb5d6690ca999f8ab46c8042e48227095`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1ed2ae2c430e9679d40d3f7310308d6343c5d7cd99df15213dc256013d3928`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8c9f5eb5c551702a1800c0f3076fe2ae8f2469b3ff0ea21933053ee9b8c947`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405217a4655eadf877a7e68cd9880660f52d012e4a9000e19e554c85c322b6d3`  
		Last Modified: Thu, 01 Feb 2024 01:50:40 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ad73330c8d96630267903e0d6b839f03d4af5086c90335e31b3eeb91d5fe5ee5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.6 MB (573643853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec54843bdfcc534cc7e7d116f81f8302f32552636da245a175cddcd718a24995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:51:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 01 Feb 2024 07:51:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 01 Feb 2024 07:51:03 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 07:51:03 GMT
ARG TARGETARCH
# Thu, 01 Feb 2024 07:52:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 01 Feb 2024 07:52:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:52:13 GMT
RUN npm install -g rtlcss
# Thu, 01 Feb 2024 07:52:13 GMT
ENV ODOO_VERSION=16.0
# Thu, 01 Feb 2024 07:52:13 GMT
ARG ODOO_RELEASE=20240126
# Thu, 01 Feb 2024 07:52:13 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Thu, 01 Feb 2024 07:53:22 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 01 Feb 2024 07:53:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 01 Feb 2024 07:53:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 01 Feb 2024 07:53:30 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 01 Feb 2024 07:53:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 01 Feb 2024 07:53:30 GMT
EXPOSE 8069 8071 8072
# Thu, 01 Feb 2024 07:53:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 01 Feb 2024 07:53:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 01 Feb 2024 07:53:30 GMT
USER odoo
# Thu, 01 Feb 2024 07:53:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Feb 2024 07:53:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801c94d9b99558dd0c91673ac235a10cd79d8fcd77503950fea57c65e927dd6a`  
		Last Modified: Thu, 01 Feb 2024 07:54:08 GMT  
		Size: 216.9 MB (216909917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159feb7898d903ca4efcdf32c36396f982df611b948792a9e6baeb14650253ad`  
		Last Modified: Thu, 01 Feb 2024 07:53:50 GMT  
		Size: 2.6 MB (2634870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2542a05a5da97fcd4df51265ddc59cd08d41ca17f355cc5652da440c6ccb8ea9`  
		Last Modified: Thu, 01 Feb 2024 07:53:50 GMT  
		Size: 460.3 KB (460323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b499ca8410ca1009649c9f66a2c7b66177d25cd0187d1538ae822c132d5ed7`  
		Last Modified: Thu, 01 Feb 2024 07:54:18 GMT  
		Size: 323.6 MB (323571940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c673013c69e2bcb978fd9f0db2780b4e30c23ca6e47546c9fcc344c702e6bab`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb50bbb581dd33660b7895930e0e5ada368eee89eac65cb2580b210438b478f`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b6a644b519a1ad1dae9fac521309e112cfb5a8c13a4bc95933a14be37c4e1b`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3c6fbfb78790b50ffa9b176e85ec21c0884faa43b8cc89be6373e226f676a6`  
		Last Modified: Thu, 01 Feb 2024 07:53:48 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:d6318f4ff0b0123a3d161ae94bc584bc767ce03ca6b5eca69585dfa02b7e78c8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592577773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82bbfbe88d8b27f97cdef42d870c90d2705a121cae8e59f2deb2530c150ffe9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:13:54 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Jan 2024 23:13:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Jan 2024 23:13:55 GMT
ENV LANG=C.UTF-8
# Wed, 31 Jan 2024 23:13:55 GMT
ARG TARGETARCH
# Wed, 31 Jan 2024 23:17:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Jan 2024 23:17:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:17:26 GMT
RUN npm install -g rtlcss
# Wed, 31 Jan 2024 23:17:26 GMT
ENV ODOO_VERSION=16.0
# Wed, 31 Jan 2024 23:17:27 GMT
ARG ODOO_RELEASE=20240126
# Wed, 31 Jan 2024 23:17:28 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Wed, 31 Jan 2024 23:19:55 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 31 Jan 2024 23:20:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 31 Jan 2024 23:20:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 31 Jan 2024 23:20:16 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 31 Jan 2024 23:20:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 31 Jan 2024 23:20:17 GMT
EXPOSE 8069 8071 8072
# Wed, 31 Jan 2024 23:20:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 31 Jan 2024 23:20:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 31 Jan 2024 23:20:18 GMT
USER odoo
# Wed, 31 Jan 2024 23:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 23:20:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9929ebe968903c7ec659cd63387380ce6d67d71d89b3aaff7e25e88498d9f4f`  
		Last Modified: Wed, 31 Jan 2024 23:21:14 GMT  
		Size: 228.6 MB (228600719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4578f48d13366c6e89de835bdb1e621b304fe3b451be28831a26dc755fdbe21`  
		Last Modified: Wed, 31 Jan 2024 23:20:45 GMT  
		Size: 2.9 MB (2875696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ded20fc2d90d22e13985962e19406b67532f1b91a78efd931c3ce6e0e3a34`  
		Last Modified: Wed, 31 Jan 2024 23:20:44 GMT  
		Size: 460.4 KB (460376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64ef0a9967542f01bae6dde2934bd0097f526d5acbe4b602c59d355e6a13e19`  
		Last Modified: Wed, 31 Jan 2024 23:21:27 GMT  
		Size: 325.3 MB (325344872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368e3921b0be526f7f11ae9913312d79589a9681e91d65d0e9cb740b5a02cf3`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40d3d76056920c26b3ba5126a7d870b69512ae8708b11ef417d2286e9a914f7`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a914ea1d0c02fa225ccdb9a275a9d3404885a3b1c8b5ba97464833ffae55d011`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e508865adb2b6eee0ae39bf16668cad1dc96edf9b47c7372a2d059d35090b`  
		Last Modified: Wed, 31 Jan 2024 23:20:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:cf2ef1de7c7bf787e684a4012bb34ef2d3393c3a15b95b57a9017badf8202073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:22eb437ee8f3ad7c95018e684610f1837cb7853f97766f8ce79868b805ec01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596746215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7807feff361297d5d25d7d9429f6663f56cc6fe220904eadd59ece90f93e91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:11:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:11:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:11:12 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:13:00 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:13:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:13:13 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:13:13 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 22:13:52 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:13:52 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 22:15:45 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:15:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:15:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:15:50 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:15:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:15:50 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:15:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:15:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:15:50 GMT
USER odoo
# Fri, 26 Jan 2024 22:15:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:15:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a19db281065cfaaff50a903f954cd8cd0ab77efd9751ee9c2bd36ef33cd941`  
		Last Modified: Wed, 17 Jan 2024 08:16:00 GMT  
		Size: 233.7 MB (233730319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498266485268b12f1ed92ca683caf8de575184ea4c681cb8b806a9f9d4d7bd9`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 2.5 MB (2526563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692263bc03dc29d26ef3660e4aa016c65b762f3ef32bc7f072ef5fd882b670ff`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3ef509e6af3adee48fb7ce327eec9ff847119a965fe9cf6923a52034d7b37`  
		Last Modified: Fri, 26 Jan 2024 22:19:49 GMT  
		Size: 329.6 MB (329578295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a08f445a01fe15f9fa5b3997fc136394ced72ac601d2d6f1ab32660aca1e89a`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84d20496b2b190895306baa2b9ace6935308c99531caf0f38faaf71de8599e9`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d48b95f5d4d3a5de0ca1d07fc7217067b0ff0885b98e91d2a093af0bf2b2ed8`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42af27a3d07d14da8db922c77dcd6b7e3d30ed40f5523ea79c80eef633a11c62`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0397252673c497f786b7707a671c1a565967b6928d3902d934d46ac018f1b62a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591668457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76402d86a4c7228a45d3d2647d5ee43cea45ba06a3681992559657cd1d99da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:43:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 07:43:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 07:43:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 07:43:08 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 07:45:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 07:45:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:45:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 07:45:29 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 19:20:33 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 19:20:33 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 19:22:33 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 19:22:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 19:22:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 19:22:43 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 19:22:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 19:22:43 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 19:22:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 19:22:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 19:22:43 GMT
USER odoo
# Fri, 26 Jan 2024 19:22:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 19:22:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b02358e221961189c89c25333bfd0ef1760807bc50d71f914a02039d400a50`  
		Last Modified: Wed, 17 Jan 2024 07:48:02 GMT  
		Size: 231.1 MB (231110379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e38938c1ef4955deb704dcf4973073668ce7eff75a9034b6a7ea8d7a4d458`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 2.5 MB (2519326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e6bddb24b8b00fae6832e4428a94c80b5a6b8ff0e710477bed35dcb3ef4565`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 461.4 KB (461390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9bf08ff0b99ee62fcedfc85cb2f210d2f09ebcdac18bb9d441468b561a9e37`  
		Last Modified: Fri, 26 Jan 2024 19:25:16 GMT  
		Size: 329.2 MB (329175291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9478b1f1c26f6ac3703a40bad1d54816abb18725ac0b8eca572de28a7180d9`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fa1e0d7935157791e0057a4ad6c868482910f9cccebdf40266bbf6808f5ed`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185607d0769caa31c9e0b764ac5af292fc29c1ff4b911b1eeebd674a722d404`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3a9c49f4b6864f8f2f24573063a1de83a98800cdd6c7666c6234ce17c0a01`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:0a2dca086f3cfd5cb56cc80d9416135b0377171d6c17586ae4c3c887dacfc933
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613524697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a07cb6993e9d27c6aeb5046502df076e628c98c102f4a542f239dbb1942e9e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:00:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:00:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:00:33 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:05:34 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:05:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:01 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:06:01 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 20:45:01 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 20:45:01 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 20:47:51 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 20:48:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 20:48:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 20:48:04 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 20:48:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 20:48:05 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 20:48:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 20:48:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 20:48:06 GMT
USER odoo
# Fri, 26 Jan 2024 20:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 20:48:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcb20763fdcfb23eafb90744955b7c8403e4c9f4e0eb528e5e52f5966a7fbd`  
		Last Modified: Wed, 17 Jan 2024 08:11:11 GMT  
		Size: 243.3 MB (243285415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb20cbe165f4e4451478c82ca6213daeab6f98bea1bcaa439eb5e081dfd17d`  
		Last Modified: Wed, 17 Jan 2024 08:10:38 GMT  
		Size: 2.8 MB (2803440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0410b6743b107a0ae4ccbab9d310eacd59731c7b95cf9a6504fed01785d284`  
		Last Modified: Wed, 17 Jan 2024 08:10:37 GMT  
		Size: 461.4 KB (461416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8bf1118851844e350846b380678de0127f301084c83a18422d84df55332be9`  
		Last Modified: Fri, 26 Jan 2024 20:51:58 GMT  
		Size: 331.3 MB (331314802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b71cb9b0b632d407931356dd3e0ac6ed9831cd21e52f485c3243731dbcc62c5`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8d3991cfdd2a2d2db3fff40e4da802286b57decdbedf2c70fefb27267d247e`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cef04d641c9b703bb62df742c0db9d495bfbeff51953aff19bc7afe782095f5`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b880801de218a65c6271331ae9c8e3ce06040cf63db4ac924162daeeb9f70fe`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cf2ef1de7c7bf787e684a4012bb34ef2d3393c3a15b95b57a9017badf8202073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:22eb437ee8f3ad7c95018e684610f1837cb7853f97766f8ce79868b805ec01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596746215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7807feff361297d5d25d7d9429f6663f56cc6fe220904eadd59ece90f93e91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:11:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:11:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:11:12 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:13:00 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:13:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:13:13 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:13:13 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 22:13:52 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:13:52 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 22:15:45 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:15:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:15:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:15:50 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:15:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:15:50 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:15:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:15:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:15:50 GMT
USER odoo
# Fri, 26 Jan 2024 22:15:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:15:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a19db281065cfaaff50a903f954cd8cd0ab77efd9751ee9c2bd36ef33cd941`  
		Last Modified: Wed, 17 Jan 2024 08:16:00 GMT  
		Size: 233.7 MB (233730319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498266485268b12f1ed92ca683caf8de575184ea4c681cb8b806a9f9d4d7bd9`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 2.5 MB (2526563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692263bc03dc29d26ef3660e4aa016c65b762f3ef32bc7f072ef5fd882b670ff`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3ef509e6af3adee48fb7ce327eec9ff847119a965fe9cf6923a52034d7b37`  
		Last Modified: Fri, 26 Jan 2024 22:19:49 GMT  
		Size: 329.6 MB (329578295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a08f445a01fe15f9fa5b3997fc136394ced72ac601d2d6f1ab32660aca1e89a`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84d20496b2b190895306baa2b9ace6935308c99531caf0f38faaf71de8599e9`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d48b95f5d4d3a5de0ca1d07fc7217067b0ff0885b98e91d2a093af0bf2b2ed8`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42af27a3d07d14da8db922c77dcd6b7e3d30ed40f5523ea79c80eef633a11c62`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0397252673c497f786b7707a671c1a565967b6928d3902d934d46ac018f1b62a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591668457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76402d86a4c7228a45d3d2647d5ee43cea45ba06a3681992559657cd1d99da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:43:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 07:43:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 07:43:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 07:43:08 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 07:45:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 07:45:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:45:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 07:45:29 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 19:20:33 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 19:20:33 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 19:22:33 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 19:22:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 19:22:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 19:22:43 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 19:22:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 19:22:43 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 19:22:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 19:22:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 19:22:43 GMT
USER odoo
# Fri, 26 Jan 2024 19:22:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 19:22:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b02358e221961189c89c25333bfd0ef1760807bc50d71f914a02039d400a50`  
		Last Modified: Wed, 17 Jan 2024 07:48:02 GMT  
		Size: 231.1 MB (231110379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e38938c1ef4955deb704dcf4973073668ce7eff75a9034b6a7ea8d7a4d458`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 2.5 MB (2519326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e6bddb24b8b00fae6832e4428a94c80b5a6b8ff0e710477bed35dcb3ef4565`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 461.4 KB (461390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9bf08ff0b99ee62fcedfc85cb2f210d2f09ebcdac18bb9d441468b561a9e37`  
		Last Modified: Fri, 26 Jan 2024 19:25:16 GMT  
		Size: 329.2 MB (329175291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9478b1f1c26f6ac3703a40bad1d54816abb18725ac0b8eca572de28a7180d9`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fa1e0d7935157791e0057a4ad6c868482910f9cccebdf40266bbf6808f5ed`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185607d0769caa31c9e0b764ac5af292fc29c1ff4b911b1eeebd674a722d404`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3a9c49f4b6864f8f2f24573063a1de83a98800cdd6c7666c6234ce17c0a01`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0a2dca086f3cfd5cb56cc80d9416135b0377171d6c17586ae4c3c887dacfc933
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613524697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a07cb6993e9d27c6aeb5046502df076e628c98c102f4a542f239dbb1942e9e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:00:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:00:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:00:33 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:05:34 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:05:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:01 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:06:01 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 20:45:01 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 20:45:01 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 20:47:51 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 20:48:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 20:48:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 20:48:04 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 20:48:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 20:48:05 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 20:48:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 20:48:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 20:48:06 GMT
USER odoo
# Fri, 26 Jan 2024 20:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 20:48:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcb20763fdcfb23eafb90744955b7c8403e4c9f4e0eb528e5e52f5966a7fbd`  
		Last Modified: Wed, 17 Jan 2024 08:11:11 GMT  
		Size: 243.3 MB (243285415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb20cbe165f4e4451478c82ca6213daeab6f98bea1bcaa439eb5e081dfd17d`  
		Last Modified: Wed, 17 Jan 2024 08:10:38 GMT  
		Size: 2.8 MB (2803440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0410b6743b107a0ae4ccbab9d310eacd59731c7b95cf9a6504fed01785d284`  
		Last Modified: Wed, 17 Jan 2024 08:10:37 GMT  
		Size: 461.4 KB (461416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8bf1118851844e350846b380678de0127f301084c83a18422d84df55332be9`  
		Last Modified: Fri, 26 Jan 2024 20:51:58 GMT  
		Size: 331.3 MB (331314802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b71cb9b0b632d407931356dd3e0ac6ed9831cd21e52f485c3243731dbcc62c5`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8d3991cfdd2a2d2db3fff40e4da802286b57decdbedf2c70fefb27267d247e`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cef04d641c9b703bb62df742c0db9d495bfbeff51953aff19bc7afe782095f5`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b880801de218a65c6271331ae9c8e3ce06040cf63db4ac924162daeeb9f70fe`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:cf2ef1de7c7bf787e684a4012bb34ef2d3393c3a15b95b57a9017badf8202073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:22eb437ee8f3ad7c95018e684610f1837cb7853f97766f8ce79868b805ec01b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596746215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7807feff361297d5d25d7d9429f6663f56cc6fe220904eadd59ece90f93e91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:11:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:11:12 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:11:12 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:13:00 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:13:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:13:13 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:13:13 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 22:13:52 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:13:52 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 22:15:45 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:15:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:15:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:15:50 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:15:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:15:50 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:15:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:15:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:15:50 GMT
USER odoo
# Fri, 26 Jan 2024 22:15:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:15:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a19db281065cfaaff50a903f954cd8cd0ab77efd9751ee9c2bd36ef33cd941`  
		Last Modified: Wed, 17 Jan 2024 08:16:00 GMT  
		Size: 233.7 MB (233730319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498266485268b12f1ed92ca683caf8de575184ea4c681cb8b806a9f9d4d7bd9`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 2.5 MB (2526563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692263bc03dc29d26ef3660e4aa016c65b762f3ef32bc7f072ef5fd882b670ff`  
		Last Modified: Wed, 17 Jan 2024 08:15:33 GMT  
		Size: 461.5 KB (461460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3ef509e6af3adee48fb7ce327eec9ff847119a965fe9cf6923a52034d7b37`  
		Last Modified: Fri, 26 Jan 2024 22:19:49 GMT  
		Size: 329.6 MB (329578295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a08f445a01fe15f9fa5b3997fc136394ced72ac601d2d6f1ab32660aca1e89a`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84d20496b2b190895306baa2b9ace6935308c99531caf0f38faaf71de8599e9`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d48b95f5d4d3a5de0ca1d07fc7217067b0ff0885b98e91d2a093af0bf2b2ed8`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42af27a3d07d14da8db922c77dcd6b7e3d30ed40f5523ea79c80eef633a11c62`  
		Last Modified: Fri, 26 Jan 2024 22:19:11 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0397252673c497f786b7707a671c1a565967b6928d3902d934d46ac018f1b62a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591668457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76402d86a4c7228a45d3d2647d5ee43cea45ba06a3681992559657cd1d99da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:43:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 07:43:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 07:43:08 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 07:43:08 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 07:45:13 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 07:45:27 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:45:29 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 07:45:29 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 19:20:33 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 19:20:33 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 19:22:33 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 19:22:42 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 19:22:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 19:22:43 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 19:22:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 19:22:43 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 19:22:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 19:22:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 19:22:43 GMT
USER odoo
# Fri, 26 Jan 2024 19:22:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 19:22:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b02358e221961189c89c25333bfd0ef1760807bc50d71f914a02039d400a50`  
		Last Modified: Wed, 17 Jan 2024 07:48:02 GMT  
		Size: 231.1 MB (231110379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e38938c1ef4955deb704dcf4973073668ce7eff75a9034b6a7ea8d7a4d458`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 2.5 MB (2519326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e6bddb24b8b00fae6832e4428a94c80b5a6b8ff0e710477bed35dcb3ef4565`  
		Last Modified: Wed, 17 Jan 2024 07:47:41 GMT  
		Size: 461.4 KB (461390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9bf08ff0b99ee62fcedfc85cb2f210d2f09ebcdac18bb9d441468b561a9e37`  
		Last Modified: Fri, 26 Jan 2024 19:25:16 GMT  
		Size: 329.2 MB (329175291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9478b1f1c26f6ac3703a40bad1d54816abb18725ac0b8eca572de28a7180d9`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fa1e0d7935157791e0057a4ad6c868482910f9cccebdf40266bbf6808f5ed`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185607d0769caa31c9e0b764ac5af292fc29c1ff4b911b1eeebd674a722d404`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3a9c49f4b6864f8f2f24573063a1de83a98800cdd6c7666c6234ce17c0a01`  
		Last Modified: Fri, 26 Jan 2024 19:24:40 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:0a2dca086f3cfd5cb56cc80d9416135b0377171d6c17586ae4c3c887dacfc933
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613524697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a07cb6993e9d27c6aeb5046502df076e628c98c102f4a542f239dbb1942e9e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:00:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 17 Jan 2024 08:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 17 Jan 2024 08:00:32 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Jan 2024 08:00:33 GMT
ARG TARGETARCH
# Wed, 17 Jan 2024 08:05:34 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 17 Jan 2024 08:05:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:01 GMT
RUN npm install -g rtlcss
# Wed, 17 Jan 2024 08:06:01 GMT
ENV ODOO_VERSION=17.0
# Fri, 26 Jan 2024 20:45:01 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 20:45:01 GMT
ARG ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
# Fri, 26 Jan 2024 20:47:51 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 20:48:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 20:48:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 20:48:04 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=b7af5d42448107e6efee183cf250e7365eb76e8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 20:48:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 20:48:05 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 20:48:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 20:48:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 20:48:06 GMT
USER odoo
# Fri, 26 Jan 2024 20:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 20:48:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bcb20763fdcfb23eafb90744955b7c8403e4c9f4e0eb528e5e52f5966a7fbd`  
		Last Modified: Wed, 17 Jan 2024 08:11:11 GMT  
		Size: 243.3 MB (243285415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb20cbe165f4e4451478c82ca6213daeab6f98bea1bcaa439eb5e081dfd17d`  
		Last Modified: Wed, 17 Jan 2024 08:10:38 GMT  
		Size: 2.8 MB (2803440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0410b6743b107a0ae4ccbab9d310eacd59731c7b95cf9a6504fed01785d284`  
		Last Modified: Wed, 17 Jan 2024 08:10:37 GMT  
		Size: 461.4 KB (461416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8bf1118851844e350846b380678de0127f301084c83a18422d84df55332be9`  
		Last Modified: Fri, 26 Jan 2024 20:51:58 GMT  
		Size: 331.3 MB (331314802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b71cb9b0b632d407931356dd3e0ac6ed9831cd21e52f485c3243731dbcc62c5`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8d3991cfdd2a2d2db3fff40e4da802286b57decdbedf2c70fefb27267d247e`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cef04d641c9b703bb62df742c0db9d495bfbeff51953aff19bc7afe782095f5`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b880801de218a65c6271331ae9c8e3ce06040cf63db4ac924162daeeb9f70fe`  
		Last Modified: Fri, 26 Jan 2024 20:51:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
