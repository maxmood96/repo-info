## `odoo:latest`

```console
$ docker pull odoo@sha256:c2ca98aef0ae99edbf9aadb35fe76b722a67607ea2cfdde8bb67304d21ba0705
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
$ docker pull odoo@sha256:8cffb46374ee8739b24fdfdc2d7cfb883d22c5705a46de413a238be49b96b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.9 MB (651869767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b2a73543257c065a7972b5280a4c659bf14846ad877ef3be9b112fb43502d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aae7ac0bfc0a6872e8969f199f134828f8b4dd51e0a07ca4f1bc4d81a32b38`  
		Last Modified: Wed, 16 Oct 2024 16:17:38 GMT  
		Size: 255.6 MB (255640144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e81a1e55bf84da6b59d98930228b4b95602851f8de4f94d293ac02d995306`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 14.1 MB (14142300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea893cee06623227ecf4ce3a79b60e25ce6610fb492df8cdbfb2712c4e41fc`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 472.4 KB (472362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a979d7246f111af62240c5bc27535061f30444300f0c1e816739fe055123f`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 351.9 MB (351862162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584808ad4aec1e455091f97c00db8b23c106db47f4fe4b6b0460bb4e99aeab`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a14f09b3a5520acd27b73266e5fe1689e5c7a9bef3a92df201c952d9824ff7`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6d64626a8b13a1068dddd36a6aab54510c89d741e6fe3d7b3a2e0f2895821`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae567b4dc9699a7e7ef77643946e0e4036062cb508eeb5c1a9c4685c6db4e07`  
		Last Modified: Wed, 16 Oct 2024 16:17:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5bcc34aa8b05e2bf812e6d6940b87247f099d7804a745dcf60a06c2c138a3e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55458329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d324599cec8f86d92586f9e49563ca19ce14e83413b2c89a386f1ba5fc5d99f`

```dockerfile
```

-	Layers:
	-	`sha256:7128d76a457b0160c1b146fc57891d0701a4bc9c726f867d7883adb73acede73`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 55.4 MB (55431410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abba925dadde0910083173c3a852324cc585c3bc169a69fd6fed7fe1441d2d3`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8913c75bd3dc6e67d8431dee9d04a6448959eed23595ce4a158a628e9dc15b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 MB (648197509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af9685a139ad32ae45805f42b3961d0e648dc1c98c0a672bd33a2be01351880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f2ad32ab69058157eb9f48b389a68262192a44a447caa6e9a96c5180bcfc2c`  
		Last Modified: Wed, 16 Oct 2024 04:02:37 GMT  
		Size: 253.0 MB (252999920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926486042f16a6a923c24027c10f3c2d2689a0db8a32b06c4399917e1e81bd6`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 14.1 MB (14115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bf12eebe020f34f21d46aafe4e3f4eceaf72d4afa3f442408799cf1f9425b`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 472.5 KB (472451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f846a6fc22fa6c4793cd243587638dc80327e57c99fecc60f28137ee0be11e9`  
		Last Modified: Wed, 16 Oct 2024 04:02:38 GMT  
		Size: 351.7 MB (351721110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07e4f294cc4a6465b993dbd7414dec1c014eb35153f3c478cc146397c7e9fbb`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e089f1a16afe87fd0ab113d21c94389129bab9b5c6fb02b52ec1e165db283`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca584cd714316a6c6a591fba9dfb5f498148da60df3bbcd858e2025ea58f8`  
		Last Modified: Wed, 16 Oct 2024 04:02:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4473992f5a5868ca9fdfcf222827bff9f51a7f4aa8daef9b59be5da4e11f4af`  
		Last Modified: Wed, 16 Oct 2024 04:02:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:48393e90ddaea262e76ad8f90481194a3305f64d2eca28e190fafcb4aa11741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8008686d2770e1e233a5dd123571bb20f6b207554fb199e21c8d160a1bdf39`

```dockerfile
```

-	Layers:
	-	`sha256:5eff6ae8306c07bacbd54720d9fbed079e3ec25611163e4d0ef6550d34749edc`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 55.4 MB (55438704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb57283523a7623245dd547c2e3b372e5b1b870c16cfc574263911e68293589`  
		Last Modified: Wed, 16 Oct 2024 04:02:30 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:10442ed383762169b4ee0554404cfe302a3ded056110a48687f471f4982a1280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.8 MB (670839250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e02133cade047be397a6a233b84134167c898e2ff7458a05f9bdeaed2218f9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Oct 2024 13:36:11 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Oct 2024 13:36:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
USER odoo
# Thu, 17 Oct 2024 13:36:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Oct 2024 13:36:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037c9b6d0c0632f5a24e8da67e2f7e0d54ab235bed1c95eaee7a713c81615c8`  
		Last Modified: Wed, 16 Oct 2024 02:26:33 GMT  
		Size: 266.4 MB (266405623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de43aba2291bddb140de3a8e00b78e9ff7f35c14f793e402c5360c40881388`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 14.7 MB (14686074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a8f06768eea9b11c0a1791df7a689ff8ceaf74ed2fdc4dfe0a2aa0f0b417a`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 472.4 KB (472411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c744076a904f296dbdea75acf29826fc0393653a790298d174edc8df37cff50`  
		Last Modified: Thu, 17 Oct 2024 21:07:22 GMT  
		Size: 354.9 MB (354883735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843bbe0207f98896ae33e0d7b9837b89149ff52bc01a13ddc7c4614f1f640e76`  
		Last Modified: Thu, 17 Oct 2024 21:07:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da43babdd763055c8210c5fa38764599174acb82c67c50d9ca980c39af55e359`  
		Last Modified: Thu, 17 Oct 2024 21:07:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25f412dc466be57ddf241dce6e5e162ce74bcb73fa3506716fd7bae9d48553`  
		Last Modified: Thu, 17 Oct 2024 21:07:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc2264934ce6f7be0c783d54324fca51ade382e2b225c7ef0febdf7cf1b9623`  
		Last Modified: Thu, 17 Oct 2024 21:07:14 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:91ed3a4a3779ad7b5df6d3354c8884b3df1928c4ee6a1dccea7578d95b7de2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55510495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b4d8561c4255836064ef3478ab667254437790d924ebd73d63aca44318b62a`

```dockerfile
```

-	Layers:
	-	`sha256:c253ded6ea9a5b1ef4bdcf8ba0fd471e8461ec33b713c0014a071b1294ce673d`  
		Last Modified: Thu, 17 Oct 2024 21:07:15 GMT  
		Size: 55.5 MB (55483521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88363c7321ffbe5740d58f6779c299c44d69bc4d18d1667b3f7fd78e5ce38282`  
		Last Modified: Thu, 17 Oct 2024 21:07:13 GMT  
		Size: 27.0 KB (26974 bytes)  
		MIME: application/vnd.in-toto+json
