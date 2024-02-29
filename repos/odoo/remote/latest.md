## `odoo:latest`

```console
$ docker pull odoo@sha256:7be75cd6e517879310f9dec9090a6b25345a5bc219c4ba22f7bab9c699faff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f065f2807c55742df979983385d59cf3d14c79b723d7d429fa505c2bb334553e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599406969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697778a8975ba915513dee14438d400acb0530fe9d081436803d284a360e678a`
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
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:26:56 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:27:01 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:27:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:27:01 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:27:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:27:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:27:01 GMT
USER odoo
# Thu, 29 Feb 2024 19:27:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:27:02 GMT
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
	-	`sha256:e22d57e76feea15161f1175c14a0a856e03dc43dbc6da22a041da58ebc88d955`  
		Last Modified: Thu, 29 Feb 2024 19:30:59 GMT  
		Size: 332.2 MB (332229624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36b42850688489fa3442c640666220579431ab3ca5b9b6e7823849711f50410`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8959e3f4c53355556f6a26b9554fa7969df4f52095ef3ab438d857b34b21537`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542d98e71ed36e5196e8e56eb51672cee90d0245955cd3a096fe7890e25988bd`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68b296b826c18e0e8ba7f34f7431a26f00c6771e9601ffa54b0918609e4496`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1c63df832deecd947510d65e5621614ffc3541271abe48a49af8110bb583956
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594346613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c2f00b9636ad33d8c21a692ded2676a4bde8e691252b5d883190024703abf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:45:16 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:45:24 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:45:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:45:24 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:45:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:45:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:45:24 GMT
USER odoo
# Thu, 29 Feb 2024 19:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:45:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13d8a9c09a0c31b0f1b434558bb21f9b19aab8848ee2ca00ae11928e2abe880`  
		Last Modified: Thu, 29 Feb 2024 19:48:04 GMT  
		Size: 331.8 MB (331839098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2faf5b2bfcea0182fc16423c651920a4b5d478285e62c59c6483b96d38ef039`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23e5d5ddfd77ab78b728e615bac24e5d20f62cec2346e1bfd6c9fbee95b495f`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f4c5f6f6f8e35d77bb355a41e6de56e4abb34dc0b3888d06f6098532b8caef`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb9bf8ad500de9273712c13cf52dae548d7dff9f91afee8f39f334e99a5b13`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:ce6893908c634487e5626800434c6689338080bb4e82a287f3fca420e3e8a0ba
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616170059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136b2c387d57e154e9f4a2ae521d18d0d52ae73df1409c3723caaf04ac4f331`
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
# Thu, 29 Feb 2024 19:16:50 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:16:51 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:21:04 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:21:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:21:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:21:22 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:21:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:21:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:21:25 GMT
USER odoo
# Thu, 29 Feb 2024 19:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:21:27 GMT
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
	-	`sha256:f6c147f01b56f517aef5569dc2b1506841c81a78033dfa7959d3a24c26d403e8`  
		Last Modified: Thu, 29 Feb 2024 19:26:59 GMT  
		Size: 334.0 MB (333973101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6114963141787810168c32632e6c3a80614e29c382ff509ef5afa13c0228a21b`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a1f7b02ac82bd9b532437758284eff1241f4d3560a49c229c0f84b9d7db0`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f60372d84f5bfaa48edebe504dce062d94a1036d2b3c0d965e439d1d9f5242`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec325085226e97230efc8b1236735a7b77194124b24ce3afeb4e1acea694c9d3`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
