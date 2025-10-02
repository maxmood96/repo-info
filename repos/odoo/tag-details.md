<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250930`](#odoo170-20250930)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250930`](#odoo180-20250930)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20250930`](#odoo190-20250930)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:de9329abb4d41197bb414cf8f46d1f142ae9a3710446868c4ef6db83c0c2532b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:33508fe5b5790ebad1ff9f13e44d925562252fff496cccdfd5483c5ecc4cbb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605315986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbd556354d4a4aca336137a13f88fd9482591d8ca5de7626b3e60e98abddd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0143d45a9742e06d1ddfdfacbc76d73bad50cbf0a88693f5736ef27a8822146f`  
		Last Modified: Wed, 01 Oct 2025 13:24:07 GMT  
		Size: 233.8 MB (233818566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee454d2e10150da2ed1a9672ae93bffed0d9420f8f0a329532014e1da7ea9a6c`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 2.6 MB (2595034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba55e5494b271093840c256abe2f85ce6c71a6f6166ca75ad7c2fb37c0dde`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 480.2 KB (480223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcedcb43660704fbbdac273689679f3060f95da95681225987b1d8965761612`  
		Last Modified: Wed, 01 Oct 2025 13:24:09 GMT  
		Size: 338.9 MB (338882791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dc6a1065b1c7dec32da7e44d168b96eea544d214f4f02df17cdfb194b162`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b3768235d630dd2b0cccaa211b4ace3629fe9e61c9ce644276df8db8b410f`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31114a2b3fbce134fe11c7e64206fd2b41113fcc0d7123fadf08c042c405e30`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd0cf0ff7b57b1fcca8333395a75c1c44bb2585cc0b80d412730a22b5e0cef`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a120fb50d3db2c0689ef51b42e3dc9cdbf1005bcdcd2c1872efda07b318f600a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985c21374756f15c70efde989cb845baa73740d5f15b7b782626b213ac41953`

```dockerfile
```

-	Layers:
	-	`sha256:048b1713d485428416888cccfdc7014105402864dee4593c2bef5066cc02ba3a`  
		Last Modified: Wed, 01 Oct 2025 16:12:24 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3125e0679c12cf13a6f9fe6714daa453cb6f034c9daf88473a2ff0f055e2a88`  
		Last Modified: Wed, 01 Oct 2025 16:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0c7d6449e09c1cc5b094f0db4877b342f08f502d9218b9bde28b59f17d2bccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600135864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91c31242be97b32479e49e48ff742fb577943889392ef04bff7ae3009dd222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300193dc1f3067e8189fc775798f750a08d65d952a91a3c57b9b9e87e7f23906`  
		Last Modified: Thu, 02 Oct 2025 04:13:21 GMT  
		Size: 231.2 MB (231188183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeca8b8d3ada08f7ba0145f036b623880df3e89ebd6fcaea81a59bc0a4e3bcb`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 2.6 MB (2590480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699de0168c5dcbad014b961839eacf1352e7b89b8bb3af44a5d9a21995230db3`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 480.3 KB (480268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99469e55203057ec1f2d1979c81a02c8035510282c35c43b4f0f4236adfdd`  
		Last Modified: Thu, 02 Oct 2025 01:31:28 GMT  
		Size: 338.5 MB (338491389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bf4370ad47631586284107342893b8806c63d7b2802697fa23663c7615e06`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1c8f002f5bb791c8f036293b5292d614787b56a0f47735c946dbe973674e8`  
		Last Modified: Thu, 02 Oct 2025 02:14:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf3a7ca8466df25bc37e2adda3c7e66acf80974d1fcdd415c70c6f3bddca07`  
		Last Modified: Thu, 02 Oct 2025 02:14:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea36c31ebd1891d8fa1e9cd399f857fdb2d6f0ddc66a571944f2cc7dda583fa`  
		Last Modified: Thu, 02 Oct 2025 02:14:52 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:08dc7b07f81b8fefb121e5d0a2a6e9739d6d9dd05ae606bf6a79ceb9c6bbddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ba7af616a61e2402d176eb870885ac1d2376f0c8bc9d160a375779bc708ff`

```dockerfile
```

-	Layers:
	-	`sha256:373bdf49d9d29f44523b1dc2baee58991f9871679760e2935c3edfc269b90a73`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599495707f89ef59c9cc38a481902dc50fa7deb94b6d37cc47007e74e18f3a83`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:de9329abb4d41197bb414cf8f46d1f142ae9a3710446868c4ef6db83c0c2532b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:33508fe5b5790ebad1ff9f13e44d925562252fff496cccdfd5483c5ecc4cbb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605315986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbd556354d4a4aca336137a13f88fd9482591d8ca5de7626b3e60e98abddd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0143d45a9742e06d1ddfdfacbc76d73bad50cbf0a88693f5736ef27a8822146f`  
		Last Modified: Wed, 01 Oct 2025 13:24:07 GMT  
		Size: 233.8 MB (233818566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee454d2e10150da2ed1a9672ae93bffed0d9420f8f0a329532014e1da7ea9a6c`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 2.6 MB (2595034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba55e5494b271093840c256abe2f85ce6c71a6f6166ca75ad7c2fb37c0dde`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 480.2 KB (480223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcedcb43660704fbbdac273689679f3060f95da95681225987b1d8965761612`  
		Last Modified: Wed, 01 Oct 2025 13:24:09 GMT  
		Size: 338.9 MB (338882791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dc6a1065b1c7dec32da7e44d168b96eea544d214f4f02df17cdfb194b162`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b3768235d630dd2b0cccaa211b4ace3629fe9e61c9ce644276df8db8b410f`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31114a2b3fbce134fe11c7e64206fd2b41113fcc0d7123fadf08c042c405e30`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd0cf0ff7b57b1fcca8333395a75c1c44bb2585cc0b80d412730a22b5e0cef`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a120fb50d3db2c0689ef51b42e3dc9cdbf1005bcdcd2c1872efda07b318f600a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985c21374756f15c70efde989cb845baa73740d5f15b7b782626b213ac41953`

```dockerfile
```

-	Layers:
	-	`sha256:048b1713d485428416888cccfdc7014105402864dee4593c2bef5066cc02ba3a`  
		Last Modified: Wed, 01 Oct 2025 16:12:24 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3125e0679c12cf13a6f9fe6714daa453cb6f034c9daf88473a2ff0f055e2a88`  
		Last Modified: Wed, 01 Oct 2025 16:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0c7d6449e09c1cc5b094f0db4877b342f08f502d9218b9bde28b59f17d2bccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600135864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91c31242be97b32479e49e48ff742fb577943889392ef04bff7ae3009dd222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300193dc1f3067e8189fc775798f750a08d65d952a91a3c57b9b9e87e7f23906`  
		Last Modified: Thu, 02 Oct 2025 04:13:21 GMT  
		Size: 231.2 MB (231188183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeca8b8d3ada08f7ba0145f036b623880df3e89ebd6fcaea81a59bc0a4e3bcb`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 2.6 MB (2590480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699de0168c5dcbad014b961839eacf1352e7b89b8bb3af44a5d9a21995230db3`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 480.3 KB (480268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99469e55203057ec1f2d1979c81a02c8035510282c35c43b4f0f4236adfdd`  
		Last Modified: Thu, 02 Oct 2025 01:31:28 GMT  
		Size: 338.5 MB (338491389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bf4370ad47631586284107342893b8806c63d7b2802697fa23663c7615e06`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1c8f002f5bb791c8f036293b5292d614787b56a0f47735c946dbe973674e8`  
		Last Modified: Thu, 02 Oct 2025 02:14:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf3a7ca8466df25bc37e2adda3c7e66acf80974d1fcdd415c70c6f3bddca07`  
		Last Modified: Thu, 02 Oct 2025 02:14:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea36c31ebd1891d8fa1e9cd399f857fdb2d6f0ddc66a571944f2cc7dda583fa`  
		Last Modified: Thu, 02 Oct 2025 02:14:52 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:08dc7b07f81b8fefb121e5d0a2a6e9739d6d9dd05ae606bf6a79ceb9c6bbddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ba7af616a61e2402d176eb870885ac1d2376f0c8bc9d160a375779bc708ff`

```dockerfile
```

-	Layers:
	-	`sha256:373bdf49d9d29f44523b1dc2baee58991f9871679760e2935c3edfc269b90a73`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599495707f89ef59c9cc38a481902dc50fa7deb94b6d37cc47007e74e18f3a83`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250930`

```console
$ docker pull odoo@sha256:de9329abb4d41197bb414cf8f46d1f142ae9a3710446868c4ef6db83c0c2532b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:33508fe5b5790ebad1ff9f13e44d925562252fff496cccdfd5483c5ecc4cbb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605315986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbd556354d4a4aca336137a13f88fd9482591d8ca5de7626b3e60e98abddd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0143d45a9742e06d1ddfdfacbc76d73bad50cbf0a88693f5736ef27a8822146f`  
		Last Modified: Wed, 01 Oct 2025 13:24:07 GMT  
		Size: 233.8 MB (233818566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee454d2e10150da2ed1a9672ae93bffed0d9420f8f0a329532014e1da7ea9a6c`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 2.6 MB (2595034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba55e5494b271093840c256abe2f85ce6c71a6f6166ca75ad7c2fb37c0dde`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 480.2 KB (480223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcedcb43660704fbbdac273689679f3060f95da95681225987b1d8965761612`  
		Last Modified: Wed, 01 Oct 2025 13:24:09 GMT  
		Size: 338.9 MB (338882791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dc6a1065b1c7dec32da7e44d168b96eea544d214f4f02df17cdfb194b162`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b3768235d630dd2b0cccaa211b4ace3629fe9e61c9ce644276df8db8b410f`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31114a2b3fbce134fe11c7e64206fd2b41113fcc0d7123fadf08c042c405e30`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd0cf0ff7b57b1fcca8333395a75c1c44bb2585cc0b80d412730a22b5e0cef`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:a120fb50d3db2c0689ef51b42e3dc9cdbf1005bcdcd2c1872efda07b318f600a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985c21374756f15c70efde989cb845baa73740d5f15b7b782626b213ac41953`

```dockerfile
```

-	Layers:
	-	`sha256:048b1713d485428416888cccfdc7014105402864dee4593c2bef5066cc02ba3a`  
		Last Modified: Wed, 01 Oct 2025 16:12:24 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3125e0679c12cf13a6f9fe6714daa453cb6f034c9daf88473a2ff0f055e2a88`  
		Last Modified: Wed, 01 Oct 2025 16:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0c7d6449e09c1cc5b094f0db4877b342f08f502d9218b9bde28b59f17d2bccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600135864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91c31242be97b32479e49e48ff742fb577943889392ef04bff7ae3009dd222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300193dc1f3067e8189fc775798f750a08d65d952a91a3c57b9b9e87e7f23906`  
		Last Modified: Thu, 02 Oct 2025 04:13:21 GMT  
		Size: 231.2 MB (231188183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeca8b8d3ada08f7ba0145f036b623880df3e89ebd6fcaea81a59bc0a4e3bcb`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 2.6 MB (2590480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699de0168c5dcbad014b961839eacf1352e7b89b8bb3af44a5d9a21995230db3`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 480.3 KB (480268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99469e55203057ec1f2d1979c81a02c8035510282c35c43b4f0f4236adfdd`  
		Last Modified: Thu, 02 Oct 2025 01:31:28 GMT  
		Size: 338.5 MB (338491389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bf4370ad47631586284107342893b8806c63d7b2802697fa23663c7615e06`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1c8f002f5bb791c8f036293b5292d614787b56a0f47735c946dbe973674e8`  
		Last Modified: Thu, 02 Oct 2025 02:14:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf3a7ca8466df25bc37e2adda3c7e66acf80974d1fcdd415c70c6f3bddca07`  
		Last Modified: Thu, 02 Oct 2025 02:14:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea36c31ebd1891d8fa1e9cd399f857fdb2d6f0ddc66a571944f2cc7dda583fa`  
		Last Modified: Thu, 02 Oct 2025 02:14:52 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:08dc7b07f81b8fefb121e5d0a2a6e9739d6d9dd05ae606bf6a79ceb9c6bbddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ba7af616a61e2402d176eb870885ac1d2376f0c8bc9d160a375779bc708ff`

```dockerfile
```

-	Layers:
	-	`sha256:373bdf49d9d29f44523b1dc2baee58991f9871679760e2935c3edfc269b90a73`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599495707f89ef59c9cc38a481902dc50fa7deb94b6d37cc47007e74e18f3a83`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:4a31e4e46b4f99338202339232f21c89730fb7a2369d0d7142f64d7e4f230b39
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
$ docker pull odoo@sha256:ae693d1d13f22f784d2a60698980fd6d89bcbee9c620b43d8de3c5d2d02f3e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676985310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0743d582402fa9a2adafc0019181e1703bde6203b08ef8ae66a3162c9f90f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c780b4ec78ec55b2bc8d6396642109b472b845987c507c55fd6681c261b3f6`  
		Last Modified: Wed, 01 Oct 2025 16:13:06 GMT  
		Size: 254.6 MB (254558403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc840923a8b46aeeb85f244632220891a12af3d147c1ca2b561a2272190312`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 14.3 MB (14339224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a307b3c18d23bb86824b608d0a0f118c5c6512684bb9aa12ba58e44a185ffa1`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 480.0 KB (480048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b088ff29347cbb747d087736e7a1a1fec1375f54a1752febd10c89d5820fcc`  
		Last Modified: Wed, 01 Oct 2025 16:13:11 GMT  
		Size: 377.9 MB (377881749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f7344c5291479931b480ae3093b47cde4aa8351e2a5002f78533619813db0`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05840729df4e10d79d6dac6ce9688776e0f9b1ec9e1d6a6bee6ebe7f7be458`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c187a6867248eb35520fe145120dc69c4b09e2993f97b5546cf06b0dc89040e`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d44d8995ecf99415603813ee414df719f1a6e3a71da704dacee6758ecf5cae`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:71e55157cc87d0c04e38118fcb7fd530429bef3867a8946772c5eb0d5ebab3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279eaccd1cde500c026ff832785f2d1d6f5c8897f28372b06cd05ca65ab54d7`

```dockerfile
```

-	Layers:
	-	`sha256:9ca83d072da7043ce952f9f7d2602341cf00856482b446d986be54ee3dc448ab`  
		Last Modified: Wed, 01 Oct 2025 16:12:33 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbd949cae4c497b0ec4b8fd1573fa9064f704ea57ad33a08aa1ceda604300de`  
		Last Modified: Wed, 01 Oct 2025 16:12:34 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0fa66f6d7b330830194b975496e69d54c59c346046d656bc25ad37d06357175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675597933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8ce80de18b947e034f7d2b8b71f080fc50692513e6e6446d38181f572d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3b4d011173c8f10be11a9ca76ac9af624f8c86c20474f6295f4072884d571`  
		Last Modified: Thu, 02 Oct 2025 04:13:17 GMT  
		Size: 254.2 MB (254201580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b841d36c3f7927cf9372c9179a26e3ad7b96e087d61987e4c3c93d130d0aba`  
		Last Modified: Thu, 02 Oct 2025 01:32:57 GMT  
		Size: 14.3 MB (14320187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ad74359b046bf5040462407d27aa5fdd24a831bba4020936ec64aa14aac0`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 480.0 KB (480010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a91a39f8ea3b3282c2f51da9c659b946e404d6006df059a8388971001bc30`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 377.7 MB (377732137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4859d7c464de422a075630e2ca4ce2be8d286ddedd847194c281a6a018bb9`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16fba96da2d114e024b8969703d742a179c5edec8a48f7633c79f79c28112f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88838d06b3d99b248a7040036e7c886b100b1bd9439a2bbe2557dd3601b2ee`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47db1384a0142d3ee7911da18de5e07c1e589452f2576c819808b679e5ca736`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:78d03bf942d9e0773375e3b891c67e19dd658088925f87ecf4725b41a235fc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f074c932f41b6417b4174a6101df0e73cb23cc333da764ab353d809a1c6fe5`

```dockerfile
```

-	Layers:
	-	`sha256:a44ec6ad328ae44c0999f11d6522aa0baf6d0dd292ee91500f7d6123291374f9`  
		Last Modified: Thu, 02 Oct 2025 04:14:06 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3455ba7fc1d3e481b7f5d5b7ab6a39aaf4fe4690a1f5affc8bcfe6409bc8cfd6`  
		Last Modified: Thu, 02 Oct 2025 04:14:08 GMT  
		Size: 27.0 KB (26993 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:a031fc8224c3c0e855415c69c5e8ba29f17e34ee47ed105ab8cc3a7008098966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3871ab77cf8d77d84740eac9945b539221876dc1d88d090723ba9f3c46ade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace7e0079a18dcf2384ec390ef90a5595128c1ea5cdcf8e5e22341a2d14dc18`  
		Last Modified: Thu, 02 Oct 2025 03:44:06 GMT  
		Size: 378.4 MB (378416838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774389e9d09b12a08960d8c8d4534f9cbc06ebc46c34de3d20f84fc33000d38`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ee5ca7ac877067f6a36562c78acb8d9a37ee3d26f4c13b70a202af84ba047`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a1090c9c1b8a9ed22ad3d9bbaafbe9c28dec0b18f25dea14862aba04c37a3`  
		Last Modified: Thu, 02 Oct 2025 03:43:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f4baba2896d6bf766aeab8aab6f5c95c6df77bceec7e6e9fb3ecc152fc6a8`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:e037e7ecf5829f94b0c0b6181b01bf014f812b2feed85cf950a43d34309e99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e90c59b5760cf46a5c5f609a411697a5c883c9f3675644744e08ef76072e7`

```dockerfile
```

-	Layers:
	-	`sha256:579761d83a62501577858d8099a228f604c49d1fa1a6ef6f6afa7f58d4ccd158`  
		Last Modified: Thu, 02 Oct 2025 04:15:53 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44edf985b4203c665ee17b86f252c11b6a52dfcbd3ac84395674243f342979a5`  
		Last Modified: Thu, 02 Oct 2025 04:15:54 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:4a31e4e46b4f99338202339232f21c89730fb7a2369d0d7142f64d7e4f230b39
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
$ docker pull odoo@sha256:ae693d1d13f22f784d2a60698980fd6d89bcbee9c620b43d8de3c5d2d02f3e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676985310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0743d582402fa9a2adafc0019181e1703bde6203b08ef8ae66a3162c9f90f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c780b4ec78ec55b2bc8d6396642109b472b845987c507c55fd6681c261b3f6`  
		Last Modified: Wed, 01 Oct 2025 16:13:06 GMT  
		Size: 254.6 MB (254558403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc840923a8b46aeeb85f244632220891a12af3d147c1ca2b561a2272190312`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 14.3 MB (14339224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a307b3c18d23bb86824b608d0a0f118c5c6512684bb9aa12ba58e44a185ffa1`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 480.0 KB (480048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b088ff29347cbb747d087736e7a1a1fec1375f54a1752febd10c89d5820fcc`  
		Last Modified: Wed, 01 Oct 2025 16:13:11 GMT  
		Size: 377.9 MB (377881749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f7344c5291479931b480ae3093b47cde4aa8351e2a5002f78533619813db0`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05840729df4e10d79d6dac6ce9688776e0f9b1ec9e1d6a6bee6ebe7f7be458`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c187a6867248eb35520fe145120dc69c4b09e2993f97b5546cf06b0dc89040e`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d44d8995ecf99415603813ee414df719f1a6e3a71da704dacee6758ecf5cae`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:71e55157cc87d0c04e38118fcb7fd530429bef3867a8946772c5eb0d5ebab3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279eaccd1cde500c026ff832785f2d1d6f5c8897f28372b06cd05ca65ab54d7`

```dockerfile
```

-	Layers:
	-	`sha256:9ca83d072da7043ce952f9f7d2602341cf00856482b446d986be54ee3dc448ab`  
		Last Modified: Wed, 01 Oct 2025 16:12:33 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbd949cae4c497b0ec4b8fd1573fa9064f704ea57ad33a08aa1ceda604300de`  
		Last Modified: Wed, 01 Oct 2025 16:12:34 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0fa66f6d7b330830194b975496e69d54c59c346046d656bc25ad37d06357175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675597933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8ce80de18b947e034f7d2b8b71f080fc50692513e6e6446d38181f572d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3b4d011173c8f10be11a9ca76ac9af624f8c86c20474f6295f4072884d571`  
		Last Modified: Thu, 02 Oct 2025 04:13:17 GMT  
		Size: 254.2 MB (254201580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b841d36c3f7927cf9372c9179a26e3ad7b96e087d61987e4c3c93d130d0aba`  
		Last Modified: Thu, 02 Oct 2025 01:32:57 GMT  
		Size: 14.3 MB (14320187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ad74359b046bf5040462407d27aa5fdd24a831bba4020936ec64aa14aac0`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 480.0 KB (480010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a91a39f8ea3b3282c2f51da9c659b946e404d6006df059a8388971001bc30`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 377.7 MB (377732137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4859d7c464de422a075630e2ca4ce2be8d286ddedd847194c281a6a018bb9`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16fba96da2d114e024b8969703d742a179c5edec8a48f7633c79f79c28112f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88838d06b3d99b248a7040036e7c886b100b1bd9439a2bbe2557dd3601b2ee`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47db1384a0142d3ee7911da18de5e07c1e589452f2576c819808b679e5ca736`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78d03bf942d9e0773375e3b891c67e19dd658088925f87ecf4725b41a235fc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f074c932f41b6417b4174a6101df0e73cb23cc333da764ab353d809a1c6fe5`

```dockerfile
```

-	Layers:
	-	`sha256:a44ec6ad328ae44c0999f11d6522aa0baf6d0dd292ee91500f7d6123291374f9`  
		Last Modified: Thu, 02 Oct 2025 04:14:06 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3455ba7fc1d3e481b7f5d5b7ab6a39aaf4fe4690a1f5affc8bcfe6409bc8cfd6`  
		Last Modified: Thu, 02 Oct 2025 04:14:08 GMT  
		Size: 27.0 KB (26993 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a031fc8224c3c0e855415c69c5e8ba29f17e34ee47ed105ab8cc3a7008098966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3871ab77cf8d77d84740eac9945b539221876dc1d88d090723ba9f3c46ade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace7e0079a18dcf2384ec390ef90a5595128c1ea5cdcf8e5e22341a2d14dc18`  
		Last Modified: Thu, 02 Oct 2025 03:44:06 GMT  
		Size: 378.4 MB (378416838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774389e9d09b12a08960d8c8d4534f9cbc06ebc46c34de3d20f84fc33000d38`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ee5ca7ac877067f6a36562c78acb8d9a37ee3d26f4c13b70a202af84ba047`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a1090c9c1b8a9ed22ad3d9bbaafbe9c28dec0b18f25dea14862aba04c37a3`  
		Last Modified: Thu, 02 Oct 2025 03:43:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f4baba2896d6bf766aeab8aab6f5c95c6df77bceec7e6e9fb3ecc152fc6a8`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e037e7ecf5829f94b0c0b6181b01bf014f812b2feed85cf950a43d34309e99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e90c59b5760cf46a5c5f609a411697a5c883c9f3675644744e08ef76072e7`

```dockerfile
```

-	Layers:
	-	`sha256:579761d83a62501577858d8099a228f604c49d1fa1a6ef6f6afa7f58d4ccd158`  
		Last Modified: Thu, 02 Oct 2025 04:15:53 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44edf985b4203c665ee17b86f252c11b6a52dfcbd3ac84395674243f342979a5`  
		Last Modified: Thu, 02 Oct 2025 04:15:54 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250930`

```console
$ docker pull odoo@sha256:4a31e4e46b4f99338202339232f21c89730fb7a2369d0d7142f64d7e4f230b39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:ae693d1d13f22f784d2a60698980fd6d89bcbee9c620b43d8de3c5d2d02f3e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676985310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0743d582402fa9a2adafc0019181e1703bde6203b08ef8ae66a3162c9f90f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c780b4ec78ec55b2bc8d6396642109b472b845987c507c55fd6681c261b3f6`  
		Last Modified: Wed, 01 Oct 2025 16:13:06 GMT  
		Size: 254.6 MB (254558403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc840923a8b46aeeb85f244632220891a12af3d147c1ca2b561a2272190312`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 14.3 MB (14339224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a307b3c18d23bb86824b608d0a0f118c5c6512684bb9aa12ba58e44a185ffa1`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 480.0 KB (480048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b088ff29347cbb747d087736e7a1a1fec1375f54a1752febd10c89d5820fcc`  
		Last Modified: Wed, 01 Oct 2025 16:13:11 GMT  
		Size: 377.9 MB (377881749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f7344c5291479931b480ae3093b47cde4aa8351e2a5002f78533619813db0`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05840729df4e10d79d6dac6ce9688776e0f9b1ec9e1d6a6bee6ebe7f7be458`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c187a6867248eb35520fe145120dc69c4b09e2993f97b5546cf06b0dc89040e`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d44d8995ecf99415603813ee414df719f1a6e3a71da704dacee6758ecf5cae`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:71e55157cc87d0c04e38118fcb7fd530429bef3867a8946772c5eb0d5ebab3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279eaccd1cde500c026ff832785f2d1d6f5c8897f28372b06cd05ca65ab54d7`

```dockerfile
```

-	Layers:
	-	`sha256:9ca83d072da7043ce952f9f7d2602341cf00856482b446d986be54ee3dc448ab`  
		Last Modified: Wed, 01 Oct 2025 16:12:33 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbd949cae4c497b0ec4b8fd1573fa9064f704ea57ad33a08aa1ceda604300de`  
		Last Modified: Wed, 01 Oct 2025 16:12:34 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0fa66f6d7b330830194b975496e69d54c59c346046d656bc25ad37d06357175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675597933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8ce80de18b947e034f7d2b8b71f080fc50692513e6e6446d38181f572d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3b4d011173c8f10be11a9ca76ac9af624f8c86c20474f6295f4072884d571`  
		Last Modified: Thu, 02 Oct 2025 04:13:17 GMT  
		Size: 254.2 MB (254201580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b841d36c3f7927cf9372c9179a26e3ad7b96e087d61987e4c3c93d130d0aba`  
		Last Modified: Thu, 02 Oct 2025 01:32:57 GMT  
		Size: 14.3 MB (14320187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ad74359b046bf5040462407d27aa5fdd24a831bba4020936ec64aa14aac0`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 480.0 KB (480010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a91a39f8ea3b3282c2f51da9c659b946e404d6006df059a8388971001bc30`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 377.7 MB (377732137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4859d7c464de422a075630e2ca4ce2be8d286ddedd847194c281a6a018bb9`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16fba96da2d114e024b8969703d742a179c5edec8a48f7633c79f79c28112f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88838d06b3d99b248a7040036e7c886b100b1bd9439a2bbe2557dd3601b2ee`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47db1384a0142d3ee7911da18de5e07c1e589452f2576c819808b679e5ca736`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:78d03bf942d9e0773375e3b891c67e19dd658088925f87ecf4725b41a235fc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f074c932f41b6417b4174a6101df0e73cb23cc333da764ab353d809a1c6fe5`

```dockerfile
```

-	Layers:
	-	`sha256:a44ec6ad328ae44c0999f11d6522aa0baf6d0dd292ee91500f7d6123291374f9`  
		Last Modified: Thu, 02 Oct 2025 04:14:06 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3455ba7fc1d3e481b7f5d5b7ab6a39aaf4fe4690a1f5affc8bcfe6409bc8cfd6`  
		Last Modified: Thu, 02 Oct 2025 04:14:08 GMT  
		Size: 27.0 KB (26993 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250930` - linux; ppc64le

```console
$ docker pull odoo@sha256:a031fc8224c3c0e855415c69c5e8ba29f17e34ee47ed105ab8cc3a7008098966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3871ab77cf8d77d84740eac9945b539221876dc1d88d090723ba9f3c46ade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace7e0079a18dcf2384ec390ef90a5595128c1ea5cdcf8e5e22341a2d14dc18`  
		Last Modified: Thu, 02 Oct 2025 03:44:06 GMT  
		Size: 378.4 MB (378416838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774389e9d09b12a08960d8c8d4534f9cbc06ebc46c34de3d20f84fc33000d38`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ee5ca7ac877067f6a36562c78acb8d9a37ee3d26f4c13b70a202af84ba047`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a1090c9c1b8a9ed22ad3d9bbaafbe9c28dec0b18f25dea14862aba04c37a3`  
		Last Modified: Thu, 02 Oct 2025 03:43:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f4baba2896d6bf766aeab8aab6f5c95c6df77bceec7e6e9fb3ecc152fc6a8`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:e037e7ecf5829f94b0c0b6181b01bf014f812b2feed85cf950a43d34309e99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e90c59b5760cf46a5c5f609a411697a5c883c9f3675644744e08ef76072e7`

```dockerfile
```

-	Layers:
	-	`sha256:579761d83a62501577858d8099a228f604c49d1fa1a6ef6f6afa7f58d4ccd158`  
		Last Modified: Thu, 02 Oct 2025 04:15:53 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44edf985b4203c665ee17b86f252c11b6a52dfcbd3ac84395674243f342979a5`  
		Last Modified: Thu, 02 Oct 2025 04:15:54 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:15a1e852727e2e9952a1e8b138f5bd0a2234c012684f4fff6124563a54e8bd0f
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
$ docker pull odoo@sha256:36da9378d08bfec1f42f975ffa53bd2e10928b7ecf8a778806b74b1994d298d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678341469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2e59f5c2b599195f9377997858b3c78588120f358e991cc89e9fa4c591fbb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78717648042f04d1bc55296335cdfd48309babd6d29ee245d8994c9eb6bfaa2e`  
		Last Modified: Wed, 01 Oct 2025 16:13:24 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e662152c908a8e728eefe42676ce8f7a1c2c98bc14462d1915f0acda428398`  
		Last Modified: Wed, 01 Oct 2025 05:10:08 GMT  
		Size: 14.3 MB (14339116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e8b0d104998320a5f4e08c7d94523fa8fd70bdae5ace26960207267cc45d4`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c290470ff834642941deb9bfd3cb197eaa3bfad5ee4e190334c647ea7189c72`  
		Last Modified: Wed, 01 Oct 2025 16:13:53 GMT  
		Size: 379.2 MB (379238542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67cf444b63eb2547b2204d181e763a34da5f6068d4ca21659793e60010e1661`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581327cc3459dbcd9847df406a552ad459447a4597e980c608ff70c5d205e28`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b6f8015343e394ad0a2efc552051c9f9c6853292461b15b2c598f2edd8b6d`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b01163d7f3be00d9fcb082594052820d6997b08b311d209bfe0df01b99302`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f800547caf96d0a22ada9a6a31715bbdcca06d9d9b0c92cca9a0e97775916ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add45288c9f74d7603471ef18cbc35065bf010e42ea23ab850930f04cae3e4a7`

```dockerfile
```

-	Layers:
	-	`sha256:84ff58b3695834647b23762d73cd8ffd7a6a74e479f4e9b55335860ead281be0`  
		Last Modified: Wed, 01 Oct 2025 16:12:43 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23dd0dc27c53023978fd555939620d6626540546d861c75cafd8ebb1aeecd9b`  
		Last Modified: Wed, 01 Oct 2025 16:12:45 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:15a1e852727e2e9952a1e8b138f5bd0a2234c012684f4fff6124563a54e8bd0f
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
$ docker pull odoo@sha256:36da9378d08bfec1f42f975ffa53bd2e10928b7ecf8a778806b74b1994d298d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678341469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2e59f5c2b599195f9377997858b3c78588120f358e991cc89e9fa4c591fbb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78717648042f04d1bc55296335cdfd48309babd6d29ee245d8994c9eb6bfaa2e`  
		Last Modified: Wed, 01 Oct 2025 16:13:24 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e662152c908a8e728eefe42676ce8f7a1c2c98bc14462d1915f0acda428398`  
		Last Modified: Wed, 01 Oct 2025 05:10:08 GMT  
		Size: 14.3 MB (14339116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e8b0d104998320a5f4e08c7d94523fa8fd70bdae5ace26960207267cc45d4`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c290470ff834642941deb9bfd3cb197eaa3bfad5ee4e190334c647ea7189c72`  
		Last Modified: Wed, 01 Oct 2025 16:13:53 GMT  
		Size: 379.2 MB (379238542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67cf444b63eb2547b2204d181e763a34da5f6068d4ca21659793e60010e1661`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581327cc3459dbcd9847df406a552ad459447a4597e980c608ff70c5d205e28`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b6f8015343e394ad0a2efc552051c9f9c6853292461b15b2c598f2edd8b6d`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b01163d7f3be00d9fcb082594052820d6997b08b311d209bfe0df01b99302`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f800547caf96d0a22ada9a6a31715bbdcca06d9d9b0c92cca9a0e97775916ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add45288c9f74d7603471ef18cbc35065bf010e42ea23ab850930f04cae3e4a7`

```dockerfile
```

-	Layers:
	-	`sha256:84ff58b3695834647b23762d73cd8ffd7a6a74e479f4e9b55335860ead281be0`  
		Last Modified: Wed, 01 Oct 2025 16:12:43 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23dd0dc27c53023978fd555939620d6626540546d861c75cafd8ebb1aeecd9b`  
		Last Modified: Wed, 01 Oct 2025 16:12:45 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20250930`

```console
$ docker pull odoo@sha256:15a1e852727e2e9952a1e8b138f5bd0a2234c012684f4fff6124563a54e8bd0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:36da9378d08bfec1f42f975ffa53bd2e10928b7ecf8a778806b74b1994d298d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678341469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2e59f5c2b599195f9377997858b3c78588120f358e991cc89e9fa4c591fbb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78717648042f04d1bc55296335cdfd48309babd6d29ee245d8994c9eb6bfaa2e`  
		Last Modified: Wed, 01 Oct 2025 16:13:24 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e662152c908a8e728eefe42676ce8f7a1c2c98bc14462d1915f0acda428398`  
		Last Modified: Wed, 01 Oct 2025 05:10:08 GMT  
		Size: 14.3 MB (14339116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e8b0d104998320a5f4e08c7d94523fa8fd70bdae5ace26960207267cc45d4`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c290470ff834642941deb9bfd3cb197eaa3bfad5ee4e190334c647ea7189c72`  
		Last Modified: Wed, 01 Oct 2025 16:13:53 GMT  
		Size: 379.2 MB (379238542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67cf444b63eb2547b2204d181e763a34da5f6068d4ca21659793e60010e1661`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581327cc3459dbcd9847df406a552ad459447a4597e980c608ff70c5d205e28`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b6f8015343e394ad0a2efc552051c9f9c6853292461b15b2c598f2edd8b6d`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b01163d7f3be00d9fcb082594052820d6997b08b311d209bfe0df01b99302`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:f800547caf96d0a22ada9a6a31715bbdcca06d9d9b0c92cca9a0e97775916ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add45288c9f74d7603471ef18cbc35065bf010e42ea23ab850930f04cae3e4a7`

```dockerfile
```

-	Layers:
	-	`sha256:84ff58b3695834647b23762d73cd8ffd7a6a74e479f4e9b55335860ead281be0`  
		Last Modified: Wed, 01 Oct 2025 16:12:43 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23dd0dc27c53023978fd555939620d6626540546d861c75cafd8ebb1aeecd9b`  
		Last Modified: Wed, 01 Oct 2025 16:12:45 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250930` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:15a1e852727e2e9952a1e8b138f5bd0a2234c012684f4fff6124563a54e8bd0f
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
$ docker pull odoo@sha256:36da9378d08bfec1f42f975ffa53bd2e10928b7ecf8a778806b74b1994d298d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678341469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2e59f5c2b599195f9377997858b3c78588120f358e991cc89e9fa4c591fbb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78717648042f04d1bc55296335cdfd48309babd6d29ee245d8994c9eb6bfaa2e`  
		Last Modified: Wed, 01 Oct 2025 16:13:24 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e662152c908a8e728eefe42676ce8f7a1c2c98bc14462d1915f0acda428398`  
		Last Modified: Wed, 01 Oct 2025 05:10:08 GMT  
		Size: 14.3 MB (14339116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e8b0d104998320a5f4e08c7d94523fa8fd70bdae5ace26960207267cc45d4`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c290470ff834642941deb9bfd3cb197eaa3bfad5ee4e190334c647ea7189c72`  
		Last Modified: Wed, 01 Oct 2025 16:13:53 GMT  
		Size: 379.2 MB (379238542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67cf444b63eb2547b2204d181e763a34da5f6068d4ca21659793e60010e1661`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581327cc3459dbcd9847df406a552ad459447a4597e980c608ff70c5d205e28`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b6f8015343e394ad0a2efc552051c9f9c6853292461b15b2c598f2edd8b6d`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b01163d7f3be00d9fcb082594052820d6997b08b311d209bfe0df01b99302`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f800547caf96d0a22ada9a6a31715bbdcca06d9d9b0c92cca9a0e97775916ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add45288c9f74d7603471ef18cbc35065bf010e42ea23ab850930f04cae3e4a7`

```dockerfile
```

-	Layers:
	-	`sha256:84ff58b3695834647b23762d73cd8ffd7a6a74e479f4e9b55335860ead281be0`  
		Last Modified: Wed, 01 Oct 2025 16:12:43 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23dd0dc27c53023978fd555939620d6626540546d861c75cafd8ebb1aeecd9b`  
		Last Modified: Wed, 01 Oct 2025 16:12:45 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
