## `odoo:latest`

```console
$ docker pull odoo@sha256:cedd12e5ee13c7bdc8591735098d083e9dadc88e6bbf49c2f95f2394f6fb4dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f53d796cbc5c47e4a0521fa608339a296d702a2343729434333451059b1241d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.4 MB (596444727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a27fdb4c82a344205d6e4de1ccb831ca53d14c716da171642be05f070187c27`
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
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:13:13 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:15:00 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:15:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:15:04 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:15:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:15:04 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:15:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:15:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:15:05 GMT
USER odoo
# Wed, 17 Jan 2024 08:15:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:15:05 GMT
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
	-	`sha256:65258011f7d95bc5c6666ff8b962a40af90eced980825c3fb9e8e1c3b2745265`  
		Last Modified: Wed, 17 Jan 2024 08:16:10 GMT  
		Size: 329.3 MB (329276798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebb976892adf6ad32a733852a334284401fba552da4b4bbc85fd6ae234e67c3`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce93c83bae47703bebe7594c6628caf21477aec318f388692bfa6a858fea849`  
		Last Modified: Wed, 17 Jan 2024 08:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df82699b4af6ed000dea119fba0cd353c552b1b3eab89193b41cba2f75d4d7`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a7624844c3f8dd7be7303cd388326c370239754d6b1f700b005871f7127685`  
		Last Modified: Wed, 17 Jan 2024 08:15:30 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f93ea522fb7d417657956707f082054e12456dd689b9d9d9a2d22a5a33c66a45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.4 MB (591381814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5893d324f528244ba33334492efe7c97cd54996716de48d2fb51890d941c1318`
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
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 07:45:29 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 07:47:17 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 07:47:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 07:47:25 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 07:47:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 07:47:25 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 07:47:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 07:47:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 07:47:25 GMT
USER odoo
# Wed, 17 Jan 2024 07:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 07:47:25 GMT
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
	-	`sha256:ce00313e2b01b8c4fa486aa894e7cf16f9256dfdc0cdb3f682e1633b60243c35`  
		Last Modified: Wed, 17 Jan 2024 07:48:08 GMT  
		Size: 328.9 MB (328888639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32acc1437d8329f75c61fbfc9f603dd3f19c2e56c219c015c38d02dbcf39b9`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970a9c4b96fe43a59e8d6a22ee80e126cc78a763ae635a80dc9829801c152dd6`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab67f1b70a5388d5e9a34c0920854bcdfd3dfa7f2d9a2d2523f971755dad42`  
		Last Modified: Wed, 17 Jan 2024 07:47:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85acac7286096ee325dc43e633e96f6034f6fb3251f948ae1ffab896c474960`  
		Last Modified: Wed, 17 Jan 2024 07:47:38 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:599f5987c233ee7ccb129cc9e3d131e8419a506d99309b169d7d99e8619510bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613241916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba4b7f923dbb6ea7ce06e12639aa0d1453ae0a44e65b2bd8ee5366fe85852a`
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
# Wed, 17 Jan 2024 08:06:02 GMT
ARG ODOO_RELEASE=20240115
# Wed, 17 Jan 2024 08:06:03 GMT
ARG ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
# Wed, 17 Jan 2024 08:09:42 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 17 Jan 2024 08:10:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 17 Jan 2024 08:10:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 17 Jan 2024 08:10:05 GMT
# ARGS: ODOO_RELEASE=20240115 ODOO_SHA=9ef9520aee0080138de7abc67497648496619e43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 17 Jan 2024 08:10:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 17 Jan 2024 08:10:09 GMT
EXPOSE 8069 8071 8072
# Wed, 17 Jan 2024 08:10:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 17 Jan 2024 08:10:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 17 Jan 2024 08:10:12 GMT
USER odoo
# Wed, 17 Jan 2024 08:10:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Jan 2024 08:10:14 GMT
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
	-	`sha256:49fe56ab53c64fbdf9020abe3e89235aa40ed426c26ed0ed8165f08ff03400f9`  
		Last Modified: Wed, 17 Jan 2024 08:11:21 GMT  
		Size: 331.0 MB (331032028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60795f77f852574e13f4810508b00822403d952c6eb71aaa35dc1d7dbeda87ab`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09571254666376b6590d9a901532820a2d9a778e069216a1d55522178e2387a`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a408b5878f9af846a86a508843791fa9a33902a2fbbe7f8b8c1402fd3b8e98`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e2fc9c7139428c40f7d6ae7c4253fc7b268be29493c4735f868667201ed64`  
		Last Modified: Wed, 17 Jan 2024 08:10:35 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
