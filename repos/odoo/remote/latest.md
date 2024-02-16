## `odoo:latest`

```console
$ docker pull odoo@sha256:5f611a42dba2807ada424ffa03d4de79fa9afdc86400ce15247e7e1536f4c010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:6a2618d78d3dc8028022349a49c6010fea05fba599474b2110bc7459eb55f735
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597715370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22abe3e67970010cb8f77000118f480ce5816448fbd6facb25ab4e067210d5ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 02:26:12 GMT
ARG ODOO_RELEASE=20240209
# Fri, 16 Feb 2024 02:26:12 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 16 Feb 2024 02:28:06 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 02:28:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 02:28:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 02:28:10 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 02:28:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 02:28:11 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 02:28:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 02:28:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 02:28:11 GMT
USER odoo
# Fri, 16 Feb 2024 02:28:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 02:28:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a0dac4d6f66e57df36fbac2f596cdf133cb3342b39924dc0bb079745b1bde0`  
		Last Modified: Fri, 16 Feb 2024 02:29:14 GMT  
		Size: 330.5 MB (330538030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1eb84f8b0975b8d939555d866b3245811df653929c8fc9a61c887151967916`  
		Last Modified: Fri, 16 Feb 2024 02:28:33 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56875c88459d1b34284bfad1be138aebd8e76de1f42e7604ab47ecdf978985cf`  
		Last Modified: Fri, 16 Feb 2024 02:28:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a1f8cc498079130ac4a7b9a2d33c75ec6566264d40376f0c6bf7b68ace20bc`  
		Last Modified: Fri, 16 Feb 2024 02:28:33 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8488c4ed205d3897b7a89e913d9bf1f95ee67406bd9d86d09b8de1078382d60a`  
		Last Modified: Fri, 16 Feb 2024 02:28:33 GMT  
		Size: 584.0 B  
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
$ docker pull odoo@sha256:e05befc52f358b2249b3cbc5330291ccfd9b043f7fdd98ea8411165a0c84e995
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614471523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8b14e8a7a6e92a70a1467ad221042c4e6598628ef589a9bb52c93c7f8fb88f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Fri, 16 Feb 2024 03:18:54 GMT
ARG ODOO_RELEASE=20240209
# Fri, 16 Feb 2024 03:18:56 GMT
ARG ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
# Fri, 16 Feb 2024 03:22:33 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 16 Feb 2024 03:22:52 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 16 Feb 2024 03:22:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 16 Feb 2024 03:22:56 GMT
# ARGS: ODOO_RELEASE=20240209 ODOO_SHA=31a181b2ed0bcd303a955ea3716e59b2c3d2c20f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 16 Feb 2024 03:22:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 16 Feb 2024 03:22:58 GMT
EXPOSE 8069 8071 8072
# Fri, 16 Feb 2024 03:22:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 16 Feb 2024 03:22:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 16 Feb 2024 03:23:00 GMT
USER odoo
# Fri, 16 Feb 2024 03:23:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Feb 2024 03:23:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf356e94b01a9c8a61e75635009dcfacdce59dcd86f2547045d3a6dfc34e9d6`  
		Last Modified: Fri, 16 Feb 2024 03:24:12 GMT  
		Size: 332.3 MB (332274565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efc8cd6aa474749d0fcadd996c7eb94540fe7b40030f018e5e4b0c7578fb3cb`  
		Last Modified: Fri, 16 Feb 2024 03:23:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4db83ba44c8583d495d22d4d8d9c8e7a9b8ed0e07ae1cc33b9abffa9aa93dc4`  
		Last Modified: Fri, 16 Feb 2024 03:23:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99602ec40ed5da3d937992921b25c03b026d25494c10b99be92f295ab5a0f06d`  
		Last Modified: Fri, 16 Feb 2024 03:23:25 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f16dfea0db05b77f974ed0a182d1dfb9d871d25c57c158da5096acac8dd786`  
		Last Modified: Fri, 16 Feb 2024 03:23:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
