<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260305`](#odoo170-20260305)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260305`](#odoo180-20260305)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260305`](#odoo190-20260305)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:cca6238d9e07a757dba73bc6abc4cda075b1e8f2ddf145253bd5be36b844b7a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:18e8c1935b47c37765afcb63a01f1fa265281c7dc07ace696c9be1168d8b5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.5 MB (610505420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94801d6e47be9d419e9bb4f76cec460708bb0adf93ebb0478c739e7e01aba16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:56 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:56 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:42:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:42:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:42:05 GMT
ENV ODOO_VERSION=17.0
# Thu, 05 Mar 2026 17:42:05 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:42:05 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Thu, 05 Mar 2026 17:43:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:43:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:43:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:43:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:43:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:43:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
USER odoo
# Thu, 05 Mar 2026 17:43:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:43:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c99b635a0059e53d9a421aeda10df65c2508b0032cb13fdd5ab2569f6b5d221`  
		Last Modified: Thu, 05 Mar 2026 17:44:39 GMT  
		Size: 235.0 MB (234960656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a15f3eeb48888a3181ddef6acfdf657e6b7e2027cce7d43f0237638c0a76e`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 2.6 MB (2604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d21cc5b0278ba7eaaed63e502bce76aa391a5c452bac7281d4e592d8406769a`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 479.8 KB (479823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4059e3c52af8cb45f4c6fa3647b5fd9b8a475b556e5219ed93d6e54f47a97810`  
		Last Modified: Thu, 05 Mar 2026 17:44:40 GMT  
		Size: 342.9 MB (342921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34380dfef9dd1559b6b15375f1080bae9c1d2c9ebefb58988b16f4b8b5827562`  
		Last Modified: Thu, 05 Mar 2026 17:44:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf94cd0ce1ce00273c5e6dacbc8e01fe6ca1ed6498d7e9e801b97f3a286091e`  
		Last Modified: Thu, 05 Mar 2026 17:44:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccdd1c24a3476fef657c916723eba1a942166e8b9e14599b0a51423b5360963`  
		Last Modified: Thu, 05 Mar 2026 17:44:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb9b7e325893206fb139b40e8e024f0ab555ed4eed292f06e98a4d9b4f398e`  
		Last Modified: Thu, 05 Mar 2026 17:44:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b4e5171785184c067165d06402be1b8f3b166a54250f629a63012fa32b51dfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42015219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69df7c95893abfe5d0a06f41e9e87b0cabd2774029dd30aa5f405a43147c975`

```dockerfile
```

-	Layers:
	-	`sha256:8971c832fea2f9a7fc85148bb2f061a98fd8c04e2f444a991745d6f7f4b30134`  
		Last Modified: Thu, 05 Mar 2026 17:44:32 GMT  
		Size: 42.0 MB (41988427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5d918efba9306e1a61e445858e4073bc47c4cbb159823c2db860e142f23634`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:31c589f20ad9d8bc1d326789ca68b1dc8bd7af2e070f8fa26b0a8fef47b781ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605293475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f804abfddf0435d7eb498a59a7a191e2962f5c68490860eadc617ff53903862e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:15 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:15 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:15 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:25 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Mar 2026 01:49:26 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:26 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Tue, 17 Mar 2026 01:50:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2275c4e483b5bf37e353b31bd102f2a8b5f4c2531b8825ce9276d5240c3c24`  
		Last Modified: Tue, 17 Mar 2026 01:52:01 GMT  
		Size: 232.3 MB (232295325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70505962ef83f2768be9c042dac2af7f0ae5a8497a7927adc314d517ea9fc343`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 2.6 MB (2598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01805ea18c65067ddb6732893641835e2ca1a7935608e4e315838756e70cc347`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03a93ee9239a9b9317f13e75bfb84702e3689dd7d1bdd7ae871ded299ba7da1`  
		Last Modified: Tue, 17 Mar 2026 01:52:03 GMT  
		Size: 342.5 MB (342528263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d92e262303c24106078c8309f5a1fd1e1707c51410b7cd550c4feb29cec349`  
		Last Modified: Tue, 17 Mar 2026 01:51:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5065412251a852a4d21bcacf9fcf2b72f2cc8e31a539441dc2d4c64d43e437d6`  
		Last Modified: Tue, 17 Mar 2026 01:51:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f822d1e007c9fa64a9f5602cb56ce6903a2f5c325b0553f8def6f31fc0c95a6`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552bea389031cfd05c284a2a5ad1557ad505ffa3d21b76f8185304ffb7cc415a`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:2994860c2b874dd27c3f4fbf7f23b87507b5a1955ad58e61a1d1863ed590a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42021878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe9c34f81735b64851cd93f7c0779a22b5d81e7beea85eef6af7561f4d3c402`

```dockerfile
```

-	Layers:
	-	`sha256:9ed5b0167c15d020272c32b250e1609ab68b75407dd8255376f018eb4444505d`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 42.0 MB (41994934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06534631ab0b9f0383abfcee4edf0e477d0062c03a5ff028e0d6255b5046be82`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:cca6238d9e07a757dba73bc6abc4cda075b1e8f2ddf145253bd5be36b844b7a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:18e8c1935b47c37765afcb63a01f1fa265281c7dc07ace696c9be1168d8b5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.5 MB (610505420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94801d6e47be9d419e9bb4f76cec460708bb0adf93ebb0478c739e7e01aba16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:56 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:56 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:42:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:42:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:42:05 GMT
ENV ODOO_VERSION=17.0
# Thu, 05 Mar 2026 17:42:05 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:42:05 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Thu, 05 Mar 2026 17:43:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:43:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:43:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:43:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:43:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:43:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
USER odoo
# Thu, 05 Mar 2026 17:43:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:43:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c99b635a0059e53d9a421aeda10df65c2508b0032cb13fdd5ab2569f6b5d221`  
		Last Modified: Thu, 05 Mar 2026 17:44:39 GMT  
		Size: 235.0 MB (234960656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a15f3eeb48888a3181ddef6acfdf657e6b7e2027cce7d43f0237638c0a76e`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 2.6 MB (2604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d21cc5b0278ba7eaaed63e502bce76aa391a5c452bac7281d4e592d8406769a`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 479.8 KB (479823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4059e3c52af8cb45f4c6fa3647b5fd9b8a475b556e5219ed93d6e54f47a97810`  
		Last Modified: Thu, 05 Mar 2026 17:44:40 GMT  
		Size: 342.9 MB (342921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34380dfef9dd1559b6b15375f1080bae9c1d2c9ebefb58988b16f4b8b5827562`  
		Last Modified: Thu, 05 Mar 2026 17:44:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf94cd0ce1ce00273c5e6dacbc8e01fe6ca1ed6498d7e9e801b97f3a286091e`  
		Last Modified: Thu, 05 Mar 2026 17:44:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccdd1c24a3476fef657c916723eba1a942166e8b9e14599b0a51423b5360963`  
		Last Modified: Thu, 05 Mar 2026 17:44:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb9b7e325893206fb139b40e8e024f0ab555ed4eed292f06e98a4d9b4f398e`  
		Last Modified: Thu, 05 Mar 2026 17:44:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b4e5171785184c067165d06402be1b8f3b166a54250f629a63012fa32b51dfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42015219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69df7c95893abfe5d0a06f41e9e87b0cabd2774029dd30aa5f405a43147c975`

```dockerfile
```

-	Layers:
	-	`sha256:8971c832fea2f9a7fc85148bb2f061a98fd8c04e2f444a991745d6f7f4b30134`  
		Last Modified: Thu, 05 Mar 2026 17:44:32 GMT  
		Size: 42.0 MB (41988427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5d918efba9306e1a61e445858e4073bc47c4cbb159823c2db860e142f23634`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:31c589f20ad9d8bc1d326789ca68b1dc8bd7af2e070f8fa26b0a8fef47b781ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605293475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f804abfddf0435d7eb498a59a7a191e2962f5c68490860eadc617ff53903862e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:15 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:15 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:15 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:25 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Mar 2026 01:49:26 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:26 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Tue, 17 Mar 2026 01:50:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2275c4e483b5bf37e353b31bd102f2a8b5f4c2531b8825ce9276d5240c3c24`  
		Last Modified: Tue, 17 Mar 2026 01:52:01 GMT  
		Size: 232.3 MB (232295325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70505962ef83f2768be9c042dac2af7f0ae5a8497a7927adc314d517ea9fc343`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 2.6 MB (2598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01805ea18c65067ddb6732893641835e2ca1a7935608e4e315838756e70cc347`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03a93ee9239a9b9317f13e75bfb84702e3689dd7d1bdd7ae871ded299ba7da1`  
		Last Modified: Tue, 17 Mar 2026 01:52:03 GMT  
		Size: 342.5 MB (342528263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d92e262303c24106078c8309f5a1fd1e1707c51410b7cd550c4feb29cec349`  
		Last Modified: Tue, 17 Mar 2026 01:51:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5065412251a852a4d21bcacf9fcf2b72f2cc8e31a539441dc2d4c64d43e437d6`  
		Last Modified: Tue, 17 Mar 2026 01:51:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f822d1e007c9fa64a9f5602cb56ce6903a2f5c325b0553f8def6f31fc0c95a6`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552bea389031cfd05c284a2a5ad1557ad505ffa3d21b76f8185304ffb7cc415a`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2994860c2b874dd27c3f4fbf7f23b87507b5a1955ad58e61a1d1863ed590a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42021878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe9c34f81735b64851cd93f7c0779a22b5d81e7beea85eef6af7561f4d3c402`

```dockerfile
```

-	Layers:
	-	`sha256:9ed5b0167c15d020272c32b250e1609ab68b75407dd8255376f018eb4444505d`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 42.0 MB (41994934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06534631ab0b9f0383abfcee4edf0e477d0062c03a5ff028e0d6255b5046be82`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260305`

```console
$ docker pull odoo@sha256:cca6238d9e07a757dba73bc6abc4cda075b1e8f2ddf145253bd5be36b844b7a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260305` - linux; amd64

```console
$ docker pull odoo@sha256:18e8c1935b47c37765afcb63a01f1fa265281c7dc07ace696c9be1168d8b5888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.5 MB (610505420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94801d6e47be9d419e9bb4f76cec460708bb0adf93ebb0478c739e7e01aba16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:56 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:56 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:42:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:42:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:42:05 GMT
ENV ODOO_VERSION=17.0
# Thu, 05 Mar 2026 17:42:05 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:42:05 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Thu, 05 Mar 2026 17:43:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:43:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:43:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:43:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:43:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:43:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:43:16 GMT
USER odoo
# Thu, 05 Mar 2026 17:43:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:43:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c99b635a0059e53d9a421aeda10df65c2508b0032cb13fdd5ab2569f6b5d221`  
		Last Modified: Thu, 05 Mar 2026 17:44:39 GMT  
		Size: 235.0 MB (234960656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a15f3eeb48888a3181ddef6acfdf657e6b7e2027cce7d43f0237638c0a76e`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 2.6 MB (2604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d21cc5b0278ba7eaaed63e502bce76aa391a5c452bac7281d4e592d8406769a`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 479.8 KB (479823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4059e3c52af8cb45f4c6fa3647b5fd9b8a475b556e5219ed93d6e54f47a97810`  
		Last Modified: Thu, 05 Mar 2026 17:44:40 GMT  
		Size: 342.9 MB (342921134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34380dfef9dd1559b6b15375f1080bae9c1d2c9ebefb58988b16f4b8b5827562`  
		Last Modified: Thu, 05 Mar 2026 17:44:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf94cd0ce1ce00273c5e6dacbc8e01fe6ca1ed6498d7e9e801b97f3a286091e`  
		Last Modified: Thu, 05 Mar 2026 17:44:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccdd1c24a3476fef657c916723eba1a942166e8b9e14599b0a51423b5360963`  
		Last Modified: Thu, 05 Mar 2026 17:44:32 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb9b7e325893206fb139b40e8e024f0ab555ed4eed292f06e98a4d9b4f398e`  
		Last Modified: Thu, 05 Mar 2026 17:44:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:b4e5171785184c067165d06402be1b8f3b166a54250f629a63012fa32b51dfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42015219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69df7c95893abfe5d0a06f41e9e87b0cabd2774029dd30aa5f405a43147c975`

```dockerfile
```

-	Layers:
	-	`sha256:8971c832fea2f9a7fc85148bb2f061a98fd8c04e2f444a991745d6f7f4b30134`  
		Last Modified: Thu, 05 Mar 2026 17:44:32 GMT  
		Size: 42.0 MB (41988427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5d918efba9306e1a61e445858e4073bc47c4cbb159823c2db860e142f23634`  
		Last Modified: Thu, 05 Mar 2026 17:44:30 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260305` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:31c589f20ad9d8bc1d326789ca68b1dc8bd7af2e070f8fa26b0a8fef47b781ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605293475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f804abfddf0435d7eb498a59a7a191e2962f5c68490860eadc617ff53903862e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:15 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:15 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:15 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:25 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:26 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:26 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Mar 2026 01:49:26 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:26 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Tue, 17 Mar 2026 01:50:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:33 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2275c4e483b5bf37e353b31bd102f2a8b5f4c2531b8825ce9276d5240c3c24`  
		Last Modified: Tue, 17 Mar 2026 01:52:01 GMT  
		Size: 232.3 MB (232295325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70505962ef83f2768be9c042dac2af7f0ae5a8497a7927adc314d517ea9fc343`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 2.6 MB (2598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01805ea18c65067ddb6732893641835e2ca1a7935608e4e315838756e70cc347`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03a93ee9239a9b9317f13e75bfb84702e3689dd7d1bdd7ae871ded299ba7da1`  
		Last Modified: Tue, 17 Mar 2026 01:52:03 GMT  
		Size: 342.5 MB (342528263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d92e262303c24106078c8309f5a1fd1e1707c51410b7cd550c4feb29cec349`  
		Last Modified: Tue, 17 Mar 2026 01:51:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5065412251a852a4d21bcacf9fcf2b72f2cc8e31a539441dc2d4c64d43e437d6`  
		Last Modified: Tue, 17 Mar 2026 01:51:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f822d1e007c9fa64a9f5602cb56ce6903a2f5c325b0553f8def6f31fc0c95a6`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552bea389031cfd05c284a2a5ad1557ad505ffa3d21b76f8185304ffb7cc415a`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:2994860c2b874dd27c3f4fbf7f23b87507b5a1955ad58e61a1d1863ed590a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42021878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe9c34f81735b64851cd93f7c0779a22b5d81e7beea85eef6af7561f4d3c402`

```dockerfile
```

-	Layers:
	-	`sha256:9ed5b0167c15d020272c32b250e1609ab68b75407dd8255376f018eb4444505d`  
		Last Modified: Tue, 17 Mar 2026 01:51:55 GMT  
		Size: 42.0 MB (41994934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06534631ab0b9f0383abfcee4edf0e477d0062c03a5ff028e0d6255b5046be82`  
		Last Modified: Tue, 17 Mar 2026 01:51:53 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:8d0db7ab881f5b599d44d277e71289eb63888d7812d11a4898fa16d5703b0c39
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
$ docker pull odoo@sha256:12eb8e83f829c1f43b4d5e0201bc8ead45607c5b0094ecf8cf0ccb6c88c0b117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.4 MB (684400494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b427b66069992a6fe5c60e669b757f928635c14088247cfa4ab0cabc11e8f85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:39:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:39:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:39:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:39:50 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:39:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:40:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:40:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:40:02 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:40:02 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:40:02 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:40:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:40:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:40:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:40:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
USER odoo
# Thu, 05 Mar 2026 17:40:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:40:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f162fb17aaac411eeb6e5b4ca2bea349a2a8789e9d0dd286d03c8ce305eb9`  
		Last Modified: Thu, 05 Mar 2026 17:42:53 GMT  
		Size: 255.7 MB (255679146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564f84663999fe61e47b842a8e4daac3282cd7c03f0bffa00adc1c9c994458ca`  
		Last Modified: Thu, 05 Mar 2026 17:42:42 GMT  
		Size: 14.4 MB (14360517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc581668db30135d73ddf2908fde63d3b4a8648ef79f766731df5d6e09d843`  
		Last Modified: Thu, 05 Mar 2026 17:42:41 GMT  
		Size: 479.6 KB (479570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce6dcca4cdb1d81da98c6733fa6cf4333d933a137d1a717c9e48c030bf05190`  
		Last Modified: Thu, 05 Mar 2026 17:42:56 GMT  
		Size: 384.2 MB (384151205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce9acdd052b1e0591203d663611e6ef09f3f0aecde3ea37b2b3662e3035607`  
		Last Modified: Thu, 05 Mar 2026 17:42:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a1b3914f458bcfea29cb19a6015e75855c94d9a0e28817b9b20cf74a72e8f`  
		Last Modified: Thu, 05 Mar 2026 17:42:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1625f3ae6610c6487172cef0fe500a3ffa4a5edcc6102276851bb4568a519e`  
		Last Modified: Thu, 05 Mar 2026 17:42:43 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58cd48661d40ad9461e75f35935bd70fdad738418a4e5fbc5919479b5e3a79c`  
		Last Modified: Thu, 05 Mar 2026 17:42:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7ad2d99f904bd00a1ecec1115b0c9d56c61e4bfa79f03fc576a7a4b87620fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61727713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f1361f913f3f9ae7f24d606fe196b29ef41ae8252c7a54bc21af902b03582b`

```dockerfile
```

-	Layers:
	-	`sha256:becbfe096dd360af047bf1e04e33096d988d9df1f5882dc1ae80aee26422ca50`  
		Last Modified: Thu, 05 Mar 2026 17:42:45 GMT  
		Size: 61.7 MB (61700914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca0df0b79e4b4b250accce8b51d2638b54611c313552132cbcee4c9ab2819177`  
		Last Modified: Thu, 05 Mar 2026 17:42:40 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5dd46efba9f38034ea7c237cf2af35a088dc33da2ac4f4287479291d38d00f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.7 MB (679670813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d5d83df697b436a2929e3aea992cce924ae105124061a65f2627c71ec1b1d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:39 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:53 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Mar 2026 01:49:53 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:53 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Tue, 17 Mar 2026 01:51:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:51:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:51:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:51:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
USER odoo
# Tue, 17 Mar 2026 01:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:51:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d36e288c96ed964f7bba46de31c0402f5814c99680bad0e0b36f6f3cb5c5`  
		Last Modified: Tue, 17 Mar 2026 01:53:44 GMT  
		Size: 252.0 MB (251995276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a473b99484bcd424575b22235b9e6e3ae565fdbbf5ff3387ffa5e5ecc806d4b`  
		Last Modified: Tue, 17 Mar 2026 01:53:36 GMT  
		Size: 14.3 MB (14340740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b639b66be58724d2796c062c28052a23873c8df39738eb618e592e3ccf50`  
		Last Modified: Tue, 17 Mar 2026 01:53:35 GMT  
		Size: 479.7 KB (479673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7302b5e9cf9bf5949bbde2469f79cd0a79aee1524468eefeb4e8d759ac8a0`  
		Last Modified: Tue, 17 Mar 2026 01:53:46 GMT  
		Size: 384.0 MB (383982975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8371afdf7841c6bd2390ac615e3fecba77d1ccefa2d132cf06fe60f4fe97b7c`  
		Last Modified: Tue, 17 Mar 2026 01:53:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2484099ad3b36d659bca301a0c1ddde58a8734ad1fecb269f37cfe683147469`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415e15324757a1272cf184ca843b6fe33444d5610f07ab353b3efc326062562a`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb94a1783065a19cff6fbe4d21bc266c4e5d1b4fa7fdf8455f08c218de0cb6d5`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:05af96970c0cd837c2a552997d5e6c167abe872658c59494fc368186a700fa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee94029de8c186438283359643022234146213854eb88b94e0cf2436559d16a9`

```dockerfile
```

-	Layers:
	-	`sha256:8f3e911c28f77ce263646b0568f8bd40963d60d55f9c0781063939b0a62f65e9`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 61.7 MB (61708201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bc06a9dace6961e78cec0e62628346a8ef14b65b25ab5868d3f2f0be1cf5548`  
		Last Modified: Tue, 17 Mar 2026 01:53:35 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:7c83ad56b95a06b44ba75a2c8c29d364d51d84be843e5214bd4a31f18f8f7a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700732320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25831679bfead5eee27a3a6ba649567ecf298968fd1de0eb0f2e0d75cdd4e30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:45:01 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a58a8d3db51b2fd61f77fb417f5b29901de461db0ce29b1c4ef5648b603227`  
		Last Modified: Thu, 05 Mar 2026 17:49:33 GMT  
		Size: 384.7 MB (384688579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6a393f52baf302d17091df36521e9dd4e93bf47a52811a79167be8e76f27a1`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a03b8256d6db1b03f82e8e65263f5e817010bcacb721f3fc202c8fbee1eb7`  
		Last Modified: Thu, 05 Mar 2026 17:49:21 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cb0c3706081839d4697da15ba9c001a1d189d63b716f0fe62aecad16935c95`  
		Last Modified: Thu, 05 Mar 2026 17:49:21 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc059f2dc67ecc8db85ce61a5c2df539376d96c4aecc66bcf871c236c586b775`  
		Last Modified: Thu, 05 Mar 2026 17:49:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:9731f20c4d36d05054a264e66aced09badc226e1770786557b9dbe8d7701976c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61736152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366431c9a410a980c27c4d11ac18a7ebfad29e1301e71faa15862e8de294948f`

```dockerfile
```

-	Layers:
	-	`sha256:1439c0911cb84450183c3dcb9b582a8633062f74e19bd58f89d06f0ec1721b03`  
		Last Modified: Thu, 05 Mar 2026 17:49:23 GMT  
		Size: 61.7 MB (61709297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a3674d9234892e548ddbfe510f71f68bc12e15b30fb12f5d7f3cdc37d256a`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:8d0db7ab881f5b599d44d277e71289eb63888d7812d11a4898fa16d5703b0c39
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
$ docker pull odoo@sha256:12eb8e83f829c1f43b4d5e0201bc8ead45607c5b0094ecf8cf0ccb6c88c0b117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.4 MB (684400494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b427b66069992a6fe5c60e669b757f928635c14088247cfa4ab0cabc11e8f85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:39:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:39:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:39:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:39:50 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:39:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:40:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:40:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:40:02 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:40:02 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:40:02 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:40:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:40:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:40:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:40:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
USER odoo
# Thu, 05 Mar 2026 17:40:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:40:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f162fb17aaac411eeb6e5b4ca2bea349a2a8789e9d0dd286d03c8ce305eb9`  
		Last Modified: Thu, 05 Mar 2026 17:42:53 GMT  
		Size: 255.7 MB (255679146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564f84663999fe61e47b842a8e4daac3282cd7c03f0bffa00adc1c9c994458ca`  
		Last Modified: Thu, 05 Mar 2026 17:42:42 GMT  
		Size: 14.4 MB (14360517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc581668db30135d73ddf2908fde63d3b4a8648ef79f766731df5d6e09d843`  
		Last Modified: Thu, 05 Mar 2026 17:42:41 GMT  
		Size: 479.6 KB (479570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce6dcca4cdb1d81da98c6733fa6cf4333d933a137d1a717c9e48c030bf05190`  
		Last Modified: Thu, 05 Mar 2026 17:42:56 GMT  
		Size: 384.2 MB (384151205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce9acdd052b1e0591203d663611e6ef09f3f0aecde3ea37b2b3662e3035607`  
		Last Modified: Thu, 05 Mar 2026 17:42:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a1b3914f458bcfea29cb19a6015e75855c94d9a0e28817b9b20cf74a72e8f`  
		Last Modified: Thu, 05 Mar 2026 17:42:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1625f3ae6610c6487172cef0fe500a3ffa4a5edcc6102276851bb4568a519e`  
		Last Modified: Thu, 05 Mar 2026 17:42:43 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58cd48661d40ad9461e75f35935bd70fdad738418a4e5fbc5919479b5e3a79c`  
		Last Modified: Thu, 05 Mar 2026 17:42:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7ad2d99f904bd00a1ecec1115b0c9d56c61e4bfa79f03fc576a7a4b87620fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61727713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f1361f913f3f9ae7f24d606fe196b29ef41ae8252c7a54bc21af902b03582b`

```dockerfile
```

-	Layers:
	-	`sha256:becbfe096dd360af047bf1e04e33096d988d9df1f5882dc1ae80aee26422ca50`  
		Last Modified: Thu, 05 Mar 2026 17:42:45 GMT  
		Size: 61.7 MB (61700914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca0df0b79e4b4b250accce8b51d2638b54611c313552132cbcee4c9ab2819177`  
		Last Modified: Thu, 05 Mar 2026 17:42:40 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5dd46efba9f38034ea7c237cf2af35a088dc33da2ac4f4287479291d38d00f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.7 MB (679670813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d5d83df697b436a2929e3aea992cce924ae105124061a65f2627c71ec1b1d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:39 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:53 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Mar 2026 01:49:53 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:53 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Tue, 17 Mar 2026 01:51:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:51:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:51:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:51:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
USER odoo
# Tue, 17 Mar 2026 01:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:51:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d36e288c96ed964f7bba46de31c0402f5814c99680bad0e0b36f6f3cb5c5`  
		Last Modified: Tue, 17 Mar 2026 01:53:44 GMT  
		Size: 252.0 MB (251995276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a473b99484bcd424575b22235b9e6e3ae565fdbbf5ff3387ffa5e5ecc806d4b`  
		Last Modified: Tue, 17 Mar 2026 01:53:36 GMT  
		Size: 14.3 MB (14340740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b639b66be58724d2796c062c28052a23873c8df39738eb618e592e3ccf50`  
		Last Modified: Tue, 17 Mar 2026 01:53:35 GMT  
		Size: 479.7 KB (479673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7302b5e9cf9bf5949bbde2469f79cd0a79aee1524468eefeb4e8d759ac8a0`  
		Last Modified: Tue, 17 Mar 2026 01:53:46 GMT  
		Size: 384.0 MB (383982975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8371afdf7841c6bd2390ac615e3fecba77d1ccefa2d132cf06fe60f4fe97b7c`  
		Last Modified: Tue, 17 Mar 2026 01:53:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2484099ad3b36d659bca301a0c1ddde58a8734ad1fecb269f37cfe683147469`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415e15324757a1272cf184ca843b6fe33444d5610f07ab353b3efc326062562a`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb94a1783065a19cff6fbe4d21bc266c4e5d1b4fa7fdf8455f08c218de0cb6d5`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:05af96970c0cd837c2a552997d5e6c167abe872658c59494fc368186a700fa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee94029de8c186438283359643022234146213854eb88b94e0cf2436559d16a9`

```dockerfile
```

-	Layers:
	-	`sha256:8f3e911c28f77ce263646b0568f8bd40963d60d55f9c0781063939b0a62f65e9`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 61.7 MB (61708201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bc06a9dace6961e78cec0e62628346a8ef14b65b25ab5868d3f2f0be1cf5548`  
		Last Modified: Tue, 17 Mar 2026 01:53:35 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:7c83ad56b95a06b44ba75a2c8c29d364d51d84be843e5214bd4a31f18f8f7a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700732320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25831679bfead5eee27a3a6ba649567ecf298968fd1de0eb0f2e0d75cdd4e30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:45:01 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a58a8d3db51b2fd61f77fb417f5b29901de461db0ce29b1c4ef5648b603227`  
		Last Modified: Thu, 05 Mar 2026 17:49:33 GMT  
		Size: 384.7 MB (384688579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6a393f52baf302d17091df36521e9dd4e93bf47a52811a79167be8e76f27a1`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a03b8256d6db1b03f82e8e65263f5e817010bcacb721f3fc202c8fbee1eb7`  
		Last Modified: Thu, 05 Mar 2026 17:49:21 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cb0c3706081839d4697da15ba9c001a1d189d63b716f0fe62aecad16935c95`  
		Last Modified: Thu, 05 Mar 2026 17:49:21 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc059f2dc67ecc8db85ce61a5c2df539376d96c4aecc66bcf871c236c586b775`  
		Last Modified: Thu, 05 Mar 2026 17:49:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9731f20c4d36d05054a264e66aced09badc226e1770786557b9dbe8d7701976c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61736152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366431c9a410a980c27c4d11ac18a7ebfad29e1301e71faa15862e8de294948f`

```dockerfile
```

-	Layers:
	-	`sha256:1439c0911cb84450183c3dcb9b582a8633062f74e19bd58f89d06f0ec1721b03`  
		Last Modified: Thu, 05 Mar 2026 17:49:23 GMT  
		Size: 61.7 MB (61709297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a3674d9234892e548ddbfe510f71f68bc12e15b30fb12f5d7f3cdc37d256a`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260305`

```console
$ docker pull odoo@sha256:8d0db7ab881f5b599d44d277e71289eb63888d7812d11a4898fa16d5703b0c39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260305` - linux; amd64

```console
$ docker pull odoo@sha256:12eb8e83f829c1f43b4d5e0201bc8ead45607c5b0094ecf8cf0ccb6c88c0b117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.4 MB (684400494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b427b66069992a6fe5c60e669b757f928635c14088247cfa4ab0cabc11e8f85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:39:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:39:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:39:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:39:50 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:39:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:40:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:40:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:40:02 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:40:02 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:40:02 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:40:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:40:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:40:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:40:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
USER odoo
# Thu, 05 Mar 2026 17:40:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:40:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f162fb17aaac411eeb6e5b4ca2bea349a2a8789e9d0dd286d03c8ce305eb9`  
		Last Modified: Thu, 05 Mar 2026 17:42:53 GMT  
		Size: 255.7 MB (255679146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564f84663999fe61e47b842a8e4daac3282cd7c03f0bffa00adc1c9c994458ca`  
		Last Modified: Thu, 05 Mar 2026 17:42:42 GMT  
		Size: 14.4 MB (14360517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc581668db30135d73ddf2908fde63d3b4a8648ef79f766731df5d6e09d843`  
		Last Modified: Thu, 05 Mar 2026 17:42:41 GMT  
		Size: 479.6 KB (479570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce6dcca4cdb1d81da98c6733fa6cf4333d933a137d1a717c9e48c030bf05190`  
		Last Modified: Thu, 05 Mar 2026 17:42:56 GMT  
		Size: 384.2 MB (384151205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce9acdd052b1e0591203d663611e6ef09f3f0aecde3ea37b2b3662e3035607`  
		Last Modified: Thu, 05 Mar 2026 17:42:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a1b3914f458bcfea29cb19a6015e75855c94d9a0e28817b9b20cf74a72e8f`  
		Last Modified: Thu, 05 Mar 2026 17:42:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1625f3ae6610c6487172cef0fe500a3ffa4a5edcc6102276851bb4568a519e`  
		Last Modified: Thu, 05 Mar 2026 17:42:43 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58cd48661d40ad9461e75f35935bd70fdad738418a4e5fbc5919479b5e3a79c`  
		Last Modified: Thu, 05 Mar 2026 17:42:45 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:7ad2d99f904bd00a1ecec1115b0c9d56c61e4bfa79f03fc576a7a4b87620fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61727713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f1361f913f3f9ae7f24d606fe196b29ef41ae8252c7a54bc21af902b03582b`

```dockerfile
```

-	Layers:
	-	`sha256:becbfe096dd360af047bf1e04e33096d988d9df1f5882dc1ae80aee26422ca50`  
		Last Modified: Thu, 05 Mar 2026 17:42:45 GMT  
		Size: 61.7 MB (61700914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca0df0b79e4b4b250accce8b51d2638b54611c313552132cbcee4c9ab2819177`  
		Last Modified: Thu, 05 Mar 2026 17:42:40 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260305` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5dd46efba9f38034ea7c237cf2af35a088dc33da2ac4f4287479291d38d00f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.7 MB (679670813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d5d83df697b436a2929e3aea992cce924ae105124061a65f2627c71ec1b1d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:39 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:53 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Mar 2026 01:49:53 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:53 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Tue, 17 Mar 2026 01:51:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:51:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:51:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:51:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:51:22 GMT
USER odoo
# Tue, 17 Mar 2026 01:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:51:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26d36e288c96ed964f7bba46de31c0402f5814c99680bad0e0b36f6f3cb5c5`  
		Last Modified: Tue, 17 Mar 2026 01:53:44 GMT  
		Size: 252.0 MB (251995276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a473b99484bcd424575b22235b9e6e3ae565fdbbf5ff3387ffa5e5ecc806d4b`  
		Last Modified: Tue, 17 Mar 2026 01:53:36 GMT  
		Size: 14.3 MB (14340740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a839b639b66be58724d2796c062c28052a23873c8df39738eb618e592e3ccf50`  
		Last Modified: Tue, 17 Mar 2026 01:53:35 GMT  
		Size: 479.7 KB (479673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb7302b5e9cf9bf5949bbde2469f79cd0a79aee1524468eefeb4e8d759ac8a0`  
		Last Modified: Tue, 17 Mar 2026 01:53:46 GMT  
		Size: 384.0 MB (383982975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8371afdf7841c6bd2390ac615e3fecba77d1ccefa2d132cf06fe60f4fe97b7c`  
		Last Modified: Tue, 17 Mar 2026 01:53:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2484099ad3b36d659bca301a0c1ddde58a8734ad1fecb269f37cfe683147469`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415e15324757a1272cf184ca843b6fe33444d5610f07ab353b3efc326062562a`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb94a1783065a19cff6fbe4d21bc266c4e5d1b4fa7fdf8455f08c218de0cb6d5`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:05af96970c0cd837c2a552997d5e6c167abe872658c59494fc368186a700fa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee94029de8c186438283359643022234146213854eb88b94e0cf2436559d16a9`

```dockerfile
```

-	Layers:
	-	`sha256:8f3e911c28f77ce263646b0568f8bd40963d60d55f9c0781063939b0a62f65e9`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 61.7 MB (61708201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bc06a9dace6961e78cec0e62628346a8ef14b65b25ab5868d3f2f0be1cf5548`  
		Last Modified: Tue, 17 Mar 2026 01:53:35 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260305` - linux; ppc64le

```console
$ docker pull odoo@sha256:7c83ad56b95a06b44ba75a2c8c29d364d51d84be843e5214bd4a31f18f8f7a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700732320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25831679bfead5eee27a3a6ba649567ecf298968fd1de0eb0f2e0d75cdd4e30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:45:01 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:04 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:04 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:04 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a58a8d3db51b2fd61f77fb417f5b29901de461db0ce29b1c4ef5648b603227`  
		Last Modified: Thu, 05 Mar 2026 17:49:33 GMT  
		Size: 384.7 MB (384688579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6a393f52baf302d17091df36521e9dd4e93bf47a52811a79167be8e76f27a1`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a03b8256d6db1b03f82e8e65263f5e817010bcacb721f3fc202c8fbee1eb7`  
		Last Modified: Thu, 05 Mar 2026 17:49:21 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cb0c3706081839d4697da15ba9c001a1d189d63b716f0fe62aecad16935c95`  
		Last Modified: Thu, 05 Mar 2026 17:49:21 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc059f2dc67ecc8db85ce61a5c2df539376d96c4aecc66bcf871c236c586b775`  
		Last Modified: Thu, 05 Mar 2026 17:49:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:9731f20c4d36d05054a264e66aced09badc226e1770786557b9dbe8d7701976c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61736152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366431c9a410a980c27c4d11ac18a7ebfad29e1301e71faa15862e8de294948f`

```dockerfile
```

-	Layers:
	-	`sha256:1439c0911cb84450183c3dcb9b582a8633062f74e19bd58f89d06f0ec1721b03`  
		Last Modified: Thu, 05 Mar 2026 17:49:23 GMT  
		Size: 61.7 MB (61709297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832a3674d9234892e548ddbfe510f71f68bc12e15b30fb12f5d7f3cdc37d256a`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:31597af53402e8cdd66d6591b41ba9b64dbf68b5d10325e7095e5a58f826796d
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
$ docker pull odoo@sha256:8ce13af31a92689d41b23e013256e64a2f6176e638f9a04ac0a99eda097486df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.0 MB (702013942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc449e25fcf4e020f6f5fc5c7acb1e2fa49bdd976a15b12c0aedd828b9c179f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:37:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:37:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:37:23 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:37:23 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:37:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:37:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:38:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:38:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:38:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:38:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:38:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525ebf947183ef0adc5687896d674aac79bbec6d1fa0d551cb07745d78373d3`  
		Last Modified: Thu, 05 Mar 2026 17:40:50 GMT  
		Size: 255.7 MB (255673660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145dd56812ce37da3f89e7b3404ecf4e1226fc4ff414254b93fc8619b0befeb9`  
		Last Modified: Thu, 05 Mar 2026 17:40:40 GMT  
		Size: 14.4 MB (14360469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533185f3b0f3c529ce8fd8febfe199281f6b78501c83fbf815271661bc24948c`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd0ebc70ddc0a6605f1e8c55699790031664afb04b6e8fa0233832f8e986b20`  
		Last Modified: Thu, 05 Mar 2026 17:40:53 GMT  
		Size: 401.8 MB (401770185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8833542f4108e0c4dfe9c3de93372457c803c7819d2eb038562afaaffc148c`  
		Last Modified: Thu, 05 Mar 2026 17:40:41 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bf903ba263dc819604ed678a04d2178195878206abaf101f69d0206a684652`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736cd3c9dcb18632fce5316e3b1946d931638e9e2c22c99cd9d31b68f37c8382`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dcf780bf720e4de4b51e35054ae3d7c48d38840986fac95b99b2639a68068a`  
		Last Modified: Thu, 05 Mar 2026 17:40:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:63db90250b37e53c199be06461ef4f62e65df70ce4912a025a2458b769b42ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69900180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ea02dbeb59360d0a97884ebcfd7121f14156bcb5f3d81a9742f12bb49492e4`

```dockerfile
```

-	Layers:
	-	`sha256:b5577ddf612a13174db1ab9faa0d8f08df14e3a527e1e80af1ac32aefca2bf03`  
		Last Modified: Thu, 05 Mar 2026 17:40:44 GMT  
		Size: 69.9 MB (69873087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e18a921bc70dc0d50eee2ecfaf0cc81dabf2d3aa7de52e20d8d0380c1d2b7`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:133e181ade01d35718437a853d7f12edb8ae0a5df7de779057464976b99c9f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.3 MB (697278928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b902e9c6d9748d0c3ba503e438ba13076d8070aab89ab71e3a02dcdd4074b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:08 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9cd1fa227158c20b72cc137091cd3ba24a7b2e4748501f22dcc76445e3d0e`  
		Last Modified: Tue, 17 Mar 2026 01:53:49 GMT  
		Size: 252.0 MB (251993469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa51190389c1a94c8f0d8cd1f9f3909b5eed87405ba604f9d053c1513a99803`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 14.3 MB (14340742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91339d5c6f0d60c723ddbcc7f33980e4108bfed1e8a7bee45e2870e9276f4e1`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 479.6 KB (479645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ed922014979a51a6c67f6fbb4a52275c64f1cc1c8d3b99970e29c9738e16b`  
		Last Modified: Tue, 17 Mar 2026 01:53:53 GMT  
		Size: 401.6 MB (401592921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4d617b3c2f8b6d4ae6bd49e36b9187db265de1207c452f2195713229ad48bd`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99af5e84ec727fb27b5e197cd67e417495d6ca03db1fd89c27feceb73da44b66`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eed69d44264886957e03ff1cedbfa5b606ce657019b5dc815648315a6523a5`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd12059778008e00fc712c6c0ecfe172dbcfca8b918a3ec856436a13dc61b15`  
		Last Modified: Tue, 17 Mar 2026 01:53:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:d55c5153ed3faabefa8a3e8aedd046b538011faefdcade9f2da94da5c61fd5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72564b5550f55c60d1adc8079f4a320ae77194afb9adea810c289eff1a0458f`

```dockerfile
```

-	Layers:
	-	`sha256:81b157ad73e350ac684ac3f10afd2ee7fb1d5cbfbde43d0818bc5d83f58d5da7`  
		Last Modified: Tue, 17 Mar 2026 01:53:43 GMT  
		Size: 69.9 MB (69880386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c379a8a6939296c23d121fd7d17b1154ae2d4f9290c53c2c54f63376b765f744`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:ae291227b3c00395bccbf1a43ec7f1a6d297fb42eb336ac500447d6231f01388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7438d9a4a31c4cc58843c89c1b8733f21a7abd5c58fd12fd9a62cac4971b4f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:45:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98298248d892919f3b8dfc67a9e79665062ccc36e77dad4a835aa335c3ef9d8`  
		Last Modified: Thu, 05 Mar 2026 17:50:40 GMT  
		Size: 402.3 MB (402304032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b95c433dd3ae2ef3dcd6429797ad8ac604ac010316d02b13bdd0f378f4e83d`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a40e69c8f0c09362c22a67ff4e2009225a4bcd9a727cc4f2288a2cccc4d05`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494a0c6c0cdd2e6c56ab9f2b364b2d35f5ca5ea9dce0930dc5122a1b9f51dd5`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59942ff85afe2aade6eacd3aa1b3bdb972d0930b3a39b5d8c7a8f508a49fe86`  
		Last Modified: Thu, 05 Mar 2026 17:50:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:57c5db338343599571a8051ce1884fad31ac57ebb7a0bd137fa6c34c981eaeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9022b1aa80952ab16c425a888348aa8f544292be066f7c40e248ed18922f44`

```dockerfile
```

-	Layers:
	-	`sha256:a57f8869aa13377f96a047a152a25a319b2a96c81c2c25bd379d65be00ee42b9`  
		Last Modified: Thu, 05 Mar 2026 17:50:33 GMT  
		Size: 69.9 MB (69881476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e551e484fa949daed08a2b3f9d3cc9be12196ca2e77183f2e50a6e43fb2113`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:31597af53402e8cdd66d6591b41ba9b64dbf68b5d10325e7095e5a58f826796d
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
$ docker pull odoo@sha256:8ce13af31a92689d41b23e013256e64a2f6176e638f9a04ac0a99eda097486df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.0 MB (702013942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc449e25fcf4e020f6f5fc5c7acb1e2fa49bdd976a15b12c0aedd828b9c179f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:37:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:37:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:37:23 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:37:23 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:37:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:37:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:38:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:38:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:38:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:38:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:38:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525ebf947183ef0adc5687896d674aac79bbec6d1fa0d551cb07745d78373d3`  
		Last Modified: Thu, 05 Mar 2026 17:40:50 GMT  
		Size: 255.7 MB (255673660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145dd56812ce37da3f89e7b3404ecf4e1226fc4ff414254b93fc8619b0befeb9`  
		Last Modified: Thu, 05 Mar 2026 17:40:40 GMT  
		Size: 14.4 MB (14360469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533185f3b0f3c529ce8fd8febfe199281f6b78501c83fbf815271661bc24948c`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd0ebc70ddc0a6605f1e8c55699790031664afb04b6e8fa0233832f8e986b20`  
		Last Modified: Thu, 05 Mar 2026 17:40:53 GMT  
		Size: 401.8 MB (401770185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8833542f4108e0c4dfe9c3de93372457c803c7819d2eb038562afaaffc148c`  
		Last Modified: Thu, 05 Mar 2026 17:40:41 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bf903ba263dc819604ed678a04d2178195878206abaf101f69d0206a684652`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736cd3c9dcb18632fce5316e3b1946d931638e9e2c22c99cd9d31b68f37c8382`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dcf780bf720e4de4b51e35054ae3d7c48d38840986fac95b99b2639a68068a`  
		Last Modified: Thu, 05 Mar 2026 17:40:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:63db90250b37e53c199be06461ef4f62e65df70ce4912a025a2458b769b42ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69900180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ea02dbeb59360d0a97884ebcfd7121f14156bcb5f3d81a9742f12bb49492e4`

```dockerfile
```

-	Layers:
	-	`sha256:b5577ddf612a13174db1ab9faa0d8f08df14e3a527e1e80af1ac32aefca2bf03`  
		Last Modified: Thu, 05 Mar 2026 17:40:44 GMT  
		Size: 69.9 MB (69873087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e18a921bc70dc0d50eee2ecfaf0cc81dabf2d3aa7de52e20d8d0380c1d2b7`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:133e181ade01d35718437a853d7f12edb8ae0a5df7de779057464976b99c9f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.3 MB (697278928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b902e9c6d9748d0c3ba503e438ba13076d8070aab89ab71e3a02dcdd4074b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:08 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9cd1fa227158c20b72cc137091cd3ba24a7b2e4748501f22dcc76445e3d0e`  
		Last Modified: Tue, 17 Mar 2026 01:53:49 GMT  
		Size: 252.0 MB (251993469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa51190389c1a94c8f0d8cd1f9f3909b5eed87405ba604f9d053c1513a99803`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 14.3 MB (14340742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91339d5c6f0d60c723ddbcc7f33980e4108bfed1e8a7bee45e2870e9276f4e1`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 479.6 KB (479645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ed922014979a51a6c67f6fbb4a52275c64f1cc1c8d3b99970e29c9738e16b`  
		Last Modified: Tue, 17 Mar 2026 01:53:53 GMT  
		Size: 401.6 MB (401592921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4d617b3c2f8b6d4ae6bd49e36b9187db265de1207c452f2195713229ad48bd`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99af5e84ec727fb27b5e197cd67e417495d6ca03db1fd89c27feceb73da44b66`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eed69d44264886957e03ff1cedbfa5b606ce657019b5dc815648315a6523a5`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd12059778008e00fc712c6c0ecfe172dbcfca8b918a3ec856436a13dc61b15`  
		Last Modified: Tue, 17 Mar 2026 01:53:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d55c5153ed3faabefa8a3e8aedd046b538011faefdcade9f2da94da5c61fd5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72564b5550f55c60d1adc8079f4a320ae77194afb9adea810c289eff1a0458f`

```dockerfile
```

-	Layers:
	-	`sha256:81b157ad73e350ac684ac3f10afd2ee7fb1d5cbfbde43d0818bc5d83f58d5da7`  
		Last Modified: Tue, 17 Mar 2026 01:53:43 GMT  
		Size: 69.9 MB (69880386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c379a8a6939296c23d121fd7d17b1154ae2d4f9290c53c2c54f63376b765f744`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ae291227b3c00395bccbf1a43ec7f1a6d297fb42eb336ac500447d6231f01388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7438d9a4a31c4cc58843c89c1b8733f21a7abd5c58fd12fd9a62cac4971b4f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:45:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98298248d892919f3b8dfc67a9e79665062ccc36e77dad4a835aa335c3ef9d8`  
		Last Modified: Thu, 05 Mar 2026 17:50:40 GMT  
		Size: 402.3 MB (402304032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b95c433dd3ae2ef3dcd6429797ad8ac604ac010316d02b13bdd0f378f4e83d`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a40e69c8f0c09362c22a67ff4e2009225a4bcd9a727cc4f2288a2cccc4d05`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494a0c6c0cdd2e6c56ab9f2b364b2d35f5ca5ea9dce0930dc5122a1b9f51dd5`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59942ff85afe2aade6eacd3aa1b3bdb972d0930b3a39b5d8c7a8f508a49fe86`  
		Last Modified: Thu, 05 Mar 2026 17:50:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:57c5db338343599571a8051ce1884fad31ac57ebb7a0bd137fa6c34c981eaeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9022b1aa80952ab16c425a888348aa8f544292be066f7c40e248ed18922f44`

```dockerfile
```

-	Layers:
	-	`sha256:a57f8869aa13377f96a047a152a25a319b2a96c81c2c25bd379d65be00ee42b9`  
		Last Modified: Thu, 05 Mar 2026 17:50:33 GMT  
		Size: 69.9 MB (69881476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e551e484fa949daed08a2b3f9d3cc9be12196ca2e77183f2e50a6e43fb2113`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260305`

```console
$ docker pull odoo@sha256:31597af53402e8cdd66d6591b41ba9b64dbf68b5d10325e7095e5a58f826796d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260305` - linux; amd64

```console
$ docker pull odoo@sha256:8ce13af31a92689d41b23e013256e64a2f6176e638f9a04ac0a99eda097486df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.0 MB (702013942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc449e25fcf4e020f6f5fc5c7acb1e2fa49bdd976a15b12c0aedd828b9c179f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:37:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:37:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:37:23 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:37:23 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:37:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:37:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:38:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:38:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:38:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:38:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:38:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525ebf947183ef0adc5687896d674aac79bbec6d1fa0d551cb07745d78373d3`  
		Last Modified: Thu, 05 Mar 2026 17:40:50 GMT  
		Size: 255.7 MB (255673660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145dd56812ce37da3f89e7b3404ecf4e1226fc4ff414254b93fc8619b0befeb9`  
		Last Modified: Thu, 05 Mar 2026 17:40:40 GMT  
		Size: 14.4 MB (14360469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533185f3b0f3c529ce8fd8febfe199281f6b78501c83fbf815271661bc24948c`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd0ebc70ddc0a6605f1e8c55699790031664afb04b6e8fa0233832f8e986b20`  
		Last Modified: Thu, 05 Mar 2026 17:40:53 GMT  
		Size: 401.8 MB (401770185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8833542f4108e0c4dfe9c3de93372457c803c7819d2eb038562afaaffc148c`  
		Last Modified: Thu, 05 Mar 2026 17:40:41 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bf903ba263dc819604ed678a04d2178195878206abaf101f69d0206a684652`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736cd3c9dcb18632fce5316e3b1946d931638e9e2c22c99cd9d31b68f37c8382`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dcf780bf720e4de4b51e35054ae3d7c48d38840986fac95b99b2639a68068a`  
		Last Modified: Thu, 05 Mar 2026 17:40:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:63db90250b37e53c199be06461ef4f62e65df70ce4912a025a2458b769b42ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69900180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ea02dbeb59360d0a97884ebcfd7121f14156bcb5f3d81a9742f12bb49492e4`

```dockerfile
```

-	Layers:
	-	`sha256:b5577ddf612a13174db1ab9faa0d8f08df14e3a527e1e80af1ac32aefca2bf03`  
		Last Modified: Thu, 05 Mar 2026 17:40:44 GMT  
		Size: 69.9 MB (69873087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e18a921bc70dc0d50eee2ecfaf0cc81dabf2d3aa7de52e20d8d0380c1d2b7`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260305` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:133e181ade01d35718437a853d7f12edb8ae0a5df7de779057464976b99c9f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.3 MB (697278928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b902e9c6d9748d0c3ba503e438ba13076d8070aab89ab71e3a02dcdd4074b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:08 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9cd1fa227158c20b72cc137091cd3ba24a7b2e4748501f22dcc76445e3d0e`  
		Last Modified: Tue, 17 Mar 2026 01:53:49 GMT  
		Size: 252.0 MB (251993469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa51190389c1a94c8f0d8cd1f9f3909b5eed87405ba604f9d053c1513a99803`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 14.3 MB (14340742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91339d5c6f0d60c723ddbcc7f33980e4108bfed1e8a7bee45e2870e9276f4e1`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 479.6 KB (479645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ed922014979a51a6c67f6fbb4a52275c64f1cc1c8d3b99970e29c9738e16b`  
		Last Modified: Tue, 17 Mar 2026 01:53:53 GMT  
		Size: 401.6 MB (401592921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4d617b3c2f8b6d4ae6bd49e36b9187db265de1207c452f2195713229ad48bd`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99af5e84ec727fb27b5e197cd67e417495d6ca03db1fd89c27feceb73da44b66`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eed69d44264886957e03ff1cedbfa5b606ce657019b5dc815648315a6523a5`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd12059778008e00fc712c6c0ecfe172dbcfca8b918a3ec856436a13dc61b15`  
		Last Modified: Tue, 17 Mar 2026 01:53:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:d55c5153ed3faabefa8a3e8aedd046b538011faefdcade9f2da94da5c61fd5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72564b5550f55c60d1adc8079f4a320ae77194afb9adea810c289eff1a0458f`

```dockerfile
```

-	Layers:
	-	`sha256:81b157ad73e350ac684ac3f10afd2ee7fb1d5cbfbde43d0818bc5d83f58d5da7`  
		Last Modified: Tue, 17 Mar 2026 01:53:43 GMT  
		Size: 69.9 MB (69880386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c379a8a6939296c23d121fd7d17b1154ae2d4f9290c53c2c54f63376b765f744`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260305` - linux; ppc64le

```console
$ docker pull odoo@sha256:ae291227b3c00395bccbf1a43ec7f1a6d297fb42eb336ac500447d6231f01388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7438d9a4a31c4cc58843c89c1b8733f21a7abd5c58fd12fd9a62cac4971b4f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:45:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98298248d892919f3b8dfc67a9e79665062ccc36e77dad4a835aa335c3ef9d8`  
		Last Modified: Thu, 05 Mar 2026 17:50:40 GMT  
		Size: 402.3 MB (402304032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b95c433dd3ae2ef3dcd6429797ad8ac604ac010316d02b13bdd0f378f4e83d`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a40e69c8f0c09362c22a67ff4e2009225a4bcd9a727cc4f2288a2cccc4d05`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494a0c6c0cdd2e6c56ab9f2b364b2d35f5ca5ea9dce0930dc5122a1b9f51dd5`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59942ff85afe2aade6eacd3aa1b3bdb972d0930b3a39b5d8c7a8f508a49fe86`  
		Last Modified: Thu, 05 Mar 2026 17:50:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:57c5db338343599571a8051ce1884fad31ac57ebb7a0bd137fa6c34c981eaeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9022b1aa80952ab16c425a888348aa8f544292be066f7c40e248ed18922f44`

```dockerfile
```

-	Layers:
	-	`sha256:a57f8869aa13377f96a047a152a25a319b2a96c81c2c25bd379d65be00ee42b9`  
		Last Modified: Thu, 05 Mar 2026 17:50:33 GMT  
		Size: 69.9 MB (69881476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e551e484fa949daed08a2b3f9d3cc9be12196ca2e77183f2e50a6e43fb2113`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:31597af53402e8cdd66d6591b41ba9b64dbf68b5d10325e7095e5a58f826796d
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
$ docker pull odoo@sha256:8ce13af31a92689d41b23e013256e64a2f6176e638f9a04ac0a99eda097486df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.0 MB (702013942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc449e25fcf4e020f6f5fc5c7acb1e2fa49bdd976a15b12c0aedd828b9c179f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:37:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:37:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:37:23 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:37:23 GMT
ARG TARGETARCH=amd64
# Thu, 05 Mar 2026 17:37:23 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:37:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:37:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:37:33 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:38:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:38:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:38:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:38:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:38:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:38:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7525ebf947183ef0adc5687896d674aac79bbec6d1fa0d551cb07745d78373d3`  
		Last Modified: Thu, 05 Mar 2026 17:40:50 GMT  
		Size: 255.7 MB (255673660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145dd56812ce37da3f89e7b3404ecf4e1226fc4ff414254b93fc8619b0befeb9`  
		Last Modified: Thu, 05 Mar 2026 17:40:40 GMT  
		Size: 14.4 MB (14360469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533185f3b0f3c529ce8fd8febfe199281f6b78501c83fbf815271661bc24948c`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd0ebc70ddc0a6605f1e8c55699790031664afb04b6e8fa0233832f8e986b20`  
		Last Modified: Thu, 05 Mar 2026 17:40:53 GMT  
		Size: 401.8 MB (401770185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8833542f4108e0c4dfe9c3de93372457c803c7819d2eb038562afaaffc148c`  
		Last Modified: Thu, 05 Mar 2026 17:40:41 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bf903ba263dc819604ed678a04d2178195878206abaf101f69d0206a684652`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736cd3c9dcb18632fce5316e3b1946d931638e9e2c22c99cd9d31b68f37c8382`  
		Last Modified: Thu, 05 Mar 2026 17:40:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dcf780bf720e4de4b51e35054ae3d7c48d38840986fac95b99b2639a68068a`  
		Last Modified: Thu, 05 Mar 2026 17:40:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:63db90250b37e53c199be06461ef4f62e65df70ce4912a025a2458b769b42ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69900180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ea02dbeb59360d0a97884ebcfd7121f14156bcb5f3d81a9742f12bb49492e4`

```dockerfile
```

-	Layers:
	-	`sha256:b5577ddf612a13174db1ab9faa0d8f08df14e3a527e1e80af1ac32aefca2bf03`  
		Last Modified: Thu, 05 Mar 2026 17:40:44 GMT  
		Size: 69.9 MB (69873087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69e18a921bc70dc0d50eee2ecfaf0cc81dabf2d3aa7de52e20d8d0380c1d2b7`  
		Last Modified: Thu, 05 Mar 2026 17:40:39 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:133e181ade01d35718437a853d7f12edb8ae0a5df7de779057464976b99c9f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.3 MB (697278928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b902e9c6d9748d0c3ba503e438ba13076d8070aab89ab71e3a02dcdd4074b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:49:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Mar 2026 01:49:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Mar 2026 01:49:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:49:08 GMT
ARG TARGETARCH=arm64
# Tue, 17 Mar 2026 01:49:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Mar 2026 01:49:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Mar 2026 01:49:21 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_RELEASE=20260305
# Tue, 17 Mar 2026 01:49:21 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Mar 2026 01:50:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Mar 2026 01:50:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Mar 2026 01:50:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Mar 2026 01:50:46 GMT
USER odoo
# Tue, 17 Mar 2026 01:50:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Mar 2026 01:50:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c9cd1fa227158c20b72cc137091cd3ba24a7b2e4748501f22dcc76445e3d0e`  
		Last Modified: Tue, 17 Mar 2026 01:53:49 GMT  
		Size: 252.0 MB (251993469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa51190389c1a94c8f0d8cd1f9f3909b5eed87405ba604f9d053c1513a99803`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 14.3 MB (14340742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91339d5c6f0d60c723ddbcc7f33980e4108bfed1e8a7bee45e2870e9276f4e1`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 479.6 KB (479645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ed922014979a51a6c67f6fbb4a52275c64f1cc1c8d3b99970e29c9738e16b`  
		Last Modified: Tue, 17 Mar 2026 01:53:53 GMT  
		Size: 401.6 MB (401592921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4d617b3c2f8b6d4ae6bd49e36b9187db265de1207c452f2195713229ad48bd`  
		Last Modified: Tue, 17 Mar 2026 01:53:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99af5e84ec727fb27b5e197cd67e417495d6ca03db1fd89c27feceb73da44b66`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eed69d44264886957e03ff1cedbfa5b606ce657019b5dc815648315a6523a5`  
		Last Modified: Tue, 17 Mar 2026 01:53:41 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd12059778008e00fc712c6c0ecfe172dbcfca8b918a3ec856436a13dc61b15`  
		Last Modified: Tue, 17 Mar 2026 01:53:42 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d55c5153ed3faabefa8a3e8aedd046b538011faefdcade9f2da94da5c61fd5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72564b5550f55c60d1adc8079f4a320ae77194afb9adea810c289eff1a0458f`

```dockerfile
```

-	Layers:
	-	`sha256:81b157ad73e350ac684ac3f10afd2ee7fb1d5cbfbde43d0818bc5d83f58d5da7`  
		Last Modified: Tue, 17 Mar 2026 01:53:43 GMT  
		Size: 69.9 MB (69880386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c379a8a6939296c23d121fd7d17b1154ae2d4f9290c53c2c54f63376b765f744`  
		Last Modified: Tue, 17 Mar 2026 01:53:38 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:ae291227b3c00395bccbf1a43ec7f1a6d297fb42eb336ac500447d6231f01388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.3 MB (718347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7438d9a4a31c4cc58843c89c1b8733f21a7abd5c58fd12fd9a62cac4971b4f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:41:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:41:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:41:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:41:38 GMT
ARG TARGETARCH=ppc64le
# Thu, 05 Mar 2026 17:41:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:41:54 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:41:56 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:41:56 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:45:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:45:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:45:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:45:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:45:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:45:15 GMT
USER odoo
# Thu, 05 Mar 2026 17:45:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:45:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec537c8ecbec2656a9333fefd57fa39e6ee6cfbe34bd5bbb7bb62b9d94640e1`  
		Last Modified: Thu, 05 Mar 2026 17:49:30 GMT  
		Size: 266.4 MB (266360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0426b1ed1bf8c49b0d99e7f98288ba271df84072708dafb0745c127467e43220`  
		Last Modified: Thu, 05 Mar 2026 17:49:20 GMT  
		Size: 14.9 MB (14894200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a018db793628db9a6a84c69d4cd429a24e53559092f826696056ffd2a28217`  
		Last Modified: Thu, 05 Mar 2026 17:49:19 GMT  
		Size: 479.6 KB (479620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98298248d892919f3b8dfc67a9e79665062ccc36e77dad4a835aa335c3ef9d8`  
		Last Modified: Thu, 05 Mar 2026 17:50:40 GMT  
		Size: 402.3 MB (402304032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b95c433dd3ae2ef3dcd6429797ad8ac604ac010316d02b13bdd0f378f4e83d`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a40e69c8f0c09362c22a67ff4e2009225a4bcd9a727cc4f2288a2cccc4d05`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494a0c6c0cdd2e6c56ab9f2b364b2d35f5ca5ea9dce0930dc5122a1b9f51dd5`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59942ff85afe2aade6eacd3aa1b3bdb972d0930b3a39b5d8c7a8f508a49fe86`  
		Last Modified: Thu, 05 Mar 2026 17:50:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:57c5db338343599571a8051ce1884fad31ac57ebb7a0bd137fa6c34c981eaeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69908631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9022b1aa80952ab16c425a888348aa8f544292be066f7c40e248ed18922f44`

```dockerfile
```

-	Layers:
	-	`sha256:a57f8869aa13377f96a047a152a25a319b2a96c81c2c25bd379d65be00ee42b9`  
		Last Modified: Thu, 05 Mar 2026 17:50:33 GMT  
		Size: 69.9 MB (69881476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e551e484fa949daed08a2b3f9d3cc9be12196ca2e77183f2e50a6e43fb2113`  
		Last Modified: Thu, 05 Mar 2026 17:50:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
