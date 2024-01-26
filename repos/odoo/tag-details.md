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
$ docker pull odoo@sha256:8bc1b2c15a982f2e84f94e1729352e7fd7b6c304730f84025488d14df0340696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:81ce93ac3a2d7c24f1818eaa351ead1a2180cb48ebbf7f428ff340de3d7e7240
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563316113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f317861bc9bc081660b7455b96653c837d703e4af46d5b5e689be8851921e385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:26:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:26:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:26:52 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:26:52 GMT
ENV ODOO_VERSION=15.0
# Fri, 26 Jan 2024 22:17:39 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:17:40 GMT
ARG ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
# Fri, 26 Jan 2024 22:18:50 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:18:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:18:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:18:53 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:18:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:18:53 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:18:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:18:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:18:54 GMT
USER odoo
# Fri, 26 Jan 2024 22:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:18:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a83c2ab42e477bbdeab88e23116d73788d2604ce89f63469bc9302abf2e18b`  
		Last Modified: Thu, 11 Jan 2024 04:29:38 GMT  
		Size: 220.3 MB (220297108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54740ee11b9fd73c810f20945af2e0b18c9b13581db15932f1f74f390bb71168`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 2.6 MB (2625737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fadd9b941961b874f97fbea1796d285ded2c1242c1c5cf5154539ea4ee5cd58`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 460.3 KB (460317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a42704fdc1a18f412670154927236f4e3ddb584e1a344aea5894a3492dd551`  
		Last Modified: Fri, 26 Jan 2024 22:21:22 GMT  
		Size: 308.5 MB (308512531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40071345c3e1d5f2096b4563986c0065ff5f7f406802d3208489bdf5b90dcd5c`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93094cfabc1baf79562b1af7129c2ad5ed3b1993bd79bdec85febe211593c082`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab76391d6ac559da3bd10f6ce25773a77f7f2ad1211afba864863f4fca6009`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9deb42eaa088c5d4e81556f9dd23b85a6ee71898479036819840240bfff3102`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:8bc1b2c15a982f2e84f94e1729352e7fd7b6c304730f84025488d14df0340696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:81ce93ac3a2d7c24f1818eaa351ead1a2180cb48ebbf7f428ff340de3d7e7240
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.3 MB (563316113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f317861bc9bc081660b7455b96653c837d703e4af46d5b5e689be8851921e385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:26:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:26:51 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:26:52 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:26:52 GMT
ENV ODOO_VERSION=15.0
# Fri, 26 Jan 2024 22:17:39 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:17:40 GMT
ARG ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
# Fri, 26 Jan 2024 22:18:50 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:18:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:18:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:18:53 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=20f3c98fb543325181d2722aa531be9084142b3c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:18:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:18:53 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:18:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:18:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:18:54 GMT
USER odoo
# Fri, 26 Jan 2024 22:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:18:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a83c2ab42e477bbdeab88e23116d73788d2604ce89f63469bc9302abf2e18b`  
		Last Modified: Thu, 11 Jan 2024 04:29:38 GMT  
		Size: 220.3 MB (220297108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54740ee11b9fd73c810f20945af2e0b18c9b13581db15932f1f74f390bb71168`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 2.6 MB (2625737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fadd9b941961b874f97fbea1796d285ded2c1242c1c5cf5154539ea4ee5cd58`  
		Last Modified: Thu, 11 Jan 2024 04:29:14 GMT  
		Size: 460.3 KB (460317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a42704fdc1a18f412670154927236f4e3ddb584e1a344aea5894a3492dd551`  
		Last Modified: Fri, 26 Jan 2024 22:21:22 GMT  
		Size: 308.5 MB (308512531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40071345c3e1d5f2096b4563986c0065ff5f7f406802d3208489bdf5b90dcd5c`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93094cfabc1baf79562b1af7129c2ad5ed3b1993bd79bdec85febe211593c082`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab76391d6ac559da3bd10f6ce25773a77f7f2ad1211afba864863f4fca6009`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9deb42eaa088c5d4e81556f9dd23b85a6ee71898479036819840240bfff3102`  
		Last Modified: Fri, 26 Jan 2024 22:20:49 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:94ff618a12a93a134d11f03dc82e066a3b60195eee794f29729316b9dcfafe2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:7f6185af13681be1acafe491510e48584ac51a2bbda0cd322196b02ba4da6bf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578050080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1707326ff7644b7356cd613d98f17d7e01643e805b09d270c3b633318b4ad0fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:22:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 04:23:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:24:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:24:08 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:24:08 GMT
ENV ODOO_VERSION=16.0
# Fri, 26 Jan 2024 22:16:01 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:16:01 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Fri, 26 Jan 2024 22:17:20 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:17:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:17:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:17:25 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:17:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:17:25 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:17:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:17:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:17:25 GMT
USER odoo
# Fri, 26 Jan 2024 22:17:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:17:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86654a69bafa33531b4fcae19511db74ec083ee8a32a4e5f68400b666ea91d3`  
		Last Modified: Thu, 11 Jan 2024 04:28:50 GMT  
		Size: 219.6 MB (219605557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ade87532781cb4a4f46880be8dc7fdde9c138904bb8d31a486c98f76224e59b`  
		Last Modified: Thu, 11 Jan 2024 04:28:26 GMT  
		Size: 2.6 MB (2629862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d092994f2bb47b54ec61d78cd536111b7c2aed38ff9c54d904acfa556f832abe`  
		Last Modified: Thu, 11 Jan 2024 04:28:25 GMT  
		Size: 460.4 KB (460351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b84941b26528dde691be92b29af38d3e26e0651f9b50a17ebaff4cb696a26cb`  
		Last Modified: Fri, 26 Jan 2024 22:20:40 GMT  
		Size: 323.9 MB (323933892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da77c7a47a8e49f7c5de832067af79be16e736007853f432c884e74ccf37f87`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d63cf6aad2baa274daa4adaabbbb975ef0bfe24faa509cc6a2e59365640d8b`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc620dfb39b6146d9fd8d792b5cd36f6287d12a9aec986803d35a996dad7448f`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aa31640195d081ed593ecb3ab5552c7869e28d52915786c2a201271f87f6dd`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:956c47b45d80bc3eec09e9c53e02ee27298c03fd8c185580c0d4b9510ea7d831
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.6 MB (573642590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc3e5a3bd6c5c98bf2d0a04947465088a12fe55dde0aa7bab9108c0198b7117`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:32:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 06:32:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 06:32:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 06:32:19 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 06:33:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 06:33:33 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:33:34 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 06:33:34 GMT
ENV ODOO_VERSION=16.0
# Fri, 26 Jan 2024 19:22:55 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 19:22:56 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Fri, 26 Jan 2024 19:24:15 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 19:24:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 19:24:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 19:24:24 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 19:24:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 19:24:25 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 19:24:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 19:24:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 19:24:25 GMT
USER odoo
# Fri, 26 Jan 2024 19:24:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 19:24:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843638cd2bb45ed1fac36d25687a35e96bac688f9925d94266efe7a01b02dbc2`  
		Last Modified: Thu, 11 Jan 2024 06:35:43 GMT  
		Size: 216.9 MB (216908953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ecca8e8834b331b36f9b4440b200f5387f9e128237d075371a1088530fe7b2`  
		Last Modified: Thu, 11 Jan 2024 06:35:23 GMT  
		Size: 2.6 MB (2634821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ce5b97e9a663db05af8bf4aac7112926f555fdc5b3f95caede4a11d02a935d`  
		Last Modified: Thu, 11 Jan 2024 06:35:22 GMT  
		Size: 460.3 KB (460316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7909ae8a6d7f01547acec8678ef246c45660314a77396af63f09cdde8636e0d9`  
		Last Modified: Fri, 26 Jan 2024 19:25:56 GMT  
		Size: 323.6 MB (323572029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4c835b0fa073c14203653157142ce0385b36cca702f1220b5fc917b48059bc`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6bb9aea991dbf291716a5053a76e49d48492ccc15a9d886a7dbad78afdb794`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef0a251669f5ddc2606822235bc6dfab09566727860301c28133587e79f659a`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e919aaa4c5e25444d61127b5b3ee3eddd2d6add964f5c59f68a33e97258404da`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:f20dee6297caa96b988a997c492e45ea8d5564251ecf8d9e0e1cc125408abdf9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592580111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88d43497f98547a272a4b8add381a1b3f6c6bcfcc5db7fb11e0366a3bde6051`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:56:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 03:56:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 03:56:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 03:56:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 03:59:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 03:59:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:59:44 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 03:59:45 GMT
ENV ODOO_VERSION=16.0
# Fri, 26 Jan 2024 20:48:11 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 20:48:11 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Fri, 26 Jan 2024 20:50:30 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 20:50:44 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 20:50:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 20:50:46 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 20:50:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 20:50:48 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 20:50:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 20:50:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 20:50:49 GMT
USER odoo
# Fri, 26 Jan 2024 20:50:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 20:50:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98645df03fa753cd35df386c12a15edceb4284519ed070b82144681b10101c7`  
		Last Modified: Thu, 11 Jan 2024 04:03:17 GMT  
		Size: 228.6 MB (228601149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e8f09bc42c4ab2ba211885268c12651fd157357bc388a9ace0b59c705a2d22`  
		Last Modified: Thu, 11 Jan 2024 04:02:47 GMT  
		Size: 2.9 MB (2875618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5ba7386839331811e9baf6be69016dc74bc0b395e5d441677af7b58038dff5`  
		Last Modified: Thu, 11 Jan 2024 04:02:46 GMT  
		Size: 460.4 KB (460388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585025124c501e07915a832153ce244a321221f3f705e34b4a50c67f0156a6a7`  
		Last Modified: Fri, 26 Jan 2024 20:52:55 GMT  
		Size: 325.3 MB (325346691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a859925722692d4c7a088a64eed49a5fe994d6306b15591dc09dfbf3d548fcb1`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc89d263a67a9f0c39ecd3687d7c5f9d81bb4f5eb4a5e8ed310aaf617b85e05`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d093d6a893077b9de6179bd5fe3d5d548d69ca51ae86dbf11a8673e51cc68b3e`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c316e8d37986e9bfbcf333e4329e0260ce83afe822e9501304231e00c60dcf6`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:94ff618a12a93a134d11f03dc82e066a3b60195eee794f29729316b9dcfafe2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:7f6185af13681be1acafe491510e48584ac51a2bbda0cd322196b02ba4da6bf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.1 MB (578050080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1707326ff7644b7356cd613d98f17d7e01643e805b09d270c3b633318b4ad0fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:22:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 04:22:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 04:22:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 04:22:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 04:23:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 04:24:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:24:08 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 04:24:08 GMT
ENV ODOO_VERSION=16.0
# Fri, 26 Jan 2024 22:16:01 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 22:16:01 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Fri, 26 Jan 2024 22:17:20 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 22:17:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 22:17:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 22:17:25 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 22:17:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 22:17:25 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 22:17:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 22:17:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 22:17:25 GMT
USER odoo
# Fri, 26 Jan 2024 22:17:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 22:17:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86654a69bafa33531b4fcae19511db74ec083ee8a32a4e5f68400b666ea91d3`  
		Last Modified: Thu, 11 Jan 2024 04:28:50 GMT  
		Size: 219.6 MB (219605557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ade87532781cb4a4f46880be8dc7fdde9c138904bb8d31a486c98f76224e59b`  
		Last Modified: Thu, 11 Jan 2024 04:28:26 GMT  
		Size: 2.6 MB (2629862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d092994f2bb47b54ec61d78cd536111b7c2aed38ff9c54d904acfa556f832abe`  
		Last Modified: Thu, 11 Jan 2024 04:28:25 GMT  
		Size: 460.4 KB (460351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b84941b26528dde691be92b29af38d3e26e0651f9b50a17ebaff4cb696a26cb`  
		Last Modified: Fri, 26 Jan 2024 22:20:40 GMT  
		Size: 323.9 MB (323933892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da77c7a47a8e49f7c5de832067af79be16e736007853f432c884e74ccf37f87`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d63cf6aad2baa274daa4adaabbbb975ef0bfe24faa509cc6a2e59365640d8b`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc620dfb39b6146d9fd8d792b5cd36f6287d12a9aec986803d35a996dad7448f`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aa31640195d081ed593ecb3ab5552c7869e28d52915786c2a201271f87f6dd`  
		Last Modified: Fri, 26 Jan 2024 22:20:03 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:956c47b45d80bc3eec09e9c53e02ee27298c03fd8c185580c0d4b9510ea7d831
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.6 MB (573642590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc3e5a3bd6c5c98bf2d0a04947465088a12fe55dde0aa7bab9108c0198b7117`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:32:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 06:32:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 06:32:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 06:32:19 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 06:33:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 06:33:33 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:33:34 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 06:33:34 GMT
ENV ODOO_VERSION=16.0
# Fri, 26 Jan 2024 19:22:55 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 19:22:56 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Fri, 26 Jan 2024 19:24:15 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 19:24:24 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 19:24:24 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 19:24:24 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 19:24:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 19:24:25 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 19:24:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 19:24:25 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 19:24:25 GMT
USER odoo
# Fri, 26 Jan 2024 19:24:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 19:24:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843638cd2bb45ed1fac36d25687a35e96bac688f9925d94266efe7a01b02dbc2`  
		Last Modified: Thu, 11 Jan 2024 06:35:43 GMT  
		Size: 216.9 MB (216908953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ecca8e8834b331b36f9b4440b200f5387f9e128237d075371a1088530fe7b2`  
		Last Modified: Thu, 11 Jan 2024 06:35:23 GMT  
		Size: 2.6 MB (2634821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ce5b97e9a663db05af8bf4aac7112926f555fdc5b3f95caede4a11d02a935d`  
		Last Modified: Thu, 11 Jan 2024 06:35:22 GMT  
		Size: 460.3 KB (460316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7909ae8a6d7f01547acec8678ef246c45660314a77396af63f09cdde8636e0d9`  
		Last Modified: Fri, 26 Jan 2024 19:25:56 GMT  
		Size: 323.6 MB (323572029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4c835b0fa073c14203653157142ce0385b36cca702f1220b5fc917b48059bc`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6bb9aea991dbf291716a5053a76e49d48492ccc15a9d886a7dbad78afdb794`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef0a251669f5ddc2606822235bc6dfab09566727860301c28133587e79f659a`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e919aaa4c5e25444d61127b5b3ee3eddd2d6add964f5c59f68a33e97258404da`  
		Last Modified: Fri, 26 Jan 2024 19:25:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f20dee6297caa96b988a997c492e45ea8d5564251ecf8d9e0e1cc125408abdf9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592580111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88d43497f98547a272a4b8add381a1b3f6c6bcfcc5db7fb11e0366a3bde6051`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:56:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 11 Jan 2024 03:56:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 11 Jan 2024 03:56:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jan 2024 03:56:43 GMT
ARG TARGETARCH
# Thu, 11 Jan 2024 03:59:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 11 Jan 2024 03:59:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:59:44 GMT
RUN npm install -g rtlcss
# Thu, 11 Jan 2024 03:59:45 GMT
ENV ODOO_VERSION=16.0
# Fri, 26 Jan 2024 20:48:11 GMT
ARG ODOO_RELEASE=20240126
# Fri, 26 Jan 2024 20:48:11 GMT
ARG ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
# Fri, 26 Jan 2024 20:50:30 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 26 Jan 2024 20:50:44 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 26 Jan 2024 20:50:44 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 26 Jan 2024 20:50:46 GMT
# ARGS: ODOO_RELEASE=20240126 ODOO_SHA=7774e76d4044e675b9d1ca64832e6a581d90a9b6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 26 Jan 2024 20:50:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 26 Jan 2024 20:50:48 GMT
EXPOSE 8069 8071 8072
# Fri, 26 Jan 2024 20:50:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 26 Jan 2024 20:50:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 26 Jan 2024 20:50:49 GMT
USER odoo
# Fri, 26 Jan 2024 20:50:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Jan 2024 20:50:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98645df03fa753cd35df386c12a15edceb4284519ed070b82144681b10101c7`  
		Last Modified: Thu, 11 Jan 2024 04:03:17 GMT  
		Size: 228.6 MB (228601149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e8f09bc42c4ab2ba211885268c12651fd157357bc388a9ace0b59c705a2d22`  
		Last Modified: Thu, 11 Jan 2024 04:02:47 GMT  
		Size: 2.9 MB (2875618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5ba7386839331811e9baf6be69016dc74bc0b395e5d441677af7b58038dff5`  
		Last Modified: Thu, 11 Jan 2024 04:02:46 GMT  
		Size: 460.4 KB (460388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585025124c501e07915a832153ce244a321221f3f705e34b4a50c67f0156a6a7`  
		Last Modified: Fri, 26 Jan 2024 20:52:55 GMT  
		Size: 325.3 MB (325346691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a859925722692d4c7a088a64eed49a5fe994d6306b15591dc09dfbf3d548fcb1`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc89d263a67a9f0c39ecd3687d7c5f9d81bb4f5eb4a5e8ed310aaf617b85e05`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d093d6a893077b9de6179bd5fe3d5d548d69ca51ae86dbf11a8673e51cc68b3e`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c316e8d37986e9bfbcf333e4329e0260ce83afe822e9501304231e00c60dcf6`  
		Last Modified: Fri, 26 Jan 2024 20:52:11 GMT  
		Size: 584.0 B  
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
