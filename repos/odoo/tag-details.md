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
$ docker pull odoo@sha256:5db395d9520c2ea629d5dd815e30dbb9872703386645ae57e73ed6a1429cd27a
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
$ docker pull odoo@sha256:4d3c9068e2c0ee7778a5a708b29d58b78f775d3077f5fb3920b84ee4fdf377a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605324053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af3892f28731b86afd95896b01827e70967e6fdcb6aafbfe08a46f6f7ac6bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:40:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:40:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:40:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:40:42 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:40:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
ENV ODOO_VERSION=17.0
# Thu, 05 Mar 2026 17:40:53 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:40:53 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Thu, 05 Mar 2026 17:41:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:41:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:41:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:41:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
USER odoo
# Thu, 05 Mar 2026 17:41:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:41:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234ed3d4d39ae00b1b5acb5a68c31f55baf27a6580a3a22ac445bca3dba6d0e`  
		Last Modified: Thu, 05 Mar 2026 17:43:31 GMT  
		Size: 232.3 MB (232305391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c39ce49df85512695821ebe8346ee20bf23231479b54e7508cee515c3b5d543`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 2.6 MB (2598561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c02017e8da9e4caaf7c6e47b262b1773be803868dae4ab44f11f30deb9ec0b3`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 479.9 KB (479925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915aeaef930763c119530777a79181735ef153e65114ce5e3d56fc10369ec43b`  
		Last Modified: Thu, 05 Mar 2026 17:43:35 GMT  
		Size: 342.6 MB (342552788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42059c8b6387b18ff90fcc5efdba0cdf42ec8452919091110bb78ef4624acaa`  
		Last Modified: Thu, 05 Mar 2026 17:43:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e460cf3d1cb51fdc4259d2425c9d04411fc2f0089931e75df81d336bd782fb8e`  
		Last Modified: Thu, 05 Mar 2026 17:43:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33acaf792e6cb9fc353c14dee0b96098b2a8657eac0fefddf392a3beeb00b082`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd5fe13048928067a60e98b6220c8c831ae0ec2c0a4d21633e2d98f3e57c97`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1724bda2ac3f2f4703303ec07910a4d10a35e291b6606989a59dde4e16f1ed14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42021878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d3e8a6040660a7af44726967dd56116ba9e27a0ae7b6fbdd644d92c426e143`

```dockerfile
```

-	Layers:
	-	`sha256:33e56f33e63f43dabb97a80a3db5fb5d21643174468dce2485cf1f6ad7d20b5c`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 42.0 MB (41994934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728ba1f40102dbc470bdb75e4dc21ca73314f6dae9631ff885e2655ffbdad18d`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:5db395d9520c2ea629d5dd815e30dbb9872703386645ae57e73ed6a1429cd27a
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
$ docker pull odoo@sha256:4d3c9068e2c0ee7778a5a708b29d58b78f775d3077f5fb3920b84ee4fdf377a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605324053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af3892f28731b86afd95896b01827e70967e6fdcb6aafbfe08a46f6f7ac6bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:40:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:40:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:40:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:40:42 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:40:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
ENV ODOO_VERSION=17.0
# Thu, 05 Mar 2026 17:40:53 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:40:53 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Thu, 05 Mar 2026 17:41:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:41:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:41:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:41:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
USER odoo
# Thu, 05 Mar 2026 17:41:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:41:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234ed3d4d39ae00b1b5acb5a68c31f55baf27a6580a3a22ac445bca3dba6d0e`  
		Last Modified: Thu, 05 Mar 2026 17:43:31 GMT  
		Size: 232.3 MB (232305391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c39ce49df85512695821ebe8346ee20bf23231479b54e7508cee515c3b5d543`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 2.6 MB (2598561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c02017e8da9e4caaf7c6e47b262b1773be803868dae4ab44f11f30deb9ec0b3`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 479.9 KB (479925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915aeaef930763c119530777a79181735ef153e65114ce5e3d56fc10369ec43b`  
		Last Modified: Thu, 05 Mar 2026 17:43:35 GMT  
		Size: 342.6 MB (342552788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42059c8b6387b18ff90fcc5efdba0cdf42ec8452919091110bb78ef4624acaa`  
		Last Modified: Thu, 05 Mar 2026 17:43:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e460cf3d1cb51fdc4259d2425c9d04411fc2f0089931e75df81d336bd782fb8e`  
		Last Modified: Thu, 05 Mar 2026 17:43:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33acaf792e6cb9fc353c14dee0b96098b2a8657eac0fefddf392a3beeb00b082`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd5fe13048928067a60e98b6220c8c831ae0ec2c0a4d21633e2d98f3e57c97`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1724bda2ac3f2f4703303ec07910a4d10a35e291b6606989a59dde4e16f1ed14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42021878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d3e8a6040660a7af44726967dd56116ba9e27a0ae7b6fbdd644d92c426e143`

```dockerfile
```

-	Layers:
	-	`sha256:33e56f33e63f43dabb97a80a3db5fb5d21643174468dce2485cf1f6ad7d20b5c`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 42.0 MB (41994934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728ba1f40102dbc470bdb75e4dc21ca73314f6dae9631ff885e2655ffbdad18d`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260305`

```console
$ docker pull odoo@sha256:5db395d9520c2ea629d5dd815e30dbb9872703386645ae57e73ed6a1429cd27a
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
$ docker pull odoo@sha256:4d3c9068e2c0ee7778a5a708b29d58b78f775d3077f5fb3920b84ee4fdf377a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605324053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af3892f28731b86afd95896b01827e70967e6fdcb6aafbfe08a46f6f7ac6bb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:40:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:40:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:40:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:40:42 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:40:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:40:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:40:53 GMT
ENV ODOO_VERSION=17.0
# Thu, 05 Mar 2026 17:40:53 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:40:53 GMT
ARG ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
# Thu, 05 Mar 2026 17:41:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=0b1c520ad8d7eb33620c0517a9ab7bb6c7b83364
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:41:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:41:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:41:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:41:58 GMT
USER odoo
# Thu, 05 Mar 2026 17:41:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:41:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234ed3d4d39ae00b1b5acb5a68c31f55baf27a6580a3a22ac445bca3dba6d0e`  
		Last Modified: Thu, 05 Mar 2026 17:43:31 GMT  
		Size: 232.3 MB (232305391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c39ce49df85512695821ebe8346ee20bf23231479b54e7508cee515c3b5d543`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 2.6 MB (2598561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c02017e8da9e4caaf7c6e47b262b1773be803868dae4ab44f11f30deb9ec0b3`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 479.9 KB (479925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915aeaef930763c119530777a79181735ef153e65114ce5e3d56fc10369ec43b`  
		Last Modified: Thu, 05 Mar 2026 17:43:35 GMT  
		Size: 342.6 MB (342552788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42059c8b6387b18ff90fcc5efdba0cdf42ec8452919091110bb78ef4624acaa`  
		Last Modified: Thu, 05 Mar 2026 17:43:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e460cf3d1cb51fdc4259d2425c9d04411fc2f0089931e75df81d336bd782fb8e`  
		Last Modified: Thu, 05 Mar 2026 17:43:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33acaf792e6cb9fc353c14dee0b96098b2a8657eac0fefddf392a3beeb00b082`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd5fe13048928067a60e98b6220c8c831ae0ec2c0a4d21633e2d98f3e57c97`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:1724bda2ac3f2f4703303ec07910a4d10a35e291b6606989a59dde4e16f1ed14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42021878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d3e8a6040660a7af44726967dd56116ba9e27a0ae7b6fbdd644d92c426e143`

```dockerfile
```

-	Layers:
	-	`sha256:33e56f33e63f43dabb97a80a3db5fb5d21643174468dce2485cf1f6ad7d20b5c`  
		Last Modified: Thu, 05 Mar 2026 17:43:20 GMT  
		Size: 42.0 MB (41994934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728ba1f40102dbc470bdb75e4dc21ca73314f6dae9631ff885e2655ffbdad18d`  
		Last Modified: Thu, 05 Mar 2026 17:43:17 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:371e92a268be52d8c96f0212a2d46b34533f506441a738ef55009c99367a50bc
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
$ docker pull odoo@sha256:2bd06230d28d06d9e4844a4f1c8bcd55a478a81581b3057481e6338285e43662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680698019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d121b46b9b94e89c384c657c46583aea3d6d077411f0a20f1ba342b555b8da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:24 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:24 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:24 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:24 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:37 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:37 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:38:37 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:37 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:39:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e736e2b97ff94fcca9419d0e88c2c780af0b16939973d3b1f461b3042b45c`  
		Last Modified: Thu, 05 Mar 2026 17:42:08 GMT  
		Size: 253.0 MB (253032071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbca75105151c915a991284093974f715fd4ec8477dfb3cf9e17b439d01798c`  
		Last Modified: Thu, 05 Mar 2026 17:41:57 GMT  
		Size: 14.3 MB (14341200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f177b5ded5ee57bf31f5ba2894db031dc6d261d2915e6ea78adf0a9adaf0e29b`  
		Last Modified: Thu, 05 Mar 2026 17:41:55 GMT  
		Size: 479.6 KB (479585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b634dcbe4b49ec683dcaf37bb473898e852abc98dd79566816bd4550199bd8b7`  
		Last Modified: Thu, 05 Mar 2026 17:42:11 GMT  
		Size: 384.0 MB (383977601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efa25a2be210fb570e8d717652622e062cde458f4005ce16c844cda3056cb`  
		Last Modified: Thu, 05 Mar 2026 17:41:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146ad29140b458f6407f7ede0aba5878c6fe3b7c57152eed05ac65818bec4c3`  
		Last Modified: Thu, 05 Mar 2026 17:41:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc748eeebeae4273433e30e18300fbd26a410b6681961305d1969a2d5f47b94b`  
		Last Modified: Thu, 05 Mar 2026 17:41:58 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef509e18ceef2bc44d07b4769a5c1ea62c88fbf224b76b50743b6bf8c874e54`  
		Last Modified: Thu, 05 Mar 2026 17:41:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c13cb154389e12af7febe8186383b80ff142b1f76a656237b6f8be4f75c5bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322f4d2364692002b7ebd02d96fc9461961e5f878ee31ea97fd7cd5155e13b35`

```dockerfile
```

-	Layers:
	-	`sha256:47d86cf978c51e4ff8f7001c3887a6c7a5c0d5d3b32325a3432571ea0218283a`  
		Last Modified: Thu, 05 Mar 2026 17:42:00 GMT  
		Size: 61.7 MB (61708189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f9507427ea3e7fa71200704a0f354a93dfbea682d3d37f7be2c6b36407a09f`  
		Last Modified: Thu, 05 Mar 2026 17:41:55 GMT  
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
$ docker pull odoo@sha256:371e92a268be52d8c96f0212a2d46b34533f506441a738ef55009c99367a50bc
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
$ docker pull odoo@sha256:2bd06230d28d06d9e4844a4f1c8bcd55a478a81581b3057481e6338285e43662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680698019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d121b46b9b94e89c384c657c46583aea3d6d077411f0a20f1ba342b555b8da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:24 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:24 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:24 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:24 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:37 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:37 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:38:37 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:37 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:39:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e736e2b97ff94fcca9419d0e88c2c780af0b16939973d3b1f461b3042b45c`  
		Last Modified: Thu, 05 Mar 2026 17:42:08 GMT  
		Size: 253.0 MB (253032071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbca75105151c915a991284093974f715fd4ec8477dfb3cf9e17b439d01798c`  
		Last Modified: Thu, 05 Mar 2026 17:41:57 GMT  
		Size: 14.3 MB (14341200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f177b5ded5ee57bf31f5ba2894db031dc6d261d2915e6ea78adf0a9adaf0e29b`  
		Last Modified: Thu, 05 Mar 2026 17:41:55 GMT  
		Size: 479.6 KB (479585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b634dcbe4b49ec683dcaf37bb473898e852abc98dd79566816bd4550199bd8b7`  
		Last Modified: Thu, 05 Mar 2026 17:42:11 GMT  
		Size: 384.0 MB (383977601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efa25a2be210fb570e8d717652622e062cde458f4005ce16c844cda3056cb`  
		Last Modified: Thu, 05 Mar 2026 17:41:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146ad29140b458f6407f7ede0aba5878c6fe3b7c57152eed05ac65818bec4c3`  
		Last Modified: Thu, 05 Mar 2026 17:41:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc748eeebeae4273433e30e18300fbd26a410b6681961305d1969a2d5f47b94b`  
		Last Modified: Thu, 05 Mar 2026 17:41:58 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef509e18ceef2bc44d07b4769a5c1ea62c88fbf224b76b50743b6bf8c874e54`  
		Last Modified: Thu, 05 Mar 2026 17:41:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c13cb154389e12af7febe8186383b80ff142b1f76a656237b6f8be4f75c5bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322f4d2364692002b7ebd02d96fc9461961e5f878ee31ea97fd7cd5155e13b35`

```dockerfile
```

-	Layers:
	-	`sha256:47d86cf978c51e4ff8f7001c3887a6c7a5c0d5d3b32325a3432571ea0218283a`  
		Last Modified: Thu, 05 Mar 2026 17:42:00 GMT  
		Size: 61.7 MB (61708189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f9507427ea3e7fa71200704a0f354a93dfbea682d3d37f7be2c6b36407a09f`  
		Last Modified: Thu, 05 Mar 2026 17:41:55 GMT  
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
$ docker pull odoo@sha256:371e92a268be52d8c96f0212a2d46b34533f506441a738ef55009c99367a50bc
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
$ docker pull odoo@sha256:2bd06230d28d06d9e4844a4f1c8bcd55a478a81581b3057481e6338285e43662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680698019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d121b46b9b94e89c384c657c46583aea3d6d077411f0a20f1ba342b555b8da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:24 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:24 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:24 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:24 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:24 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:37 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:37 GMT
ENV ODOO_VERSION=18.0
# Thu, 05 Mar 2026 17:38:37 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:37 GMT
ARG ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
# Thu, 05 Mar 2026 17:39:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=b085e04780b300e662cd621bf7f7da7037214f30
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:47 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e736e2b97ff94fcca9419d0e88c2c780af0b16939973d3b1f461b3042b45c`  
		Last Modified: Thu, 05 Mar 2026 17:42:08 GMT  
		Size: 253.0 MB (253032071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbca75105151c915a991284093974f715fd4ec8477dfb3cf9e17b439d01798c`  
		Last Modified: Thu, 05 Mar 2026 17:41:57 GMT  
		Size: 14.3 MB (14341200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f177b5ded5ee57bf31f5ba2894db031dc6d261d2915e6ea78adf0a9adaf0e29b`  
		Last Modified: Thu, 05 Mar 2026 17:41:55 GMT  
		Size: 479.6 KB (479585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b634dcbe4b49ec683dcaf37bb473898e852abc98dd79566816bd4550199bd8b7`  
		Last Modified: Thu, 05 Mar 2026 17:42:11 GMT  
		Size: 384.0 MB (383977601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0efa25a2be210fb570e8d717652622e062cde458f4005ce16c844cda3056cb`  
		Last Modified: Thu, 05 Mar 2026 17:41:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146ad29140b458f6407f7ede0aba5878c6fe3b7c57152eed05ac65818bec4c3`  
		Last Modified: Thu, 05 Mar 2026 17:41:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc748eeebeae4273433e30e18300fbd26a410b6681961305d1969a2d5f47b94b`  
		Last Modified: Thu, 05 Mar 2026 17:41:58 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef509e18ceef2bc44d07b4769a5c1ea62c88fbf224b76b50743b6bf8c874e54`  
		Last Modified: Thu, 05 Mar 2026 17:41:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:c13cb154389e12af7febe8186383b80ff142b1f76a656237b6f8be4f75c5bebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322f4d2364692002b7ebd02d96fc9461961e5f878ee31ea97fd7cd5155e13b35`

```dockerfile
```

-	Layers:
	-	`sha256:47d86cf978c51e4ff8f7001c3887a6c7a5c0d5d3b32325a3432571ea0218283a`  
		Last Modified: Thu, 05 Mar 2026 17:42:00 GMT  
		Size: 61.7 MB (61708189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1f9507427ea3e7fa71200704a0f354a93dfbea682d3d37f7be2c6b36407a09f`  
		Last Modified: Thu, 05 Mar 2026 17:41:55 GMT  
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
$ docker pull odoo@sha256:fe9ce229f15bf4965e1526d8950cc67cd6682c72190d699e1737f66f8bf3d012
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
$ docker pull odoo@sha256:c74c3c0728ad97e295f67895d01f1bcd249457c04564c4cb164b758ed44c19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.3 MB (698312953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9171ea3ecfd22b2345d339d37c894b8e81edb661c16c2241773937697d417fb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:18 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:39:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f9535b3854e03c3a5265d8be2219b6d12ce8fe0f728b95a26d960071a266e`  
		Last Modified: Thu, 05 Mar 2026 17:42:12 GMT  
		Size: 253.0 MB (253031805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b6a091616c087a75a9c1c9c99802410afb6a8ea808d3dfa69c47b3b2561452`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 14.3 MB (14341237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682d925084e13b06c6b260550401c09d4f65cfbc1ef7898d890079dd2d68c65a`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd838b13d01151ba60e0c85ca71bc4a444ec44979df7a20095d47146531c65`  
		Last Modified: Thu, 05 Mar 2026 17:42:15 GMT  
		Size: 401.6 MB (401592772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409181d9d4e6122ed3575128ec1c061ff1ed8b7f9610ca9b40e6a917c28c189e`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1811634c85a782b2342ca241a3851da110b03a5b229673f0348ae0525e930daa`  
		Last Modified: Thu, 05 Mar 2026 17:42:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c778d0d183c43293f0a5a7a0077e07ce499b0845dd4278b751d54745193f77`  
		Last Modified: Thu, 05 Mar 2026 17:42:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa86bbbd7a0857033e246f0d52e1272a4efcf71b88f8c6871f8e28de233f863`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:b87b7234414966b57e33591fa8195a823af500e67e5e2de4e945f75ab730c795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98820a09abee6e6ee697190c23b017b4e4b6a5d7d7d5a16e39af2263071c1e7`

```dockerfile
```

-	Layers:
	-	`sha256:2205ccdbd2de3d9fbad6e3d4051a6b2c0c21de27f47ce398c42b19efdf0f4f27`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 69.9 MB (69880374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0b10579e3c78dc937fe33a1ddd010186244b82c1bfdaf4909770858129a1a8`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
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
$ docker pull odoo@sha256:fe9ce229f15bf4965e1526d8950cc67cd6682c72190d699e1737f66f8bf3d012
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
$ docker pull odoo@sha256:c74c3c0728ad97e295f67895d01f1bcd249457c04564c4cb164b758ed44c19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.3 MB (698312953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9171ea3ecfd22b2345d339d37c894b8e81edb661c16c2241773937697d417fb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:18 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:39:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f9535b3854e03c3a5265d8be2219b6d12ce8fe0f728b95a26d960071a266e`  
		Last Modified: Thu, 05 Mar 2026 17:42:12 GMT  
		Size: 253.0 MB (253031805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b6a091616c087a75a9c1c9c99802410afb6a8ea808d3dfa69c47b3b2561452`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 14.3 MB (14341237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682d925084e13b06c6b260550401c09d4f65cfbc1ef7898d890079dd2d68c65a`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd838b13d01151ba60e0c85ca71bc4a444ec44979df7a20095d47146531c65`  
		Last Modified: Thu, 05 Mar 2026 17:42:15 GMT  
		Size: 401.6 MB (401592772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409181d9d4e6122ed3575128ec1c061ff1ed8b7f9610ca9b40e6a917c28c189e`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1811634c85a782b2342ca241a3851da110b03a5b229673f0348ae0525e930daa`  
		Last Modified: Thu, 05 Mar 2026 17:42:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c778d0d183c43293f0a5a7a0077e07ce499b0845dd4278b751d54745193f77`  
		Last Modified: Thu, 05 Mar 2026 17:42:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa86bbbd7a0857033e246f0d52e1272a4efcf71b88f8c6871f8e28de233f863`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b87b7234414966b57e33591fa8195a823af500e67e5e2de4e945f75ab730c795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98820a09abee6e6ee697190c23b017b4e4b6a5d7d7d5a16e39af2263071c1e7`

```dockerfile
```

-	Layers:
	-	`sha256:2205ccdbd2de3d9fbad6e3d4051a6b2c0c21de27f47ce398c42b19efdf0f4f27`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 69.9 MB (69880374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0b10579e3c78dc937fe33a1ddd010186244b82c1bfdaf4909770858129a1a8`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
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
$ docker pull odoo@sha256:fe9ce229f15bf4965e1526d8950cc67cd6682c72190d699e1737f66f8bf3d012
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
$ docker pull odoo@sha256:c74c3c0728ad97e295f67895d01f1bcd249457c04564c4cb164b758ed44c19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.3 MB (698312953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9171ea3ecfd22b2345d339d37c894b8e81edb661c16c2241773937697d417fb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:18 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:39:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f9535b3854e03c3a5265d8be2219b6d12ce8fe0f728b95a26d960071a266e`  
		Last Modified: Thu, 05 Mar 2026 17:42:12 GMT  
		Size: 253.0 MB (253031805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b6a091616c087a75a9c1c9c99802410afb6a8ea808d3dfa69c47b3b2561452`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 14.3 MB (14341237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682d925084e13b06c6b260550401c09d4f65cfbc1ef7898d890079dd2d68c65a`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd838b13d01151ba60e0c85ca71bc4a444ec44979df7a20095d47146531c65`  
		Last Modified: Thu, 05 Mar 2026 17:42:15 GMT  
		Size: 401.6 MB (401592772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409181d9d4e6122ed3575128ec1c061ff1ed8b7f9610ca9b40e6a917c28c189e`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1811634c85a782b2342ca241a3851da110b03a5b229673f0348ae0525e930daa`  
		Last Modified: Thu, 05 Mar 2026 17:42:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c778d0d183c43293f0a5a7a0077e07ce499b0845dd4278b751d54745193f77`  
		Last Modified: Thu, 05 Mar 2026 17:42:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa86bbbd7a0857033e246f0d52e1272a4efcf71b88f8c6871f8e28de233f863`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260305` - unknown; unknown

```console
$ docker pull odoo@sha256:b87b7234414966b57e33591fa8195a823af500e67e5e2de4e945f75ab730c795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98820a09abee6e6ee697190c23b017b4e4b6a5d7d7d5a16e39af2263071c1e7`

```dockerfile
```

-	Layers:
	-	`sha256:2205ccdbd2de3d9fbad6e3d4051a6b2c0c21de27f47ce398c42b19efdf0f4f27`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 69.9 MB (69880374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0b10579e3c78dc937fe33a1ddd010186244b82c1bfdaf4909770858129a1a8`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
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
$ docker pull odoo@sha256:fe9ce229f15bf4965e1526d8950cc67cd6682c72190d699e1737f66f8bf3d012
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
$ docker pull odoo@sha256:c74c3c0728ad97e295f67895d01f1bcd249457c04564c4cb164b758ed44c19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.3 MB (698312953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9171ea3ecfd22b2345d339d37c894b8e81edb661c16c2241773937697d417fb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 05 Mar 2026 17:38:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 05 Mar 2026 17:38:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 05 Mar 2026 17:38:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 05 Mar 2026 17:38:18 GMT
ARG TARGETARCH=arm64
# Thu, 05 Mar 2026 17:38:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 05 Mar 2026 17:38:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 05 Mar 2026 17:38:27 GMT
ENV ODOO_VERSION=19.0
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_RELEASE=20260305
# Thu, 05 Mar 2026 17:38:27 GMT
ARG ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
# Thu, 05 Mar 2026 17:39:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260305 ODOO_SHA=6230161cecd093e01589589291ee66ba7bf7759d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 05 Mar 2026 17:39:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 05 Mar 2026 17:39:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 05 Mar 2026 17:39:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 05 Mar 2026 17:39:36 GMT
USER odoo
# Thu, 05 Mar 2026 17:39:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 17:39:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f9535b3854e03c3a5265d8be2219b6d12ce8fe0f728b95a26d960071a266e`  
		Last Modified: Thu, 05 Mar 2026 17:42:12 GMT  
		Size: 253.0 MB (253031805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b6a091616c087a75a9c1c9c99802410afb6a8ea808d3dfa69c47b3b2561452`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 14.3 MB (14341237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682d925084e13b06c6b260550401c09d4f65cfbc1ef7898d890079dd2d68c65a`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
		Size: 479.6 KB (479580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd838b13d01151ba60e0c85ca71bc4a444ec44979df7a20095d47146531c65`  
		Last Modified: Thu, 05 Mar 2026 17:42:15 GMT  
		Size: 401.6 MB (401592772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409181d9d4e6122ed3575128ec1c061ff1ed8b7f9610ca9b40e6a917c28c189e`  
		Last Modified: Thu, 05 Mar 2026 17:42:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1811634c85a782b2342ca241a3851da110b03a5b229673f0348ae0525e930daa`  
		Last Modified: Thu, 05 Mar 2026 17:42:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c778d0d183c43293f0a5a7a0077e07ce499b0845dd4278b751d54745193f77`  
		Last Modified: Thu, 05 Mar 2026 17:42:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa86bbbd7a0857033e246f0d52e1272a4efcf71b88f8c6871f8e28de233f863`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b87b7234414966b57e33591fa8195a823af500e67e5e2de4e945f75ab730c795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69907631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98820a09abee6e6ee697190c23b017b4e4b6a5d7d7d5a16e39af2263071c1e7`

```dockerfile
```

-	Layers:
	-	`sha256:2205ccdbd2de3d9fbad6e3d4051a6b2c0c21de27f47ce398c42b19efdf0f4f27`  
		Last Modified: Thu, 05 Mar 2026 17:42:07 GMT  
		Size: 69.9 MB (69880374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0b10579e3c78dc937fe33a1ddd010186244b82c1bfdaf4909770858129a1a8`  
		Last Modified: Thu, 05 Mar 2026 17:42:03 GMT  
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
