## `odoo:latest`

```console
$ docker pull odoo@sha256:507db31947781213279f6dfa45fc3ca1743a614559c137462c02129a0fde3a98
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
$ docker pull odoo@sha256:9482cc5899cae5bc5d80db544fd3adaf748afc299ec93a20fe155bfd1bc0d9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.1 MB (657145483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87060708396a04cc8cff7407619ea7542330ec2c90560715198b05e377b972a`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH=amd64
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=18.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf0467a4651e565d4f2552e800855021bb0621464b7c5cea079b3210abbfb24`  
		Last Modified: Sat, 16 Nov 2024 03:00:11 GMT  
		Size: 254.5 MB (254514719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e890072b6ba5717918e218949776c54aaad8b50dd2b968487537484a4bc9619`  
		Last Modified: Sat, 16 Nov 2024 03:00:08 GMT  
		Size: 14.2 MB (14229362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a678965c778880fac8ce912668f8ebe065829382cc0a746371ac46a9eb62030f`  
		Last Modified: Sat, 16 Nov 2024 03:00:07 GMT  
		Size: 469.7 KB (469732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf1637a3ec2f38f2f5393c3da5254b9b50841b21c6d8a5626cbc13b630dce5`  
		Last Modified: Sat, 16 Nov 2024 03:00:12 GMT  
		Size: 358.2 MB (358177453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f233e3685ed99d080d20d75569f52721780af423282e3938b3fa811a546cb`  
		Last Modified: Sat, 16 Nov 2024 03:00:08 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8134f8582e1c00aef5bfd8f91b7bd23d11c7bc6d1b41b60a32b70db021dde3be`  
		Last Modified: Sat, 16 Nov 2024 03:00:09 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d077b54d523fe4a8fdf344eb0ebfb9c9e12310a867b4a5eb02a0d894e43a02f`  
		Last Modified: Sat, 16 Nov 2024 03:00:09 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd4803c50973c28c8199ffcfcf3a676b06db55218696291242de619708f04d0`  
		Last Modified: Sat, 16 Nov 2024 03:00:10 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e06bdac4cf84a476f0d1de8110f169a288283cfa3789fc24cbcb9031c87ffd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56235909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f99d830d6dcbf7c1f1ade0aa817424d7eee032afd3afd33fb88da75046025d`

```dockerfile
```

-	Layers:
	-	`sha256:339e0507385d01d271803bd8d8a3fcfad1d1e756a39329fc49b23c20f5bbc27c`  
		Last Modified: Sat, 16 Nov 2024 03:00:08 GMT  
		Size: 56.2 MB (56208773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6f5c7ebd2e3df4243983d9cc3478e6a0511f0a8e5ef0c08fd47802cae26259`  
		Last Modified: Sat, 16 Nov 2024 03:00:09 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:213f0eab609cdf75296dd76239283bd518c93445cf0d0c5260228c26a58d5961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 MB (653538738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d46240844d7c6c83477a1cce47a8490b77318eff89ef8cddaa67f6d654e5e7`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH=arm64
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=18.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=919f386aa25f0a10d537f09c945349b20c502f73
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
	-	`sha256:233a767f9f9ce3f01ec556e67c8df11519fde2d4bb1a94f9c8b113d20d173526`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 358.0 MB (358026084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e2eb7533e1377dd46b95d8def4261e069239a89305b03c1417fc46f6526bf9`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06c91ae14aaf8bfc45d3dfb68cdc121ddd496742169ae45d281390a2021df38`  
		Last Modified: Sat, 16 Nov 2024 03:28:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0a9a9d045b2885d98deca6003b330171e41f37d5e10364721b00e5703dcd16`  
		Last Modified: Sat, 16 Nov 2024 03:28:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c369e8d6e104a731056db9f84c33b46605bafd7a8fe6665cabec7368e8284f7`  
		Last Modified: Sat, 16 Nov 2024 03:28:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5c63308372e6e6659c27c53b913fe98a8ee585116239969abf4abc7689272785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56243371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47284503def0dd3896a9d0b50e4f44fc039a4b0d7773189ffbb83ebabfe254ec`

```dockerfile
```

-	Layers:
	-	`sha256:c5997196d1ed56b4e4f0cd5beeec6fa3a517956f80401a2eb7b27802131a0cb1`  
		Last Modified: Sat, 16 Nov 2024 03:28:08 GMT  
		Size: 56.2 MB (56216071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad22010ccab6853296ec2f37dee147633da1e56c2b04b514fa61178f2effd42c`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
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
