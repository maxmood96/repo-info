## `odoo:latest`

```console
$ docker pull odoo@sha256:be16d3cb13eb8f0b75a0d6afc61d36b58341b69769739544a2769f0815b80291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:34686e2e2e11aa291eb19dd7fa5fecdb5e76ba0869795832bdaa015994c2cee3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596442551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a770ff11013f1e31263ebc64e0c24bc364e128e63ea312a8bf42942223666f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:29:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 09:29:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 09:29:57 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 09:29:57 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 09:32:06 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 09:32:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:32:18 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 09:32:18 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:35:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:37:20 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:37:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:37:24 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:37:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:37:24 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:37:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:37:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:37:25 GMT
USER odoo
# Tue, 16 Jan 2024 18:37:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:37:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89681bc3d92fa58300c17f37a8c00221342b77325e00deb20e71ea410071d500`  
		Last Modified: Sat, 16 Dec 2023 09:34:46 GMT  
		Size: 233.7 MB (233730172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5a3dc4306b241f9806eface9e5fe3c10ef771e41f03509a141414da8bb7c04`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 2.5 MB (2526485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746699b2b8c3aebf90f574a4692f492e2e617506c92d7a00874d79e4fddaf014`  
		Last Modified: Sat, 16 Dec 2023 09:34:19 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9312bd794422cccecb264eb665eb9d60e8e07f9e5dcfd762cdae2858b581c5`  
		Last Modified: Tue, 16 Jan 2024 18:41:26 GMT  
		Size: 329.3 MB (329275713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d040fa2098f3c95eef1cd85963e35c1be2cb1d7813579c8db848019ca444eb32`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff7d4d6049c2b3b10f5d2836254c47a75878be3b16dae7efb9fadad5623912e`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6813d9b0620ed15ec31190029d7ee73762ec76ebb99b55dafd4555b615d3e3`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036555d3f0b2644cc421f7dc5f1ff4c983d9c17572a8e630103390836f0f2bf`  
		Last Modified: Tue, 16 Jan 2024 18:40:48 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fea3c2e90c2f105a4f3e7c5a5cb866d01f6f294a570fc16d5a6b6f15b3abb6b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591382864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5c91da6daa2abf3f05f79f785ac6e846571b16b7ff4b7ff878adb26b9e1716`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:59:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 10:59:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 10:59:32 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 10:59:32 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:01:54 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:02:08 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:02:09 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:02:09 GMT
ENV ODOO_VERSION=17.0
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_RELEASE=20240115
# Tue, 16 Jan 2024 18:41:14 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Tue, 16 Jan 2024 18:43:38 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 16 Jan 2024 18:43:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 16 Jan 2024 18:43:40 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 16 Jan 2024 18:43:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 16 Jan 2024 18:43:40 GMT
EXPOSE 8069 8071 8072
# Tue, 16 Jan 2024 18:43:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 16 Jan 2024 18:43:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 16 Jan 2024 18:43:40 GMT
USER odoo
# Tue, 16 Jan 2024 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jan 2024 18:43:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed064f4459a4f1ab48040e16f6b55972797bd014de0d33737d676d7a1a25db4`  
		Last Modified: Sat, 16 Dec 2023 11:04:40 GMT  
		Size: 231.1 MB (231107542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217c6a3bbcbbb21c659f79f47bd7f96d743d57cfd0fe0b1678b81f7ff769a77`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 2.5 MB (2520464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce39a7573fc5d23b0ecb7a2dc95f9c6c6ea441c6712f6c192b2807e2aa72feb`  
		Last Modified: Sat, 16 Dec 2023 11:04:20 GMT  
		Size: 461.1 KB (461075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8365cc03105765cbac69f6af6ab40ee50e70f99e8588525212a99b3109015265`  
		Last Modified: Tue, 16 Jan 2024 18:46:17 GMT  
		Size: 328.9 MB (328891032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8bebed78a1ea93f549f2bdb8ddadcdfcc0677a47e0e34e55e3eb433035df28`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1bdd1ab1c23fc5f02c8030847ffdba019119c85ad58893912478aac4027a56`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e854652194f0c7ba3c4140b0a0b3cd58cf3485c4facf6905a0f1539a0d8834`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b474447fb3a94bcc6d563776c31968090b5d60b27f31f29e84474c3d39ca07b`  
		Last Modified: Tue, 16 Jan 2024 18:45:36 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:7fe7fe925fab08ac8ef939ca19bba24340b8163a26807cda0e12d23be1ef0a58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613189453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073370c528f7a6b6e027696d4d13f6c57d45bc4e7087d70b699d1748855d9c76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:18:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 16 Dec 2023 11:18:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 16 Dec 2023 11:18:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 11:18:23 GMT
ARG TARGETARCH
# Sat, 16 Dec 2023 11:22:08 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 16 Dec 2023 11:22:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:22:30 GMT
RUN npm install -g rtlcss
# Sat, 16 Dec 2023 11:22:30 GMT
ENV ODOO_VERSION=17.0
# Thu, 04 Jan 2024 20:39:57 GMT
ARG ODOO_RELEASE=20240104
# Thu, 04 Jan 2024 20:39:58 GMT
ARG ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
# Thu, 04 Jan 2024 20:43:11 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 04 Jan 2024 20:43:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 04 Jan 2024 20:43:29 GMT
# ARGS: ODOO_RELEASE=20240104 ODOO_SHA=d6f7e9309786857f820333698010903b1c621c5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 04 Jan 2024 20:43:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 04 Jan 2024 20:43:30 GMT
EXPOSE 8069 8071 8072
# Thu, 04 Jan 2024 20:43:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 04 Jan 2024 20:43:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 04 Jan 2024 20:43:32 GMT
USER odoo
# Thu, 04 Jan 2024 20:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jan 2024 20:43:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc829e9bac0988cf5b8041cc64556998568034e96cd72e93b700c2ac4d3f6330`  
		Last Modified: Sat, 16 Dec 2023 11:26:30 GMT  
		Size: 243.3 MB (243296411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77915009472ee87b9142650dd27d791d648dc1cb35fd84a5b5e471802c2476ab`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b76a07b6810b56620d5e557ab7a8e64c61a46a1af3a1452dc22677cd585e67`  
		Last Modified: Sat, 16 Dec 2023 11:25:58 GMT  
		Size: 461.2 KB (461168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280397ddd60459cc8aaccada3a3e2dbaee17a792d80e29704706d28e00631371`  
		Last Modified: Thu, 04 Jan 2024 20:47:38 GMT  
		Size: 331.0 MB (330970863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3cb092fd02e8e0e54aa4e1cb3f55d5bc88ab2bcb659ddfd3d4bdf082963733`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1423ad8516811b7707b8770003a0e47af59b799e3d4120a56dfb3376fd77bf`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d518f7ee4905a3980f6fc47020d7368b1a206e8f39e19eb220a69035123545b3`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b109be03f47c8824d4ede96171b9dc3bf26949515e105f259ca6242e8dcb29a`  
		Last Modified: Thu, 04 Jan 2024 20:46:45 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
