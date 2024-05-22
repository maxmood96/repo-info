## `odoo:latest`

```console
$ docker pull odoo@sha256:0997f730dce9110b12d7e6eb25d38f90837386905b8cf4444214f323df803b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:b2d63bb6503b43bcc3f3c6d922c94ad88006ec3f6cbff3a70e64d0215630f035
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.1 MB (603142296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de380444ec672807196166f4aea402d8fb9593d0d9f39edbcb9a4c45a3f856`
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
# Thu, 02 May 2024 01:48:45 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:48:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:48:45 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:48:45 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:50:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:51:11 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 19:54:41 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 19:54:41 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 19:56:51 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 22 May 2024 19:56:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 22 May 2024 19:56:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 22 May 2024 19:56:56 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 22 May 2024 19:56:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 19:56:56 GMT
EXPOSE 8069 8071 8072
# Wed, 22 May 2024 19:56:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 19:56:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 22 May 2024 19:56:56 GMT
USER odoo
# Wed, 22 May 2024 19:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 19:56:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc6a2729a2817ef06e9dda70829f42a53a97239cae20c2bacedb195d297ba0b`  
		Last Modified: Thu, 02 May 2024 01:54:19 GMT  
		Size: 233.7 MB (233722654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be642aed9f10700697e78c3c790686681140e29aac403b5a36a0bf73d128f74`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 2.5 MB (2530493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e6603812dc2dc31a6600fde661fd0f472c1db60ffdf7f131ca3a241518b9b`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 459.5 KB (459460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc882985350334532d250ce22c1332d0c16622dad0d5b9c1392bb19a7b5e623b`  
		Last Modified: Wed, 22 May 2024 20:00:58 GMT  
		Size: 336.0 MB (335987571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dc08bfef559acd6ec0d49cfffb61183f7e92918497be04bb8767f6f73674a9`  
		Last Modified: Wed, 22 May 2024 20:00:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3e89552c05aaf7fcceb22da4a4112a484e3e9bfbd691b4212517ba80f91c30`  
		Last Modified: Wed, 22 May 2024 20:00:20 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0719fa2ff700d2c98c7d531b1f8ccbcfa595365f09c3c9af751c25830a4298`  
		Last Modified: Wed, 22 May 2024 20:00:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56733b9557595fbb0347888d4835a8eb23584948b87a426a904246e9ad0ba2de`  
		Last Modified: Wed, 22 May 2024 20:00:19 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:576a3ca2d18d74f5aee91d26921573b84805b6a1e4edf8447c650ae0becc3734
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598088280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3418aa89ab7b164589c9602211aaacaee64319124d8cda9d93e537427ded844`
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
# Thu, 02 May 2024 01:28:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:28:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:28:33 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:28:33 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:30:55 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:31:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:31:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:31:11 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 19:58:58 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 19:58:58 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 20:01:20 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 22 May 2024 20:01:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 22 May 2024 20:01:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 22 May 2024 20:01:30 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 22 May 2024 20:01:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 20:01:30 GMT
EXPOSE 8069 8071 8072
# Wed, 22 May 2024 20:01:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 20:01:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 22 May 2024 20:01:30 GMT
USER odoo
# Wed, 22 May 2024 20:01:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 20:01:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5983fdb42d6e446c61ffd23ea73a31d297eb116faab716b0a05982385aef7`  
		Last Modified: Thu, 02 May 2024 01:33:56 GMT  
		Size: 231.1 MB (231130596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51c84c847e95593779366fe62fbfc47376ab1cbb6b6a2891c096fbce365476`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 2.5 MB (2523315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821493b21fb69aad8b99473d2e8c6fbc2c2ef7b66fe8255b0856b3929182b80`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 459.4 KB (459401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395097b419f1653ad2f1bd560801bd7445fbfa6b5fa3cf4058aaf2dd117314e6`  
		Last Modified: Wed, 22 May 2024 20:03:53 GMT  
		Size: 335.6 MB (335571319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3022d74fcd3ee7b048231cd8d267a277018b56628a0e82e9831a071924143e9`  
		Last Modified: Wed, 22 May 2024 20:03:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef30f983608477172c69e8c399ea1488d8771405243a0ad20dd3e18c7852d17a`  
		Last Modified: Wed, 22 May 2024 20:03:22 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6db5452f9e3e9c79377e441f5c2b65ba5ebf66766f3f63a9a8587fdebfd440`  
		Last Modified: Wed, 22 May 2024 20:03:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9703cbc51fd3a98443851c5003332ca3191290e461fe9b5c7a82cffddf28ffa9`  
		Last Modified: Wed, 22 May 2024 20:03:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a908e7398e0a3b12c5200bf8bed3c9159a38035448cfe3d27a975be3434d0cb7
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.9 MB (619898937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a65e4f1e0733f97750d43fce19955c5a9aea0a3c16950ad5717aa9a21234a0`
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
# Thu, 02 May 2024 02:35:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 02:35:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 02:35:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 02:35:02 GMT
ARG TARGETARCH
# Thu, 02 May 2024 02:39:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 02:39:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:39:35 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 02:39:35 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 19:10:58 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 19:10:59 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 19:13:58 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 22 May 2024 19:14:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 22 May 2024 19:14:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 22 May 2024 19:14:15 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 22 May 2024 19:14:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 19:14:16 GMT
EXPOSE 8069 8071 8072
# Wed, 22 May 2024 19:14:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 19:14:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 22 May 2024 19:14:17 GMT
USER odoo
# Wed, 22 May 2024 19:14:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 19:14:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25675fc6cdcee8d4016b34ff54239a1de0278ba15b6ac0af402ce732889c506`  
		Last Modified: Thu, 02 May 2024 02:44:10 GMT  
		Size: 243.3 MB (243299854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366bfa6d5ff39e1ec4aa3977efc2d8ae2e82fea7a6c2dd6b4cc84294fcb1146`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 2.8 MB (2806021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273121e099b8f0742274ce6668b942df2b9a2e52972b6c0d594210cbec8bc9d`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 459.4 KB (459395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fd93296112c531c8714ae25fab3dac2a55cdc5d4162f691ca720c6127b018b`  
		Last Modified: Wed, 22 May 2024 19:17:57 GMT  
		Size: 337.7 MB (337742675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5bc9c2a4d949dd9cc9353046c5bf086a8b5b7bbe956ef1b03f318624fd2835`  
		Last Modified: Wed, 22 May 2024 19:17:10 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb5a658683a31c97a5facb8c57da12a5e106344c7eb67906dc1168a25385a88`  
		Last Modified: Wed, 22 May 2024 19:17:10 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f49e372640b698a1ede3fa257fffe15275480f9545c1a789b46cd976a6c65`  
		Last Modified: Wed, 22 May 2024 19:17:10 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f6f89108c411071f7a331958c817166f3a92c4ea79103cabbfe92673590f8`  
		Last Modified: Wed, 22 May 2024 19:17:10 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
