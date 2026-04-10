<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260409`](#odoo170-20260409)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260409`](#odoo180-20260409)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260409`](#odoo190-20260409)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:a8bcc45a0175c4d05b7eab2f26b6b3e5d68ace02bb21014cbd01516914c02a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:ec85cb8f67cd10e35c38a776dd540aabe1fe09547760d1baf1c800c3b32c8f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.3 MB (612258075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cd557b7a3d47011c1699ad718422fddc60dde8e4dd0ec12046ba52cb75ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:10 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:10 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
ENV ODOO_VERSION=17.0
# Thu, 09 Apr 2026 22:23:19 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:19 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Thu, 09 Apr 2026 22:24:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea37081b859fff4e0ed40220233728ed53a9f4cab3e71ef1ea58b8fde2132581`  
		Last Modified: Thu, 09 Apr 2026 22:25:43 GMT  
		Size: 236.1 MB (236107806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f1276903914d8fb9075922446a9dd8c4c2d422a32e4beb5b8b0dd16d5558f`  
		Last Modified: Thu, 09 Apr 2026 22:25:34 GMT  
		Size: 2.6 MB (2603843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99861e228da7527fb3745373af4f69893c4455c7b1432d07c197ece04cec90`  
		Last Modified: Thu, 09 Apr 2026 22:25:34 GMT  
		Size: 481.9 KB (481906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b204cea69cc7b5cb4d36e2fec5023748443ca00a2bb458034c1bab2b3d45b505`  
		Last Modified: Thu, 09 Apr 2026 22:25:44 GMT  
		Size: 343.3 MB (343325675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10952f24ffc179d1d1fc3bbd58cca9ff4ff319b66444ad249a1157b6aaea8c61`  
		Last Modified: Thu, 09 Apr 2026 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91d9666c365738d2c2eedd60c6d095d6c84d0aecbdba0f29b2630d8f2172c7`  
		Last Modified: Thu, 09 Apr 2026 22:25:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c58b66921594701e8dc3847088061c2f42d87cdc98712f7dcca9ecba448ed3`  
		Last Modified: Thu, 09 Apr 2026 22:25:36 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13f9b8635b462b10b59076bdefc68d26ac990b5a35086f93676dc30585a8493`  
		Last Modified: Thu, 09 Apr 2026 22:25:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:2917524294e0e2a2b7257f3e4243ee807afba307f6f1c9184f46cd32f83b78a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd8b481db816345665a7ec8b8b009119da133490034c550b5e6b19c382edf72`

```dockerfile
```

-	Layers:
	-	`sha256:298fe9871f847ab028826b68765e29483aa16a8fadcd451bf7c6abcfe91b44f7`  
		Last Modified: Thu, 09 Apr 2026 22:25:36 GMT  
		Size: 42.9 MB (42873378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b361d91b85bae908ea136d8c2173d564b1468d234ad637530a89213999f6cd2`  
		Last Modified: Thu, 09 Apr 2026 22:25:33 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:46b23862b2e99a6da5e00517b5a89779f0513991a24f18f8acd835bc43a0aac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.0 MB (606977778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1311522f48202d5245f971600468b1a50644c50d8004967e64454726bde79f43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:24 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:24 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:24 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:24 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:31 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:32 GMT
ENV ODOO_VERSION=17.0
# Thu, 09 Apr 2026 22:24:32 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:32 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Thu, 09 Apr 2026 22:25:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dba037a6046235e9904ab5437a5e90246c5c56a177bedb1079ba240267ffa12`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 233.3 MB (233336734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248be8bf8ef6fed756aecf9bf8537d64f334196e13dc2ff6399fc9969f0c5884`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 2.6 MB (2598241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7bc5bc392e0d28eb11a61fc449d9d271e1acc5be57efb326df6f3cf9cdf35`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 481.9 KB (481921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9de383eed55269a87b9d225a21c53c7e736fc3439c16ffc6aab0b7bdcf6843`  
		Last Modified: Thu, 09 Apr 2026 22:27:05 GMT  
		Size: 343.0 MB (342951503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7657d67bb1bbd7283f2d55c302a2eab002ac248aadbadf4aa4362e3a7fe36d6`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d454f2bf8a7beb283ea45ea1f811495c3363be81509007d56f1df08d0f0609d`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff09057af371102d002a975a15c93ee9dffd0df8ce2fab7faf09ceae446cf44d`  
		Last Modified: Thu, 09 Apr 2026 22:26:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd74610b481571dadc2e25aa4f50e7a73654898a317e99a74f548a15078c36c`  
		Last Modified: Thu, 09 Apr 2026 22:26:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:20cacf5721fb173ca0c22cf56d09f57e3f99b454276d5a3b39fb8c0e470e86fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42906829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b908af89da6e778c892c00eda56b065ef216dde46f5c01809e654f26fddf57c`

```dockerfile
```

-	Layers:
	-	`sha256:fb53d3fdf1baf7997a922cbc0c811cc79ac4763f13b6a4cb710ae4f4e66f1328`  
		Last Modified: Thu, 09 Apr 2026 22:26:57 GMT  
		Size: 42.9 MB (42879885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d322dabc2bcccd02048635698b8bfb68f97e2e365acefee04d0518b8b28b4d9e`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:a8bcc45a0175c4d05b7eab2f26b6b3e5d68ace02bb21014cbd01516914c02a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:ec85cb8f67cd10e35c38a776dd540aabe1fe09547760d1baf1c800c3b32c8f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.3 MB (612258075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cd557b7a3d47011c1699ad718422fddc60dde8e4dd0ec12046ba52cb75ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:10 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:10 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
ENV ODOO_VERSION=17.0
# Thu, 09 Apr 2026 22:23:19 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:19 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Thu, 09 Apr 2026 22:24:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea37081b859fff4e0ed40220233728ed53a9f4cab3e71ef1ea58b8fde2132581`  
		Last Modified: Thu, 09 Apr 2026 22:25:43 GMT  
		Size: 236.1 MB (236107806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f1276903914d8fb9075922446a9dd8c4c2d422a32e4beb5b8b0dd16d5558f`  
		Last Modified: Thu, 09 Apr 2026 22:25:34 GMT  
		Size: 2.6 MB (2603843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99861e228da7527fb3745373af4f69893c4455c7b1432d07c197ece04cec90`  
		Last Modified: Thu, 09 Apr 2026 22:25:34 GMT  
		Size: 481.9 KB (481906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b204cea69cc7b5cb4d36e2fec5023748443ca00a2bb458034c1bab2b3d45b505`  
		Last Modified: Thu, 09 Apr 2026 22:25:44 GMT  
		Size: 343.3 MB (343325675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10952f24ffc179d1d1fc3bbd58cca9ff4ff319b66444ad249a1157b6aaea8c61`  
		Last Modified: Thu, 09 Apr 2026 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91d9666c365738d2c2eedd60c6d095d6c84d0aecbdba0f29b2630d8f2172c7`  
		Last Modified: Thu, 09 Apr 2026 22:25:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c58b66921594701e8dc3847088061c2f42d87cdc98712f7dcca9ecba448ed3`  
		Last Modified: Thu, 09 Apr 2026 22:25:36 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13f9b8635b462b10b59076bdefc68d26ac990b5a35086f93676dc30585a8493`  
		Last Modified: Thu, 09 Apr 2026 22:25:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2917524294e0e2a2b7257f3e4243ee807afba307f6f1c9184f46cd32f83b78a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd8b481db816345665a7ec8b8b009119da133490034c550b5e6b19c382edf72`

```dockerfile
```

-	Layers:
	-	`sha256:298fe9871f847ab028826b68765e29483aa16a8fadcd451bf7c6abcfe91b44f7`  
		Last Modified: Thu, 09 Apr 2026 22:25:36 GMT  
		Size: 42.9 MB (42873378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b361d91b85bae908ea136d8c2173d564b1468d234ad637530a89213999f6cd2`  
		Last Modified: Thu, 09 Apr 2026 22:25:33 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:46b23862b2e99a6da5e00517b5a89779f0513991a24f18f8acd835bc43a0aac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.0 MB (606977778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1311522f48202d5245f971600468b1a50644c50d8004967e64454726bde79f43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:24 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:24 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:24 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:24 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:31 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:32 GMT
ENV ODOO_VERSION=17.0
# Thu, 09 Apr 2026 22:24:32 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:32 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Thu, 09 Apr 2026 22:25:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dba037a6046235e9904ab5437a5e90246c5c56a177bedb1079ba240267ffa12`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 233.3 MB (233336734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248be8bf8ef6fed756aecf9bf8537d64f334196e13dc2ff6399fc9969f0c5884`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 2.6 MB (2598241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7bc5bc392e0d28eb11a61fc449d9d271e1acc5be57efb326df6f3cf9cdf35`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 481.9 KB (481921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9de383eed55269a87b9d225a21c53c7e736fc3439c16ffc6aab0b7bdcf6843`  
		Last Modified: Thu, 09 Apr 2026 22:27:05 GMT  
		Size: 343.0 MB (342951503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7657d67bb1bbd7283f2d55c302a2eab002ac248aadbadf4aa4362e3a7fe36d6`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d454f2bf8a7beb283ea45ea1f811495c3363be81509007d56f1df08d0f0609d`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff09057af371102d002a975a15c93ee9dffd0df8ce2fab7faf09ceae446cf44d`  
		Last Modified: Thu, 09 Apr 2026 22:26:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd74610b481571dadc2e25aa4f50e7a73654898a317e99a74f548a15078c36c`  
		Last Modified: Thu, 09 Apr 2026 22:26:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:20cacf5721fb173ca0c22cf56d09f57e3f99b454276d5a3b39fb8c0e470e86fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42906829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b908af89da6e778c892c00eda56b065ef216dde46f5c01809e654f26fddf57c`

```dockerfile
```

-	Layers:
	-	`sha256:fb53d3fdf1baf7997a922cbc0c811cc79ac4763f13b6a4cb710ae4f4e66f1328`  
		Last Modified: Thu, 09 Apr 2026 22:26:57 GMT  
		Size: 42.9 MB (42879885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d322dabc2bcccd02048635698b8bfb68f97e2e365acefee04d0518b8b28b4d9e`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260409`

```console
$ docker pull odoo@sha256:a8bcc45a0175c4d05b7eab2f26b6b3e5d68ace02bb21014cbd01516914c02a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260409` - linux; amd64

```console
$ docker pull odoo@sha256:ec85cb8f67cd10e35c38a776dd540aabe1fe09547760d1baf1c800c3b32c8f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.3 MB (612258075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cd557b7a3d47011c1699ad718422fddc60dde8e4dd0ec12046ba52cb75ead9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:10 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:10 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:19 GMT
ENV ODOO_VERSION=17.0
# Thu, 09 Apr 2026 22:23:19 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:19 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Thu, 09 Apr 2026 22:24:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:20 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea37081b859fff4e0ed40220233728ed53a9f4cab3e71ef1ea58b8fde2132581`  
		Last Modified: Thu, 09 Apr 2026 22:25:43 GMT  
		Size: 236.1 MB (236107806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4f1276903914d8fb9075922446a9dd8c4c2d422a32e4beb5b8b0dd16d5558f`  
		Last Modified: Thu, 09 Apr 2026 22:25:34 GMT  
		Size: 2.6 MB (2603843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99861e228da7527fb3745373af4f69893c4455c7b1432d07c197ece04cec90`  
		Last Modified: Thu, 09 Apr 2026 22:25:34 GMT  
		Size: 481.9 KB (481906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b204cea69cc7b5cb4d36e2fec5023748443ca00a2bb458034c1bab2b3d45b505`  
		Last Modified: Thu, 09 Apr 2026 22:25:44 GMT  
		Size: 343.3 MB (343325675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10952f24ffc179d1d1fc3bbd58cca9ff4ff319b66444ad249a1157b6aaea8c61`  
		Last Modified: Thu, 09 Apr 2026 22:25:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91d9666c365738d2c2eedd60c6d095d6c84d0aecbdba0f29b2630d8f2172c7`  
		Last Modified: Thu, 09 Apr 2026 22:25:35 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c58b66921594701e8dc3847088061c2f42d87cdc98712f7dcca9ecba448ed3`  
		Last Modified: Thu, 09 Apr 2026 22:25:36 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13f9b8635b462b10b59076bdefc68d26ac990b5a35086f93676dc30585a8493`  
		Last Modified: Thu, 09 Apr 2026 22:25:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:2917524294e0e2a2b7257f3e4243ee807afba307f6f1c9184f46cd32f83b78a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd8b481db816345665a7ec8b8b009119da133490034c550b5e6b19c382edf72`

```dockerfile
```

-	Layers:
	-	`sha256:298fe9871f847ab028826b68765e29483aa16a8fadcd451bf7c6abcfe91b44f7`  
		Last Modified: Thu, 09 Apr 2026 22:25:36 GMT  
		Size: 42.9 MB (42873378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b361d91b85bae908ea136d8c2173d564b1468d234ad637530a89213999f6cd2`  
		Last Modified: Thu, 09 Apr 2026 22:25:33 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260409` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:46b23862b2e99a6da5e00517b5a89779f0513991a24f18f8acd835bc43a0aac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.0 MB (606977778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1311522f48202d5245f971600468b1a50644c50d8004967e64454726bde79f43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:24 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:24 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:24 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:24 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:31 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:32 GMT
ENV ODOO_VERSION=17.0
# Thu, 09 Apr 2026 22:24:32 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:32 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Thu, 09 Apr 2026 22:25:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:38 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dba037a6046235e9904ab5437a5e90246c5c56a177bedb1079ba240267ffa12`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 233.3 MB (233336734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248be8bf8ef6fed756aecf9bf8537d64f334196e13dc2ff6399fc9969f0c5884`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 2.6 MB (2598241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7bc5bc392e0d28eb11a61fc449d9d271e1acc5be57efb326df6f3cf9cdf35`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 481.9 KB (481921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9de383eed55269a87b9d225a21c53c7e736fc3439c16ffc6aab0b7bdcf6843`  
		Last Modified: Thu, 09 Apr 2026 22:27:05 GMT  
		Size: 343.0 MB (342951503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7657d67bb1bbd7283f2d55c302a2eab002ac248aadbadf4aa4362e3a7fe36d6`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d454f2bf8a7beb283ea45ea1f811495c3363be81509007d56f1df08d0f0609d`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff09057af371102d002a975a15c93ee9dffd0df8ce2fab7faf09ceae446cf44d`  
		Last Modified: Thu, 09 Apr 2026 22:26:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd74610b481571dadc2e25aa4f50e7a73654898a317e99a74f548a15078c36c`  
		Last Modified: Thu, 09 Apr 2026 22:26:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:20cacf5721fb173ca0c22cf56d09f57e3f99b454276d5a3b39fb8c0e470e86fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42906829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b908af89da6e778c892c00eda56b065ef216dde46f5c01809e654f26fddf57c`

```dockerfile
```

-	Layers:
	-	`sha256:fb53d3fdf1baf7997a922cbc0c811cc79ac4763f13b6a4cb710ae4f4e66f1328`  
		Last Modified: Thu, 09 Apr 2026 22:26:57 GMT  
		Size: 42.9 MB (42879885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d322dabc2bcccd02048635698b8bfb68f97e2e365acefee04d0518b8b28b4d9e`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:4a1f2e3d6b812d113cb0f4d04b5b7174e3c08d934d632e3b82b8129ef0ff317c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:0117ade4ad4cac2b0c1c5787b350b1ed5ed973c3a893352ee02a978d26f2cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686444291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a526308a2ffc8aad6af5268e3d8b613a689d542246451daf7cd2682415dd8bc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:32 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 22:23:41 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:41 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 22:24:30 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:30 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc117335c43f4befb474691c5888ebf1ad71fb25ab1abbb8ef6ac9163e8618`  
		Last Modified: Thu, 09 Apr 2026 22:26:21 GMT  
		Size: 257.0 MB (256957204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08565cd72af2c0be66a341ddc6d8c082166655b3d5ea0cc365c7bfc9bd2ac1ae`  
		Last Modified: Thu, 09 Apr 2026 22:26:12 GMT  
		Size: 14.4 MB (14360316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe1b7a0a4e0cf3e2c15abeac918bb09d076e2f2bf4e9b028726c5bc850c0a20`  
		Last Modified: Thu, 09 Apr 2026 22:26:11 GMT  
		Size: 481.7 KB (481711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d42a3b9034894b658eab3c92fbf0704d01b1c961597aced3fb65439679eb7ed`  
		Last Modified: Thu, 09 Apr 2026 22:26:24 GMT  
		Size: 384.9 MB (384909162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6323990bf6fc8c431dc8580c462b66a54a1e7f79bf77ca50dd770af7bccf6256`  
		Last Modified: Thu, 09 Apr 2026 22:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3169b8018e1a3c59192e1ee0307c2c9666dedf76648baf5d155a1219718879e9`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea09febbb86602230b82894c9a94a1657aac2f3eb510feef316e9cb1eb661f7`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d17e17b36862fd9c12118d65d2d7702ec4f46982911e2c8e4fb04416935203`  
		Last Modified: Thu, 09 Apr 2026 22:26:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:38b39494c9d7b98ee3c515f1d5c961a8081e49ea08617b187de08f53fd623cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62223460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bac20c2d3ce7652a85181f80473de234fd89ba08a05d316b22d43a14074971`

```dockerfile
```

-	Layers:
	-	`sha256:b68176c91e891ec20767932a442991725ed0278a30db67604128f92e45529fdc`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 62.2 MB (62196661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe52c0b53224a57766b9523d73ca912d4727df7fb54033cbb53bc8f07ec9eb7`  
		Last Modified: Thu, 09 Apr 2026 22:26:11 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:504ccbaf4250045ef85c501afca810e679eefea27ac6de94d9ec19ac260ddd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682670287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2880f6219204085d218d2ba53b3ceb283aa38f6b4014d10c66d82570211261`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:53 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 22:24:53 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:53 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 22:25:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270ec91e1ae3becd0bb584b4885595d34f9700f39c08633979cac795a695e2d`  
		Last Modified: Thu, 09 Apr 2026 22:28:02 GMT  
		Size: 254.2 MB (254211743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d534585805e0b4a2eadea35be7794b8a133160b05e10ab2c7a922bbec24ec8ba`  
		Last Modified: Thu, 09 Apr 2026 22:27:54 GMT  
		Size: 14.3 MB (14341023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef47bc35b07e9b92bc9f6f344160bef703f315e3a40f1856f7ae7f3680e0b5fb`  
		Last Modified: Thu, 09 Apr 2026 22:27:53 GMT  
		Size: 481.7 KB (481694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362be533c78848405d225dee8e2b9b44f21d17b24b786ccbe04ff2d9636229c2`  
		Last Modified: Thu, 09 Apr 2026 22:28:05 GMT  
		Size: 384.8 MB (384759309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f8674664e79feef02a873984fbf0cbc4b3ca3f11f97b3c475cb00c816f2b9d`  
		Last Modified: Thu, 09 Apr 2026 22:27:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ac31ef833b23409a09ae6e6dba17404a8b1930e42aa6a3e06945fdfff15aed`  
		Last Modified: Thu, 09 Apr 2026 22:27:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a341e42fbaf1c93c46a6ba16dc8141414544e8f4d3fbaaac64a5ad6f3d433`  
		Last Modified: Thu, 09 Apr 2026 22:27:56 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52584e5bd1a3582d1ed57f1d9b9769f96b5535ef2fb468b4a0d91f6845b3ca8`  
		Last Modified: Thu, 09 Apr 2026 22:27:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:38981ef17e3fc18a234991819de86739e97fdcdff481f8481af5b2bf5fe0e295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62230887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e231d55feb4c5329ea86c9b315b2258d903275fcf864e95ba233234c3fa6c00c`

```dockerfile
```

-	Layers:
	-	`sha256:cdf735457fbcbf196467e4e0bed0a0a80035de0782373ae7e27e5e4e8dc5193c`  
		Last Modified: Thu, 09 Apr 2026 22:27:57 GMT  
		Size: 62.2 MB (62203936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cc62d391d98b7ccebec16a2804eee7733f2000989540c13987d7b8f5942fa6`  
		Last Modified: Thu, 09 Apr 2026 22:27:53 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:08e26ab9110a807f60a3a177ef79db21dcd5eba0a531f57c166efa6fefe41c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702878154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85328acd43aeb27f464465f75ef2122d4313a505c0bc82a2e8fd4d6ba395fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 23:41:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:12 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:14 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe349b85490880a88231c1c0942cf37db9a8401fb1da89eb5b7fd1d3dcc846a0`  
		Last Modified: Thu, 09 Apr 2026 23:46:00 GMT  
		Size: 385.4 MB (385449619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70c525eef82e2b32ebce0a5e86c127e68fc41b955c75a980171ff9da77bb464`  
		Last Modified: Thu, 09 Apr 2026 23:45:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4294c4bb207407a3fd56dd48d8900dca500e5a9367de13c42b2a1c126e82ba`  
		Last Modified: Thu, 09 Apr 2026 23:45:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b97894e483df2d54da85ac73d9fcfdf73a966f28074d5ac9d64839d3ced0a`  
		Last Modified: Thu, 09 Apr 2026 23:45:49 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c6c01cddb14e84c9a0dcd7e06d0021f69e96fb5d654592899cad74c7fb5207`  
		Last Modified: Thu, 09 Apr 2026 23:45:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:10ddc246c17ae6e7537117a172920eb7d9337f1898ec3e7bfec631105882f6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e35ae7aa3aa27c4cd372a4a8db23f7f41c68338139ee7d312e3cbd998a33d`

```dockerfile
```

-	Layers:
	-	`sha256:805c966006eda13cda9c7358a0ace5f9f57c576981083c41c2a7d0770352de1a`  
		Last Modified: Thu, 09 Apr 2026 23:45:50 GMT  
		Size: 62.2 MB (62205044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1563cf07474f4c97f5f34bc45f13f5fd461026ba7e517347f5ee175bdf1e2d`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:4a1f2e3d6b812d113cb0f4d04b5b7174e3c08d934d632e3b82b8129ef0ff317c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:0117ade4ad4cac2b0c1c5787b350b1ed5ed973c3a893352ee02a978d26f2cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686444291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a526308a2ffc8aad6af5268e3d8b613a689d542246451daf7cd2682415dd8bc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:32 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 22:23:41 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:41 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 22:24:30 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:30 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc117335c43f4befb474691c5888ebf1ad71fb25ab1abbb8ef6ac9163e8618`  
		Last Modified: Thu, 09 Apr 2026 22:26:21 GMT  
		Size: 257.0 MB (256957204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08565cd72af2c0be66a341ddc6d8c082166655b3d5ea0cc365c7bfc9bd2ac1ae`  
		Last Modified: Thu, 09 Apr 2026 22:26:12 GMT  
		Size: 14.4 MB (14360316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe1b7a0a4e0cf3e2c15abeac918bb09d076e2f2bf4e9b028726c5bc850c0a20`  
		Last Modified: Thu, 09 Apr 2026 22:26:11 GMT  
		Size: 481.7 KB (481711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d42a3b9034894b658eab3c92fbf0704d01b1c961597aced3fb65439679eb7ed`  
		Last Modified: Thu, 09 Apr 2026 22:26:24 GMT  
		Size: 384.9 MB (384909162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6323990bf6fc8c431dc8580c462b66a54a1e7f79bf77ca50dd770af7bccf6256`  
		Last Modified: Thu, 09 Apr 2026 22:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3169b8018e1a3c59192e1ee0307c2c9666dedf76648baf5d155a1219718879e9`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea09febbb86602230b82894c9a94a1657aac2f3eb510feef316e9cb1eb661f7`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d17e17b36862fd9c12118d65d2d7702ec4f46982911e2c8e4fb04416935203`  
		Last Modified: Thu, 09 Apr 2026 22:26:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:38b39494c9d7b98ee3c515f1d5c961a8081e49ea08617b187de08f53fd623cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62223460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bac20c2d3ce7652a85181f80473de234fd89ba08a05d316b22d43a14074971`

```dockerfile
```

-	Layers:
	-	`sha256:b68176c91e891ec20767932a442991725ed0278a30db67604128f92e45529fdc`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 62.2 MB (62196661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe52c0b53224a57766b9523d73ca912d4727df7fb54033cbb53bc8f07ec9eb7`  
		Last Modified: Thu, 09 Apr 2026 22:26:11 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:504ccbaf4250045ef85c501afca810e679eefea27ac6de94d9ec19ac260ddd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682670287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2880f6219204085d218d2ba53b3ceb283aa38f6b4014d10c66d82570211261`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:53 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 22:24:53 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:53 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 22:25:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270ec91e1ae3becd0bb584b4885595d34f9700f39c08633979cac795a695e2d`  
		Last Modified: Thu, 09 Apr 2026 22:28:02 GMT  
		Size: 254.2 MB (254211743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d534585805e0b4a2eadea35be7794b8a133160b05e10ab2c7a922bbec24ec8ba`  
		Last Modified: Thu, 09 Apr 2026 22:27:54 GMT  
		Size: 14.3 MB (14341023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef47bc35b07e9b92bc9f6f344160bef703f315e3a40f1856f7ae7f3680e0b5fb`  
		Last Modified: Thu, 09 Apr 2026 22:27:53 GMT  
		Size: 481.7 KB (481694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362be533c78848405d225dee8e2b9b44f21d17b24b786ccbe04ff2d9636229c2`  
		Last Modified: Thu, 09 Apr 2026 22:28:05 GMT  
		Size: 384.8 MB (384759309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f8674664e79feef02a873984fbf0cbc4b3ca3f11f97b3c475cb00c816f2b9d`  
		Last Modified: Thu, 09 Apr 2026 22:27:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ac31ef833b23409a09ae6e6dba17404a8b1930e42aa6a3e06945fdfff15aed`  
		Last Modified: Thu, 09 Apr 2026 22:27:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a341e42fbaf1c93c46a6ba16dc8141414544e8f4d3fbaaac64a5ad6f3d433`  
		Last Modified: Thu, 09 Apr 2026 22:27:56 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52584e5bd1a3582d1ed57f1d9b9769f96b5535ef2fb468b4a0d91f6845b3ca8`  
		Last Modified: Thu, 09 Apr 2026 22:27:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:38981ef17e3fc18a234991819de86739e97fdcdff481f8481af5b2bf5fe0e295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62230887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e231d55feb4c5329ea86c9b315b2258d903275fcf864e95ba233234c3fa6c00c`

```dockerfile
```

-	Layers:
	-	`sha256:cdf735457fbcbf196467e4e0bed0a0a80035de0782373ae7e27e5e4e8dc5193c`  
		Last Modified: Thu, 09 Apr 2026 22:27:57 GMT  
		Size: 62.2 MB (62203936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cc62d391d98b7ccebec16a2804eee7733f2000989540c13987d7b8f5942fa6`  
		Last Modified: Thu, 09 Apr 2026 22:27:53 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:08e26ab9110a807f60a3a177ef79db21dcd5eba0a531f57c166efa6fefe41c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702878154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85328acd43aeb27f464465f75ef2122d4313a505c0bc82a2e8fd4d6ba395fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 23:41:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:12 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:14 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe349b85490880a88231c1c0942cf37db9a8401fb1da89eb5b7fd1d3dcc846a0`  
		Last Modified: Thu, 09 Apr 2026 23:46:00 GMT  
		Size: 385.4 MB (385449619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70c525eef82e2b32ebce0a5e86c127e68fc41b955c75a980171ff9da77bb464`  
		Last Modified: Thu, 09 Apr 2026 23:45:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4294c4bb207407a3fd56dd48d8900dca500e5a9367de13c42b2a1c126e82ba`  
		Last Modified: Thu, 09 Apr 2026 23:45:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b97894e483df2d54da85ac73d9fcfdf73a966f28074d5ac9d64839d3ced0a`  
		Last Modified: Thu, 09 Apr 2026 23:45:49 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c6c01cddb14e84c9a0dcd7e06d0021f69e96fb5d654592899cad74c7fb5207`  
		Last Modified: Thu, 09 Apr 2026 23:45:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:10ddc246c17ae6e7537117a172920eb7d9337f1898ec3e7bfec631105882f6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e35ae7aa3aa27c4cd372a4a8db23f7f41c68338139ee7d312e3cbd998a33d`

```dockerfile
```

-	Layers:
	-	`sha256:805c966006eda13cda9c7358a0ace5f9f57c576981083c41c2a7d0770352de1a`  
		Last Modified: Thu, 09 Apr 2026 23:45:50 GMT  
		Size: 62.2 MB (62205044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1563cf07474f4c97f5f34bc45f13f5fd461026ba7e517347f5ee175bdf1e2d`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260409`

```console
$ docker pull odoo@sha256:4a1f2e3d6b812d113cb0f4d04b5b7174e3c08d934d632e3b82b8129ef0ff317c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260409` - linux; amd64

```console
$ docker pull odoo@sha256:0117ade4ad4cac2b0c1c5787b350b1ed5ed973c3a893352ee02a978d26f2cbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686444291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a526308a2ffc8aad6af5268e3d8b613a689d542246451daf7cd2682415dd8bc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:32 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:40 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 22:23:41 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:41 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 22:24:30 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:30 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:30 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc117335c43f4befb474691c5888ebf1ad71fb25ab1abbb8ef6ac9163e8618`  
		Last Modified: Thu, 09 Apr 2026 22:26:21 GMT  
		Size: 257.0 MB (256957204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08565cd72af2c0be66a341ddc6d8c082166655b3d5ea0cc365c7bfc9bd2ac1ae`  
		Last Modified: Thu, 09 Apr 2026 22:26:12 GMT  
		Size: 14.4 MB (14360316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe1b7a0a4e0cf3e2c15abeac918bb09d076e2f2bf4e9b028726c5bc850c0a20`  
		Last Modified: Thu, 09 Apr 2026 22:26:11 GMT  
		Size: 481.7 KB (481711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d42a3b9034894b658eab3c92fbf0704d01b1c961597aced3fb65439679eb7ed`  
		Last Modified: Thu, 09 Apr 2026 22:26:24 GMT  
		Size: 384.9 MB (384909162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6323990bf6fc8c431dc8580c462b66a54a1e7f79bf77ca50dd770af7bccf6256`  
		Last Modified: Thu, 09 Apr 2026 22:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3169b8018e1a3c59192e1ee0307c2c9666dedf76648baf5d155a1219718879e9`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea09febbb86602230b82894c9a94a1657aac2f3eb510feef316e9cb1eb661f7`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d17e17b36862fd9c12118d65d2d7702ec4f46982911e2c8e4fb04416935203`  
		Last Modified: Thu, 09 Apr 2026 22:26:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:38b39494c9d7b98ee3c515f1d5c961a8081e49ea08617b187de08f53fd623cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62223460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bac20c2d3ce7652a85181f80473de234fd89ba08a05d316b22d43a14074971`

```dockerfile
```

-	Layers:
	-	`sha256:b68176c91e891ec20767932a442991725ed0278a30db67604128f92e45529fdc`  
		Last Modified: Thu, 09 Apr 2026 22:26:14 GMT  
		Size: 62.2 MB (62196661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe52c0b53224a57766b9523d73ca912d4727df7fb54033cbb53bc8f07ec9eb7`  
		Last Modified: Thu, 09 Apr 2026 22:26:11 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260409` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:504ccbaf4250045ef85c501afca810e679eefea27ac6de94d9ec19ac260ddd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682670287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2880f6219204085d218d2ba53b3ceb283aa38f6b4014d10c66d82570211261`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:53 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 22:24:53 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:53 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 22:25:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:51 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270ec91e1ae3becd0bb584b4885595d34f9700f39c08633979cac795a695e2d`  
		Last Modified: Thu, 09 Apr 2026 22:28:02 GMT  
		Size: 254.2 MB (254211743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d534585805e0b4a2eadea35be7794b8a133160b05e10ab2c7a922bbec24ec8ba`  
		Last Modified: Thu, 09 Apr 2026 22:27:54 GMT  
		Size: 14.3 MB (14341023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef47bc35b07e9b92bc9f6f344160bef703f315e3a40f1856f7ae7f3680e0b5fb`  
		Last Modified: Thu, 09 Apr 2026 22:27:53 GMT  
		Size: 481.7 KB (481694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362be533c78848405d225dee8e2b9b44f21d17b24b786ccbe04ff2d9636229c2`  
		Last Modified: Thu, 09 Apr 2026 22:28:05 GMT  
		Size: 384.8 MB (384759309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f8674664e79feef02a873984fbf0cbc4b3ca3f11f97b3c475cb00c816f2b9d`  
		Last Modified: Thu, 09 Apr 2026 22:27:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ac31ef833b23409a09ae6e6dba17404a8b1930e42aa6a3e06945fdfff15aed`  
		Last Modified: Thu, 09 Apr 2026 22:27:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a341e42fbaf1c93c46a6ba16dc8141414544e8f4d3fbaaac64a5ad6f3d433`  
		Last Modified: Thu, 09 Apr 2026 22:27:56 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52584e5bd1a3582d1ed57f1d9b9769f96b5535ef2fb468b4a0d91f6845b3ca8`  
		Last Modified: Thu, 09 Apr 2026 22:27:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:38981ef17e3fc18a234991819de86739e97fdcdff481f8481af5b2bf5fe0e295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62230887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e231d55feb4c5329ea86c9b315b2258d903275fcf864e95ba233234c3fa6c00c`

```dockerfile
```

-	Layers:
	-	`sha256:cdf735457fbcbf196467e4e0bed0a0a80035de0782373ae7e27e5e4e8dc5193c`  
		Last Modified: Thu, 09 Apr 2026 22:27:57 GMT  
		Size: 62.2 MB (62203936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cc62d391d98b7ccebec16a2804eee7733f2000989540c13987d7b8f5942fa6`  
		Last Modified: Thu, 09 Apr 2026 22:27:53 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260409` - linux; ppc64le

```console
$ docker pull odoo@sha256:08e26ab9110a807f60a3a177ef79db21dcd5eba0a531f57c166efa6fefe41c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702878154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85328acd43aeb27f464465f75ef2122d4313a505c0bc82a2e8fd4d6ba395fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=18.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Thu, 09 Apr 2026 23:41:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:12 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:14 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe349b85490880a88231c1c0942cf37db9a8401fb1da89eb5b7fd1d3dcc846a0`  
		Last Modified: Thu, 09 Apr 2026 23:46:00 GMT  
		Size: 385.4 MB (385449619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70c525eef82e2b32ebce0a5e86c127e68fc41b955c75a980171ff9da77bb464`  
		Last Modified: Thu, 09 Apr 2026 23:45:48 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4294c4bb207407a3fd56dd48d8900dca500e5a9367de13c42b2a1c126e82ba`  
		Last Modified: Thu, 09 Apr 2026 23:45:49 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b97894e483df2d54da85ac73d9fcfdf73a966f28074d5ac9d64839d3ced0a`  
		Last Modified: Thu, 09 Apr 2026 23:45:49 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c6c01cddb14e84c9a0dcd7e06d0021f69e96fb5d654592899cad74c7fb5207`  
		Last Modified: Thu, 09 Apr 2026 23:45:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:10ddc246c17ae6e7537117a172920eb7d9337f1898ec3e7bfec631105882f6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20e35ae7aa3aa27c4cd372a4a8db23f7f41c68338139ee7d312e3cbd998a33d`

```dockerfile
```

-	Layers:
	-	`sha256:805c966006eda13cda9c7358a0ace5f9f57c576981083c41c2a7d0770352de1a`  
		Last Modified: Thu, 09 Apr 2026 23:45:50 GMT  
		Size: 62.2 MB (62205044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1563cf07474f4c97f5f34bc45f13f5fd461026ba7e517347f5ee175bdf1e2d`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:6eb3573f6486599e3c88626cb3eef00852fe6e4f814d9622ac9bde8105fbebab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:79b2ef63f1848ec4d670c67a3b7b8c5ae9aaf973500324f6da2e1bd07c2d4808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.3 MB (705252815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4303fb5446af5ce9ce52d54422e3129c2608308ab5e5a95db593c398c12af41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:25 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:25 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:24:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9677a3f60ed82918a2b05f2480dfa892c951f69986d8f55220b20838def8fc`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 257.0 MB (256958760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8d89584f97bfd850a90d36dc925acee6f4fea5df93e4f8383246c1e4a6440`  
		Last Modified: Thu, 09 Apr 2026 22:26:53 GMT  
		Size: 14.4 MB (14360407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8fda1794311c23d7f7e240cd018b1e9fa41ef64b127cdb602d873595e5025`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 481.8 KB (481766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fe14aad69cad6f3b684a444d186a2cdf856de82e623eb56a4aba5548d9a224`  
		Last Modified: Thu, 09 Apr 2026 22:27:06 GMT  
		Size: 403.7 MB (403715986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff206674a0625e104dc5b8814425e71cbb9fcfa189e06f4f82c150521cf85d`  
		Last Modified: Thu, 09 Apr 2026 22:26:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed06373ee96815d446889f0e106823d238aafe97290113b2e6da75706bd373f`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dcfcdb41101194acdd859400380c7621589462315903d9afb767a864cd0ded`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76674ac897af088337ca0fb6e4ca31a94df26afa66f029295e5bad9b36e7292b`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:9968375774f9b0c9a8e81263f05bec08546d9e01bbdee456a50bfef1972a0a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1011c0dadb8a9b1aa88144194ede95988bb33cec97ed503576270012b260ed67`

```dockerfile
```

-	Layers:
	-	`sha256:9481575ab59927b71e3bdc921c1ca707e15d251ee70a5508224c2b47db68f9c7`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 70.0 MB (69986879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07874adf8ffcaa4965cafe0a8b49422f9ae6a066aa4aa3263d78f229d41a8ebe`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c7c23aa7568963c03515f23e29ad49fe680968a5ee2c8cba24c067091bbac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.4 MB (701429390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de75c983129a92e56e2c9432656a28c8a9dbd1f47c4e9e73ad99b01f0a281392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:36 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:25:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf5ca75919c1363ba6ff93737daef5e90d636e7761428d8fc08da995b96ab8`  
		Last Modified: Thu, 09 Apr 2026 22:28:47 GMT  
		Size: 254.2 MB (254211656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54893e61957e389e7db6a46f41244f4fbcfe553be7cf55afe18a53da39900ab`  
		Last Modified: Thu, 09 Apr 2026 22:28:34 GMT  
		Size: 14.3 MB (14340986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d72a79263be7fc15b55734f076359b3feb714e06f8191773d6499182d97536`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 481.8 KB (481768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1779a68e379365151155243bceaf57301a49a1a49923b766464d9d128a8be43d`  
		Last Modified: Thu, 09 Apr 2026 22:28:51 GMT  
		Size: 403.5 MB (403518466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612a65a30045f6abfb9d3fa22c2e06a7c987d7b60603acde2002f3110d2b5f0`  
		Last Modified: Thu, 09 Apr 2026 22:28:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df9541de98e12c12ba7a96f89909048fe75b85c28bcbb1694b64df650fb845`  
		Last Modified: Thu, 09 Apr 2026 22:28:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e872554e4447d8dfa9251f6b94c0c14b5a1e02ff62515a69d180a19557d525`  
		Last Modified: Thu, 09 Apr 2026 22:28:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef1ccc6564d1d5881d5325fb388320cb0828c190296f2a75ffc71d8a99d27f`  
		Last Modified: Thu, 09 Apr 2026 22:28:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:d2dccbd76adae86e7013728c98be82f802e2cb0212120030c7588ffe162aacf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f9420716d0e0e3cbea9cf90eb25e84a3b762954774995b27e3d2726110b169`

```dockerfile
```

-	Layers:
	-	`sha256:a0687c05e9aba8dc3566d2b8a87ddb1167111078eebbdafd27d3835a357e1bf2`  
		Last Modified: Thu, 09 Apr 2026 22:28:39 GMT  
		Size: 70.0 MB (69994166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942ddde8ba548ef3787f2f685202dd0e1af02d021d492f8b8c83b361df288630`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d99c8452344fae6c66fb0ae6fc427236652459f4d770cb541bcfbc803f05e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.7 MB (721675575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500b9adfd00baea5fb031cffa2d6d90c9fbae5496c83e51e4adae8173d0f295e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 23:41:25 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:28 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27157e3fb6d3ac05979ecf688cdf0f6aee136d53cf986e94e4437f9562e1c19`  
		Last Modified: Thu, 09 Apr 2026 23:47:28 GMT  
		Size: 404.2 MB (404247038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7ea05369d5e150735c7c811dbd33599d8454d6f0572a0b93e3bb75fa803d4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae81cf2a2cde4f3ee39e47239416e6671f631dbf4087028cf3b96bde66e3bf4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ada916bcdbbb36bfda1c8af8a31ceb37e185e58bd5b3e37c4240a5616db4c`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237261e06badfa7b6274d0a01c72e2b465e0efa8ad13bf8af4c0ef24f4d8996`  
		Last Modified: Thu, 09 Apr 2026 23:47:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:0402678e8e587bda5d36714b5166198cf2e61910b2a9a02d4f5edebe84bdae30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e5a11c0def144d25bc7e2d898335c279b3f316738d94209dad35789ff66f5`

```dockerfile
```

-	Layers:
	-	`sha256:e0125d8699b92dae9ca782f344b4cbc90fb37c88071c0d2a7f0d9310fb44d488`  
		Last Modified: Thu, 09 Apr 2026 23:47:22 GMT  
		Size: 70.0 MB (69995268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f098b82d33e3aff0819e0a00ab51a9c518006e7f0d981c94a7a8789addad5073`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:6eb3573f6486599e3c88626cb3eef00852fe6e4f814d9622ac9bde8105fbebab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:79b2ef63f1848ec4d670c67a3b7b8c5ae9aaf973500324f6da2e1bd07c2d4808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.3 MB (705252815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4303fb5446af5ce9ce52d54422e3129c2608308ab5e5a95db593c398c12af41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:25 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:25 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:24:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9677a3f60ed82918a2b05f2480dfa892c951f69986d8f55220b20838def8fc`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 257.0 MB (256958760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8d89584f97bfd850a90d36dc925acee6f4fea5df93e4f8383246c1e4a6440`  
		Last Modified: Thu, 09 Apr 2026 22:26:53 GMT  
		Size: 14.4 MB (14360407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8fda1794311c23d7f7e240cd018b1e9fa41ef64b127cdb602d873595e5025`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 481.8 KB (481766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fe14aad69cad6f3b684a444d186a2cdf856de82e623eb56a4aba5548d9a224`  
		Last Modified: Thu, 09 Apr 2026 22:27:06 GMT  
		Size: 403.7 MB (403715986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff206674a0625e104dc5b8814425e71cbb9fcfa189e06f4f82c150521cf85d`  
		Last Modified: Thu, 09 Apr 2026 22:26:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed06373ee96815d446889f0e106823d238aafe97290113b2e6da75706bd373f`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dcfcdb41101194acdd859400380c7621589462315903d9afb767a864cd0ded`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76674ac897af088337ca0fb6e4ca31a94df26afa66f029295e5bad9b36e7292b`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9968375774f9b0c9a8e81263f05bec08546d9e01bbdee456a50bfef1972a0a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1011c0dadb8a9b1aa88144194ede95988bb33cec97ed503576270012b260ed67`

```dockerfile
```

-	Layers:
	-	`sha256:9481575ab59927b71e3bdc921c1ca707e15d251ee70a5508224c2b47db68f9c7`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 70.0 MB (69986879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07874adf8ffcaa4965cafe0a8b49422f9ae6a066aa4aa3263d78f229d41a8ebe`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c7c23aa7568963c03515f23e29ad49fe680968a5ee2c8cba24c067091bbac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.4 MB (701429390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de75c983129a92e56e2c9432656a28c8a9dbd1f47c4e9e73ad99b01f0a281392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:36 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:25:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf5ca75919c1363ba6ff93737daef5e90d636e7761428d8fc08da995b96ab8`  
		Last Modified: Thu, 09 Apr 2026 22:28:47 GMT  
		Size: 254.2 MB (254211656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54893e61957e389e7db6a46f41244f4fbcfe553be7cf55afe18a53da39900ab`  
		Last Modified: Thu, 09 Apr 2026 22:28:34 GMT  
		Size: 14.3 MB (14340986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d72a79263be7fc15b55734f076359b3feb714e06f8191773d6499182d97536`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 481.8 KB (481768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1779a68e379365151155243bceaf57301a49a1a49923b766464d9d128a8be43d`  
		Last Modified: Thu, 09 Apr 2026 22:28:51 GMT  
		Size: 403.5 MB (403518466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612a65a30045f6abfb9d3fa22c2e06a7c987d7b60603acde2002f3110d2b5f0`  
		Last Modified: Thu, 09 Apr 2026 22:28:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df9541de98e12c12ba7a96f89909048fe75b85c28bcbb1694b64df650fb845`  
		Last Modified: Thu, 09 Apr 2026 22:28:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e872554e4447d8dfa9251f6b94c0c14b5a1e02ff62515a69d180a19557d525`  
		Last Modified: Thu, 09 Apr 2026 22:28:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef1ccc6564d1d5881d5325fb388320cb0828c190296f2a75ffc71d8a99d27f`  
		Last Modified: Thu, 09 Apr 2026 22:28:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d2dccbd76adae86e7013728c98be82f802e2cb0212120030c7588ffe162aacf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f9420716d0e0e3cbea9cf90eb25e84a3b762954774995b27e3d2726110b169`

```dockerfile
```

-	Layers:
	-	`sha256:a0687c05e9aba8dc3566d2b8a87ddb1167111078eebbdafd27d3835a357e1bf2`  
		Last Modified: Thu, 09 Apr 2026 22:28:39 GMT  
		Size: 70.0 MB (69994166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942ddde8ba548ef3787f2f685202dd0e1af02d021d492f8b8c83b361df288630`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d99c8452344fae6c66fb0ae6fc427236652459f4d770cb541bcfbc803f05e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.7 MB (721675575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500b9adfd00baea5fb031cffa2d6d90c9fbae5496c83e51e4adae8173d0f295e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 23:41:25 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:28 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27157e3fb6d3ac05979ecf688cdf0f6aee136d53cf986e94e4437f9562e1c19`  
		Last Modified: Thu, 09 Apr 2026 23:47:28 GMT  
		Size: 404.2 MB (404247038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7ea05369d5e150735c7c811dbd33599d8454d6f0572a0b93e3bb75fa803d4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae81cf2a2cde4f3ee39e47239416e6671f631dbf4087028cf3b96bde66e3bf4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ada916bcdbbb36bfda1c8af8a31ceb37e185e58bd5b3e37c4240a5616db4c`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237261e06badfa7b6274d0a01c72e2b465e0efa8ad13bf8af4c0ef24f4d8996`  
		Last Modified: Thu, 09 Apr 2026 23:47:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0402678e8e587bda5d36714b5166198cf2e61910b2a9a02d4f5edebe84bdae30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e5a11c0def144d25bc7e2d898335c279b3f316738d94209dad35789ff66f5`

```dockerfile
```

-	Layers:
	-	`sha256:e0125d8699b92dae9ca782f344b4cbc90fb37c88071c0d2a7f0d9310fb44d488`  
		Last Modified: Thu, 09 Apr 2026 23:47:22 GMT  
		Size: 70.0 MB (69995268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f098b82d33e3aff0819e0a00ab51a9c518006e7f0d981c94a7a8789addad5073`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260409`

```console
$ docker pull odoo@sha256:6eb3573f6486599e3c88626cb3eef00852fe6e4f814d9622ac9bde8105fbebab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260409` - linux; amd64

```console
$ docker pull odoo@sha256:79b2ef63f1848ec4d670c67a3b7b8c5ae9aaf973500324f6da2e1bd07c2d4808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.3 MB (705252815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4303fb5446af5ce9ce52d54422e3129c2608308ab5e5a95db593c398c12af41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:25 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:25 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:24:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9677a3f60ed82918a2b05f2480dfa892c951f69986d8f55220b20838def8fc`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 257.0 MB (256958760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8d89584f97bfd850a90d36dc925acee6f4fea5df93e4f8383246c1e4a6440`  
		Last Modified: Thu, 09 Apr 2026 22:26:53 GMT  
		Size: 14.4 MB (14360407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8fda1794311c23d7f7e240cd018b1e9fa41ef64b127cdb602d873595e5025`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 481.8 KB (481766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fe14aad69cad6f3b684a444d186a2cdf856de82e623eb56a4aba5548d9a224`  
		Last Modified: Thu, 09 Apr 2026 22:27:06 GMT  
		Size: 403.7 MB (403715986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff206674a0625e104dc5b8814425e71cbb9fcfa189e06f4f82c150521cf85d`  
		Last Modified: Thu, 09 Apr 2026 22:26:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed06373ee96815d446889f0e106823d238aafe97290113b2e6da75706bd373f`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dcfcdb41101194acdd859400380c7621589462315903d9afb767a864cd0ded`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76674ac897af088337ca0fb6e4ca31a94df26afa66f029295e5bad9b36e7292b`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:9968375774f9b0c9a8e81263f05bec08546d9e01bbdee456a50bfef1972a0a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1011c0dadb8a9b1aa88144194ede95988bb33cec97ed503576270012b260ed67`

```dockerfile
```

-	Layers:
	-	`sha256:9481575ab59927b71e3bdc921c1ca707e15d251ee70a5508224c2b47db68f9c7`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 70.0 MB (69986879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07874adf8ffcaa4965cafe0a8b49422f9ae6a066aa4aa3263d78f229d41a8ebe`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260409` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c7c23aa7568963c03515f23e29ad49fe680968a5ee2c8cba24c067091bbac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.4 MB (701429390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de75c983129a92e56e2c9432656a28c8a9dbd1f47c4e9e73ad99b01f0a281392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:36 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:25:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf5ca75919c1363ba6ff93737daef5e90d636e7761428d8fc08da995b96ab8`  
		Last Modified: Thu, 09 Apr 2026 22:28:47 GMT  
		Size: 254.2 MB (254211656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54893e61957e389e7db6a46f41244f4fbcfe553be7cf55afe18a53da39900ab`  
		Last Modified: Thu, 09 Apr 2026 22:28:34 GMT  
		Size: 14.3 MB (14340986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d72a79263be7fc15b55734f076359b3feb714e06f8191773d6499182d97536`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 481.8 KB (481768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1779a68e379365151155243bceaf57301a49a1a49923b766464d9d128a8be43d`  
		Last Modified: Thu, 09 Apr 2026 22:28:51 GMT  
		Size: 403.5 MB (403518466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612a65a30045f6abfb9d3fa22c2e06a7c987d7b60603acde2002f3110d2b5f0`  
		Last Modified: Thu, 09 Apr 2026 22:28:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df9541de98e12c12ba7a96f89909048fe75b85c28bcbb1694b64df650fb845`  
		Last Modified: Thu, 09 Apr 2026 22:28:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e872554e4447d8dfa9251f6b94c0c14b5a1e02ff62515a69d180a19557d525`  
		Last Modified: Thu, 09 Apr 2026 22:28:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef1ccc6564d1d5881d5325fb388320cb0828c190296f2a75ffc71d8a99d27f`  
		Last Modified: Thu, 09 Apr 2026 22:28:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:d2dccbd76adae86e7013728c98be82f802e2cb0212120030c7588ffe162aacf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f9420716d0e0e3cbea9cf90eb25e84a3b762954774995b27e3d2726110b169`

```dockerfile
```

-	Layers:
	-	`sha256:a0687c05e9aba8dc3566d2b8a87ddb1167111078eebbdafd27d3835a357e1bf2`  
		Last Modified: Thu, 09 Apr 2026 22:28:39 GMT  
		Size: 70.0 MB (69994166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942ddde8ba548ef3787f2f685202dd0e1af02d021d492f8b8c83b361df288630`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260409` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d99c8452344fae6c66fb0ae6fc427236652459f4d770cb541bcfbc803f05e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.7 MB (721675575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500b9adfd00baea5fb031cffa2d6d90c9fbae5496c83e51e4adae8173d0f295e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 23:41:25 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:28 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27157e3fb6d3ac05979ecf688cdf0f6aee136d53cf986e94e4437f9562e1c19`  
		Last Modified: Thu, 09 Apr 2026 23:47:28 GMT  
		Size: 404.2 MB (404247038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7ea05369d5e150735c7c811dbd33599d8454d6f0572a0b93e3bb75fa803d4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae81cf2a2cde4f3ee39e47239416e6671f631dbf4087028cf3b96bde66e3bf4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ada916bcdbbb36bfda1c8af8a31ceb37e185e58bd5b3e37c4240a5616db4c`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237261e06badfa7b6274d0a01c72e2b465e0efa8ad13bf8af4c0ef24f4d8996`  
		Last Modified: Thu, 09 Apr 2026 23:47:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:0402678e8e587bda5d36714b5166198cf2e61910b2a9a02d4f5edebe84bdae30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e5a11c0def144d25bc7e2d898335c279b3f316738d94209dad35789ff66f5`

```dockerfile
```

-	Layers:
	-	`sha256:e0125d8699b92dae9ca782f344b4cbc90fb37c88071c0d2a7f0d9310fb44d488`  
		Last Modified: Thu, 09 Apr 2026 23:47:22 GMT  
		Size: 70.0 MB (69995268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f098b82d33e3aff0819e0a00ab51a9c518006e7f0d981c94a7a8789addad5073`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:6eb3573f6486599e3c88626cb3eef00852fe6e4f814d9622ac9bde8105fbebab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:79b2ef63f1848ec4d670c67a3b7b8c5ae9aaf973500324f6da2e1bd07c2d4808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.3 MB (705252815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4303fb5446af5ce9ce52d54422e3129c2608308ab5e5a95db593c398c12af41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:23:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:23:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:23:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:23:25 GMT
ARG TARGETARCH=amd64
# Thu, 09 Apr 2026 22:23:25 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:23:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:23:36 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:24:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:24:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:24:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:24:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:24:43 GMT
USER odoo
# Thu, 09 Apr 2026 22:24:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:24:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9677a3f60ed82918a2b05f2480dfa892c951f69986d8f55220b20838def8fc`  
		Last Modified: Thu, 09 Apr 2026 22:27:03 GMT  
		Size: 257.0 MB (256958760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8d89584f97bfd850a90d36dc925acee6f4fea5df93e4f8383246c1e4a6440`  
		Last Modified: Thu, 09 Apr 2026 22:26:53 GMT  
		Size: 14.4 MB (14360407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8fda1794311c23d7f7e240cd018b1e9fa41ef64b127cdb602d873595e5025`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 481.8 KB (481766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fe14aad69cad6f3b684a444d186a2cdf856de82e623eb56a4aba5548d9a224`  
		Last Modified: Thu, 09 Apr 2026 22:27:06 GMT  
		Size: 403.7 MB (403715986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff206674a0625e104dc5b8814425e71cbb9fcfa189e06f4f82c150521cf85d`  
		Last Modified: Thu, 09 Apr 2026 22:26:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed06373ee96815d446889f0e106823d238aafe97290113b2e6da75706bd373f`  
		Last Modified: Thu, 09 Apr 2026 22:26:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dcfcdb41101194acdd859400380c7621589462315903d9afb767a864cd0ded`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76674ac897af088337ca0fb6e4ca31a94df26afa66f029295e5bad9b36e7292b`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9968375774f9b0c9a8e81263f05bec08546d9e01bbdee456a50bfef1972a0a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1011c0dadb8a9b1aa88144194ede95988bb33cec97ed503576270012b260ed67`

```dockerfile
```

-	Layers:
	-	`sha256:9481575ab59927b71e3bdc921c1ca707e15d251ee70a5508224c2b47db68f9c7`  
		Last Modified: Thu, 09 Apr 2026 22:26:56 GMT  
		Size: 70.0 MB (69986879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07874adf8ffcaa4965cafe0a8b49422f9ae6a066aa4aa3263d78f229d41a8ebe`  
		Last Modified: Thu, 09 Apr 2026 22:26:52 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c7c23aa7568963c03515f23e29ad49fe680968a5ee2c8cba24c067091bbac0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.4 MB (701429390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de75c983129a92e56e2c9432656a28c8a9dbd1f47c4e9e73ad99b01f0a281392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 22:24:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 22:24:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 22:24:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 22:24:36 GMT
ARG TARGETARCH=arm64
# Thu, 09 Apr 2026 22:24:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 22:24:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 22:24:49 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 22:24:49 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 22:25:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 22:25:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 22:25:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 22:25:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 22:25:57 GMT
USER odoo
# Thu, 09 Apr 2026 22:25:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf5ca75919c1363ba6ff93737daef5e90d636e7761428d8fc08da995b96ab8`  
		Last Modified: Thu, 09 Apr 2026 22:28:47 GMT  
		Size: 254.2 MB (254211656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54893e61957e389e7db6a46f41244f4fbcfe553be7cf55afe18a53da39900ab`  
		Last Modified: Thu, 09 Apr 2026 22:28:34 GMT  
		Size: 14.3 MB (14340986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d72a79263be7fc15b55734f076359b3feb714e06f8191773d6499182d97536`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 481.8 KB (481768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1779a68e379365151155243bceaf57301a49a1a49923b766464d9d128a8be43d`  
		Last Modified: Thu, 09 Apr 2026 22:28:51 GMT  
		Size: 403.5 MB (403518466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7612a65a30045f6abfb9d3fa22c2e06a7c987d7b60603acde2002f3110d2b5f0`  
		Last Modified: Thu, 09 Apr 2026 22:28:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df9541de98e12c12ba7a96f89909048fe75b85c28bcbb1694b64df650fb845`  
		Last Modified: Thu, 09 Apr 2026 22:28:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e872554e4447d8dfa9251f6b94c0c14b5a1e02ff62515a69d180a19557d525`  
		Last Modified: Thu, 09 Apr 2026 22:28:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef1ccc6564d1d5881d5325fb388320cb0828c190296f2a75ffc71d8a99d27f`  
		Last Modified: Thu, 09 Apr 2026 22:28:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d2dccbd76adae86e7013728c98be82f802e2cb0212120030c7588ffe162aacf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f9420716d0e0e3cbea9cf90eb25e84a3b762954774995b27e3d2726110b169`

```dockerfile
```

-	Layers:
	-	`sha256:a0687c05e9aba8dc3566d2b8a87ddb1167111078eebbdafd27d3835a357e1bf2`  
		Last Modified: Thu, 09 Apr 2026 22:28:39 GMT  
		Size: 70.0 MB (69994166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942ddde8ba548ef3787f2f685202dd0e1af02d021d492f8b8c83b361df288630`  
		Last Modified: Thu, 09 Apr 2026 22:28:33 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d99c8452344fae6c66fb0ae6fc427236652459f4d770cb541bcfbc803f05e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.7 MB (721675575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500b9adfd00baea5fb031cffa2d6d90c9fbae5496c83e51e4adae8173d0f295e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 23:38:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 09 Apr 2026 23:38:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 09 Apr 2026 23:38:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Apr 2026 23:38:16 GMT
ARG TARGETARCH=ppc64le
# Thu, 09 Apr 2026 23:38:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 09 Apr 2026 23:38:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 09 Apr 2026 23:38:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_RELEASE=20260409
# Thu, 09 Apr 2026 23:38:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Thu, 09 Apr 2026 23:41:25 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 09 Apr 2026 23:41:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 09 Apr 2026 23:41:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 09 Apr 2026 23:41:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 09 Apr 2026 23:41:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 09 Apr 2026 23:41:28 GMT
USER odoo
# Thu, 09 Apr 2026 23:41:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 09 Apr 2026 23:41:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e401337cc322eedc2eeb0580259cb74b1431988b911d7484179e584598f66274`  
		Last Modified: Thu, 09 Apr 2026 23:45:58 GMT  
		Size: 267.7 MB (267737273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330b1c720f1dab439d1594ab26d0d75a287eda2ec3a33b74914c7a95d6b8dab`  
		Last Modified: Thu, 09 Apr 2026 23:45:47 GMT  
		Size: 14.9 MB (14893744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc109024b9ccf1316b8e2e30656c5ed5bd615ec729109700e8127db4485098`  
		Last Modified: Thu, 09 Apr 2026 23:45:46 GMT  
		Size: 481.7 KB (481745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27157e3fb6d3ac05979ecf688cdf0f6aee136d53cf986e94e4437f9562e1c19`  
		Last Modified: Thu, 09 Apr 2026 23:47:28 GMT  
		Size: 404.2 MB (404247038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7ea05369d5e150735c7c811dbd33599d8454d6f0572a0b93e3bb75fa803d4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae81cf2a2cde4f3ee39e47239416e6671f631dbf4087028cf3b96bde66e3bf4`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ada916bcdbbb36bfda1c8af8a31ceb37e185e58bd5b3e37c4240a5616db4c`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d237261e06badfa7b6274d0a01c72e2b465e0efa8ad13bf8af4c0ef24f4d8996`  
		Last Modified: Thu, 09 Apr 2026 23:47:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:0402678e8e587bda5d36714b5166198cf2e61910b2a9a02d4f5edebe84bdae30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e5a11c0def144d25bc7e2d898335c279b3f316738d94209dad35789ff66f5`

```dockerfile
```

-	Layers:
	-	`sha256:e0125d8699b92dae9ca782f344b4cbc90fb37c88071c0d2a7f0d9310fb44d488`  
		Last Modified: Thu, 09 Apr 2026 23:47:22 GMT  
		Size: 70.0 MB (69995268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f098b82d33e3aff0819e0a00ab51a9c518006e7f0d981c94a7a8789addad5073`  
		Last Modified: Thu, 09 Apr 2026 23:47:18 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
