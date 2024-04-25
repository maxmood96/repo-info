## `odoo:latest`

```console
$ docker pull odoo@sha256:253f0399cadbc6afa6db28ce061922915e23b0b3aad05d926cd53182e46cde5a
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
$ docker pull odoo@sha256:5f66d3efdcbe28ab83f36abfb4789a661bac3258a462e9fc5fa65ba1d9ca4ddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.9 MB (596908645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c77fe27ff032764471d4dca973b3d868e5d00a17862ac892c68b7843dc8e6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:25:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:25:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:25:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:25:32 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:31:21 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:31:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:31:38 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:31:38 GMT
ENV ODOO_VERSION=17.0
# Thu, 25 Apr 2024 22:31:38 GMT
ARG ODOO_RELEASE=20240416
# Thu, 25 Apr 2024 22:31:38 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Thu, 25 Apr 2024 22:33:59 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 25 Apr 2024 22:34:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 25 Apr 2024 22:34:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 25 Apr 2024 22:34:07 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 25 Apr 2024 22:34:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 25 Apr 2024 22:34:08 GMT
EXPOSE 8069 8071 8072
# Thu, 25 Apr 2024 22:34:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 25 Apr 2024 22:34:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 25 Apr 2024 22:34:08 GMT
USER odoo
# Thu, 25 Apr 2024 22:34:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:34:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187da141906722001c5c359161c4fe85507227149b57a2fbc0d342d6432cc5ea`  
		Last Modified: Thu, 25 Apr 2024 22:34:42 GMT  
		Size: 231.1 MB (231128133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569f8a9def1cf1035c2c0e5425ec4126c5b091a2450610fc976052c36d763d76`  
		Last Modified: Thu, 25 Apr 2024 22:34:23 GMT  
		Size: 2.5 MB (2523264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497241b34f7a0544bba89f995df2b40714055c5de05a0933ce8978b7b12923b2`  
		Last Modified: Thu, 25 Apr 2024 22:34:22 GMT  
		Size: 459.4 KB (459361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e1af510a91f3b47f16cd391ea9db0c10c85dd785641dccc2eb9db3f6c0b425`  
		Last Modified: Thu, 25 Apr 2024 22:34:51 GMT  
		Size: 334.4 MB (334394420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a7f770b97f2a09089135c34094380aae23bfd70c74c53b349ef3af4a937eed`  
		Last Modified: Thu, 25 Apr 2024 22:34:20 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560c3d4cef932c6e16bfece90183bfe8241bf6debf2e8bbced47fcd0a0ff6aae`  
		Last Modified: Thu, 25 Apr 2024 22:34:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd926b72d43fa1d7a2976b1d72615542ac96030961e6c8cc74063d1a8e90712d`  
		Last Modified: Thu, 25 Apr 2024 22:34:20 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb82d37cb1f308b3781b457d9d2eb898bd13ff1d1f261d89b6d57c515e4e9c2d`  
		Last Modified: Thu, 25 Apr 2024 22:34:20 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:d3920c02f1c561521fd34b88a954da2a2fd963477e6afa0d23723fa9fcbad4a0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618687575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04951a38706438f9938e62e9ee3640c4f0e3759590633e38e9ee3c1c2065d36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:09:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 25 Apr 2024 22:09:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 25 Apr 2024 22:09:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Apr 2024 22:09:04 GMT
ARG TARGETARCH
# Thu, 25 Apr 2024 22:19:56 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 25 Apr 2024 22:20:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:20:28 GMT
RUN npm install -g rtlcss
# Thu, 25 Apr 2024 22:20:30 GMT
ENV ODOO_VERSION=17.0
# Thu, 25 Apr 2024 22:20:30 GMT
ARG ODOO_RELEASE=20240416
# Thu, 25 Apr 2024 22:20:31 GMT
ARG ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
# Thu, 25 Apr 2024 22:24:17 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 25 Apr 2024 22:24:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 25 Apr 2024 22:24:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 25 Apr 2024 22:24:39 GMT
# ARGS: ODOO_RELEASE=20240416 ODOO_SHA=994057dc6db742f62b0666b8edf5cd1623df78d0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 25 Apr 2024 22:24:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 25 Apr 2024 22:24:40 GMT
EXPOSE 8069 8071 8072
# Thu, 25 Apr 2024 22:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 25 Apr 2024 22:24:41 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 25 Apr 2024 22:24:41 GMT
USER odoo
# Thu, 25 Apr 2024 22:24:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:24:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb89ed4f3fd92c20d209ee65962139d76e94701ca7dd1ecb0319b3fbfc79a2ea`  
		Last Modified: Thu, 25 Apr 2024 22:25:42 GMT  
		Size: 243.3 MB (243300752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0047e358abc545022c8cc2538c8b6f5acc0dc41dc0d7a2089da028723faf8c8`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 2.8 MB (2806239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab156d194b91801d0e0f992582594aabab33ed2f800afcee7c191f844958720`  
		Last Modified: Thu, 25 Apr 2024 22:25:10 GMT  
		Size: 459.4 KB (459389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ded6ecf8ef6a0c16c84ce307d1d4cbdfa1e5a9a52adc542bc9c9883dd25486`  
		Last Modified: Thu, 25 Apr 2024 22:25:53 GMT  
		Size: 336.5 MB (336530415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc49e284a3d7da9d44fb71f3979575f30ade9cc92a141d1a2e353cc4d46aeaad`  
		Last Modified: Thu, 25 Apr 2024 22:25:07 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd97f71ea82a1c2f47e09bed136376e2a08285b937c3bd2fd3e36670dc533ec`  
		Last Modified: Thu, 25 Apr 2024 22:25:07 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84d7de73f6f29c4551a59b9939c5011928970b62371d0c216cd104e1c075ea6`  
		Last Modified: Thu, 25 Apr 2024 22:25:07 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adeb5b1ad28a3d0c18e537c42ebbd0981f8dd3538e40486ac6cb5d89f53a3dd9`  
		Last Modified: Thu, 25 Apr 2024 22:25:07 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
