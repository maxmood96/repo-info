## `odoo:latest`

```console
$ docker pull odoo@sha256:c009d5e389fefaebd8e278424b778b71b14007c4de9683fed74b331fd74c0bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f247de51bf0bd27033eddb3aa76158d2c645d2cf61c864389cbc8436e97dc946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601198776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45d7945bd144b41261f9fda39f2b6b1225374f44bf20a2aba766ce058e6a73`
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
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:15:27 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:15:33 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:15:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:15:33 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:15:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:15:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:15:33 GMT
USER odoo
# Mon, 25 Mar 2024 20:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:15:34 GMT
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
	-	`sha256:f8af06cc4793bb719ec879b5341adaf15a265ab59f7b1dcfdaf0b765ad688351`  
		Last Modified: Mon, 25 Mar 2024 20:19:33 GMT  
		Size: 334.0 MB (334028714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ea0e32bd1422ccc747f0bca5a5ede791c8bb751e49db07752f0c733a2384f`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8085f62d18ad15f5745dc2c4315ec3c6a05a2acdde8165c37105e65c1172b38d`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068834d6e97533438f89c2da813f4874ac424066326774976b4d9c9995a0dc15`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a244eff3b4db5e4f40e8521c00d6593a1a7f6a39fd0c788298773ec4cccdbc9`  
		Last Modified: Mon, 25 Mar 2024 20:18:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3436f1f52ed0d937f9f9fd642fd19faf245958421dd33df225e80899e0fd3078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596700020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63329b547b9d753138a0812b754b7818a9ae406e7f818bd52042da63e6697c6d`
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
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:44:48 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:44:50 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:44:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:44:50 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:44:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:44:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:44:50 GMT
USER odoo
# Fri, 05 Apr 2024 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:44:50 GMT
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
	-	`sha256:07a8dcbe3d3be7a497a7500f37739e8aeb86ea2c42ff1bae253313b0c6004e2a`  
		Last Modified: Fri, 05 Apr 2024 19:47:21 GMT  
		Size: 334.2 MB (334186364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5495fd7423c2f5479b06dcab10def2ad75d471539b0d5e233c46f6e4ea6c6377`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff6cb284fc6a1f38c5633be835922e13409bf310526c76f7c80a9ba5e9f0f4`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f9b73f88f99e62897eb57e325da70b4ca3d1c6d743c4fb3df902bde36d821b`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13bb0a340f0f26a2a350b300498403219eef0709d44dc502726f5dd24491ac`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a6d65d05878e547e0b0ddb8be3b102112fdd9d08f061f8021538f8db8060b9fd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d337b5fbf0262bba7d88a6d512c3d000da22d70d2cb31e7444ccd0255504b13c`
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
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:28:00 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:28:13 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:28:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:28:14 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:28:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:28:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:28:16 GMT
USER odoo
# Fri, 05 Apr 2024 19:28:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:28:16 GMT
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
	-	`sha256:34a1a5d3ad9ee702093094672b17fb5230874af0fb63555cd4f4799cd648c1ee`  
		Last Modified: Fri, 05 Apr 2024 19:31:41 GMT  
		Size: 336.3 MB (336310237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b762bbea18b46227a8d765144ab51fed19ce2fe29c8f26f3e51d8b0dd0429419`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f4bcfa89f66dc107e007f5c68618c44b747d3b23b08dd42e7ca34f79839a8`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ca0b4f48ffeb04d27fe364dd6fbf50385d133575f6070e03dc631fdea549ab`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379759df926f53ef1a7c24ac561da96972009ee1654efffbb14dfc70d4b78ca`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
