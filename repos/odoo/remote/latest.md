## `odoo:latest`

```console
$ docker pull odoo@sha256:999836643734365e0b442d11c064b0da98ab41351d47187d5fa6cc6bd0979e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:c097985f4243b7d057715118b98eae309d1c963ac4ba496065094a4970248d67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.9 MB (600880596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a117dd3eff1275e66067c47ce92c119f6ec01a3bdbbaac307dfa31c2e4eaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:58:02 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 18:00:03 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 18:00:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 18:00:08 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 18:00:08 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 18:00:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 18:00:08 GMT
USER odoo
# Tue, 12 Mar 2024 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e690b7354eb75e119ec42b72ccc5128ba6233158c10fb963500f5056304efacf`  
		Last Modified: Tue, 12 Mar 2024 18:03:59 GMT  
		Size: 333.7 MB (333710535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529d45c0119d1973d1b79b9c578129f51e2262b554a502d4f1c62bbca9447a7`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a51b5089356d97fb773c804884a9a212bd14d917704ac07a03a689859ad77c`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a71476cf6d9ad48c07e4132d9d404b97c9ae3d970f08e64c16829476d9cfbee`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c83c4741a0aaa79b05350e564691153b2f2e5a0248b77651e93cc0a7871f77`  
		Last Modified: Tue, 12 Mar 2024 18:03:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ea848e7067d43101ca6d5509a94a787962c060ab77ee2dbff2f1a0e6e3b2ec81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595845243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34df8c4e9dcc31ef75afe067b00eda22cc9cd31392853781e6733865322e88be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_RELEASE=20240312
# Tue, 12 Mar 2024 17:16:34 GMT
ARG ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
# Tue, 12 Mar 2024 17:18:55 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 17:19:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 17:19:04 GMT
# ARGS: ODOO_RELEASE=20240312 ODOO_SHA=467f514f90cf8cdc36dddd84129adefc4624be36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 17:19:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 17:19:04 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 17:19:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 17:19:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 17:19:05 GMT
USER odoo
# Tue, 12 Mar 2024 17:19:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:19:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3be5e5d50a421dd890930bfb95b1fe77d1ff92e350cd6c162187b6d675851b`  
		Last Modified: Tue, 12 Mar 2024 17:21:31 GMT  
		Size: 333.3 MB (333331582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695c01490528a61fffeb7dfc44d25d3d2ae760bae68280b595ec4eab88fadb8d`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e22e664cf1ded17a59155829cca757ea678212c7ad5e2d256ea97feea889ab4`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772bfac9ac02fd36bf0f3bcd1d231cc4f8e82f42a4d01fa44ffe59f9e88c8a18`  
		Last Modified: Tue, 12 Mar 2024 17:20:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c93b6c4da4abc860c51a63c7e4153def0e9d396218b3fb5a7b3d9d72b1306b`  
		Last Modified: Tue, 12 Mar 2024 17:20:57 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
