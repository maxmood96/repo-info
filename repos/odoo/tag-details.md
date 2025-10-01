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
$ docker pull odoo@sha256:7373edbfc5a7fadab9976c6c984c8018cfe9226257a55736a2cf4330d29ece97
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
$ docker pull odoo@sha256:cdd33bea26fc1f4a877c560c6f22b27431729bc6e9efb42bb5b988d610a7469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599903358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ac1a041eadb6e3c7dff51e9d6266513ce9e5c9b63b1dc0e5fe5420c0df11e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0af3946187b52df9bb21ca2713b1b174d8c8982bbfb8efe6adb00424b46b83`  
		Last Modified: Thu, 18 Sep 2025 19:13:55 GMT  
		Size: 231.2 MB (231161126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620292b0a4e9b1a99b6167939d6468b0d59edc2eb4f8f0dee10e7324cd7d16`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 2.5 MB (2521508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b0a546491dc8896852597210e73f86097733ac77891f99f709d8ec1a61ccb`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 481.3 KB (481251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04875e21b98e3749d2b3171a5a72d6d9d14751b037aed370c26c3573ee5fbda9`  
		Last Modified: Thu, 18 Sep 2025 19:14:24 GMT  
		Size: 338.4 MB (338375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7368013eaf0296809510e70772020221d4d9cb5ab6138690a7f2bd3e0c27bce`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61accb0ef02d1397b3d058df4a9a9f16c6879545aeca666b2f1b9ba2ad55`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38896011bef64c25122d6f013c9893348822bb84efd8d9e5ebe2fbf773cf0cb`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c475a492e5ce20aadc72ac7a8ead4f540f95d957adfc94d04b4f9b0af82ac`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d3434415c361f06faf39bd4b3bd98d79d94a69182e8971cec1660bd26d47738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41488148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f3dc0cf1612097c604ea168d2c325947f039e157115f13a309235531d2c706`

```dockerfile
```

-	Layers:
	-	`sha256:cb049bb71dd0500fd5ff2448e0e31366b24296fb582e154701dd796b6dc8e38e`  
		Last Modified: Thu, 18 Sep 2025 19:13:26 GMT  
		Size: 41.5 MB (41461161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4615c42bb02b9ea7b2c202f6775c688aebbb39c2e178fa82007ddd5769099f69`  
		Last Modified: Thu, 18 Sep 2025 19:13:27 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7373edbfc5a7fadab9976c6c984c8018cfe9226257a55736a2cf4330d29ece97
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
$ docker pull odoo@sha256:cdd33bea26fc1f4a877c560c6f22b27431729bc6e9efb42bb5b988d610a7469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599903358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ac1a041eadb6e3c7dff51e9d6266513ce9e5c9b63b1dc0e5fe5420c0df11e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0af3946187b52df9bb21ca2713b1b174d8c8982bbfb8efe6adb00424b46b83`  
		Last Modified: Thu, 18 Sep 2025 19:13:55 GMT  
		Size: 231.2 MB (231161126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620292b0a4e9b1a99b6167939d6468b0d59edc2eb4f8f0dee10e7324cd7d16`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 2.5 MB (2521508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b0a546491dc8896852597210e73f86097733ac77891f99f709d8ec1a61ccb`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 481.3 KB (481251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04875e21b98e3749d2b3171a5a72d6d9d14751b037aed370c26c3573ee5fbda9`  
		Last Modified: Thu, 18 Sep 2025 19:14:24 GMT  
		Size: 338.4 MB (338375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7368013eaf0296809510e70772020221d4d9cb5ab6138690a7f2bd3e0c27bce`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61accb0ef02d1397b3d058df4a9a9f16c6879545aeca666b2f1b9ba2ad55`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38896011bef64c25122d6f013c9893348822bb84efd8d9e5ebe2fbf773cf0cb`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c475a492e5ce20aadc72ac7a8ead4f540f95d957adfc94d04b4f9b0af82ac`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d3434415c361f06faf39bd4b3bd98d79d94a69182e8971cec1660bd26d47738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41488148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f3dc0cf1612097c604ea168d2c325947f039e157115f13a309235531d2c706`

```dockerfile
```

-	Layers:
	-	`sha256:cb049bb71dd0500fd5ff2448e0e31366b24296fb582e154701dd796b6dc8e38e`  
		Last Modified: Thu, 18 Sep 2025 19:13:26 GMT  
		Size: 41.5 MB (41461161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4615c42bb02b9ea7b2c202f6775c688aebbb39c2e178fa82007ddd5769099f69`  
		Last Modified: Thu, 18 Sep 2025 19:13:27 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250930`

```console
$ docker pull odoo@sha256:6623b7a0f5236377445026140d89dc85fb16e53accd520f715f7e1af81f91f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `odoo:18`

```console
$ docker pull odoo@sha256:8668b4d48b321050c4a4ed76616e65ae9eb300b7180360c3194196706a618a7e
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
$ docker pull odoo@sha256:a97e29fdc50bf6ed2738af08d5967bc3774bb312d0d2a40926e7dcc37c58eee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672859386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b1fd69299877af080877e444a708e203f04127fdd8c5fb68d01df1083e0ab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a6d053a570812ace1190bb458e68c3ad521f2f44fab26bcfe50a3d96d2317`  
		Last Modified: Thu, 18 Sep 2025 19:11:09 GMT  
		Size: 251.9 MB (251920107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54993715cb009df3afb88fe2e60f30258ced84577c1c4ca8dd89ee76be7237c`  
		Last Modified: Thu, 18 Sep 2025 19:05:55 GMT  
		Size: 14.3 MB (14263328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876e1f734147ae19637596f3ca841f4c9b0bda7b15f4d3f4741eeff2bd621d2`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (481039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de81b36cc2f1bcf4ca7b2d423215a6204dc47bdebb50d9b2274498624200ece`  
		Last Modified: Thu, 18 Sep 2025 19:11:53 GMT  
		Size: 377.3 MB (377331160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc893b56c09bf225da1e9f352a791b2f62af4bcb1e2df93f0b28c224e96163d3`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53dc2c9338b283567f17c4f2be4a15844d34afd988286234599487e757de77c`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5abecbfa71b32a8d400da8cb347861d198af77ab3291ddc1601f058b5c0d2b`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee3eb0f3e820bd55225f5124c9c08be3b6a8181f984f754f673f717b71501a`  
		Last Modified: Thu, 18 Sep 2025 19:05:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d660cfba5b5bd98ee6e746dd3627882ade593bad347302fd86c97d15f972f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8692fd95001884b69260379870661aded9135b3f882e87f8f8fae6b29c5a0cf5`

```dockerfile
```

-	Layers:
	-	`sha256:00ac6ea860dcfe64a791ecc214c58a4d871c28c5fa4f7d8628b0815c78c99f46`  
		Last Modified: Thu, 18 Sep 2025 19:14:27 GMT  
		Size: 60.9 MB (60906505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629f014b1b2ae240e89c895aedf98ef5c0f1d70be84853fa72fce68878103cfb`  
		Last Modified: Thu, 18 Sep 2025 19:14:28 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:1ea8e6b87e33903a37d8184b875587564401aee9b718e359e9747c401943ba23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 MB (692714949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c078b0b24f174f3742bebfd9ece821a18a684f3d0076a8079b8454a7ce8edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483929c4f2f077e54a74531d873099c888fbbefefab480aec6143eeac4b0a981`  
		Last Modified: Thu, 18 Sep 2025 19:09:48 GMT  
		Size: 378.0 MB (378039171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb6f25dd7fcf67cb4c510e5bad670fda04157e1d1ef47ade35f2280844cdcb`  
		Last Modified: Thu, 18 Sep 2025 19:06:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1524bc775fa8bf45939a39195e79414363b2a24048a25d032e0eaa8ba95212ee`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc835a5499c5fbb74cb38f2ee0da910d8d7575ce974900a3b73f329165683c`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70ee9eaac68f92f2ab457338e9094e216a9afc54a67120c51b93eee909b0a7`  
		Last Modified: Thu, 18 Sep 2025 19:06:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:cb88912076dcfdf8d83fe6b40c9f402114e936587ebf3a2f7215213873cff645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fec01cf8330b81cf510bb8fdee54641282eb4048f22c8515e7c8c0ee2d0415`

```dockerfile
```

-	Layers:
	-	`sha256:cc4ffb36059dafcd91edc728121c26a9581f66a5caab4dd025cc94d4726c018c`  
		Last Modified: Thu, 18 Sep 2025 19:16:17 GMT  
		Size: 60.9 MB (60907613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea0552ae0be32e8a92901e3f81f33b2442ca13218788735736cb21be301f5d6`  
		Last Modified: Thu, 18 Sep 2025 19:16:18 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:8668b4d48b321050c4a4ed76616e65ae9eb300b7180360c3194196706a618a7e
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
$ docker pull odoo@sha256:a97e29fdc50bf6ed2738af08d5967bc3774bb312d0d2a40926e7dcc37c58eee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672859386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b1fd69299877af080877e444a708e203f04127fdd8c5fb68d01df1083e0ab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a6d053a570812ace1190bb458e68c3ad521f2f44fab26bcfe50a3d96d2317`  
		Last Modified: Thu, 18 Sep 2025 19:11:09 GMT  
		Size: 251.9 MB (251920107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54993715cb009df3afb88fe2e60f30258ced84577c1c4ca8dd89ee76be7237c`  
		Last Modified: Thu, 18 Sep 2025 19:05:55 GMT  
		Size: 14.3 MB (14263328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876e1f734147ae19637596f3ca841f4c9b0bda7b15f4d3f4741eeff2bd621d2`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (481039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de81b36cc2f1bcf4ca7b2d423215a6204dc47bdebb50d9b2274498624200ece`  
		Last Modified: Thu, 18 Sep 2025 19:11:53 GMT  
		Size: 377.3 MB (377331160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc893b56c09bf225da1e9f352a791b2f62af4bcb1e2df93f0b28c224e96163d3`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53dc2c9338b283567f17c4f2be4a15844d34afd988286234599487e757de77c`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5abecbfa71b32a8d400da8cb347861d198af77ab3291ddc1601f058b5c0d2b`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee3eb0f3e820bd55225f5124c9c08be3b6a8181f984f754f673f717b71501a`  
		Last Modified: Thu, 18 Sep 2025 19:05:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d660cfba5b5bd98ee6e746dd3627882ade593bad347302fd86c97d15f972f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8692fd95001884b69260379870661aded9135b3f882e87f8f8fae6b29c5a0cf5`

```dockerfile
```

-	Layers:
	-	`sha256:00ac6ea860dcfe64a791ecc214c58a4d871c28c5fa4f7d8628b0815c78c99f46`  
		Last Modified: Thu, 18 Sep 2025 19:14:27 GMT  
		Size: 60.9 MB (60906505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629f014b1b2ae240e89c895aedf98ef5c0f1d70be84853fa72fce68878103cfb`  
		Last Modified: Thu, 18 Sep 2025 19:14:28 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1ea8e6b87e33903a37d8184b875587564401aee9b718e359e9747c401943ba23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 MB (692714949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c078b0b24f174f3742bebfd9ece821a18a684f3d0076a8079b8454a7ce8edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483929c4f2f077e54a74531d873099c888fbbefefab480aec6143eeac4b0a981`  
		Last Modified: Thu, 18 Sep 2025 19:09:48 GMT  
		Size: 378.0 MB (378039171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb6f25dd7fcf67cb4c510e5bad670fda04157e1d1ef47ade35f2280844cdcb`  
		Last Modified: Thu, 18 Sep 2025 19:06:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1524bc775fa8bf45939a39195e79414363b2a24048a25d032e0eaa8ba95212ee`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc835a5499c5fbb74cb38f2ee0da910d8d7575ce974900a3b73f329165683c`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70ee9eaac68f92f2ab457338e9094e216a9afc54a67120c51b93eee909b0a7`  
		Last Modified: Thu, 18 Sep 2025 19:06:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cb88912076dcfdf8d83fe6b40c9f402114e936587ebf3a2f7215213873cff645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fec01cf8330b81cf510bb8fdee54641282eb4048f22c8515e7c8c0ee2d0415`

```dockerfile
```

-	Layers:
	-	`sha256:cc4ffb36059dafcd91edc728121c26a9581f66a5caab4dd025cc94d4726c018c`  
		Last Modified: Thu, 18 Sep 2025 19:16:17 GMT  
		Size: 60.9 MB (60907613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea0552ae0be32e8a92901e3f81f33b2442ca13218788735736cb21be301f5d6`  
		Last Modified: Thu, 18 Sep 2025 19:16:18 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250930`

```console
$ docker pull odoo@sha256:d27b52c3eae4277ec8235bf5e740b6c0058a3bdacfb3b03afe10a39bb0f45117
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `odoo:19`

```console
$ docker pull odoo@sha256:df39eb63135257c16a9ad4489b12b36e264db0d96ac0372d46e96e901463088b
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
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:df39eb63135257c16a9ad4489b12b36e264db0d96ac0372d46e96e901463088b
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
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20250930`

```console
$ docker pull odoo@sha256:2161256486a1d7e385cb260af1e4fc0fdfdfe74b34f6290f77ec6a5d6bc37bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `odoo:latest`

```console
$ docker pull odoo@sha256:df39eb63135257c16a9ad4489b12b36e264db0d96ac0372d46e96e901463088b
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
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
