## `odoo:latest`

```console
$ docker pull odoo@sha256:ce162277d5d4c5749a0095f7bac4fffb7945f5cc94b666edbe7a43e2742fa1ab
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
$ docker pull odoo@sha256:44c9d6655704b4c808bfd7afc53552ca1119498c09e8c7ab0fbc600f412064bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.3 MB (661320497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01f61490654912d47a1dea92186b0ed4d025f65ffd660805a456a01f229bf19`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=amd64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c811f2769f5655f1b553436e1bd4ac7dbafb67fbfa24cf633f447496859e2`  
		Last Modified: Mon, 18 Nov 2024 19:08:52 GMT  
		Size: 254.5 MB (254518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c211ec785169346e1360589fc3e4f43e0afda8c2b4a4f9d4c3a44ec0952f17dc`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 14.2 MB (14229406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33fdea272cf641940b9da8ee256cf315556e27f5bcd2b7db3a90cbd0ab183d`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 469.7 KB (469720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f829bc51b2b5cb60228763f1e0b9fc104c07db459f40a7be09cefd11632cc732`  
		Last Modified: Mon, 18 Nov 2024 19:08:51 GMT  
		Size: 362.3 MB (362348225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c98ea5d4950ff0c3cf61e178ea96ea1d1f1c430674c9f9402d874a2e239766`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d68fec9796cc057fd575122afc4ecb3bd22775f8446b7b148ef9ad7573296`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a928543ef7a3ff998ebad925a3d67a110b89cb1da8e4c4b3ae2628b1e5eb3c`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5124a8beecc6f7906280bb4a2fedec2399c912d20445f93064ee9623d2fbafd0`  
		Last Modified: Mon, 18 Nov 2024 19:08:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:61e153527ed10347ea03987a880c29d759024dbf48dc44aa245774978ec4ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d11b46d10f0f18795facc88857c97241e49093681f8a94d332b1f95d1c315`

```dockerfile
```

-	Layers:
	-	`sha256:080368baa645d2e98594a7adb727369dd50165f521745d7e3fb02c6a840a38b3`  
		Last Modified: Mon, 18 Nov 2024 19:08:47 GMT  
		Size: 57.1 MB (57134158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a78ecc4869b1944b966abb6bd3ab8b9c2b4b51ca594e35944aeb6219dc817e`  
		Last Modified: Mon, 18 Nov 2024 19:08:46 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:17ef06bac5f5c6cf4b557407cce807a805b1aeb9943a51a58128314404ae6703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 MB (657715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb7453482fb703c5d73f9b33900550c000766c828805ea2de8dbcf6b1ccc199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 18 Nov 2024 09:26:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 18 Nov 2024 09:26:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 09:26:19 GMT
ARG TARGETARCH=arm64
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_VERSION=18.0
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_RELEASE=20241118
# Mon, 18 Nov 2024 09:26:19 GMT
ARG ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241118 ODOO_SHA=1b907c8c28df9e8e1ef0593b995e8c3408c65c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 18 Nov 2024 09:26:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 18 Nov 2024 09:26:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 18 Nov 2024 09:26:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 18 Nov 2024 09:26:19 GMT
USER odoo
# Mon, 18 Nov 2024 09:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Nov 2024 09:26:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587d98cf945cc8b8cb28976463626a968b75cfb85a7bc134788ca4acf3a2f07`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 251.9 MB (251945445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea938de0828dade1c18a83a12fb524e0eee9b0c70216313f5a11e1971311d3`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 14.2 MB (14202621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236ec3799ba5acb8613b5e789989e4eb51b91db56eac165301dd71ba9e697ac`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
		Size: 469.7 KB (469730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae744a10d78391b1110f44e4e2585783da7a29067fb0718b3b2398655b48f9`  
		Last Modified: Mon, 18 Nov 2024 19:39:38 GMT  
		Size: 362.2 MB (362202828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded0787ed2f89bc64a24e6a27e302391658fbaf6b5758fcb73113bb9098ffae`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4327210ce516c942bc9b45b3cf3d8c0c47495a2ddd46d950bb165bfebbf85`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b109be8ba62f57b86d0d64e12414ef04fe07e87e1955f307a974563a720b34d`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f03ff1ae92dbbe58ca9e9db750bc1ece93c801371abec4f4e39ad61dc26ca8`  
		Last Modified: Mon, 18 Nov 2024 19:39:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:80080bd49bf069e36c65c2bca225f09a9d2c99d026aaf0cb2281e2abdf8fa818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57168756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823669a151334d2bc22dce408fc214ffc70f433048525f44a99cd7b94cd135a2`

```dockerfile
```

-	Layers:
	-	`sha256:d9ee007c2e5beb374719cac79457babe810a21a7602b732f62766779bfd2da01`  
		Last Modified: Mon, 18 Nov 2024 19:39:30 GMT  
		Size: 57.1 MB (57141456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31beb1a3516f7fdd51d49d2668fb6e177ff01104b86bafc07eddbb6868b014cf`  
		Last Modified: Mon, 18 Nov 2024 19:39:28 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:340a5bf63bc2fc3aa0663cc2699208ac14cd208ff8ce241157c3ee3587300af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673485802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72209b810e7c03a90e1302d1cdf65519f21a851ce1bae5a680ace7feb1efb09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH=ppc64le
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=18.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Nov 2024 10:31:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Nov 2024 10:31:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
USER odoo
# Fri, 08 Nov 2024 10:31:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Nov 2024 10:31:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ece3150b789ddce6e306870839a2059e2166b1c870f50ce72bb0f64f7afb0`  
		Last Modified: Sat, 16 Nov 2024 03:26:15 GMT  
		Size: 265.1 MB (265135565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a057cad9c1029c466b8b4485c7e9959db3377ccb15d544d27fa01baa45706`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 14.8 MB (14775605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086a5a3d25f4fd37742c7ca85a30675397dbfa6a99c4be7c0ab236712db1ef5`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 469.7 KB (469725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce447a254bc792745bb555d659b8570eb45b78857c9f33c10c4385ec6adff9c`  
		Last Modified: Sat, 16 Nov 2024 03:26:20 GMT  
		Size: 358.7 MB (358713640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf14132444dbbc50de4ebe2ce68febb45bf5ec43727376dbc4efa0cb071610`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06809f175fbe14aa96cedf61d4c9d32eff7a34b7f55f84824d98236b7797241a`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12b23d972c03b0aa31bf060e706565ec93ad2b360dda1bda5356f1f9a2d513`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a1aa9136a4acf671cfeaed4605678bf84aac4926c2c1077f5b416112623060`  
		Last Modified: Sat, 16 Nov 2024 03:25:57 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9899f7a6f770a2b964a449814007a151172779306701c5012d102904792c9b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56244134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42dc5c9cc4536282e7cecf3a21cb3636a2ae5daa2cc734c243207301340c013`

```dockerfile
```

-	Layers:
	-	`sha256:d0218e9110853cc6bbc61f6c3dc242ae94dcbe9b3316f39f86e6fa8499e56cd0`  
		Last Modified: Sat, 16 Nov 2024 03:25:56 GMT  
		Size: 56.2 MB (56216936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874e08d8c63b2defede13b4a514fa7b34609d35445469b3a1599e8546c4abc76`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
