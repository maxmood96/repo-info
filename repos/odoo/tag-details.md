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
$ docker pull odoo@sha256:17ba5e620bb98e844ac8e2b1c70291f836b5de53e8b6b7db05bdbac7c7d30b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:2d5b9c907d1ab945bacca02e68cddad2b5e3791bca48f9b8ebc213ebf99e983f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564216244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500c04ca7cbe469f3e952921bdc1fe4f200db30ec5ee9f0652ef1ad2dca3a493`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:41:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:41:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:41:41 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:41:41 GMT
ENV ODOO_VERSION=15.0
# Mon, 13 May 2024 18:32:30 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:32:30 GMT
ARG ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
# Mon, 13 May 2024 18:33:45 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:33:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:33:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:33:49 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:33:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:33:50 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:33:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:33:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:33:50 GMT
USER odoo
# Mon, 13 May 2024 18:33:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:33:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844298f77b5290c77d07c814122b04a5a0c27837cb2bdc442a97a023172f418`  
		Last Modified: Wed, 24 Apr 2024 13:44:26 GMT  
		Size: 220.3 MB (220294160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8352c49f618af1258a6a53a2b11a11831bdec468a8a9cfb443fe2064119b09`  
		Last Modified: Wed, 24 Apr 2024 13:44:02 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637b99e2b29aaa41f154e2a407ca74a4895714a3e8bcfd19aebecead0a2f61cb`  
		Last Modified: Wed, 24 Apr 2024 13:44:01 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5258504c445e70a1026ba5612d6e08a0442b6089c2f23cd660d03336f211bf`  
		Last Modified: Mon, 13 May 2024 18:36:11 GMT  
		Size: 309.4 MB (309400101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38ed03a5f450b6e7df843c0bacb42f92a4b3813eb73d9332057933008cbd6fb`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2708f21743e168e6df3ac54dc8c34ab065560728c53e42ee49d583cf04e157`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4337e3155a6fedf0e08bcb8b939fc3b547a0fbe183ae2ee066a6e1245ee43d`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c5af9c2425b7c19906dc98f1e9d484e35cc4623d4819e1a7e6e5527bc5517`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:17ba5e620bb98e844ac8e2b1c70291f836b5de53e8b6b7db05bdbac7c7d30b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:2d5b9c907d1ab945bacca02e68cddad2b5e3791bca48f9b8ebc213ebf99e983f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564216244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500c04ca7cbe469f3e952921bdc1fe4f200db30ec5ee9f0652ef1ad2dca3a493`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:41:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:41:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:41:41 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:41:41 GMT
ENV ODOO_VERSION=15.0
# Mon, 13 May 2024 18:32:30 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:32:30 GMT
ARG ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
# Mon, 13 May 2024 18:33:45 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:33:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:33:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:33:49 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:33:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:33:50 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:33:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:33:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:33:50 GMT
USER odoo
# Mon, 13 May 2024 18:33:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:33:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844298f77b5290c77d07c814122b04a5a0c27837cb2bdc442a97a023172f418`  
		Last Modified: Wed, 24 Apr 2024 13:44:26 GMT  
		Size: 220.3 MB (220294160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8352c49f618af1258a6a53a2b11a11831bdec468a8a9cfb443fe2064119b09`  
		Last Modified: Wed, 24 Apr 2024 13:44:02 GMT  
		Size: 2.6 MB (2626832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637b99e2b29aaa41f154e2a407ca74a4895714a3e8bcfd19aebecead0a2f61cb`  
		Last Modified: Wed, 24 Apr 2024 13:44:01 GMT  
		Size: 458.4 KB (458430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5258504c445e70a1026ba5612d6e08a0442b6089c2f23cd660d03336f211bf`  
		Last Modified: Mon, 13 May 2024 18:36:11 GMT  
		Size: 309.4 MB (309400101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38ed03a5f450b6e7df843c0bacb42f92a4b3813eb73d9332057933008cbd6fb`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2708f21743e168e6df3ac54dc8c34ab065560728c53e42ee49d583cf04e157`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4337e3155a6fedf0e08bcb8b939fc3b547a0fbe183ae2ee066a6e1245ee43d`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2c5af9c2425b7c19906dc98f1e9d484e35cc4623d4819e1a7e6e5527bc5517`  
		Last Modified: Mon, 13 May 2024 18:35:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:688b47e570f93d5f82f73aa4eb70abbc775577276e35407d9c8fe8fe9a4394f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:9d9e4684c801ec9e3eef74f507e0f6e2b6a5bf7347733d9a3bfa1ae024bf98d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.4 MB (583414098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80342c50f511ab1c47f2f1e60ed6a2e713de8c30ca0f05e0d823ea6f3449516c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:37:44 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 13:38:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:39:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:39:03 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:39:04 GMT
ENV ODOO_VERSION=16.0
# Mon, 13 May 2024 18:30:51 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:30:51 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Mon, 13 May 2024 18:32:16 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:32:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:32:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:32:21 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:32:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:32:21 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:32:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:32:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:32:21 GMT
USER odoo
# Mon, 13 May 2024 18:32:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:32:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b10b512b443a629773a6151d15753e241d9c89e695fc8769376c36816475426`  
		Last Modified: Wed, 24 Apr 2024 13:43:38 GMT  
		Size: 219.6 MB (219605091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f954fd7c585d0f341393980922d2e5b0e829b07f8a927c1ef49cb5b9a1e28`  
		Last Modified: Wed, 24 Apr 2024 13:43:13 GMT  
		Size: 2.6 MB (2631177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255380b0477fe6a4565c69b731391d7194a57d85be15c9c95945f92214994e2f`  
		Last Modified: Wed, 24 Apr 2024 13:43:12 GMT  
		Size: 458.4 KB (458387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156c5cd1f3b641877a96a5596fbf8d699553fea025b1905adb937708b286f9b2`  
		Last Modified: Mon, 13 May 2024 18:35:29 GMT  
		Size: 329.3 MB (329282712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275f2158339b82e0b32e5094b3065a21d2abd46be6845dcead57bd797c18d433`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee60baa372a2c4d0cf6587f700134d8499f30c0a3761da125de564efbb8c927c`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94d8a2dd62aff905f61edded72a7d35e4afb1b4e3c39dfb88707d6e0cd49e82`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84126fff3d5f20437e755d9d21bc8f1aea120f5ecf9f4c0c4eb96c039615745b`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:72187508e5b1a09542c9db930ade8bc1919b38cdfb587d966d135c6481fefe94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (579035930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72075d8960e219f13b260e5fe252c5f90b0e6f8371212d6bcbadf64e2e12ac08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Mon, 13 May 2024 18:43:47 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:43:47 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Mon, 13 May 2024 18:45:02 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:45:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:45:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:45:11 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:45:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:45:11 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:45:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:45:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:45:11 GMT
USER odoo
# Mon, 13 May 2024 18:45:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:45:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f9e7523cbfc1337318620934a176f24b59f0d0d2503bd102039760c64ad0f`  
		Last Modified: Mon, 13 May 2024 18:46:52 GMT  
		Size: 328.9 MB (328948298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7982744c4d9e57ab71037208a364fe330a63c0c7c7781e63260ce5e418add2f`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d526a4b9317e4040ba6258c5599df23af828024139748bba23563bb1369c8c`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d36ed45083ba37baa54c70cd4c2dee536736d1c5751e585d3c1809cc37463f2`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf4f0df080744f7fa9088e7e661c79c8eba83bc59b30c51db08ed2c3eaf7eb`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:ded0349af4897de56d9f2550b95a9b08663cdbb18b1fc17581df4db3232207dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (597979617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907e3f7ac74c74fb3d57def73406e4e832bc8a81f316ab3f656c4f5c83af70ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 13 May 2024 18:22:59 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:23:00 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Mon, 13 May 2024 18:25:00 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:25:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:25:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:25:17 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:25:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:25:18 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:25:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:25:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:25:19 GMT
USER odoo
# Mon, 13 May 2024 18:25:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:25:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0fc460d14972ff904a487783d097784dbfc4ce470613a7a06a549f8dff9db4`  
		Last Modified: Mon, 13 May 2024 18:27:22 GMT  
		Size: 330.7 MB (330727900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7956bc30236398733df42f18a5eeb8ce70bb9f119e68c888128a4ce01335ee4`  
		Last Modified: Mon, 13 May 2024 18:26:39 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ded220f76d6552755e3d1144366cc43dede6812780132a72695dfe447dda47`  
		Last Modified: Mon, 13 May 2024 18:26:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00a469d0f625743adf455c024b0a5f52dcd7205db7a03984f8df485a6aa08f2`  
		Last Modified: Mon, 13 May 2024 18:26:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0266b4348eec2a2072e3444c1fea28607dedb661d25e987c0ae811833bd533c6`  
		Last Modified: Mon, 13 May 2024 18:26:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:688b47e570f93d5f82f73aa4eb70abbc775577276e35407d9c8fe8fe9a4394f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:9d9e4684c801ec9e3eef74f507e0f6e2b6a5bf7347733d9a3bfa1ae024bf98d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.4 MB (583414098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80342c50f511ab1c47f2f1e60ed6a2e713de8c30ca0f05e0d823ea6f3449516c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 13:37:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 13:37:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 13:37:44 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 13:37:44 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 13:38:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 13:39:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:39:03 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 13:39:04 GMT
ENV ODOO_VERSION=16.0
# Mon, 13 May 2024 18:30:51 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:30:51 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Mon, 13 May 2024 18:32:16 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:32:20 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:32:20 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:32:21 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:32:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:32:21 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:32:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:32:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:32:21 GMT
USER odoo
# Mon, 13 May 2024 18:32:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:32:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b10b512b443a629773a6151d15753e241d9c89e695fc8769376c36816475426`  
		Last Modified: Wed, 24 Apr 2024 13:43:38 GMT  
		Size: 219.6 MB (219605091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851f954fd7c585d0f341393980922d2e5b0e829b07f8a927c1ef49cb5b9a1e28`  
		Last Modified: Wed, 24 Apr 2024 13:43:13 GMT  
		Size: 2.6 MB (2631177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255380b0477fe6a4565c69b731391d7194a57d85be15c9c95945f92214994e2f`  
		Last Modified: Wed, 24 Apr 2024 13:43:12 GMT  
		Size: 458.4 KB (458387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156c5cd1f3b641877a96a5596fbf8d699553fea025b1905adb937708b286f9b2`  
		Last Modified: Mon, 13 May 2024 18:35:29 GMT  
		Size: 329.3 MB (329282712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275f2158339b82e0b32e5094b3065a21d2abd46be6845dcead57bd797c18d433`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee60baa372a2c4d0cf6587f700134d8499f30c0a3761da125de564efbb8c927c`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94d8a2dd62aff905f61edded72a7d35e4afb1b4e3c39dfb88707d6e0cd49e82`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84126fff3d5f20437e755d9d21bc8f1aea120f5ecf9f4c0c4eb96c039615745b`  
		Last Modified: Mon, 13 May 2024 18:34:50 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:72187508e5b1a09542c9db930ade8bc1919b38cdfb587d966d135c6481fefe94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (579035930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72075d8960e219f13b260e5fe252c5f90b0e6f8371212d6bcbadf64e2e12ac08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:43:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 04:43:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 04:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:43:40 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 04:44:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 04:44:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:44:58 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 04:44:58 GMT
ENV ODOO_VERSION=16.0
# Mon, 13 May 2024 18:43:47 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:43:47 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Mon, 13 May 2024 18:45:02 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:45:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:45:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:45:11 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:45:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:45:11 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:45:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:45:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:45:11 GMT
USER odoo
# Mon, 13 May 2024 18:45:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:45:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bed6bdb2849b11e9cb12a1fffe19e52e97d28c8be064ec768cd96bfd5f33b6`  
		Last Modified: Wed, 24 Apr 2024 04:47:00 GMT  
		Size: 216.9 MB (216903771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb00fee4acf6d59301bd01ab0c80c6fc218007abfcf891f80fa91abda10deac1`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 2.6 MB (2635659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ece9562809bea7931d2d8921750c225cbc4b836e599d50550924f82a1bc6a20`  
		Last Modified: Wed, 24 Apr 2024 04:46:43 GMT  
		Size: 458.4 KB (458402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4f9e7523cbfc1337318620934a176f24b59f0d0d2503bd102039760c64ad0f`  
		Last Modified: Mon, 13 May 2024 18:46:52 GMT  
		Size: 328.9 MB (328948298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7982744c4d9e57ab71037208a364fe330a63c0c7c7781e63260ce5e418add2f`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d526a4b9317e4040ba6258c5599df23af828024139748bba23563bb1369c8c`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d36ed45083ba37baa54c70cd4c2dee536736d1c5751e585d3c1809cc37463f2`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cf4f0df080744f7fa9088e7e661c79c8eba83bc59b30c51db08ed2c3eaf7eb`  
		Last Modified: Mon, 13 May 2024 18:46:22 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ded0349af4897de56d9f2550b95a9b08663cdbb18b1fc17581df4db3232207dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (597979617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907e3f7ac74c74fb3d57def73406e4e832bc8a81f316ab3f656c4f5c83af70ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:50:46 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Apr 2024 05:50:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Apr 2024 05:50:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 05:50:47 GMT
ARG TARGETARCH
# Wed, 24 Apr 2024 05:54:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 24 Apr 2024 05:54:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:54:43 GMT
RUN npm install -g rtlcss
# Wed, 24 Apr 2024 05:54:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 13 May 2024 18:22:59 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:23:00 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Mon, 13 May 2024 18:25:00 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:25:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:25:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:25:17 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:25:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:25:18 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:25:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:25:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:25:19 GMT
USER odoo
# Mon, 13 May 2024 18:25:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:25:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e008b860f0356a4dc545708d47ab68b40e8cdfc14d93da99f233f315417db`  
		Last Modified: Wed, 24 Apr 2024 05:58:21 GMT  
		Size: 228.6 MB (228602532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805f8f76f41f4c5d5883335f4378b2550b6e8b3428f5009beaf0520abc9bb7de`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 2.9 MB (2876532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd326b52bec9f624e9d8dcb6e8d7ceab438222aa8a46954e8263bb896fdb4d7`  
		Last Modified: Wed, 24 Apr 2024 05:57:52 GMT  
		Size: 458.5 KB (458464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0fc460d14972ff904a487783d097784dbfc4ce470613a7a06a549f8dff9db4`  
		Last Modified: Mon, 13 May 2024 18:27:22 GMT  
		Size: 330.7 MB (330727900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7956bc30236398733df42f18a5eeb8ce70bb9f119e68c888128a4ce01335ee4`  
		Last Modified: Mon, 13 May 2024 18:26:39 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ded220f76d6552755e3d1144366cc43dede6812780132a72695dfe447dda47`  
		Last Modified: Mon, 13 May 2024 18:26:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00a469d0f625743adf455c024b0a5f52dcd7205db7a03984f8df485a6aa08f2`  
		Last Modified: Mon, 13 May 2024 18:26:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0266b4348eec2a2072e3444c1fea28607dedb661d25e987c0ae811833bd533c6`  
		Last Modified: Mon, 13 May 2024 18:26:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:bab5b91bba6efa9c3a8d7344869f23017408c9f691dd11640082ddcba8efaeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:6e5ba0d61b58fc7b96ade28cc5629b5f692856ed384a9108d15c8206e487deb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602978917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa2814a4c9a50904788e5d5f506b01d8a60522430409949170317fa91aa3f1e`
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
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:30:35 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:30:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:30:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:30:39 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:30:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:30:39 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:30:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:30:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:30:40 GMT
USER odoo
# Mon, 13 May 2024 18:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:30:40 GMT
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
	-	`sha256:65861a35542bca13181ce6ae828b535c337ec8897b9c5a9b8240c840d3ec1434`  
		Last Modified: Mon, 13 May 2024 18:34:39 GMT  
		Size: 335.8 MB (335824189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3c424a2c0119aaae6dc6c0c7c36f6015fd141576e8681dd796fb5ac9dda24`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc686ff2f80940cdf1f1b51d3a964529d48714241428611384d8e419dcfdfd`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d90839dd1bbc5aac92b108f886a9913e8894a7e727e616896200cb8d66b59b`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b54b8005a8d54a591ee56f9c4191b6d76968ef966bcef57950a803eb8753765`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3c0ca70dd35b3b9cef81b809cd61330031f5d8d83267890045d4cba7633d3b66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597933367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebd7e8f7746af6b8c3dcad0d5ded350a10d66dd39d85d9cbc29991a9bdef3a`
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
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:43:29 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:43:32 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:43:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:43:32 GMT
USER odoo
# Mon, 13 May 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:43:32 GMT
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
	-	`sha256:7d0ee49d1eabf028301ea2a11a1775c4af9248d3b185413b84b12748d4036ce3`  
		Last Modified: Mon, 13 May 2024 18:46:11 GMT  
		Size: 335.4 MB (335416400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bac3b6f3c326d9f185b80d4cb49521f4802280e7a9467caea5707140f5ab42`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ed1b1c23e00865a567d859c903725f72f925814e87b4b4478d0e9f219f609`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03076fe297bd9ca2328b3894bf5aa4b030baba681f8ea5b3020ec6813b590b76`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e5be11ac4fe759e0b1541348ed40421f5cd8e4682b691ad72fa7f9fbd0027`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:e55c6407a34bb127e07f326fc982540c2739056ffac68d5973869a5bf6529214
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619729556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331cab68dcb4e956dec4edc771ec19218d5fb00ea34e159303513a85eb38f468`
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
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:22:25 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:22:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:22:40 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:22:41 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:22:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:22:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:22:42 GMT
USER odoo
# Mon, 13 May 2024 18:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:22:43 GMT
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
	-	`sha256:ab1a470130561a48fae6876b48e9254b884e31dc27190aba1481b59737628f46`  
		Last Modified: Mon, 13 May 2024 18:26:26 GMT  
		Size: 337.6 MB (337573295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda04e11bc01f4929cf74507168fdd8ba877aeac1b0c6ed8a8f294b5d9fed06`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086883b3f68b91457cf2cc2aef14fc4ead0c6f3786a176c8242d78917148c9c9`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5fba5cd3adda80bc4eec30943db60c7205635d565322a472cbb4a7d9def70f`  
		Last Modified: Mon, 13 May 2024 18:25:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975520576c156a7b790fa9a782efc2c4a786168fb235f2213f59a93cb8393d0f`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:bab5b91bba6efa9c3a8d7344869f23017408c9f691dd11640082ddcba8efaeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:6e5ba0d61b58fc7b96ade28cc5629b5f692856ed384a9108d15c8206e487deb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602978917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa2814a4c9a50904788e5d5f506b01d8a60522430409949170317fa91aa3f1e`
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
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:30:35 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:30:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:30:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:30:39 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:30:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:30:39 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:30:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:30:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:30:40 GMT
USER odoo
# Mon, 13 May 2024 18:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:30:40 GMT
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
	-	`sha256:65861a35542bca13181ce6ae828b535c337ec8897b9c5a9b8240c840d3ec1434`  
		Last Modified: Mon, 13 May 2024 18:34:39 GMT  
		Size: 335.8 MB (335824189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3c424a2c0119aaae6dc6c0c7c36f6015fd141576e8681dd796fb5ac9dda24`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc686ff2f80940cdf1f1b51d3a964529d48714241428611384d8e419dcfdfd`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d90839dd1bbc5aac92b108f886a9913e8894a7e727e616896200cb8d66b59b`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b54b8005a8d54a591ee56f9c4191b6d76968ef966bcef57950a803eb8753765`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3c0ca70dd35b3b9cef81b809cd61330031f5d8d83267890045d4cba7633d3b66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597933367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebd7e8f7746af6b8c3dcad0d5ded350a10d66dd39d85d9cbc29991a9bdef3a`
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
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:43:29 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:43:32 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:43:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:43:32 GMT
USER odoo
# Mon, 13 May 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:43:32 GMT
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
	-	`sha256:7d0ee49d1eabf028301ea2a11a1775c4af9248d3b185413b84b12748d4036ce3`  
		Last Modified: Mon, 13 May 2024 18:46:11 GMT  
		Size: 335.4 MB (335416400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bac3b6f3c326d9f185b80d4cb49521f4802280e7a9467caea5707140f5ab42`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ed1b1c23e00865a567d859c903725f72f925814e87b4b4478d0e9f219f609`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03076fe297bd9ca2328b3894bf5aa4b030baba681f8ea5b3020ec6813b590b76`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e5be11ac4fe759e0b1541348ed40421f5cd8e4682b691ad72fa7f9fbd0027`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e55c6407a34bb127e07f326fc982540c2739056ffac68d5973869a5bf6529214
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619729556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331cab68dcb4e956dec4edc771ec19218d5fb00ea34e159303513a85eb38f468`
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
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:22:25 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:22:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:22:40 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:22:41 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:22:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:22:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:22:42 GMT
USER odoo
# Mon, 13 May 2024 18:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:22:43 GMT
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
	-	`sha256:ab1a470130561a48fae6876b48e9254b884e31dc27190aba1481b59737628f46`  
		Last Modified: Mon, 13 May 2024 18:26:26 GMT  
		Size: 337.6 MB (337573295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda04e11bc01f4929cf74507168fdd8ba877aeac1b0c6ed8a8f294b5d9fed06`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086883b3f68b91457cf2cc2aef14fc4ead0c6f3786a176c8242d78917148c9c9`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5fba5cd3adda80bc4eec30943db60c7205635d565322a472cbb4a7d9def70f`  
		Last Modified: Mon, 13 May 2024 18:25:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975520576c156a7b790fa9a782efc2c4a786168fb235f2213f59a93cb8393d0f`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:bab5b91bba6efa9c3a8d7344869f23017408c9f691dd11640082ddcba8efaeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:6e5ba0d61b58fc7b96ade28cc5629b5f692856ed384a9108d15c8206e487deb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602978917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa2814a4c9a50904788e5d5f506b01d8a60522430409949170317fa91aa3f1e`
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
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:30:35 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:30:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:30:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:30:39 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:30:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:30:39 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:30:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:30:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:30:40 GMT
USER odoo
# Mon, 13 May 2024 18:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:30:40 GMT
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
	-	`sha256:65861a35542bca13181ce6ae828b535c337ec8897b9c5a9b8240c840d3ec1434`  
		Last Modified: Mon, 13 May 2024 18:34:39 GMT  
		Size: 335.8 MB (335824189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3c424a2c0119aaae6dc6c0c7c36f6015fd141576e8681dd796fb5ac9dda24`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc686ff2f80940cdf1f1b51d3a964529d48714241428611384d8e419dcfdfd`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d90839dd1bbc5aac92b108f886a9913e8894a7e727e616896200cb8d66b59b`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b54b8005a8d54a591ee56f9c4191b6d76968ef966bcef57950a803eb8753765`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3c0ca70dd35b3b9cef81b809cd61330031f5d8d83267890045d4cba7633d3b66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597933367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebd7e8f7746af6b8c3dcad0d5ded350a10d66dd39d85d9cbc29991a9bdef3a`
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
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:43:29 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:43:32 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:43:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:43:32 GMT
USER odoo
# Mon, 13 May 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:43:32 GMT
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
	-	`sha256:7d0ee49d1eabf028301ea2a11a1775c4af9248d3b185413b84b12748d4036ce3`  
		Last Modified: Mon, 13 May 2024 18:46:11 GMT  
		Size: 335.4 MB (335416400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bac3b6f3c326d9f185b80d4cb49521f4802280e7a9467caea5707140f5ab42`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ed1b1c23e00865a567d859c903725f72f925814e87b4b4478d0e9f219f609`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03076fe297bd9ca2328b3894bf5aa4b030baba681f8ea5b3020ec6813b590b76`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e5be11ac4fe759e0b1541348ed40421f5cd8e4682b691ad72fa7f9fbd0027`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:e55c6407a34bb127e07f326fc982540c2739056ffac68d5973869a5bf6529214
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619729556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331cab68dcb4e956dec4edc771ec19218d5fb00ea34e159303513a85eb38f468`
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
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:22:25 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:22:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:22:40 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:22:41 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:22:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:22:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:22:42 GMT
USER odoo
# Mon, 13 May 2024 18:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:22:43 GMT
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
	-	`sha256:ab1a470130561a48fae6876b48e9254b884e31dc27190aba1481b59737628f46`  
		Last Modified: Mon, 13 May 2024 18:26:26 GMT  
		Size: 337.6 MB (337573295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda04e11bc01f4929cf74507168fdd8ba877aeac1b0c6ed8a8f294b5d9fed06`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086883b3f68b91457cf2cc2aef14fc4ead0c6f3786a176c8242d78917148c9c9`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5fba5cd3adda80bc4eec30943db60c7205635d565322a472cbb4a7d9def70f`  
		Last Modified: Mon, 13 May 2024 18:25:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975520576c156a7b790fa9a782efc2c4a786168fb235f2213f59a93cb8393d0f`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
