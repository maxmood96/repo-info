## `odoo:latest`

```console
$ docker pull odoo@sha256:a547953da01ebbc81643be61ad5deee2bd0051b963f89ebaf983da15226aa6d0
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
$ docker pull odoo@sha256:3bc6d6bf6224bc097a705c4d2905824e105efbd854d0de7a8c008c01576852bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.8 MB (665761275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f799527e2bd6f8d3580c44f985c2eb13fef29a83470c38f846cd86c33d167259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d4f3c37ee8c8cd4f16437a8e1efc4c02b17f3879151e2f0c40baf1ccf0b01b`  
		Last Modified: Wed, 15 Jan 2025 20:32:42 GMT  
		Size: 254.5 MB (254515407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1583cd1bd81f938057cdcc9bf8a5b81bdda563d440bab2c1210e6c3f83cc68`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 14.2 MB (14231187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75d22c8f8037a74816c0da373f35df336f72a785f2b2578e8baf9c26282cf7`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 485.8 KB (485773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f630fa1de8ed9e0b2cf2619eb82c27f34965293378c0bd43e25101b7c88970`  
		Last Modified: Wed, 15 Jan 2025 20:32:45 GMT  
		Size: 366.8 MB (366774502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d3d19fa96b20b2664e80464dce895b03ce6fba2d8e027eda90eb99830ec81`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e5f17843f510dfab7af49c284270a17445f472a81c85169a00e5143db0f6c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5b0d5d644c44ec897ba083e23ca6f2a9a1ac72021119ca8ec34c1d73a11e`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bad202dba96f5d0c3641e77fc541cbf37cec4384d36835edf3e5df780da08c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2e58b4d6f3c5accde02163c933b57ce50d33012651333605abab18b8d2d5bb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58396083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd78a039d8f37339b3109cfeb44448a7798eda508f2f31276765662860eb7b7`

```dockerfile
```

-	Layers:
	-	`sha256:73fa6a9bff23ad7edbe125c695020e1648cc56af28aaf8de7220be77f50344c5`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 58.4 MB (58368947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe9a3b3d4abf003516f872ab11ff8e65c532c01dd4d579096f971cba7f3163`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29244f05b35308e6b0dcc11a74f394b80097a4b72c828beadcd783dcdcf11194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 MB (662290322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cc35601dc86e58a2140f16f592500147d92a91abe6e55a765712633f3ff6df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=arm64
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db86ce3dd26b502fae6356f1be60d20f60bca1257b178d439b027dd3d1551e8`  
		Last Modified: Thu, 23 Jan 2025 19:12:22 GMT  
		Size: 366.8 MB (366762952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc2a74806b232f6c02e473854dd4b67b0f3df220feb3ec6159234556ba688e`  
		Last Modified: Thu, 23 Jan 2025 19:12:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e19f402f1113207312deb900ba4cd2d014644efb8c400558900d0283c5b090`  
		Last Modified: Thu, 23 Jan 2025 19:12:21 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa11488a63d584ccad9cf0cf01eeecf6374787cd959fb75d0d5e0c9f8ab312`  
		Last Modified: Thu, 23 Jan 2025 19:12:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e181922030ccc2bec60dd5227083af70ef9853bb81db3ea8a848a6501baaa8a8`  
		Last Modified: Thu, 23 Jan 2025 19:12:18 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9da8fbd404ec6c26419b2701a384c9cabc9fe5c74903c5e93119c6bc8c6aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58423432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee151e4feb6ba7bca0095c696c64e8a86f5a5b47000f65526c4b70c9740e3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:0c05270638dd0a3ea03ca8574027da77a052eb512f3ca81c0100daf17ce2db81`  
		Last Modified: Thu, 23 Jan 2025 19:12:15 GMT  
		Size: 58.4 MB (58396132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b28159976b0b036069f5e558914a334f2497bd1993291ccaa87ccfa029d5723`  
		Last Modified: Thu, 23 Jan 2025 19:12:13 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:f7dec6e90a76beb82e54e21b2ee5e8c41cce7f3d09596dcad1b1216d5e8d4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.2 MB (682198668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c543545e2f6ce3c4072185d911b2e440dc50210525a043333c9fdd8b2bee9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 09:24:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jan 2025 09:24:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Jan 2025 09:24:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_VERSION=18.0
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_RELEASE=20250123
# Thu, 23 Jan 2025 09:24:41 GMT
ARG ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250123 ODOO_SHA=b455a34a4c6e7d7325d1a5c6033d04c2f9b2810f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jan 2025 09:24:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 23 Jan 2025 09:24:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jan 2025 09:24:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 23 Jan 2025 09:24:41 GMT
USER odoo
# Thu, 23 Jan 2025 09:24:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2025 09:24:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca86fa2495de7cdd13fac0b048f953ea403243242c7c29b21193f3f3e6cbd72`  
		Last Modified: Thu, 23 Jan 2025 18:33:51 GMT  
		Size: 367.5 MB (367455965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c6daff8c8e8af849f8d909e99e4734669fa1a1b780d82f78599281064bb3f`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6883ffaa3307bb091332b5f1e9a37e18d13feb0eb673a4509d8403ad4cdaddb`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334934d145a22292a420dd908b841d2fae1d68d7fb65a7f5087d73912abc67fc`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831a255fc926f8c449d4e06ca65fdedbe2034d7db0e1a61b9194bf68090a9e6`  
		Last Modified: Thu, 23 Jan 2025 18:33:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:34d060256482cc498352e732aff4b950df314764b091fbb3dfb682a66582a9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58424202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3226f58de0c39291f7bea03d567d75a377e916614b9055141e5ed92846edaa`

```dockerfile
```

-	Layers:
	-	`sha256:16dbc78fb2a481f1dc2f5b22d98c44bb9fa7a4909357bfdbec935e15fda8295b`  
		Last Modified: Thu, 23 Jan 2025 18:33:28 GMT  
		Size: 58.4 MB (58397004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ad14f054bba01aed51ca9bc58c55721c30d9644fc87fbb87de9494a1c0172b`  
		Last Modified: Thu, 23 Jan 2025 18:33:26 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
