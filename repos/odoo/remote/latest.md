## `odoo:latest`

```console
$ docker pull odoo@sha256:c4ee957e5d5c915b3cd0bd820ccd04607b3f905081450fe4d10f73a7c075d053
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
$ docker pull odoo@sha256:402357ccf5047c11bb68d4929ed961edc4e9b2a0ec100853b990ea02a843da6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672868266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e27862e2945ab8823f663c6b825b3ca96a063dd9ddd68f12377e4ee22e11f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4ee5ab3aa0011d78744362dcece8f0974b85bad79781fdd6a01fb0a3e11f3`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 254.5 MB (254516693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d98f3c2a15d4d4b6d3989d4f7ac5597f027a1bb5fef2f9d2594899861cf1f0`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 16.7 MB (16680393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179c4f8f8efe635f2b6ba667c1dcfdbe93bd84e5a9b1f3becae7fa86f82a706`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 478.6 KB (478559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfb621b7c01fbe3a1a260334e0e098a6dced0de7324941d54c875639d78b8a9`  
		Last Modified: Tue, 15 Apr 2025 16:55:17 GMT  
		Size: 371.5 MB (371472527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8cf938cfb5473a0c2727ea0807c7bf5007d633cc972fa543435eac01e1daf8`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b504b70f7a36801c30a77d95dc46ff1a2183a268b614e8e34c818868d3c20`  
		Last Modified: Tue, 15 Apr 2025 16:55:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e24694663c798a195e0bc60c0b045d12ef193cee903c96d2a9dd4ea059d899`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf6ec58fce63b80be03d5d483003659f564ebdf068a28dd8c670166f114193`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e5e06fa27c2dbbda81fee6dd880581966d91207a2dfb976926a80d15d1cfacc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59242574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47509d04dc0fdcd86fb3e580686a8bdbb6521b7ef81d5e6dab37bddb84944464`

```dockerfile
```

-	Layers:
	-	`sha256:d1cb8d06c3142968c048436e542661c0c715a4786e5719381d333df7a7617880`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 59.2 MB (59215438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2b592bdc6dff1214486a3e76feddc4573e3a8e9ab460fdff9f94709960db16`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:eaab25ee64bf1f82dc06c3b041a4e7c7a374491a696db36e66694ace7d181d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.8 MB (666838623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd11069852e1df0ca4b100ed431dd910823fdeb63d0b84cb4eb509282ddcc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0786f5ebd97ae80c7ee53223d7a832ebec632e35763f4face06e160c648ac50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:34 GMT  
		Size: 371.3 MB (371319907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e608d1ebac4cda0a3efcc645b6d427a3bcf7e6d6d0b754910a6795ae38838d`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7369ea4c4bc01f06a0f685320401febc7151eefdfb1220b5c355ad312ccb50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06819af0622f591d0e09a8a37a327a6547650ac6fc24a782708837d017c03fa9`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208c8276edbe0dfa10f9c22d3ebaa9cc429f766491d2ee6c1553cfb3829dbb7`  
		Last Modified: Tue, 15 Apr 2025 16:58:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7e9483256482934f3f37362228b16c2cd10d63510f3c144dd28b5c1afac8083d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21841822065535879d0caa22440de17f73e1c475fcfec6e44c5f0b4c1e85938e`

```dockerfile
```

-	Layers:
	-	`sha256:887d28860681d1db5475e9000d0acddb388645dcab172e012cc82739d918d795`  
		Last Modified: Tue, 15 Apr 2025 16:58:28 GMT  
		Size: 59.2 MB (59222717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9dca536cf1630ff686e3b286b00d1cef945b78e76935f273bc4e064e1d428c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c4ae5c38aecccc284a1202cc58b69b7a48dff2715a3df5e7c962294504558fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686708135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394175eff43e420b10480dae496577f495bccecd7e5ae648a14e1bd6dd68a99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=ppc64le
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a97ed06e8627565e4e91626c0fbe528714703d50ee993b4094587768ed9b`  
		Last Modified: Tue, 15 Apr 2025 16:59:45 GMT  
		Size: 372.0 MB (372007811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8baafa7ebd79730dc3cb116e7275602a9b3a964d5935579eeca19038b9408b`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee42e6afa025999d10d70d30c48f5ddea4d8523ed09028bd85b8b2311676a2`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7381ee871fd664d625c9f0d3b24bbc88507a1364a8fd7a9f7b32869709f14db4`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef06ffcc6e95febf4f543c62624953a0c3e64fae96de0bd9fd82f5c80f31c42`  
		Last Modified: Tue, 15 Apr 2025 16:59:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1d704842eb6a4249de5910ecc03b2e55627f9d3a8bc7ffbdb092f0cfbc6af9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59aa84fae3d26819be0ae583dd3f27552996e34c75cf6b5f0dca6f60093b102`

```dockerfile
```

-	Layers:
	-	`sha256:901deb28d47ba3e908cfb0ee29e11cb8bfbd163bb72424f813e11070d3bb2a21`  
		Last Modified: Tue, 15 Apr 2025 16:59:36 GMT  
		Size: 59.2 MB (59223573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443ac72e492b1877dffb01289de8db477a441f5d88770260d2bdee5cff9e8fc5`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
